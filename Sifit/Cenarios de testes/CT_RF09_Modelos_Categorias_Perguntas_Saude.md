## Cenário 09: Consulta e cadastro de Modelos, Categorias e Perguntas de Saúde.

### Caso de Teste 01: Acesso aos Modelos de Anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT01 | A tela de Modelos deve apresentar a busca e as ações disponíveis. |

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

### Caso de Teste 02: Abertura do formulário de novo modelo de anamnese.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT02 | O formulário de novo modelo deve apresentar os campos observados. |

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

### Caso de Teste 03: Acesso à tela de Perguntas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT03 | A tela de Perguntas deve apresentar filtros e ações de consulta. |

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

### Caso de Teste 04: Abertura do formulário de nova pergunta.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT04 | O formulário de pergunta deve apresentar os campos observados. |

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

### Caso de Teste 05: Acesso à tela de Categorias de Saúde.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT05 | A tela de Categorias deve apresentar a busca e a opção de cadastro. |

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

### Caso de Teste 06: Abertura do formulário de nova categoria.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT06 | O formulário de categoria deve apresentar os campos observados. |

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
