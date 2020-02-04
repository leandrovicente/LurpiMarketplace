<h1 align="center">
  <img  src="https://raw.githubusercontent.com/leandrovicente/LurpiMarketplace/master/src/app/img/logo.png" width="400px" />
</h1>

<h3 align="center">
Lurpi Marketplace</h3>



# Sobre o LurpiMarketplace

Uma aplicação criada para desenvolver os conhecimentos em node.js.
Codigo totalmente aberto, então sinta-se a vontade a para modificar, utilizar, vender etc.


### **No desenvolvimento da aplicação foi utilizado:**
Em todas Instalações foi utilizado o yarn
-  Node; 
- Express;
- ESLint;
- Prettier;
- EditorConfig;
- Handlebarsjs;
-  Redis;
- Mongoose (Utilizei o Banco De Dados Do MongoAtlas);
- BcryptJS (Para Criptografia Dos Dados);
- Mailtrap (Caixa de entrada, usada para testar envio de email),
- Sentry (Para Monitorar Erros No Sistema),
- JWT (Para Gerar o Token de Autenticação)


### **Funcionalidades**

### **1. Autenticação**
Após logar na aplicação a mesma gerar um token de acesso , ficando disponivel por 6 horas.
Após isso e necessario realizar outro login.
Para se Cadastrar Neccesario :
POST EM http://localhost:3333/users

E passar o Nome, Email e Senha Via Json :

	{
	"name":"Seu Nome"
	"email":"EmailCadastrado@gmai.com",
	"password":"SuaSenha"
	}


Para Realizar o login e necessiario :
POST EM http://localhost:3333/sessions

E passar o Email e Senha Via Json :

	{
	"email":"EmailCadastrado@gmai.com",
	"password":"SuaSenha"
	}


### **2. Anuncios**

A WebApi Permite fazer o CRUD(Create, Read, Update and Delete) de anuncios.
Para o cadastro do anuncio e necessario informa: 
POST EM http://localhost:3333/ads/

E passar o Titulo, Descricão e Preço Via Json :

	{
	"title":"Titulo",
	"description":"Descricão",
	"price":1000
	}


Lembrando que e necessario passar o token do usuario.

Para as demais funcionalides do crud basta passar, a URL + ID (o id do anuncio)
exemplo : http://localhost:3333/ads/1

Para visualizar todos os anuncios GET em: http://localhost:3333/ads/ 


A WebApi Contém paginação e filtros pro Preço Maximo , Preço Minino e Titulo
Exemplos:

	http://localhost:3333/ads/price_max=2000
	http://localhost:3333/ads/price_min=1000
	http://localhost:3333/ads/title=REact


### **3. Envio de E-mails**
O envio de email e feito quando alguém se interessa pelo o anuncio.
Para isso e necessario:
POST EM http://localhost:3333/purchases/

Passando o ID do Anuncio e Conteúdo do Email :

	{
        "ad": "id do anuncio",
	    "content":"Conteudo do email"
	}

Fazendo isso você irar receber um email no MAILTRAP.IO.


## Contato
Email: leandro.vicente98@outlook.com
Linkedin : https://www.linkedin.com/in/leandro-vicente/


