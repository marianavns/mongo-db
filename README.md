# Guia Introdutório do MongoDB

Olá, este é um guia introdutório sobre o banco de dados MongoDB. 🍃 

Seja bem-vinda!

<img src=https://i.imgur.com/uF1tXio.gif alt="Ilustração. Tela de computador suspensa, com várias pastas. Na frente da tela, uma lupa. Atrás da tela, um móvel com várias gavetas, fazendo alusão ao banco de dados." width="400" height="200">

# Sumário

0. [Preparando a Máquina](#Preparando-a-Máquina)

1. [Conceitos Introdutórios](#Conceitos-Introdutórios)

2. [Bancos de Dados NoSQL](#Bancos-de-Dados-NoSQL)

2.1 [Tipos de Bancos de Dados NoSQL](#Tipos-de-Bancos-de-Dados-NoSQL)

3. [O MongoDB](#O-MongoDB)

# Preparando a Máquina

  Antes de começar, é preciso ter o MongoDB instalado: [Link para instalação](#https://medium.com/@NetoVieiraLeo/instalando-e-configurando-o-mongodb-no-windows-b1d4e1e58911).

# Conceitos Introdutórios

1. Banco de dados: É o conjunto de arquivos onde ficam salvas informações muito importantes para a aplicação. Por exemplo: estamos desenvolvendo um site de empregos onde candidatos adicionam seus nomes, cidade, cursos feitos e experiências, e as empresas adicionam nome, cidade e o tipo de profissional que precisam. Tanto as informações dos candidatos quanto as informações das empresas ficam salvas no banco de dados da aplicação (do site). 

💡 A partir deste banco de dados, o backend vai criar os métodos para manipular e visualizar todas as informações adicionadas pelos usuários.

2. Prompt de Comando: É aquela tela preta usada para digitar códigos. Para ativá-la, digite cmd na barra de pesquisa do seu Windows e abra o prompt de comando. Nessa primeira etapa, vamos aprender banco de dados inserindo, excluindo, editando e visualizando os dados pelo prompt de comando. Não vai ser pelo VSCode desta vez e nem vamos adicionar como faríamos num site (pois ainda não temos nenhum site construído).

3. Banco de Dados Relacional: É um banco de dados que guarda e manipula as informações de maneira estruturada, ordenada. Eles usam uma linguagem própria para a comunicação, a *Structured Query Language*, ou SQL. Por isso os bancos relacionais também são chamados de *Bancos SQL*. 

Eles são baseado em esquemas, criando tabelas, campos e relacionamentos entre as informações para depois adicionar os dados. Construí-lo é como construir uma casa do zero: é necessário dividir o terreno, fazer a base, instalar as colunas para só depois colocar os tijolos, formar os cômodos, telhado, etc. **A estrutura vem primeiro**.

4. Banco de Dados Não Relacional: Aqui os esquemas relacionais não são necessários, é só adicionar os dados. Também são chamados de Bancos NoSQL, ou **Not Only** *Structured Query Language*, "não apenas SQL". Ou seja: ele pode usar SQL ou não. 

> Vale ressaltar que NoSQL não é apenas um tipo de banco de dados. Existe um mundo de tecnologias, ferramentas e conceitos que são NoSQL.

Por dispensar uma estrutura prévia e outros diferenciais, os Bancos NoSQL têm algumas vantagens:

 - São mais flexíveis;
 - Escalabilidade: são pensados para disribuir dados usando clusters, que são várias máquinas como se fossem uma só, unidas por nós, de amarração mesmo.
 - Disponibilidade: o banco de dados não cai tanto, rs. A arquitetura deles é muito robusta para replicar os dados. A clusterização garante que, se um nó cair, o outro assume sem perdas de dados.
 - Vem do Open Source: a comunidade só cresce!
 - Baixo custo operacional: o custo para migrar é muito baixo! Os relacionais precisam de equipamentos mais parrudos;
 - Trabalham melhor com APIs Restful. :D

# Bancos de Dados NoSQL

## Tipos de Bancos de Dados NoSQL

Para entender melhor os tipos de Bancos de Dados NoSQL explicados a seguir, acompanha esta imagem abaixo enquanto vai lendo: 🔎

<img src=https://micreiros.com/wp-content/uploads/art1.jpg alt="Imagem com resumo dos tipos de bancos NoSQL tratados a seguir" width="700" height="200">

1. Tipo Chave-valor: São mais usados em aplicações de jogos, publicidade online, internet das coisas. Possuem "escalabilidade horizontal", podem crescer quase que sem fronteiras, e as consultas são bem rápidas. Bancos deste tipo armazenam dados no padrão chave-valor, como as tabelas de dispersão. Exemplos: MemcacheD, Riak e Redis. 

<img src=https://upload.wikimedia.org/wikipedia/commons/1/1c/Hash2.JPG alt="tabela de dispersão" width="800" height="150">

¹Exemplo de uma tabela hash ou tabela de dispersão.
 
2. Tipo Grafos: Utilizam vértices e arestas e são usados em aplicativos que precisam de um conjunto de dados altamente conectados, como redes sociais, mecanismos de reconhecimento e controle de fraudes. Exemplos: Property Grafh e RDF. Ferramentas para gerenciá-los: Neo4j e Giraph. 
 
3. Tipo Colunar ou Orientado a Colunas: Importante para performance de consulta analítica, pois reduz a necessidade de entrada e saída de dados o tempo todo. Exemplos: Cassandra e Hbase. 
 
4. Tipo Pesquisa: Importante para indexação, agregação e pesquisa de registros em **dados semiestruturados**. É caracterizado pela alta performance, baixa latência e análise de dados praticamente em tempo real. Exemplos: Amazon ES, usado pelo pessoal da Expedia.
 
5. Tipo Documentos: Armazena documentos e também é conhecido como Modelo de Dados semi-estruturados, usando o próprio formato "chave-valor", como o JSON. Os documentos são criados e se tornam unidades independentes. Exemplos: MongoDB e CouchDB.

# O MongoDB

Finamente chegamos nele!




