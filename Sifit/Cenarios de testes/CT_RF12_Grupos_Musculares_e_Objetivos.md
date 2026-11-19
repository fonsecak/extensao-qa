## Cenário 12: Consulta e cadastro de Grupos Musculares e Objetivos de Treino.

### Caso de Teste 01: Acesso à tela de Grupos Musculares.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT01 | A tela de Grupos Musculares deve apresentar os filtros e a ação de cadastro. |

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
| [Assistir ao vídeo](../Videos/7.5.mp4)

---

### Caso de Teste 02: Abertura do formulário de grupo muscular.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT02 | O formulário de grupo muscular deve apresentar os campos observados. |

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
| [Assistir ao vídeo](../Videos/7.6.mp4)

---

### Caso de Teste 03: Acesso à tela de Objetivos Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT03 | A tela de Objetivos Treino deve apresentar filtros e a opção de cadastro. |

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
| [Assistir ao vídeo](../Videos/7.7.mp4)

---

### Caso de Teste 04: Abertura do formulário de objetivo de treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT04 | O formulário de objetivo deve apresentar os campos observados. |

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
| [Assistir ao vídeo](../Videos/7.8.mp4)

---

### Caso de Teste 05: Cadastro e exclusão de Grupo Muscular.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT05 | O sistema deve permitir cadastrar um novo grupo muscular e excluí-lo em seguida. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e no formulário de novo grupo muscular. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Grupo Muscular" |
| **QUANDO** preenchermos Nome e Tipo Membro |
| **E** clicarmos em "Salvar" |
| **ENTÃO** o grupo deve ser criado e listado |
| **QUANDO** buscarmos esse grupo e clicarmos em excluir, confirmando |
| **ENTÃO** o grupo deve ser removido da listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O cadastro e a exclusão devem ser concluídos com sucesso. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/e4e3b172-39d6-4845-b2e3-28eeb95085ab |

---

### Caso de Teste 06: Cadastro e exclusão de Objetivo de Treino.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C12-CT06 | O sistema deve permitir cadastrar um novo objetivo de treino e excluí-lo em seguida. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e no formulário de novo objetivo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Novo Objetivo" |
| **QUANDO** preenchermos o campo "Nome" |
| **E** clicarmos em "Salvar" |
| **ENTÃO** o objetivo deve ser criado e listado |
| **QUANDO** clicarmos em excluir esse objetivo e confirmarmos |
| **ENTÃO** o objetivo deve ser removido da listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O cadastro e a exclusão devem ser concluídos com sucesso. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Cadastro e exclusão funcionaram, mas o indicador "Objetivos" e a contagem "N registro(s)" não refletiram o novo item logo após o cadastro, exigindo rolagem/nova busca para ver o registro na lista — comportamento semelhante ao observado em outros indicadores do sistema (não bloqueante). |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/f440bf8c-a468-4311-820a-1dadb3bf2d8a |
