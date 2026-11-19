## Cenário 15: Consulta de Contas a Receber.

### Caso de Teste 01: Acesso e visualização de Contas a Receber.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C15-CT01 | A tela de Contas a Receber deve apresentar os registros financeiros disponíveis para consulta. |

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
| C15-CT02 | Os filtros disponíveis devem apresentar contas a receber compatíveis com os critérios informados. |

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
