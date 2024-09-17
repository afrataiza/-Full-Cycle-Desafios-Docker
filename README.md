# Curso Full Cycle 🚀

## Desafios Docker
Este repositório contém os desafios do módulo sobre Docker.

### Desafio Go!
Consiste em criar uma imagem docker em Go, que imprima a seguinte frase ao ser executada: **Full Cycle Rocks!!**
Além disso deve atender aos seguintes requisitos:
- A imagem precisa ter apenas 2Mb
- A imagem precisa ser armazenada no Docker Hub

[Link Público Docker Hub - Desafio Go!](https://hub.docker.com/r/afrataiza/desafio-go)

### Desafio Nginx com Node.js
Esse desafio consistem em criar uma aplicação docker em que ao chamar o nginx ele acesso o node.js que por sua vez vai inserir no banco de dados MySql, um nome na tabela people. 
O retorno da aplicação node.js para o nginx deverá ser:
```
<h1>Full Cycle Rocks!</h1>
- Lista de nomes cadastrada no banco de dados.
```

Além disso será necessário atender alguns requisitos:
- Gere o `docker-compose` de uma forma que basta apenas rodar: `docker-compose up -d` que tudo deverá estar funcionando e disponível na _porta: 8080_
- Adicione volume na aplicação para o ambiente de desenvolvimento. 
