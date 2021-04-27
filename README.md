
<p align="center">
<img src="http://vetorit.com.br/images/logo-vetor-b-01.png" align="center"/>
<br/>
<br/>
<img src="https://www.zema.com/file/general/logo-zema-azul.png" width="240" align="center"/>
</p>

<h1 align="center">
  FastTaxWS - API
</h1> 


<h4 align="center">
	API para consultas fiscais ao FastTax 🚀
	<br />
	<br />
	<img src="https://img.shields.io/badge/Current Version-1.0.0.Latest-%238257E6.svg" alt="Vetor IT" />
	<img src="https://img.shields.io/badge/Stable-%238257E6.svg" alt="Vetor IT" />
	<img src="https://img.shields.io/badge/Company-Vetor IT-%238257E6.svg" alt="Vetor IT" />
	<img alt="License" src="https://img.shields.io/badge/License-MIT-%238257E6">
</h4>

## ⚙️ Especificações & Setup
O projeto se encontra em fase de construção, atualmente na versão 1.0.0 e recebendo atualizações novas constantemente.

<br>

Tecnologias do WebService:

- [X] Selenium Web Driver
- [X] OAuth2.0 Resource/Authorization Server
- [X] JWT
- [X] PostgreSQL 11

<br>

Funcionalidades Implementadas:

- [X] Monitoramento de situação fiscal no e-CAC
- [ ] Monitoramento de domicílio tributário eletrônico
- [ ] Consulta das CND's
Federal: FGTS e INSS
Estadual: Tributos estaduais
- [ ] Monitoramento das contas correntes fiscais e estaduais
- [ ] Controle de entrega das obrigações acessórias (Sped fiscal, EFD contribuições, sped contábil, ECF)
- [ ] Monitoramento e captura das DARF’s recolhidas

<br>
<br>

## ⚗️ Configuração para laboratório de testes de requisições
Atualmente, o WebService está realizando consultas de situação fiscal no e-CAC, mas novas funcionalidades já estão sendo trabalhadas e serão implantadas para teste o mais rápido possível. ⚡️

<br>

### Consulta Fiscal ao e-CAC 🧾
- ⏱ O tempo de resposta para este enpoint foi otimizado em 90% do seu tempo inicial (~98s). Ou seja, a requisição hoje, demora em média para ser respondida ~12s.
- As requisições agora utilizam o cliente OAuth2 criado no banco de dados e designado para cada cliente OAuth da aplicação, isso requer uma nova configuração no cliente REST, porém o modelo continua o mesmo:

<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/53920696/116194945-ec89de00-a707-11eb-8e36-90c47e645ec6.png">
</p>

<br>

- Será disponibilizado via chat, o endpoint atual para cadastro de novos clientes de acesso à aplicação, o corpo da requisição (já com validações inclusa), segue o seguinte padrão (este endpoint não requer autorização nem autenticação):

<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/53920696/116197266-ea754e80-a70a-11eb-98ef-a5c756c0e294.png">
</p>

<br>

- Para realizar a consulta no e-CAC para averiguação da situação fiscal, o novo endpoint, além do cliente OAuth para o teste, será disponibilizado via chat para execução. Seus três parâmetros (já incluso validação no endpoint) seguem o seguinte formato (este endpoint requer autenticação OAuth completa (primeira foto)):

<br>

<p align="center">
  <img src="https://user-images.githubusercontent.com/53920696/116196111-78e8d080-a709-11eb-84c4-c6fe3b5f4428.png">
</p>

<br>

- Após os passos descritos, o endpoint retornará o PDF com a situação fiscal atual sobre a inclusão do CNPJ no Cadin Sisbacen, relembrando que o cliente OAuth (não usuário), será fornecido via chat para testes.
- Por ser uma API REST, a aplicação não realiza cache de senhas nem certificados, ambos são utilizados única e exclusivamente durante a execução da consulta, sendo armazenado APENAS os dados relacionados ao cliente para autenticação na aplicação.

<br>
<br>
<br>
<p align="center">
  Feito com 🧡 pela Vetor IT
</p>

