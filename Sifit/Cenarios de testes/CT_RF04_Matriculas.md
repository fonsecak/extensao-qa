## Cenário 04: Consulta, cadastro, edição e cancelamento de matrículas.

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

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/18699c5a-cab8-42da-ad76-884623c80b3d

---

### Caso de Teste 04: Cadastro de nova matrícula.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT04 | O sistema deve permitir vincular uma matrícula a um cliente existente. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir um cliente sem matrícula ativa. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Matrículas |
| **QUANDO** clicarmos em "Cadastrar Matrícula" |
| **E** selecionarmos um cliente pela busca |
| **E** selecionarmos uma Modalidade, um Tipo de Pagamento e um Dia de Vencimento |
| **E** clicarmos em "Salvar" |
| **ENTÃO** a matrícula deve ser criada e vinculada ao cliente |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A matrícula deve ser salva com sucesso para qualquer combinação válida de modalidade e tipo de pagamento. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O cadastro falha em toda tentativa, com a mensagem "Erro ao Cadastrar com Assinatura" e resposta HTTP 400 em `POST /api/salvar/matricula/1`. Testado com dois planos diferentes ("Treino Livre" e "Teste Final") e dois tipos de pagamento ("Manual SIFIT Pix" e "Dinheiro"), todos com o mesmo erro. Não foi possível concluir nenhum cadastro novo de matrícula. Falha crítica registrada em SIFIT-BUG-009. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 05: Edição de matrícula existente.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT05 | O sistema deve permitir editar os dados de uma matrícula já cadastrada. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir uma matrícula de teste cadastrada. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na visualização de uma matrícula de teste |
| **QUANDO** clicarmos no ícone de editar |
| **E** alterarmos o campo "Observação" |
| **E** clicarmos em "Salvar" |
| **ENTÃO** a alteração deve ser refletida na visualização da matrícula |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A alteração deve ser salva e exibida corretamente ao reabrir a visualização. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 06: Cancelamento de matrícula.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C04-CT06 | O sistema deve permitir cancelar uma matrícula ativa, mediante confirmação. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir uma matrícula de teste com status "Ativo". |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na listagem de Matrículas |
| **QUANDO** clicarmos em "Cancelar" em uma matrícula de teste |
| **ENTÃO** deve ser exibido o campo "Motivo de Cancelamento" |
| **QUANDO** clicarmos em "Cancelar Matrícula" sem preencher o motivo |
| **ENTÃO** o sistema deve exibir a confirmação "Deseja cancelar essa matrícula?" |
| **QUANDO** confirmarmos |
| **ENTÃO** a matrícula deve mudar para o status "Cancelado" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O cancelamento deve exigir confirmação explícita. |
| A matrícula cancelada deve sair da contagem de matrículas ativas. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O cancelamento foi concluído com sucesso. O campo "Motivo de Cancelamento" não possui indicação visual de obrigatório e o sistema aceita o cancelamento mesmo sem texto informado — comportamento a confirmar com o time se é intencional. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |
