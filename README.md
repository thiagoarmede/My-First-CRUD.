# Minha primeira aplicação CRUD com Node.js
Minha primeira aplicação CRUD(create, read, update, delete) apenas para praticar os conhecimentos básicos de NodeJS.

## Instalação e execução

Para testar a aplicação, você deve ter o MySQL instalado, com a estrutura de banco de dados e tabela já criados. Você pode executar o script a seguir para gerar a tabela.

```sql
CREATE DATABASE `db`;
USE `db`;

CREATE TABLE `rest` (
  `id` int(11) NOT NULL,
  `name` varchar(30) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

INSERT INTO `rest` VALUES(1, 'Ricardo Teixeira');
INSERT INTO `rest` VALUES(2, 'Maria Joaquina');


ALTER TABLE `rest`
  ADD PRIMARY KEY (`id`);
```

No arquivo index.js, troque os valores de configuração do MySQL por aqueles utilizados por você.

```javascript
var knex = require('knex')({
  client: 'mysql',
  connection: {
    host : 'seu_host',
    user : 'seu_usuario',
    password : 'sua_senha',
    database : 'seu_banco'
    }
});
```

Acesse o terminal e execute o comando `npm install -g nodemon` para instalar o nodemon como global.

Em seguida, dentro da pasta do projeto, execute

```
npm install
```

Após concluída a instalação, execute o comando `nodemon index.js` ou `node index.js` para executar sem o nodemon.

