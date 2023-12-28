# Coleta de Dados I

Antes de começar

Faça login na sua conta da Google. Acesse o **Google Colab** e faça o download do arquivo notebook “Profissão Analista de dados M10 Material de apoio”. 

# Nesta tarefa, iremos praticar 2 exercícios. 

Prepare o ambiente

Vamos explorar dados de crédito presentes no arquivo Profissão Analista de dados M10 Pratique Material de apoio.xlsx. Os dados estão no formato de Excel (XLSX) e contém informações sobre clientes de uma instituição financeira. Em especial, estamos interessados em explicar a segunda coluna, chamada de default, que indica se um cliente é adimplente (default = 0), ou inadimplente (default = 1), ou seja, queremos entender o porquê um cliente deixa de honrar com suas dívidas baseado no comportamento de outros atributos, como salário, escolaridade e movimentação financeira. Segue uma descrição completa dos atributos:



Faça o download do arquivo Profissão Analista de dados M10 Exercício Material de apoio.xlsx com a célula de código indicada no material de apoio.

# 1º Exercício: Excel para CSV

Utilizando o pacote Python openpyxl, extraia as colunas id, sexo e idade para os clientes inadimplentes (default = 1 ) e solteiros (estado_civil = 'solteiro'). 

Salve os dados extraídos no arquivo csv “credito.csv” separado por ; . 

Dica: O arquivo credito.csv deve ter 669 linhas, contando com o cabeçalho. 

Obs: Escreva o código da sua solução em uma ou mais células. Você não precisa enviar o arquivo csv gerado. 

Ficou com dúvidas sobre como extrair as colunas filtrando clientes inadimplentes e solteiros?

Realize a extração de cada coluna separadamente e depois junte quando for salvar no arquivo CSV. Você vai precisar:

1) Criar índices para as colunas:

 id
sexo
idade
inadimplência (default)
estado civil (estado_civil)

2) Extrair a coluna de ‘id’ dos clientes inadimplentes e solteiros. Em seguida, vai realizar o mesmo procedimento para a coluna ‘sexo’ e ‘idade’. Tenha como base o exemplo ‘Média dos saldos’ que estudamos anteriormente.

3) Quando for fazer o filtro dos clientes inadimplentes e solteiros, inclua no código de extração da coluna, dentro da estrutura condicional ‘if’, as condições:

(linha[indice_default] == 1) e (linha[indice_estado_civil] == 'solteiro')
Ficou com dúvidas sobre como salvar os dados no arquivo CSV?

Caso tenha seguido a nossa sugestão para a extração de cada coluna em variáveis diferentes, quando for salvar os dados, utilize as três variáveis para compor o arquivo CSV. Como no exemplo da aula: 



A parte indicada pela seta laranja é a escrita do cabeçalho, no exemplo é o nome de uma coluna, no caso do seu exercício serão os nomes das três colunas.

A parte destacada em azul é a função recebida como parâmetro para ser aplicada a todos os elementos da coleção (destacado em amarelo). Essa função só está estruturando os dados nesse formato de lista. No caso do exercício do módulo 10, a estrutura será uma lista com três parâmetros. Exemplo: [id, sexo, idade].

A parte destacada em amarelo é a coleção de dados que a função ‘map’ utiliza para aplicar a função lambda. No caso, a função ‘map’ vai receber as três variáveis que contém os dados extraídos.

Obs.: se a parte da função ‘map’ ainda estiver muito confusa, revisite as aulas do módulo 5. 

# 2º Exercício: Excel para JSON

Como preparação para o próximo módulo, vamos trabalhar com o JSON, um formato semi-estruturado, muito utilizado em transmissão de dados da web e equivalente a um dicionário Python. 

Utilizando o pacote Python openpyxl, extraia os dados das colunas “escolaridade” e “tipo_cartao”, removendo duplicados. Com os dados, construa o dicionário Python “crédito” com a estrutura indicada no material de apoio.

Para finalizar, utilize o código indicado no material de apoio para converter o dicionário “crédito” no formato JSON.

Dica: Sua solução deve gerar o dicionário Python “crédito” igual ao exemplo, mas a ordem dos elementos pode variar tranquilamente. Uma excelente forma de remover elementos duplicados de uma lista é convertê-la para “set” e depois para “list” novamente. Encaminhe à equipe de tutoria o código com a solução do exercício.

## Autor: Genésio Moreira Coutinho 
- Graduado: Bacharelado em Sistemas de Informação | Pós Graduando:  MBA em Gestão da Qualidade em Tecnologia da Informação |Analista de Dados| 1x Azure - AZ900
- Date Analyst | Cloud Infrastructure | Azure | Analista Cloud | Analista Dados | Infraestrutura Cloud | Python
- Linkedin: https://www.linkedin.com/in/genesio-coutinho-554733124/
- Kaggle:https://www.kaggle.com/genesiomoreira

- Notebook para execução dos códigos Google Collab: https://colab.research.google.com/drive/1nXA33UTy_n4NLgdyiOCXiTLNPGXFPKrG?usp=sharing
