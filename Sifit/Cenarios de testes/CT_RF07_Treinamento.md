## Cenário 07: Consulta e manutenção de itens de treinamento.

### Caso de Teste 01: Acesso à tela de Ficha de Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT01 | A tela de Ficha de Treino deve apresentar filtros e ações de consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Ficha de Treino" |
| **ENTÃO** a tela de Ficha de Treino deve ser exibida |
| **E** devem estar disponíveis os filtros "Código", "Nome do Aluno" e "Status" |
| **E** devem estar disponíveis as ações "Buscar", "Limpar filtros" e "Cadastrar Ficha" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 02: Abertura do formulário de Ficha de Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT02 | O formulário de Ficha de Treino deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Ficha de Treino. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Ficha de Treino |
| **QUANDO** clicarmos em "Cadastrar Ficha" |
| **ENTÃO** o formulário de Ficha de Treino deve ser exibido |
| **E** devem estar disponíveis os campos "Código e Nome do aluno", "Personal", "Data Inicial" e "Data Final" |
| **E** devem estar disponíveis os campos "Objetivo" e "Observação" |
| **E** devem estar disponíveis as ações "Pesquisar", "Cancelar", "Criar Nova Ficha" e "Usar Modelo de Ficha" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não selecionar aluno nem criar ficha. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 03: Acesso à biblioteca de Exercícios.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT03 | A biblioteca de Exercícios deve ser exibida organizada por grupos musculares. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Exercícios" |
| **ENTÃO** a biblioteca de exercícios deve ser exibida |
| **E** os exercícios devem estar organizados por grupos musculares |
| **E** deve estar disponível a ação "Adicionar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A biblioteca deve carregar sem apresentar mensagem de erro. |
| A organização por grupos musculares e a ação "Adicionar" devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 04: Abertura do formulário de exercício.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT04 | O formulário de exercício deve apresentar os campos de cadastro observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Exercícios. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na biblioteca de Exercícios |
| **QUANDO** clicarmos em "Adicionar" |
| **ENTÃO** o formulário de exercício deve ser exibido |
| **E** o campo "Nome" deve estar identificado como obrigatório |
| **E** devem estar disponíveis os campos "Código", "Imagem" e "Vídeo" |
| **E** devem estar disponíveis as ações "Fechar", "Cancelar" e "Salvar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não enviar arquivos nem salvar o exercício. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 05: Acesso à tela de Grupos Musculares.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT05 | A tela de Grupos Musculares deve apresentar os filtros e a ação de cadastro. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Grupos Musculares" |
| **ENTÃO** a tela de Grupos Musculares deve ser exibida |
| **E** devem estar disponíveis os filtros "Código", "Nome" e "Tipo Membro" |
| **E** devem estar disponíveis as ações "Buscar", "Limpar filtros" e "Cadastrar grupo" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 06: Abertura do formulário de grupo muscular.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT06 | O formulário de grupo muscular deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Grupos Musculares. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Grupos Musculares |
| **QUANDO** clicarmos em "Cadastrar grupo" |
| **ENTÃO** o formulário de grupo muscular deve ser exibido |
| **E** devem estar disponíveis os campos "Código", "Nome", "Tipo Membro" e "Imagem" |
| **E** devem estar disponíveis as ações "Salvar" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não enviar imagem nem salvar o grupo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 07: Acesso à tela de Objetivos Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT07 | A tela de Objetivos Treino deve apresentar filtros e a opção de cadastro. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Objetivos Treino" |
| **ENTÃO** a tela de Objetivos Treino deve ser exibida |
| **E** devem estar disponíveis os filtros "Código" e "Nome" |
| **E** devem estar disponíveis as ações "Buscar" e "Novo Objetivo" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |

---

### Caso de Teste 08: Abertura do formulário de objetivo de treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C07-CT08 | O formulário de objetivo deve apresentar os campos observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Objetivos Treino. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Objetivos Treino |
| **QUANDO** clicarmos em "Novo Objetivo" |
| **ENTÃO** o formulário de objetivo deve ser exibido |
| **E** devem estar disponíveis os campos "Código", "Nome" e "Descrição" |
| **E** devem estar disponíveis as ações "Salvar" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não salvar o objetivo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: |
