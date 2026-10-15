## Cenário 04: Consulta de matrículas e planos.

### Caso de Teste 01: Acesso à tela de Matrículas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT01 | A tela de Matrículas deve apresentar os filtros e as ações disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Matrículas" |
| **ENTÃO** a tela de Matrículas deve ser exibida |
| **E** devem estar disponíveis os campos "Código" e "Nome" |
| **E** devem estar disponíveis as ações "Buscar", "Buscar por data" e "Cadastrar Matrícula" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Matrículas deve carregar sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/173298ab-ca02-4148-984a-7b017b57c0fd

---

### Caso de Teste 02: Busca de matrícula por código ou nome.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT02 | A busca deve apresentar a matrícula correspondente ao código ou nome informado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Matrículas. |
| Deve existir uma matrícula de teste conhecida e autorizada para consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Matrículas |
| **E** informamos o código ou nome conhecido nos campos correspondentes |
| **QUANDO** clicarmos no botão "Buscar" |
| **ENTÃO** o sistema deve apresentar a matrícula correspondente aos dados informados |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O resultado deve corresponder ao código ou nome usado na busca. |
| Os dados exibidos devem corresponder à matrícula de teste consultada. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d4864384-da0e-4714-b2d9-85133579ac68

---

### Caso de Teste 03: Abertura do formulário de cadastro de matrícula.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT03 | O formulário de matrícula deve apresentar os campos de cadastro observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Matrículas. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Matrículas |
| **QUANDO** clicarmos em "Cadastrar Matrícula" |
| **ENTÃO** o formulário de matrícula deve ser exibido |
| **E** devem estar disponíveis os campos "Nome", "Modalidade", "Data Inicial" e "Data Final" |
| **E** devem estar disponíveis os campos "Tipo Pagamento", "Taxa Matrícula", "Dia Vencimento", "Valor Parcela", "Desconto" e "Valor Total" |
| **E** devem estar disponíveis as ações "Salvar" e "Cancelar" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos e as ações descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não selecionar cliente ou modalidade nem salvar a matrícula. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/18699c5a-cab8-42da-ad76-884623c80b3d

---

### Caso de Teste 04: Acesso e busca de planos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT04 | A tela de Planos deve permitir consultar planos pelos filtros disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Planos" |
| **ENTÃO** a tela de Planos deve ser exibida com os filtros "Código", "Nome" e "Status" |
| **E** devem estar disponíveis as ações "Buscar" e "Novo Plano" |
| **QUANDO** informarmos o nome de um plano de teste conhecido no filtro "Nome" e clicarmos em "Buscar" |
| **ENTÃO** o sistema deve apresentar o plano correspondente ao nome informado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os filtros e as ações descritos devem estar disponíveis. |
| A busca deve apresentar o plano correspondente ao nome utilizado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/e585dca2-d7a1-4d6b-9083-c07768215220

---

### Caso de Teste 05: Abertura do formulário de novo plano.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT05 | O formulário de plano deve apresentar os campos de cadastro observados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Planos. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Planos |
| **QUANDO** clicarmos em "Novo Plano" |
| **ENTÃO** o formulário de plano deve ser exibido |
| **E** devem estar disponíveis os campos "Nome", "Grupo", "Status", "Cobrança", "Parcelas", "Valor Mensal" e "Valor Matrícula" |
| **E** deve estar disponível a ação "Salvar Plano" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O formulário deve abrir sem apresentar mensagem de erro. |
| Os campos descritos devem estar disponíveis. |
| O caso verifica a abertura do formulário; não salvar o plano nem selecionar a opção "Salvar também na Pagar.me". |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/e585dca2-d7a1-4d6b-9083-c07768215220
