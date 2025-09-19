### Tabelas de Users Stories
| Nome | Descrição |
|------|-----------|
| US01 | Manter Cliente |
| US02 | Manter Colaborador |
| US03 | Manter Produto |
| US04 | Manter Ramo de Negócio |
| US05 | Vender Produto |
| US06 | Realizar Pagamento |

---

### User Story US01 - Manter Cliente.
| Campo                    | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| **Título**                | Gerenciar Clientes                                   |
| **Identificação**          | US01 - Manter Cliente                                                        |
| **Story**                  | Como gerente, quero poder cadastrar, visualizar, editar e excluir clientes no sistema, preenchendo campos como nome, CPF, endereço e contato, para manter um registro completo, atualizado e confiável de todos os clientes da loja.  |
| **Requisitos Relacionados**| RF06                                                            |
| **Critérios de Aceitação** | - O sistema permite cadastrar clientes com **nome, CPF, endereço e contato**.<br> - O sistema valida CPF (único e formato correto).<br> - O sistema permite consultar, editar e excluir clientes corretamente.<br> - O sistema exibe mensagens claras de sucesso ou erro. |
| **Testes de Aceitação**    | - TA01.01 - Cadastro de cliente com todos os campos obrigatórios preenchidos é bem-sucedido.<br>- TA01.02 - Consulta de cliente pelo CPF retorna dados corretos ou mensagem de erro se não existir.<br>- TA01.03 - Edição e exclusão atualizam ou desativam corretamente o cliente no sistema. |
| **Estimativa**              | 6h                                                                      |
| **Tempo Real Gasto**        |                                                                       |
| **Tamanho Funcional**        | x PF                                                                   |
| **Prioridade**               | Essencial                                      |
| **Responsáveis**             | - Analista: Anderson Gabriel<br>- Desenvolvedor: Paulo Douglas<br>- Revisor: Diana Rodrigues<br>- Testador: Diana Rodrigues |
| **Protótipo**                | *(inserir link ou imagem do protótipo)*                                |

---

### User Story US02 - Manter Colaborador.
| Campo                    | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| **Título**                | Gerenciar Colaboradores                                  |
| **Identificação**          | US02 - Manter Colaborador                                                       |
| **Story**                  | Como gerente, quero poder cadastrar, visualizar, editar e remover colaboradores no sistema, preenchendo campos como **nome, data de nascimento, CPF e ramo de negócio**, para manter um registro completo e atualizado de todos os colaboradores da loja.  |
| **Requisitos Relacionados**| RF01, RF02, RF03, RF04, RF05, RF06                                                           |
| **Critérios de Aceitação** | - O sistema permite cadastrar colaboradores com nome, data de nascimento, CPF e ramo de negócio.<br> - O sistema valida CPF (único e formato correto) e impede cadastro de ramo de negócio duplicado.<br> - O sistema permite consultar, editar e remover colaboradores corretamente.<br> - O sistema exibe mensagens claras de sucesso ou erro. | |
| **Testes de Aceitação**    | - TA01.01 - Cadastro de colaborador com todos os campos obrigatórios preenchidos é bem-sucedido.<br>- TA01.02 - Consulta, edição e remoção retornam resultados corretos.<br>- TA01.03 - Tentativa de cadastro com CPF ou ramo já existente retorna mensagem de erro. |
| **Estimativa**              | 6h                                                                      |

---

### User Story US03 - Manter Produto.

| Campo                    | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| **Título**                | Gerenciar Produto                                  |
| **Identificação**          | US03 - Manter Produto                                                       |
| **Story**                  | (também serve para gerente) Como colaborador, quero poder cadastrar, visualizar, editar e remover produtos no sistema, preenchendo campos como **Nome, Descrição, Quantidade e Valor Unitário**, para manter um registro completo e atualizado de todos os meus produtos na loja.  |
| **Requisitos Relacionados**| RF01, RF02, RF03, RF04                                                          |
| **Critérios de Aceitação** | - O sistema permite cadastrar produtos com Nome, Descrição, Quantidade e Valor Unitário<br> - O sistema impede cadastro de produtos duplicados duplicado.<br> - O sistema permite consultar, editar e remover produtos corretamente.<br> - O sistema exibe mensagens claras de sucesso ou erro. |
| **Testes de Aceitação**    | - TA01.01 - Cadastro de produto com todos os campos obrigatórios preenchidos é bem-sucedido.<br>- TA01.02 - Consulta, edição e remoção retornam resultados corretos.<br>- TA01.03 - Tentativa de cadastro de produto duplicado retorna mensagem de erro. |
| **Estimativa**              | 36h                                                                |

