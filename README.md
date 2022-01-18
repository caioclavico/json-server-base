# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Habits

GET /habits

Exibe todos os habitos cadastrados de todos os usuários

POST /habits

O endpoint é usado para cadastrar um novo hábito, sendo necessario o ID do usuário e token

exemplo:

    {
        "title": "aulas de dança",
        "category": "Lazer",
        "frequency": "Diário",
        "userId": 2
    }

### Goals

GET /goals

Exibe todas as metas cadastradas de todos os usuários

POST /goals

O endpoint é usado para cadastrar uma nova Meta, sendo necessário o ID do usuário e token

exemplo:

    {
    	"title": "Emagrecer 10kg",
    	"difficulty": "Dificil",
    	"achieved": false,
    	"how_much_achieved": 50,
    	"userId": 1,
    }
