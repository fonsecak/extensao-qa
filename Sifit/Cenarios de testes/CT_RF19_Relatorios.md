## Cenário 19: Geração e consulta de relatórios.

### Caso de Teste 01: Acesso à tela de Relatórios.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C19-CT01 | A tela de Relatórios deve apresentar os modelos disponíveis e os filtros de geração. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Relatórios" |
| **ENTÃO** a tela de Relatórios deve ser exibida |
| **E** devem ser apresentados os indicadores "Relatórios", "Filtros ativos", "Período" e "Saída" |
| **E** deve estar disponível o painel "Tipos" com os modelos de relatório |
| **E** deve estar disponível o painel "Gerar Relatório" com os filtros e a ação "Gerar Relatório" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| Os sete modelos devem ser listados: Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar e Caixas. |
| O indicador de saída deve informar o formato PDF. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/35999e03-d751-472b-8910-72e6da8b5d1b |

---

### Caso de Teste 02: Seleção do tipo de relatório.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C19-CT02 | A seleção de um modelo deve atualizar o formulário de geração. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Relatórios. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Relatórios |
| **E** o modelo "Avaliações" está selecionado por padrão |
| **QUANDO** selecionarmos o modelo "Clientes" no painel "Tipos" |
| **ENTÃO** o campo "Tipo de Relatório" deve ser atualizado para "Clientes" |
| **E** a descrição do painel deve ser atualizada para "Cadastro e situação dos alunos" |
| **E** o indicador do modelo selecionado deve ser atualizado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A troca de modelo deve ser refletida no formulário sem recarregar a página. |
| A descrição apresentada deve corresponder ao modelo selecionado. |
| O caso verifica a seleção do modelo; a geração do arquivo é tratada no C19-CT04. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/a6c6264c-f7dd-442c-b66e-3e269c9b2620 |

---

### Caso de Teste 03: Exibição dos filtros específicos por modelo.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C19-CT03 | Os filtros apresentados devem variar conforme o modelo de relatório selecionado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Relatórios. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Relatórios com o modelo "Clientes" selecionado |
| **E** observamos que são exibidos apenas os filtros "Data Início" e "Data Fim" |
| **QUANDO** selecionarmos o modelo "Matrículas" |
| **ENTÃO** devem ser exibidos também os filtros "Planos" e "Tipo de Plano" |
| **E** os filtros adicionais devem apresentar a opção "Todos" como valor inicial |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os filtros adicionais devem ser exibidos apenas para os modelos que os utilizam. |
| O formulário deve se reorganizar sem apresentar mensagem de erro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/53e80559-5b9e-4149-baea-38d7a9516e60 |

---

### Caso de Teste 04: Geração de relatório com período válido.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C19-CT04 | O relatório deve ser gerado quando os filtros forem preenchidos corretamente. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Relatórios. |
| Um modelo de relatório deve estar selecionado. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Relatórios com o modelo "Avaliações" selecionado |
| **E** informamos "01/11/2026" no campo "Data Início" |
| **E** informamos "18/11/2026" no campo "Data Fim" |
| **QUANDO** clicarmos em "Gerar Relatório" |
| **ENTÃO** o sistema deve processar a solicitação sem apresentar erro |
| **E** o arquivo em formato PDF deve ser disponibilizado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A solicitação deve ser concluída com sucesso. |
| O conteúdo do arquivo deve corresponder ao modelo e ao período informados. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O relatório gerado estava vazio e não abria  |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/86160793-0630-4919-9606-9e728c458bc0 |

---

### Caso de Teste 05: Tentativa de geração com período invertido.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C19-CT05 | O sistema deve validar o período quando a data inicial for posterior à data final. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Relatórios. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Relatórios com um modelo selecionado |
| **E** informamos "31/12/2026" no campo "Data Início" |
| **E** informamos "18/11/2026" no campo "Data Fim" |
| **QUANDO** clicarmos em "Gerar Relatório" |
| **ENTÃO** o sistema deve apresentar uma mensagem informando que o período é inválido |
| **E** a solicitação não deve ser enviada para processamento |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O sistema deve impedir a geração quando a data inicial for posterior à data final. |
| A mensagem apresentada deve indicar a correção necessária. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O sistema aceita o período invertido, não apresenta mensagem de validação e envia a solicitação para processamento. Falha registrada em SIFIT-BUG-002. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/8b73b890-09dd-438c-a4b5-acd34e979e43 |

---
