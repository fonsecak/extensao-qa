## Cenário 30: Consulta de Modelo Ficha.

### Caso de Teste 01: Acesso à tela de Modelo Ficha.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C30-CT01 | A tela de Modelo Ficha deve listar os modelos cadastrados com o título correspondente. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Modelo Ficha" |
| **ENTÃO** a tela "Modelos de Ficha" deve ser exibida com os indicadores "Modelos", "Criadores", "Listados" e "Sem Criador" |
| **E** a coluna "Título" deve exibir o título cadastrado de cada modelo |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A coluna "Título" deve corresponder ao nome cadastrado de cada modelo. |
| A ação de alterar um modelo deve abrir a edição do próprio modelo de ficha. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Todos os seis registros da listagem exibem "Sem título" na coluna "Título". A ação "Alterar" de cada linha direciona para a rota "/ficha-treino/alterar/{codigo}", que abre a tela de Ficha de Treino de um aluno específico ("Treino de Manual SIFIT Aluno Exemplo"), e não um editor de modelo de ficha. Falha registrada em SIFIT-BUG-007. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: [Assistir ao vídeo C30-CT01](https://jam.dev/c/cd2a7b2e-2296-4561-b515-2f66d89006be) | 
