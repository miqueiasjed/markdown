#Modelagem de Dados

#Fases do Projeto

**1 - Levantamento dos Requisitos (Regras de Negócio)**
	Listar todas as regras de negócio
 
**2 - Identificação de Entidades e Relacionamentos**
	Um relacionamento propõe uma entidade
	Procurar verbos na regras de negócios, para possível entidade
	Fazer uma lista dos relacionamentos
	Fazer uma lista de atributos

**3 - Modelo E-R **
	Fazer um diagrama básico 

**4 - Diagrama E-R **
	Definir cardinalidades (1,1 - 0,N - NM - 1,N)
	Nos relacionamentos NM, criar as entidades associativas

**5 - Dicionário de Dados**
	Criar a tabela de dados e descrever 
	Entidades e Atributos
	
	ENTIDADE | RELACIONAMENTO | NOME DO RELACIONAMENTO | DESCRIÇÃO
	  curso		  turma					gera				cadastro de cursos

	ATRIBUTO 		| TIPO DE DADOS  | COMPRIMENTO | RESTRIÇOES | DESCRIÇÃO 
	cod_curso             inteiro         4 bytes    PK, NOT NULL  Código de identificação   

**6 - Modelo lógico**
	Transformar o modelo conceitual em lógico

**7 - Normalização**
	
	1FN 
	** Existir uma chave primária
	** Possui somente valores atômicos (Não divisível)
	** Relação não possui atributos multivalorados ou relações aninhadas
	** Relação não possui atributos compostos

	2FN
	** Está na 1FN
	** Todos os atributos não-chave são funcionalmente dependentes de de todas as partes da PK
	** Não existem dependências parciais, e atributos não dependem de chaves candidatas
	Caso contrário, deve-se gerar uma nova tabela com os dados.
	Um atributo-chave é um que é uma PK ou parte de uma PK composta

	3FN
	** Está na 2FN
	** Não existirem dependências transitivas¹
	** Uma tabela está na 3FN se ela estiver na 2FN e se nenhuma coluna não chave depender de 		       outra coluna não chave
	** Para cada atributo (ou grupo) não-chave que for um determinante na relação, crie uma nova 		   tabela.
	** Esse atributo será a PK na nova relação
	** Mova então todos os atributos que são dependentes funcionalmente do atributo chave para a 		   nova tabela.
	** O atributo (PK na nova relação) fica também na tabela original, e servirá como uma chave 		   estrangeira para associar as relações.
	
	¹Dependência transitiva é uma dependência funcional entre dois ou mais atributos não-chave.
	Deve depender apenas dos atributos chaves da tabela
	Caso contrário, deve-se gerar uma nova tabela.


	Por fim refaz o Dicionário de Dados sem especificar as relações.

**8 - Implementação**

**9 - Testes Básicos**
