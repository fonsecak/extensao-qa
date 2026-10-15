# Relatório de Bugs

**Software:** Sifit

**QA responsável:** Gabriel Fonseca Proenca

**Data do registro:** 13/10/2026

---

### **Bug 01: Erro interno ao buscar matrícula pelo código**

| **ID** | **Descrição** |
| :--- | :--- |
| SIFIT-BUG-001 | Ao buscar uma matrícula pelo código, informando o valor `3` como exemplo, o sistema apresenta um erro interno. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| A avaliar | A avaliar | Aberto |

| **Passo a passo para simular o bug** |
| :--- |
| 1. Acessar o menu "Matrículas". |
| 2. Informar `3` no campo "Código". |
| 3. Clicar em "Buscar". |
| 4. Observar o erro interno exibido pelo sistema. |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :--- | :--- |
| O sistema deve apresentar a matrícula correspondente ao código informado ou indicar que nenhum resultado foi encontrado. | O sistema apresenta um erro interno durante a busca. |

| **Ambiente** |
| :--- |
| Endereço: https://sifit.centrion.com.br/ |
| Navegador, versão e tipo de ambiente: a registrar. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :--- | :--- |
| Matrículas — busca por código | C04-CT02: Busca de matrícula por código ou nome |

| **Evidência(s)** |
| :--- |
| Link do vídeo do JAM: a adicionar. |
