## Cenário 01: Login na plataforma.

### Caso de Teste 01: Login com as credenciais válidas.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C01-CT01 | O login será realizado com um login e uma senha válidos. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| A conta administrativa deve estar ativa e possuir credenciais válidas. |
| A página de login do Sifit deve estar aberta, sem sessão autenticada. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do Sifit |
| **E** preenchemos o login válido da conta no campo "Login" |
| **E** preenchemos a senha válida no campo "Senha" |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** seremos redirecionados para a área inicial do sistema |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O login deve ser realizado e a área inicial do sistema deve ser exibida. |
| Os menus disponíveis para o perfil administrativo devem ser apresentados. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/0189e56d-fe2b-492e-9e97-53d1e7ccfbc3 |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C01-CT02 | O login falhará quando a senha for inválida. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| A conta administrativa deve existir e estar ativa. |
| A página de login do Sifit deve estar aberta, sem sessão autenticada. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do Sifit |
| **E** preenchemos o login válido da conta no campo "Login" |
| **E** preenchemos uma senha incorreta no campo "Senha" |
| **QUANDO** clicarmos uma vez no botão "Entrar" |
| **ENTÃO** uma mensagem de falha na autenticação será exibida |
| **E** permaneceremos na página de login, sem acesso à área inicial |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| Uma mensagem de falha na autenticação deve ser exibida. |
| O sistema não deve permitir o acesso com a senha incorreta. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/bd79d82e-02e2-441a-940c-16d472f3288f |

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C01-CT03 | O login falhará quando os campos obrigatórios estiverem em branco. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| A página de login do Sifit deve estar aberta, sem sessão autenticada. |
| Os campos "Login" e "Senha" devem estar vazios, sem preenchimento automático. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do Sifit |
| **E** deixamos os campos "Login" e "Senha" em branco |
| **QUANDO** clicarmos no botão "Entrar" |
| **ENTÃO** deve ser indicada a necessidade de preencher os campos obrigatórios |
| **E** permaneceremos na página de login, sem acesso à área inicial |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| O sistema deve indicar a necessidade de preencher os campos obrigatórios. |
| O sistema não deve permitir o acesso com os campos vazios. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| Link: https://jam.dev/c/80cf7328-80b1-4ec4-a065-9e97be6c9c66 |
