## Cenário 06: Check-in e consulta de presenças.

### Caso de Teste 01: Acesso à tela de Check-in.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT01 | A tela de Check-in deve apresentar os filtros e as ações disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Check-in" |
| **ENTÃO** a tela de Check-in deve ser exibida |
| **E** devem estar disponíveis as opções "Todos", "Presentes agora", "Não compareceram" e "Check-in pendente" |
| **E** devem estar disponíveis as ações "Filtros", "Check-in manual" e "Escanear QR Code" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela de Check-in deve carregar sem apresentar mensagem de erro. |
| As opções e ações descritas devem estar disponíveis. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/e95ff95c-6701-447f-9b9c-0875c321de45

---

### Caso de Teste 02: Busca de cliente na tela de Check-in.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT02 | A busca deve localizar o cliente conforme o dado informado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Check-in. |
| Deve existir um cliente de teste conhecido e autorizado para consulta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Check-in |
| **E** informamos o nome, código ou plano conhecido no campo de busca |
| **QUANDO** realizarmos a busca |
| **ENTÃO** o sistema deve exibir os registros correspondentes ao dado informado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder ao nome, código ou plano informado. |
| Os dados exibidos devem pertencer ao cliente de teste consultado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d6b24cd6-57f2-47c7-9d89-0cec822c27df

---

### Caso de Teste 03: Abertura do registro manual de entrada.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT03 | A opção de Check-in manual deve apresentar o formulário de entrada. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Check-in. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Check-in |
| **QUANDO** clicarmos em "Check-in manual" |
| **ENTÃO** a janela "Entrada manual" deve ser exibida |
| **E** deve estar disponível a busca por nome, código, CPF ou telefone |
| **E** devem estar disponíveis as opções "Cliente existente", "Visitante/Aula experimental" e "Sem biometria" |
| **E** devem estar disponíveis as ações "Fechar", "Cancelar" e "Registrar entrada" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A janela "Entrada manual" deve abrir e apresentar os controles descritos. |
| O caso verifica a abertura do formulário; não registrar entrada. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d6b24cd6-57f2-47c7-9d89-0cec822c27df

---

### Caso de Teste 04: Consulta de presenças por período.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT04 | A consulta deve exibir as presenças do cliente no período informado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |
| Deve existir um cliente de teste conhecido com presença registrada no período consultado. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Presenças" |
| **ENTÃO** a tela de Presenças deve ser exibida com os campos "Cliente", "De" e "Até" |
| **E** devem estar disponíveis as ações "Buscar", "Hoje", "Esta semana" e "Este mês" |
| **QUANDO** selecionarmos o cliente de teste e informarmos um período conhecido |
| **E** clicarmos em "Buscar" |
| **ENTÃO** o sistema deve exibir as presenças do cliente dentro do período informado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Os campos e ações de consulta devem estar disponíveis. |
| As presenças exibidas devem pertencer ao cliente e ao período informados. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: | https://jam.dev/c/d6b24cd6-57f2-47c7-9d89-0cec822c27df

---

### Caso de Teste 05: Registro de entrada e atualização da tela de Check-ins.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C06-CT05 | O registro de um check-in deve atualizar o status da linha e o indicador "Check-ins hoje" na mesma tela. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| Deve existir um cliente pendente na listagem de Check-ins. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Check-ins, com um cliente de teste listado como "Pendente" |
| **QUANDO** clicarmos em "Registrar entrada" na linha desse cliente |
| **ENTÃO** o status da linha deve mudar de "Pendente" para indicar entrada registrada |
| **E** o indicador "Check-ins hoje" deve ser incrementado |
| **QUANDO** repetirmos o check-in pelo campo "Entrada rápida", informando o código do mesmo cliente |
| **ENTÃO** o indicador "Check-ins hoje" deve refletir o novo check-in registrado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Cada check-in bem-sucedido deve ser refletido imediatamente no status da linha e no indicador "Check-ins hoje", sem necessidade de recarregar a página. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Em ambos os casos, a requisição `POST /api/checkin/entrada/1` retornou HTTP 201 (sucesso) e o "Total de check-ins" no perfil do cliente foi incrementado corretamente. Porém, na tela de Check-ins: (1) a linha do cliente continuou exibindo status "Pendente" e o botão "Registrar entrada" após o primeiro check-in, mesmo após recarregar a página; (2) o indicador "Check-ins hoje" permaneceu em 1 após o segundo check-in via "Entrada rápida", não refletindo o novo registro. Falha registrada em SIFIT-BUG-010. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/1434d0db-c0df-40b0-87df-bd654b14c63e |
