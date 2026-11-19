## Cenário 24: Consulta de Fornecedores e Tipos de Documentos.

### Caso de Teste 01: Acesso à tela de Fornecedores.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C24-CT01 | A tela de Fornecedores deve apresentar a lista de fornecedores cadastrados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Fornecedores" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Fornecedores Cadastrados" e "Fornecedores Ativos" |
| **E** a lista deve apresentar código, nome e status |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |

| **Vídeo Local** |
| :-------------------------------------------------------------- |
| Assistir vídeo: (../Videos/13.mp4) |

---

### Caso de Teste 02: Acesso à tela de Tipos de Documentos.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C24-CT02 | A tela de Tipos de Documentos deve apresentar a lista e os filtros de aplicação. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Tipos de Documentos" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Total", "Fornecedor" e "Colaborador" |
| **E** a lista deve apresentar o código, o nome e a aplicação de cada tipo |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A aplicação exibida deve corresponder ao tipo de documento (Colaborador ou Conta/Fornecedor). |

| **Vídeo Local** |
| :-------------------------------------------------------------- |
| Assistir vídeo: (../Videos/13.mp4) |
