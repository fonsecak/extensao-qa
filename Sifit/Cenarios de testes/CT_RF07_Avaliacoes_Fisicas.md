## Cenário 07: Consulta, agendamento e preenchimento de avaliações físicas.

### Caso de Teste 01: Acesso à tela de Avaliações.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT01 | A tela de Avaliações deve apresentar os filtros e as ações disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Avaliações" |
| **ENTÃO** a tela de Avaliações deve ser exibida |
| **E** devem estar disponíveis os filtros "Código", "Nome" e "Status" |
| **E** devem estar disponíveis as ações "Buscar" e "Cadastrar Avaliação" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Avaliações deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/703c8795-d8b7-4940-a50e-0472082c95f0 |

---

### Caso de Teste 02: Abertura do formulário de cadastro de avaliação.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT02 | O formulário de cadastro de avaliação deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Avaliações. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Avaliações |
| **QUANDO** clicarmos em "Cadastrar Avaliação" |
| **ENTÃO** o formulário de cadastro deve ser exibido |
| **E** devem estar disponíveis os campos de aluno, Personal, Data e Hora |
| **E** devem estar disponíveis as ações "Buscar aluno", "Salvar" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não selecionar aluno nem salvar avaliação. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link:  https://jam.dev/c/6c1ac3b7-3e65-4cd5-810d-467aca48afa6 |

---

### Caso de Teste 03: Preenchimento de uma avaliação agendada.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT03 | O sistema deve permitir preencher os dados de uma avaliação já agendada para um cliente. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir uma avaliação agendada, com status "Pendente", para um cliente de teste. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na listagem de Avaliações |
| **QUANDO** clicarmos em "Fazer Avaliação" em uma avaliação pendente |
| **ENTÃO** o formulário com as abas "IMC", "Circunferência", "Teste Físico" e "Composição Corporal" deve ser exibido |
| **E** devem estar disponíveis os campos "Altura" e "Peso" na aba "IMC" |
| **QUANDO** preenchermos Altura e Peso e clicarmos em "Salvar" |
| **ENTÃO** a avaliação deve ser salva com status "Realizado" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O IMC deve ser calculado automaticamente a partir da altura e do peso informados. |
| A avaliação deve ser salva com sucesso. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O IMC foi calculado corretamente na pré-visualização do formulário ("26 - Sobrepeso"), mas ao clicar em "Salvar" o sistema apresenta a mensagem "Erro ao salvar avaliação", com `POST /api/avaliacao/salvarFeita/1` retornando HTTP 500. Falha registrada em SIFIT-BUG-011. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/aaf7b244-047b-4d35-81f0-6fb0923db243 |
