## Cenário 27: Consulta de Enquetes.

### Caso de Teste 01: Acesso à tela de Enquetes e consistência da pergunta cadastrada.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C27-CT01 | A listagem de Enquetes deve exibir a pergunta cadastrada de cada enquete. |

| **Pré-condições** |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com o perfil administrativo. |
| Deve existir ao menos uma enquete com pergunta cadastrada. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos autenticados no Sifit |
| **QUANDO** clicarmos no menu "Enquetes" |
| **ENTÃO** a tela deve ser exibida com os indicadores "Enquetes", "Ativas", "Inativas" e "Respostas" |
| **E** a coluna "Pergunta" deve exibir a pergunta cadastrada de cada enquete |
| **QUANDO** abrirmos a visualização de uma enquete cuja listagem exibe "Sem pergunta cadastrada" |
| **ENTÃO** verificamos se a pergunta está de fato preenchida no cadastro |

| **Critérios de aceitação** |
| :-------------------------------------------------------------- |
| A coluna "Pergunta" da listagem deve corresponder ao conteúdo cadastrado em cada enquete. |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| Todas as 35 enquetes listadas exibem "Sem pergunta cadastrada" na coluna "Pergunta". Ao abrir a enquete "Manual SIFIT Horário preferido" (código 28), o campo "Pergunta" do formulário está preenchido com "Qual horário você prefere treinar?". A listagem não reflete o dado cadastrado. Falha registrada em SIFIT-BUG-005. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/16.mp4) |

---

### Caso de Teste 02: Cadastro de enquete com pergunta e resposta.

| ID | Descrição |
| :------- | :------------------------------------------------------- |
| C27-CT02 | O sistema deve permitir cadastrar uma nova enquete com nome, pergunta e resposta, exibindo mensagem de sucesso e persistindo a pergunta. |

| **Passos** |
| :---------------------------------------------------------------- |
| **DADO** que estamos no formulário "Nova Enquete" |
| **QUANDO** preenchermos Nome, Pergunta e uma Resposta |
| **E** clicarmos em "Salvar" |
| **ENTÃO** a enquete deve ser criada com sucesso, sem mensagem de erro |
| **E** a pergunta deve aparecer corretamente na listagem |

| **Resultado obtido** |
| :-------------------------------------------------------------- |
| O sistema exibiu "Erro ao salvar enquete" (SIFIT-BUG-016), apesar do backend retornar HTTP 200. A enquete foi criada, mas a pergunta não foi persistida — reproduzindo exatamente o sintoma do SIFIT-BUG-005, confirmando que a causa raiz está no cadastro, não na listagem. |

| **Vídeo do JAM** |
| :-------------------------------------------------------------- |
| [Assistir ao vídeo](../Videos/16.mp4) |
