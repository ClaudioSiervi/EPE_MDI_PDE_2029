### Instruções Básicas do Modelo Computacional MDI   

#### Introdução
O modelo computacional MDI (modelo de decisão de investimentos), empregado na elaboração do Plano Decenal de Expansão de Energia 2029 (PDE 2029), é disponibilizado em código-fonte aberto para permitir máxima transparência na modelagem matemática e implementação. Esta disponibilização também permite que instituições, centros de pesquisa e agentes do setor, bem como a comunidade acadêmica, possam contribuir efetivamente para o aprimoramento do modelo.


#### Pré-requisitos mínimos

• Python 3.x;
• Bibliotecas da própria linguagem importadas ao longo do código (pyomo, openpyxl, etc);
* As bibliotecas utilizadas pelo MDI podem ser obtidas diretamente pela ferramenta de gerenciamento de pacotes pip, disponibilizada na instalação padrão do Python.

• Pacote de otimização (CPLEX, COIN-OR, Gurobi, etc).


#### Ambiente computacional utilizado nos estudos do PDE 2029
•	Python 3.6
•	CPLEX Studio 12.2
•	MS Windows Server 2012 R2
•	MS Excel 2013

#### Instruções básicas para execução


_Interface para execução_
A execução é feita a partir da pasta de trabalho MS Excel “Dados_MDI_PDE_2029.xlsx” (disponibilizada junto com o código-fonte), que também contém todos os dados necessários para a montagem do problema de otimização resolvido pelo MDI.

_Configurações Iniciais_
Inicialmente é necessário configurar o caminho para o pacote de otimização, editando-se o arquivo "Control. py" (linha 36), conforme figura a seguir:

![Figura1](https://user-images.githubusercontent.com/16821891/70325274-63bb8b00-1810-11ea-803f-d613413e63f6.png?raw=true "Editar Control.py")

Em seguida, é necessário configurar, na planilha “Inicial” da pasta de trabalho “Dados_MDI_PDE_2029.xlsx”, o caminho completo do arquivo “Principal .py”, que deve estar salvo na mesma pasta dos demais arquivos de código-fonte. Outra informação declarada nesta planilha é o executável do Python 3.x, conforme destacado na figura a seguir:

![Figura2](https://user-images.githubusercontent.com/16821891/70325410-ab421700-1810-11ea-91b2-3f3422a4930b.png?raw=true "Editar Principal.py")


_Execução_
A execução é feita a partir do botão “Executar MDI” disponível na mesma planilha onde foram feitas as configurações iniciais.

#### Saídas
As saídas (em formato txt ou csv) são geradas no mesmo caminho onde se encontra a pasta de trabalho que iniciou a execução.
A pasta de trabalho “Resumo.xlsx”, que deve também estar no mesmo caminho, ao final da execução, será preenchida com o resumo da expansão bem como os valores de CME solicitados anualmente.

