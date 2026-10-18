## Cenário 09: Consultas Financeiras.

### Caso de Teste 01: Acesso e visualização de Contas a Receber.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT01 | A tela de Contas a Receber deve apresentar os registros financeiros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Contas a Receber" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** os registros disponíveis devem ser apresentados para consulta |
| **E** valores, datas e situações devem estar visíveis quando disponíveis na listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não receber pagamentos nem alterar lançamentos. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.1.mp4) |

---

### Caso de Teste 02: Consulta e conferência de Contas a Receber.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT02 | Os filtros disponíveis devem apresentar contas a receber compatíveis com os critérios informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Contas a Receber. |
| Deve existir um registro financeiro autorizado para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Contas a Receber |
| **E** conhecemos um dado do registro que será consultado |
| **QUANDO** informarmos o critério nos filtros disponíveis e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar os registros correspondentes ao critério informado |
| **E** devemos conferir valor, data e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder aos critérios utilizados. |
| Valores, datas e situações apresentados devem corresponder ao registro consultado. |
| Não realizar recebimento ou alteração financeira. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.2.mp4) |

---

### Caso de Teste 03: Acesso e visualização de Contas a Pagar.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT03 | A tela de Contas a Pagar deve apresentar os registros financeiros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Contas a Pagar" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** os registros disponíveis devem ser apresentados para consulta |
| **E** valores, datas e situações devem estar visíveis quando disponíveis na listagem |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não pagar contas nem alterar lançamentos. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.3.mp4) |

---

### Caso de Teste 04: Consulta e conferência de Contas a Pagar.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT04 | Os filtros disponíveis devem apresentar contas a pagar compatíveis com os critérios informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Contas a Pagar. |
| Deve existir um registro financeiro autorizado para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Contas a Pagar |
| **E** conhecemos um dado do registro que será consultado |
| **QUANDO** informarmos o critério nos filtros disponíveis e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar os registros correspondentes ao critério informado |
| **E** devemos conferir valor, data e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder aos critérios utilizados. |
| Valores, datas e situações apresentados devem corresponder ao registro consultado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.4.mp4) |

---

### Caso de Teste 05: Acesso e visualização de Caixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT05 | A tela de Caixas deve apresentar os registros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Caixas" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** os registros de caixa disponíveis devem ser apresentados para consulta |
| **E** os valores, datas e situações devem estar visíveis quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não abrir, fechar ou movimentar caixa. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.5.mp4) |

---

### Caso de Teste 06: Consulta e conferência de informações de Caixa.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT06 | A consulta de um registro de caixa deve apresentar suas informações corretamente. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Caixas. |
| Deve existir um registro de caixa autorizado para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Caixas |
| **E** conhecemos um registro de caixa disponível |
| **QUANDO** abrirmos a opção de consulta desse registro, se disponível |
| **ENTÃO** as informações do caixa devem ser exibidas |
| **E** devemos conferir valores, datas e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| As informações exibidas devem corresponder ao registro de caixa consultado. |
| Caso não haja uma tela ou ação separada para visualizar detalhes, conferir os dados apresentados na listagem e registrar isso na evidência. |
| A consulta não deve abrir, fechar ou movimentar o caixa. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.6.mp4) |

---

### Caso de Teste 07: Acesso e visualização de Despesas Fixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT07 | A tela de Despesas Fixas deve apresentar os registros disponíveis para consulta. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** acessarmos o menu "Despesas Fixas" |
| **ENTÃO** a tela deve ser exibida sem mensagem de erro |
| **E** as despesas fixas disponíveis devem ser apresentadas para consulta |
| **E** os valores, datas e situações devem estar visíveis quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os registros devem ser exibidos ou o sistema deve indicar que não há registros para apresentar. |
| Este caso é somente de consulta; não cadastrar, editar ou excluir despesas. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.7.mp4) |

---

### Caso de Teste 08: Consulta e conferência de Despesas Fixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C09-CT08 | Os filtros disponíveis devem apresentar despesas fixas compatíveis com os critérios informados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Despesas Fixas. |
| Deve existir uma despesa fixa autorizada para consulta, com dados conhecidos para conferência. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Despesas Fixas |
| **E** conhecemos um dado da despesa fixa que será consultada |
| **QUANDO** informarmos o critério nos filtros disponíveis e realizarmos a consulta |
| **ENTÃO** o sistema deve apresentar as despesas correspondentes ao critério informado |
| **E** devemos conferir valor, data e situação com o registro consultado, quando disponíveis |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder aos critérios utilizados. |
| Valores, datas e situações apresentados devem corresponder à despesa consultada. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/9.8.mp4) |
