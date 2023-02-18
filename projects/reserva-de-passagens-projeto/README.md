# Consulta de reservas de passagens de ônibus

Nesse projeto, é feita a simulação de consulta pública de horários de ônibus. 

Tecnologias: Python, PostgreSQL, PGAdmin, EC2 AWS, construção de API, acesso SSH.

Foram implementados:

* Um serviço na nuvem com os métodos de consulta.
* Uma API
* Um banco de dados na nuvem
* Uma aplicação para teste

## Banco de dados
Abaixo os campos dos banco de dados

**campos | tipo                  | exemplo**
id       | integer identity PK   | 364
linha    | Varchar(60)           | Santa Maria/Novo Hambugo
origem   | Varchar(30)           | Santa Maria
Destino  | Varchar(30)           | Novo Hamburgo
DiaSemana| Varchar(60)           | Segunda-Feira
Hora     | Time                  | 20:30

## Serviços públicos da API

A solução vai fornecer uma API para a consulta das linhas por origem e horário.

A API retornará todas as informações em formato JSON.

O código contém tratamento de erros com mensagens ao usuário, logs e usa arquivos de configuração.

Foi implementado:

* Todos os horários por linha
    * Santa Maria/Novo Hamburgo
* Todos os horários por linha e dia da semana
    * Santa Maria/Novo Hamburgo, segunda-feira
* Todos os horários por Destino
    * Novo hamburgo
* Todos os horários por origem e destino
    * Novo Hamburgo, Santa Maria
* Todos os horários por origem, destino e dia da semana
    * Novo hamburgo, Santa Maria, segunda-feira

## Solução proposta

* Instalação do PGAdmin
* Criação de instância do SGBD PostgreSQL
    * Configuração para acesso remoto
* Conexão ao PostgreSQL
    * Criação do Banco de Dados
    * Inserção dos Dados
* Criação de instância no EC2
    * Configuração do acesso a porta
* Criação do serviço no EC2 com Python
    * Testar no navegador
* Criação da aplicação no Google Colab para teste do serviço

