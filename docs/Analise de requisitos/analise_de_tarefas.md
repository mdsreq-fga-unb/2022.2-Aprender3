# <center>Análise de Tarefas

### Histórico de Versão
| Data       | Versão | Descrição            | Autor             |
|:----------:|:------:|:--------------------:|:-----------------:|
| 06.12.2022 | 1.0 | Realização da Análise de Tarefas | Igor Thiago |

## 1. Introdução
A análise de tarefas nada mais é do que uma ferramenta de análise de dados para entender as etapas do processo de interação do usuário com o sistema. Isso consiste em dividir as tarefas em subtarefas, de forma que seja possível entender a sequência, hierarquia, condições e critérios de desempenho das tarefas a serem executadas. A análise de tarefas não tem o objetivo de avaliar a usabilidade do produto, somente de documentar o fluxo dos processos. 

## 2. Análise Hierárquica de Tarefas (AHT)
Esta análise se inicia a partir dos objetivos do usuário para identificar as tarefas a serem realizadas a fim de atingir tais objetivos. Um plano serve para indicar a sequencia de tarefas que se deve realizar para atingir um determinado objetivo. Na notação textual, os itens de número zero representam os objetivos, os itens subsequentes são as tarefas e seus subitens representam sub tarefas.

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

Plano 1: faça 1.1 - 1.2

Plano 2: faça 2.1 - 2.2 - 2.3

Plano 3: faça 3.1 - 3.2

| Objetivos/ operações | Problemas e recomendações |
|:--------------------|:-------------------------|
| 0. Matrícula em disciplina | |
| 1. Faça login |  **Input**: página do aprender 3 aberta.|
| 1.1 Acesse o site do aprender 3 | **Input**: Tela de login|
| 1.2 Insira CPF e senha |  **Input**: identificação/senha; <br> **Action**: Inserir a identificação de usuário , senha e clicar no botão de acessar; <br>**Feedback**: Quando o site está com um grande número de acessos simultâneos se torna praticamente impossível o login; <br>**Problema**: Falha ao efetuar o login;<br> **Recomendação**: Aumentar a capacidade de usuários simultâneos da plataforma|
| 2. Localize a matéia desejada |  **Input**: Tela inicial do aprender após o login |
| 2.1 Acesse a busca de matérias (no "Search courses) |  **Input**: Barra de pesquisa na parte superior direita do site; <br> **Action**: clique no campo de pesquisa|
| 2.2 Insira o nome da matéria desejada |  **Input**: Barra de pesquisa na parte superior direita do site;<br> **Action**: Digite o nome da matéria desejada|
| 2.3 Pesquise pela matéria clicando na lupa |  **Input**: Barra de pesquisa na parte superior direita do site;<br>**Action**: clique na lupa;<br> **Feedback**: Ao pesquisar uma matéria a plataforma não oferece nenhum tipo de filtro, ou seja, mostra todos os resultados que contenham o nome pesquisado; <br>**Problema**: Como não tem filtro, se torna confuso achar a matéria desejada , pois além de ter 4 campus na universidade cada matéria tem várias turmas;<br> **Recomendação**: Realizar a criação de filtros para facilitar a pesquisa |
| 3. Matricule-se na matéria | **Input**: Tela de pesquisa (após clicar na lupa) | 
| 3.1 Selecione a matéria desejada |  **Input**: Tela de pesquisa (após clicar na lupa);<br>**Feedback**: Assim que clicar na matéria selecionada o usuário será direcionado para a tela de matrícula da disciplina;<br>**Action**: Clicar na matéria selecionada|
| 3.2 Insira a chave de inscrição (no campo "senha") |  **Input**: página de matrícula na disciplina; <br>**Feedback**: Esta tela mostra o nome do professor responsável pela matéria, uma menssagem de apresentação da disciplina e o grau da disciplina<br>**Problema**: Esta tela não tem a opção de vizualizar a senha antes de se matricular, o que atrapalha o usuário;<br>**Recomendações**: Criação de uma opção que permita o usuário vizualizar a senha que está sendo digitada antes de se matricular|