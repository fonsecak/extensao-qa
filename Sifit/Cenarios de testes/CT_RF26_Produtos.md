## Cenário 26: Consulta de Produtos.

### Caso de Teste 01: Acesso à tela de Produtos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C26-CT01 | A tela de Produtos deve apresentar a lista de produtos com nome, tipo, valor e status. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Produtos" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Total de produtos", "Ativos" e "Para venda" |
| **E** cada produto listado deve apresentar o nome, o tipo, o valor e o status |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Todo produto ativo e disponível para venda deve apresentar um nome preenchido. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O produto de código 8 está listado com o campo "Nome" em branco, status "Ativo" e disponível para venda com valor definido. Falha registrada em SIFIT-BUG-004. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/15.1.mp4) |

---

### Caso de Teste 02: Cadastro e exclusão de produto.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C26-CT02 | O sistema deve permitir cadastrar um novo produto com nome preenchido e excluí-lo em seguida. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Produto" |
| **QUANDO** preenchermos Nome, Tipo e Preço |
| **E** clicarmos em "Salvar" |
| **ENTÃO** o produto deve ser criado e listado; excluído em seguida pela ação de deletar |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Cadastro e exclusão concluídos com sucesso. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/15.2.mp4) |
