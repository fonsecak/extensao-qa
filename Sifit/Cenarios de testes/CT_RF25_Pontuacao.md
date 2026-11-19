## Cenário 25: Consulta de Pontuação.

### Caso de Teste 01: Acesso à tela de Pontuação e visualização de um registro.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C25-CT01 | A tela de Pontuação deve apresentar a lista de desafios e permitir a visualização dos detalhes e dos produtos de resgate vinculados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Pontuação" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Total", "Ativos", "Por período" e "Mensais" |
| **QUANDO** clicarmos na ação de visualizar de uma pontuação |
| **ENTÃO** devem ser exibidos o nome, o período, o tipo, o status e a seção "Produtos de resgate" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os dados exibidos na visualização devem corresponder ao registro selecionado. |
| O caso verifica a visualização; não alterar a pontuação. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/14.mp4) |
