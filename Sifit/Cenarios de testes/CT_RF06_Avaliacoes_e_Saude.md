## Cenário 06: Avaliações e Saúde.

### Caso de Teste 01: Acesso à tela de Avaliações.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT01 | A tela de Avaliações deve apresentar os filtros e as ações disponíveis. |

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
| Link: | https://jam.dev/c/703c8795-d8b7-4940-a50e-0472082c95f0

---

### Caso de Teste 02: Abertura do formulário de cadastro de avaliação.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT02 | O formulário de cadastro de avaliação deve apresentar os campos observados. |

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
| Link: | https://jam.dev/c/6c1ac3b7-3e65-4cd5-810d-467aca48afa6

---

### Caso de Teste 03: Acesso à tela de Fichas Anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT03 | A tela de Fichas Anamnese deve apresentar a busca e a opção de nova anamnese. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Fichas Anamnese" |
| **ENTÃO** a tela de Fichas Anamnese deve ser exibida |
| **E** deve estar disponível a busca por cliente |
| **E** deve estar disponível a ação "Nova Anamnese" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Fichas Anamnese deve carregar sem apresentar mensagem de erro. |
| A busca e a ação "Nova Anamnese" devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/ceb02381-78af-44e8-a599-efbac11d7b6e

---

### Caso de Teste 04: Abertura do fluxo de aplicação de anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT04 | O fluxo de nova anamnese deve iniciar pela seleção do aluno. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Fichas Anamnese. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Fichas Anamnese |
| **QUANDO** clicarmos em "Nova Anamnese" |
| **ENTÃO** o primeiro passo para aplicar anamnese deve ser exibido |
| **E** deve estar disponível a busca pelo nome do aluno |
| **E** deve ser apresentada a etapa "Selecionar Aluno" e a ação "Próxima" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O primeiro passo deve abrir sem apresentar mensagem de erro. |
| A busca do aluno, a etapa e a ação descritas devem estar disponíveis. |
| O caso verifica o primeiro passo; não selecionar aluno nem avançar. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/eee96adc-dd9c-4464-8f1c-6e2fd3aabb50

---

### Caso de Teste 05: Acesso aos Modelos de Anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT05 | A tela de Modelos deve apresentar a busca e as ações disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Modelos" da área de Saúde |
| **ENTÃO** a tela de Modelos deve ser exibida |
| **E** deve estar disponível a busca por modelo |
| **E** devem estar disponíveis as ações "Novo Modelo", "Editar" e "Preview" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Modelos deve carregar sem apresentar mensagem de erro. |
| A busca e as ações descritas devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/eee96adc-dd9c-4464-8f1c-6e2fd3aabb50

---

### Caso de Teste 06: Abertura do formulário de novo modelo de anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT06 | O formulário de novo modelo deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Modelos da área de Saúde. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Modelos da área de Saúde |
| **QUANDO** clicarmos em "Novo Modelo" |
| **ENTÃO** o formulário de modelo de anamnese deve ser exibido |
| **E** o campo "Nome do Modelo" deve estar identificado como obrigatório |
| **E** devem estar disponíveis os campos "Status" e "Descrição" |
| **E** devem estar disponíveis a busca por pergunta e as ações "Salvar Modelo" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| O campo obrigatório, os demais campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não incluir perguntas nem salvar o modelo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/eee96adc-dd9c-4464-8f1c-6e2fd3aabb50

---

### Caso de Teste 07: Acesso à tela de Perguntas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT07 | A tela de Perguntas deve apresentar filtros e ações de consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Perguntas" da área de Saúde |
| **ENTÃO** a tela de Perguntas deve ser exibida com os campos "Código", "Nome" e "Status" |
| **E** devem estar disponíveis as ações "Buscar" e "Nova Pergunta" |
| **E** a listagem deve apresentar as colunas "Código", "Nome", "Pergunta", "Tipo Resposta" e "Status" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os campos, ações e colunas descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/1a7a7a63-6199-4340-bc47-e674c4a2b1d8

---

### Caso de Teste 08: Abertura do formulário de nova pergunta.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT08 | O formulário de pergunta deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Perguntas da área de Saúde. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Perguntas da área de Saúde |
| **QUANDO** clicarmos em "Nova Pergunta" |
| **ENTÃO** o formulário de pergunta deve ser exibido |
| **E** devem estar disponíveis os campos "Código", "Nome", "Status", "Pergunta", "Número" e "Tipo Resposta" |
| **E** devem estar disponíveis as ações "Salvar" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não salvar a pergunta. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/1a7a7a63-6199-4340-bc47-e674c4a2b1d8

---

### Caso de Teste 09: Acesso à tela de Categorias de Saúde.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT09 | A tela de Categorias deve apresentar a busca e a opção de cadastro. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Categorias" da área de Saúde |
| **ENTÃO** a tela de Categorias deve ser exibida |
| **E** deve estar disponível a busca por categoria |
| **E** deve estar disponível a ação "Nova Categoria" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Categorias deve carregar sem apresentar mensagem de erro. |
| A busca e a ação "Nova Categoria" devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/5b61fd5b-6075-439d-8709-47c2587de42a

---

### Caso de Teste 10: Abertura do formulário de nova categoria.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT10 | O formulário de categoria deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Categorias da área de Saúde. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Categorias da área de Saúde |
| **QUANDO** clicarmos em "Nova Categoria" |
| **ENTÃO** o formulário de categoria deve ser exibido |
| **E** o campo "Nome da Categoria" deve estar identificado como obrigatório |
| **E** devem estar disponíveis os campos "Status", "Ícone" e "Cor" |
| **E** devem estar disponíveis as ações "Cancelar" e "Criar Categoria" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| O campo obrigatório, os demais campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não salvar a categoria. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/e4718dfe-0b85-400a-8eda-767e6159137a
