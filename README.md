
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

Tecnologias do WebService:

- [X] Selenium Web Driver
- [X] OAuth2.0 Resource/Authorization Server
- [X] JWT
- [X] PostgreSQL 11

Funcionalidades Implementadas:

- [X] Monitoramento de situação fiscal no e-CAC
- [ ] Monitoramento de domicílio tributário eletrônico
- [ ] Consulta das CND's
Federal: FGTS e INSS
Estadual: Tributos estaduais
- [ ] Monitoramento das contas correntes fiscais e estaduais
- [ ] Controle de entrega das obrigações acessórias (Sped fiscal, EFD contribuições, sped contábil, ECF)
- [ ] Monitoramento e captura das DARF’s recolhidas

## ⚗️ Configuração para laboratório de testes de requisições
Atualmente, o WebService está realizando consultas de situação fiscal no e-CAC, mas novas funcionalidades já estão sendo trabalhadas e serão implantadas para teste o mais rápido possível. ⚡️

### Consulta Fiscal ao e-CAC 🧾
- ⏱ O tempo de resposta para este enpoint foi otimizado em 90% do seu tempo inicial (~98s). Ou seja, a requisição hoje, demora em média para ser respondida ~12s.
- As requisições agora utilizam o cliente OAuth2 criado no banco de dados e designado para cada cliente OAuth da aplicação, isso requer uma nova configuração no cliente REST, porém o modelo continua o mesmo:

![image](https://user-images.githubusercontent.com/53920696/116194945-ec89de00-a707-11eb-8e36-90c47e645ec6.png)

- Será disponibilizado via chat, o endpoint atual para cadastro de novos clientes de acesso à aplicação, o corpo da requisição (já com validações inclusa), segue o seguinte padrão (este endpoint não requer autorização):

![image](https://user-images.githubusercontent.com/53920696/116195446-9c5f4b80-a708-11eb-88b6-cf03fd75123c.png)