---

### User Story US04 - Manter Ramo de Negócio.

| Campo                    | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| **Título**                | Gerenciar Ramo de Negócio                                  |
| **Identificação**          | US04 - Manter Ramo de Negócio                                                       |
| **Story**                  | Como gerente, quero poder cadastrar, visualizar, editar e remover ramos de negócio no sistema, preenchendo campos como **Nome, SupTipo**, para manter um registro completo e atualizado de todos os ramos de negócio da loja.  |
| **Requisitos Relacionados**| RF06                                                         |
| **Critérios de Aceitação** | - O sistema permite cadastrar produtos com Nome, SubTipo<br> - Impedir que mais de dois colaboradores tenham o mesmo ramo de negócio.<br> - O sistema permite consultar, editar corretamente.<br> - O sistema exibe mensagens claras de sucesso ou erro. |
| **Testes de Aceitação**    | - TA01.01 - Cadastro de ramo de negócio com todos os campos obrigatórios preenchidos é bem-sucedido.<br>- TA01.02 - Consulta, edição e remoção retornam resultados corretos.<br>- TA01.03 - Tentativa de cadastro de dois colaboradores tenham o mesmo ramo de negócio retorna mensagem de erro. |
| **Estimativa**              | 8h                                                                 |

---

### User Story US05 - Vender Produto.

| Campo                    | Descrição                                                                 |
|---------------------------|---------------------------------------------------------------------------|
| **Título**                | Vender Produto                                  |
| **Identificação**          | US05 - Vender produto                          |
| **Story**                  | Como gerente quero vender produtos e que a venda desse produto seja cadastrado no sistema com seu **código de venda**, **código do produto**, **quantidade do produto** e que o **estoque** do produto seja atualizado.  |
| **Requisitos Relacionados**| RF03                                                         |
| **Critérios de Aceitação** | -O sistema deve permitir a inserção do **código do produto** e a **quantidade do produto** |
| **Testes de Aceitação**    | - TA01.01 - Cadastro de uma venda com estoque de produto suficiente.<br>- TA01.02 - Cadastro de venda com **código do produto** inválido. <br>- TA01.03 - Cadastro de venda com estoque insuficiente ou inválido.<br>- TA01.04 - Cancelamento de venda antes da confirmação do pagamento.  |
| **Estimativa**              | 8h                                                                 |

---

### User Story US06 - Realizar Pagamento

| Campo                     | Descrição                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Título**                 | Realizar Pagamento                                                                                                                                    |
| **Identificação**          | US06 - Realizar Pagamento                                                                                                                             |
| **Story**                  | Como **gerente**, quero registrar o pagamento de uma venda, informando a forma de pagamento (dinheiro, cartão, pix, etc.), para que a venda seja finalizada corretamente e o cliente receba o comprovante. |
| **Requisitos Relacionados**| RF04                                                                                                                                                  |
| **Critérios de Aceitação** | - O sistema deve exibir o **valor total da venda** antes do pagamento.<br>- O sistema deve permitir escolher a **forma de pagamento** (dinheiro, cartão, pix, etc.).<br>- O sistema deve confirmar o pagamento e gerar **comprovante**.<br>- O sistema deve permitir o **cancelamento da venda** caso o cliente desista antes da confirmação do pagamento. |
| **Testes de Aceitação**    | - TA02.01 - Realização de pagamento em dinheiro com sucesso.<br>- TA02.02 - Realização de pagamento via cartão com sucesso.<br>- TA02.03 - Realização de pagamento via pix com sucesso.<br>- TA02.04 - Tentativa de pagamento cancelada pelo cliente antes da confirmação.<br>- TA02.05 - Validação de forma de pagamento inválida. |
| **Estimativa**             | 6h                                                                                                                                                    |



















