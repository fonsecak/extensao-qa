## Cenário 28: Consulta dos recursos de Inteligência e Automação.

### Caso de Teste 01: Acesso à Central de Automações.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C28-CT01 | A tela de Inteligência e Automação deve apresentar as automações ativas e disponíveis. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Inteligência & Automação" |
| **ENTÃO** a tela deve ser exibida com o resumo "automações ativas", "última execução" e "canal principal" |
| **E** devem ser listadas as automações ativas, com as ações "Executar agora", "Configurar" e "Ver resultados" |
| **E** devem ser listadas as automações disponíveis, ainda não implementadas |
| **E** deve ser exibido o painel "Atividade recente" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| As automações ativas devem corresponder às exibidas no resumo. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 02: Abertura da configuração de uma automação.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C28-CT02 | O painel de configuração de uma automação deve apresentar frequência, canais, destinatários e critérios analisados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Inteligência & Automação. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de Inteligência & Automação |
| **QUANDO** clicarmos em "Configurar" na automação "Risco de Evasão" |
| **ENTÃO** deve ser exibido o painel com as seções "Frequência", "Canais de envio", "Destinatários" e "Critérios analisados" |
| **E** deve estar disponível o controle "Automação ativa" |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O painel deve abrir sem apresentar mensagem de erro. |
| As seções e os controles descritos devem estar disponíveis. |
| O caso verifica a abertura do painel; não alterar a configuração. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Caso de Teste 03: Acesso à tela de Resultados IA e filtro por período.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C28-CT03 | A tela de Resultados da Inteligência deve atualizar os indicadores conforme o período selecionado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Resultados IA" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Automações executadas", "Relatórios enviados", "Alunos em risco identificados" e demais indicadores do período |
| **E** devem estar disponíveis os painéis "O que o Sifit identificou" e "Inteligência Sifit" |
| **QUANDO** selecionarmos o filtro "Últimos 30 dias" |
| **ENTÃO** os indicadores e o histórico devem ser atualizados conforme o novo período |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A troca de período deve atualizar os indicadores e a lista de identificações sem apresentar erro. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---
