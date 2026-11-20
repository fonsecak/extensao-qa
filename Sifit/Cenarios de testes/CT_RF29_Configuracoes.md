
## Cenário 29: Consulta e alteração de Configurações.

### Caso de Teste 01: Acesso à tela de Configurações e navegação entre abas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C29-CT01 | A tela de Configurações deve apresentar as abas "Home", "Biometria", "Avaliação", "Aniversário", "Pagamento", "Integrações" e "Design". |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Configurações" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Desktop", "Presença", "Avaliação" e "SifitBox" |
| **E** devem estar disponíveis as sete abas de configuração |
| **QUANDO** navegarmos entre as abas |
| **ENTÃO** cada aba deve exibir seus próprios campos sem apresentar mensagem de erro |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| A navegação entre abas deve preservar o restante da tela. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: [Assistir ao vídeo CT01](https://jam.dev/c/98bc40ee-ce2c-40f4-a2f1-5f4e38cd2c34) |

---

### Caso de Teste 02: Exibição da senha de acesso na aba Biometria.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C29-CT02 | Os campos de credenciais de acesso ao aparelho biométrico devem ser mascarados. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Configurações, aba Biometria. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na aba "Biometria" da tela de Configurações |
| **QUANDO** observarmos os campos "Login" e "Senha" de acesso ao aparelho |
| **ENTÃO** o campo "Senha" deve ser exibido mascarado, no padrão de um campo de senha |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O conteúdo do campo "Senha" não deve ficar visível em texto plano na tela. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O campo "Senha" da aba Biometria exibe o valor em texto plano, sem máscara, da mesma forma que o campo "Login". Falha registrada em SIFIT-BUG-006. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Vídeo não realizado por motivos de segurança da informação. |

A gravação deste caso de teste não será realizada por motivos de segurança da informação. Durante a execução, foi identificado que o campo "Senha", na aba Biometria, apresenta seu conteúdo em texto plano, sem o mascaramento adequado. A gravação poderia expor credenciais de acesso e comprometer a segurança do sistema.

Dessa forma, optou-se por não registrar evidência em vídeo, preservando a confidencialidade das informações.

---

### Caso de Teste 03: Exibição do token na aba Pagamento.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C29-CT03 | O campo de token de integração de pagamento deve ser mascarado. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Configurações, aba Pagamento. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na aba "Pagamento" da tela de Configurações |
| **QUANDO** observarmos o campo "Token Pagar.me" |
| **ENTÃO** o valor do token deve ser exibido mascarado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O conteúdo do campo "Token Pagar.me" não deve ficar visível em texto plano na tela. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O campo "Token Pagar.me" exibe o valor cadastrado em texto plano, sem máscara. Para comparação, o campo "Access Token" da aba Integrações é corretamente mascarado. Falha registrada em SIFIT-BUG-006. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
|| Vídeo não realizado por motivos de segurança da informação. |
**Justificativa — C29-CT03**
A gravação deste caso de teste não será realizada por motivos de segurança da informação. Durante a execução, foi identificado que o campo "Token Pagar.me", localizado na aba Pagamento, apresenta seu conteúdo em texto plano, sem o mascaramento adequado.

A gravação poderia expor informações sensíveis de integração com o sistema de pagamentos, comprometendo a confidencialidade e a segurança dos dados. Dessa forma, optou-se por não registrar evidência em vídeo, evitando a possível divulgação de credenciais de acesso.

**Resultado:** Reprovado — Falha SIFIT-BUG-006. |

---

### Caso de Teste 04: Acesso à aba Integrações.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C29-CT04 | A aba Integrações deve apresentar o status da conexão do WhatsApp Business e as opções de configuração. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado e na tela de Configurações. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na aba "Integrações" da tela de Configurações |
| **ENTÃO** deve ser exibido o painel "Status da Conexão" com status, telefone, provedor e última verificação |
| **E** deve ser exibido o painel "Configuração" com as opções "Evolution API", "Z-API" e "API oficial da Meta" |
| **E** o campo "Access Token" deve ser exibido mascarado |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A tela deve carregar sem apresentar mensagem de erro. |
| O campo de token da API oficial da Meta deve estar mascarado. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: a adicionar. |

---

### Observação sobre testes de escrita em Configurações

As abas de Configurações alteram parâmetros globais da academia (ex.: regras de acesso, biometria, integrações de pagamento), que afetam a operação real e não podem ser isoladas como um registro de teste criável e excluível. Por esse motivo, nenhuma alteração de escrita foi aplicada nesta rodada; os testes permanecem limitados à consulta, já documentados nos casos C29-CT01 a C29-CT04.
