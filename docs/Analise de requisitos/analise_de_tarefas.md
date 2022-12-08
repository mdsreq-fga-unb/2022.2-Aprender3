# <center>Análise de Tarefas

## 1. Introdução

A análise de tarefas nada mais é do que uma ferramenta de análise de dados para entender as etapas do processo de interação do usuário com o sistema. Isso consiste em dividir as tarefas em subtarefas, de forma que seja possível entender a sequência, hierarquia, condições e critérios de desempenho das tarefas a serem executadas. A análise de tarefas não tem o objetivo de avaliar a usabilidade do produto, somente de documentar o fluxo dos processos.

## 2. Análise Hierárquica de Tarefas (AHT)

Esta análise se inicia a partir dos objetivos do usuário para identificar as tarefas a serem realizadas a fim de atingir tais objetivos. Um plano serve para indicar a sequencia de tarefas que se deve realizar para atingir um determinado objetivo. Na notação textual, os itens de número zero representam os objetivos, os itens subsequentes são as tarefas e seus subitens representam sub tarefas. Uma operação é especiﬁcada pelas circunstâncias nas quais o objetivo é ativado (input ou entrada), pelas atividades ou ações (actions) que contribuem para atingi-lo e pelas condições que indicam o seu atingimento (feedback).Existem 3 tipos de notação[Tabela 1]:
 
 * **1>2** indica que o objetivo é sequencial;
 * **1+2** indica que o objetivo pode se executado em paralelo;
 * **1/2** indica que o objetivo é de seleção, ou seja, quando o usuário seleciona uma determinada opção.

![TabelaHTA](/docs/images/TabelaHTA.png)
 <figcaption align="center">Tabela HTA, Fonte([1])</figcaption>

### 2.1 Representação textual

#### 2.1.1 Representação textual do objetivo de se matricular em uma disciplina

