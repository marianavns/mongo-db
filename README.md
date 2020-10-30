# Guia Introdutório do MongoDB

Olá, este é um guia introdutório sobre o banco de dados MongoDB. 🍃 

Seja bem-vinda!

<img src=https://i.imgur.com/tc753FH.gif alt="Ilustração. Tela de computador suspensa, com várias pastas. Na frente da tela, uma lupa. Atrás da tela, um móvel com várias gavetas, fazendo alusão ao banco de dados." width="400" height="400">

# Sumário

0. [Preparando a Máquina](#Preparando-a-Máquina)

1. [Conceitos Introdutórios](#Conceitos-Introdutórios)

1.1 [Banco de Dados](#Banco-de-Dados)

1.2 [Prompt de Comando](#Prompt-de-Comando)

1.3 [Bancos de Dados Relacional](#Banco-de-Dados-Relacional)

1.4 [Banco de Dados Não Relacional](#Banco-de-Dados-Não-Relacional)

2. [Detalhando Bancos de Dados Não Relacionais](#Detalhando-Bancos-de-Dados-Não-Relacionais)

2.1 [Tipos de Bancos de Dados NoSQL](#Tipos-de-Bancos-de-Dados-NoSQL)

3. [O MongoDB](#O-MongoDB)

# Preparando a Máquina

  Antes de começar, é preciso ter o MongoDB instalado: [Link para instalação](#https://medium.com/@NetoVieiraLeo/instalando-e-configurando-o-mongodb-no-windows-b1d4e1e58911).

# Conceitos Introdutórios

## Banco de dados

É o conjunto de arquivos onde informações muito importantes para a aplicação ficam salvas. 

Por exemplo: estamos desenvolvendo um site de empregos (a aplicação) onde candidatos adicionam seus nomes, cidade, cursos feitos e experiências, e as empresas adicionam nome, cidade e o tipo de profissional que precisam. Tanto as informações dos candidatos quanto das empresas ficam salvas no banco de dados da aplicação. 

> :bulb: A partir deste banco de dados, o backend vai criar os métodos para manipular e visualizar todas as informações adicionadas pelos usuários.

## Prompt de Comando 

É aquela tela preta usada para digitar códigos. Para ativá-la, digite cmd na barra de pesquisa do seu Windows e abra o prompt de comando. 

Nessa primeira etapa, vamos aprender banco de dados inserindo, excluindo, editando e visualizando os dados pelo prompt de comando. Não vai ser pelo VSCode desta vez e nem vamos adicionar como faríamos num site (pois ainda não temos nenhum site construído).

## Banco de Dados Relacional

É um banco de dados que guarda e manipula as informações de maneira estruturada, ordenada. Eles usam uma linguagem própria para a comunicação, a *Structured Query Language*, ou SQL. Por isso os bancos relacionais também são chamados de *Bancos SQL*. Eles são baseado em esquemas, criando tabelas, campos e relacionamentos entre as informações, para só depois adicionar os dados. 

Construí-lo é como se você fosse preparar uma casa do zero: é necessário dividir o terreno, fazer a base, instalar as colunas, construir as paredes, telhado, etc, para depois decorar, colocar o sofá, camas, fogão, TV... **A construção vem primeiro e é feita por você. Só depois que a decoração e utensílios são adicionados.**. 

Neste exemplo, a construção da casa seria construir a estrutura do seu banco de dados. Colocar a decoração, os eletrodomésticos, móveis e todo o resto seria finalmente adicionar os dados no banco.

## Banco de Dados Não Relacional

Aqui, os esquemas relacionais não são necessários, é só adicionar os dados. Eles também são chamados de *Bancos NoSQL*, ou **Not Only** *Structured Query Language*, "não apenas SQL". Ou seja: ele pode usar SQL ou não. 

Fazendo uma analogia com a construção da casa, usar o banco NoSQL seria **apenas não construir a casa** e ir morar num  galpão enorme, onde você pode deixar seus móveis só num cantinho, se quiser, e não precisa preencher necessariamente todos os espaços. Pode, quem sabe, chamar mais umas 50 pessoas para morar com você. É livre? É livre. Mas pode trazer problemas posteriores se essa não é a vida que você desejou... 

Por dispensar uma estrutura prévia e outros diferenciais, os Bancos NoSQL têm algumas vantagens:

 - São mais flexíveis;
 - Escalabilidade: são pensados para disribuir dados usando clusters, que são várias máquinas como se fossem uma só, unidas por nós, de amarração mesmo.
 - Disponibilidade: o banco de dados não cai tanto, rs. A arquitetura deles é muito robusta para replicar os dados. A clusterização garante que, se um nó cair, o outro assume sem perdas de dados.
 - Vem do Open Source: a comunidade só cresce!
 - Baixo custo operacional: o custo para migrar é muito baixo! Os relacionais precisam de equipamentos mais parrudos;
 - Trabalham melhor com APIs Restful. :D
 
 > Observação importante: "NoSQL" não é apenas um tipo de banco de dados. Existe um mundo de tecnologias, ferramentas e conceitos que são NoSQL.

# Detalhando Bancos de Dados Não Relacionais

## Tipos de Bancos de Dados NoSQL

Para entender melhor os tipos de Bancos de Dados NoSQL explicados a seguir, acompanha esta imagem abaixo enquanto vai lendo: 🔎

<img src=https://micreiros.com/wp-content/uploads/art1.jpg alt="Imagem com resumo dos tipos de bancos NoSQL tratados a seguir" width="700" height="200">

**1. Tipo Chave-valor**: São mais usados em aplicações de jogos, publicidade online, internet das coisas. Possuem "escalabilidade horizontal", podem crescer quase que sem fronteiras, e as consultas são bem rápidas. Bancos deste tipo armazenam dados no padrão chave-valor, como as tabelas de dispersão. Exemplos: MemcacheD, Riak e Redis. 
 
**2. Tipo Grafos**: Utilizam vértices e arestas e são usados em aplicativos que precisam de um conjunto de dados altamente conectados, como redes sociais, mecanismos de reconhecimento e controle de fraudes. Exemplos: Property Grafh e RDF. Ferramentas para gerenciá-los: Neo4j e Giraph. 
 
**3. Tipo Colunar** ou Orientado a Colunas: Importante para performance de consulta analítica, pois reduz a necessidade de entrada e saída de dados o tempo todo. Exemplos: Cassandra e Hbase. 
 
**4. Tipo Pesquisa**: Importante para indexação, agregação e pesquisa de registros em **dados semiestruturados**. É caracterizado pela alta performance, baixa latência e análise de dados praticamente em tempo real. Exemplos: Amazon ES, usado pelo pessoal da Expedia.
 
**5. Tipo Documentos**: Armazena documentos e também é conhecido como Modelo de Dados semi-estruturados, usando o próprio formato "chave-valor", como o JSON. Os documentos são criados e se tornam unidades independentes. Exemplos: MongoDB e CouchDB.

# O MongoDB

Finamente chegamos nele!

O Mongo ajuda a criar **documentos, collections e databases**:

**1. Documentos**: Os documentos são as informações que ficam guardadas dentro de um par de chaves. Exemplo:
{"nome": "Mariana", "idade":29}.

**2. Collections**: É um conjunto de documentos. Se você já estudou arquivos JSON - o que é muito provável -, a collection é como se fosse o arquivo JSON, guardando vários objetos. Exemplo:
`pessoas.json` ou `collection pessoas`:
```js
[
  {"nome":"Mariana","idade":29},
  {"nome":"Jorge","idade":53},
  {"nome":"Gustavo","idade":48}
]
```

**3. Databases**: É o conjunto de collections. É como se fosse a pasta de JSONs ou a pasta Model da API.

## Mão no Código

Depois do Mongo instalado, trabalharemos sempre com **dois prompts de comando abertos**: O primeiro para "acionar" o MongoDB e deixá-lo rodando na máquina e o segundo para manipular os dados que iremos adicionar.

Então vamos lá:
- No primeiro prompt, digite o comando `mongod`. Agora o server está rodando e é possível mexer nos dados no segundo prompt sem perder nada. 
- No segundo prompt, digite `mongo` para que o terminal consiga ler os comandos Mongo.

### Preenchendo o database
> Vamos criar um banco de dados com matérias a ser estudadas nos nichos "programação" e "humanas".

**1.** A primeira coisa a fazer é **criar o banco de dados e entrar nele**. Para isso, digite `use <nome-do-banco-de-dados>` no segundo terminal. Pronto, está criado e você já está dentro dele. 

> Aqui, criaremos a database `cursos`.

**2.** Segundo passo: **Crie sua primeira collection** com o comando `db.createCollection(<"nomedacollection">)`. 

> Aqui, criaremos as collections `collectionCursosProgramacao` e `collectionCursosHumanas`)

**3.** Verifique se o banco realmente foi criado, digitando `show databases`. Seu novo banco deve estar na lista que vai aparecer.

**4.** Hora de rechear seus JSONs, opa, suas collections 😅. Lembre-se, aqui é tudo pelo prompt de comando, então não será tão divertido quanto digitar no VSCode. Digite o comando `db.<nome-da-collection>.insertOne({<informações-a-adicionar>})`. Para inserir vários documentos, o comando é `db.<nomedacollection>.insertMany({<informações-a-adicionar>})`.

### Manupulando os dados





