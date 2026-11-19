## Cenário 17: Consulta de Caixas.

### Caso de Teste 01: Acesso e visualização de Caixas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C17-CT01 | A tela de Caixas deve apresentar os registros disponíveis para consulta. |

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

### Caso de Teste 02: Consulta e conferência de informações de Caixa.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C17-CT02 | A consulta de um registro de caixa deve apresentar suas informações corretamente. |

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