**0.** Matrícula em disciplina
<br>&emsp;&emsp;**1.** Faça login
<br>&emsp;&emsp;&emsp;**1.1** Acesse o site do aprender 3
<br>&emsp;&emsp;&emsp;**1.2** Insira CPF e senha
<br>&emsp;&emsp;**2.** Localize a matéia desejada
<br>&emsp;&emsp;&emsp;**2.1** Acesse a busca de matérias (no "Search courses)
<br>&emsp;&emsp;&emsp;**2.2** Insira o nome da matéria desejada
<br>&emsp;&emsp;&emsp;**2.3** Pesquise pela matéria clicando na lupa
<br>&emsp;&emsp;**3.** Matricule-se na matéria
<br>&emsp;&emsp;&emsp;**3.1** Selecione a matéria desejada
<br>&emsp;&emsp;&emsp;**3.2** Insira a chave de inscrição (no campo "senha")

Plano 0: faça 1 - 2 - 3

Plano 1: faça 1 - 2 - 3 - 4

| Objetivos/ operações | Problemas e recomendações |
|:--------------------|:-------------------------|
| 0. Matrícula em disciplina | |
| 1. Faça login 1>2 |  **Input**: página do aprender 3 aberta.|
| 1.1 Acesse o site do aprender 3 1/2 | **Input**: Tela de login|
| 1.2 Insira CPF e senha 1+2 |  **Input**: identificação/senha; <br> **Action**: Inserir a identificação de usuário , senha e clicar no botão de acessar; <br>**Feedback**: Quando o site está com um grande número de acessos simultâneos se torna praticamente impossível o login; <br>**Problema**: Falha ao efetuar o login;<br> **Recomendação**: Tornar o sistema mais escalável|
| 2. Localize a matéia desejada 1>2 |  **Input**: Tela inicial do aprender após o login |
| 2.1 Acesse a busca de matérias  (no "Search courses) 1>2 |  **Input**: Barra de pesquisa na parte superior direita do site; <br> **Action**: clique no campo de pesquisa|
| 2.2 Insira o nome da matéria desejada 1>2 |  **Input**: Barra de pesquisa na parte superior direita do site;<br> **Action**: Digite o nome da matéria desejada|
| 2.3 Pesquise pela matéria clicando na lupa 1>2 |  **Input**: Barra de pesquisa na parte superior direita do site;<br>**Action**: clique na lupa;<br> **Feedback**: Ao pesquisar uma matéria a plataforma não oferece nenhum tipo de filtro, ou seja, mostra todos os resultados que contenham o nome pesquisado; <br>**Problema**: Como não tem filtro, se torna confuso achar a matéria desejada , pois além de ter 4 campus na universidade cada matéria tem várias turmas;<br> **Recomendação**: Realizar a criação de filtros para facilitar a pesquisa |
| 3. Matricule-se na matéria 1>2 | **Input**: Tela de pesquisa (após clicar na lupa) |
| 3.1 Selecione a matéria desejada 1/2 |  **Input**: Tela de pesquisa (após clicar na lupa);<br>**Feedback**: Assim que clicar na matéria selecionada o usuário será direcionado para a tela de matrícula da disciplina;<br>**Action**: Clicar na matéria selecionada|
| 3.2 Insira a chave de inscrição (no campo "senha") 1>2 |  **Input**: página de matrícula na disciplina; <br>**Feedback**: Esta tela mostra o nome do professor responsável pela matéria, uma menssagem de apresentação da disciplina e o grau da disciplina<br>**Problema**: Esta tela não tem a opção de vizualizar a senha antes de se matricular, o que atrapalha o usuário;<br>**Recomendações**: Criação de uma opção que permita o usuário vizualizar a senha que está sendo digitada antes de se matricular|


## 3. GOMS (Objetivos, Operadores, Métodos e Regras de seleção)
De acordo com Barbosa et al [1], o conjunto de modelos GOMS (Goals, Operators, Methods and Selection Rules - Objetivos, Operadores, Métodos e Regras de Seleção), visa analisar o desempenho de usuários que já dominam a ferramenta e não cometem erros, para fornecer uma representação formalizada que pode ser utilizada para prever o desempenho da tarefa.

### 3.1 Representação da tarefa de entregar um trabalho
O modelo GOMS a seguir é feito para analisar um usuário experiente utilizando a plataforma do aprender 3 para entregar um trabalho

GOAL 0
GOAL 0: Entregar um trabalho

GOAL 1: Fazer login

OP. 1.1: Acessar o site aprender

OP. 1.2: Preencher dados(CPF e Senha)

OP. 1.3: Clicar no botão acessar

GOAL 2: Localizar matéria

OP. 2.1: reupousar o mouse em cima do botão Meus cursos

OP. 2.2: clicar na opção desejada

GOAL 3: Localizar tarefa no meu matéria

OP. 3.1: clicar na tarefa

GOAL 4: Enviar tarefa

OP. 4.1: Clicar no botão adicionar tarefa

OP. 4.2: Clicar em Arquivos

OP. 4.3: Selecionar arquivo para fazer upload

OP. 4.4: Clicar em Salvar Mudanças


## Bibliografia
 [1] Barbosa, S. D. J.; Silva, B. S. da; Silveira, M. S.; Gasparini, I.; Darin, T.; Barbosa, G. D. J. (2021) Interação Humano-Computador e Experiência do usuário. Autopublicação. ISBN: 978-65-00-19677-1.
### Histórico de Versão
 
| Data       | Versão | Descrição            | Autor             | Revisor |
|:----------:|:------:|:--------------------:|:-----------------:|:-------:|
| 06.12.2022 | 1.0 | Realização da Análise de Tarefas | Igor Thiago | Milena Aires |
| 07.12.2022 | 1.1 | Padronizando histórico de versão | Milena Aires | Milena Aires |
| 07.12.2022 | 1.2 | Adicionado o GOMS | Thiago Vivan | Igor Thiago |
 
 
