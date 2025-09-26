# Documentação De Visão

## Resumo

O projeto COLAB é um sistema de gestão desenvolvido para lojas colaborativas, onde diferentes colaboradores compartilham um mesmo espa¸co físico para vender seus produtos. O sistema visa facilitar a administração de estoque, vendas, e pagamentos, além de fornecer ferramentas para gerenciar colaboradores e clientes.

#### Definição dos usuários

| Número | Perfil              | Descrição                                                                                                  |
|--------|---------------------|------------------------------------------------------------------------------------------------------------|
| 1      | Colaborador         | Usuário do sistema com função de colaborador na loja. Pode adicionar, solicitar baixa e alterar produtos. Pode visualizar apenas seus próprios produtos no sistema. |
| 2      | Gerente             | Usuário do sistema que gerencia os colaboradores, possuindo visão geral dos colaboradores, estoque, vendas e pagamentos de aluguel.                          |
| 3      | Cliente             | Ator passivo que participa das vendas, tendo seus dados registrados no sistema, mas sem acesso direto ao sistema.                                            |
| 4      | Sistema de Pagamento | Sistema externo de pagamento.                                                                          |

## Requisitos Funcionais

| ID | Módulo | Requisito Funcional | Visão |
| :---: | :---: | :--- | :--- |
| **RF01** | **Usuários/Acesso** | Permitir o **cadastro** e a **gestão** de usuários (Gestores e Colaboradores). | Geral |
| **RF02** | **Multi-Loja** | Permitir o **cadastro** e a **gestão** de múltiplas lojas no sistema (por um Gestor Principal). | Gerente |
| **RF03** | **Produtos/Estoque** | Permitir ao Colaborador **cadastrar** e **gestão** de seus produtos (fotos, descrição, preço). | Colaborador |
| **RF04** | **Produtos/Estoque** | Permitir ao Colaborador **acompanhar o estoque em tempo real** dos seus produtos. | Colaborador |
| **RF05** | **Alerta/Estoque** | Gerar **notificações** ao Gerente e/ou Colaborador quando um produto atingir um nível mínimo de estoque (ponto de reposição). | Gerente/Colaborador |
| **RF06** | **Vendas/Financeiro** | Registrar as **vendas** de produtos, associando-as ao Colaborador e loja corretos. | Geral |
| **RF07** | **Vendas/Financeiro** | Permitir ao Colaborador **visualizar** suas comissões e repasses detalhados por venda, incluindo os gastos envolvidos (taxas). | Colaborador |
| **RF08** | **Vendas/Relatórios** | Gerar **relatórios** de vendas (semanal/mensal) para o Colaborador, indicando os produtos com mais saídas. | Colaborador |
| **RF09** | **Promoções** | Permitir ao Colaborador **cadastrar promoções/descontos** em seus produtos. | Colaborador |
| **RF10** | **Promoções** | Gerar uma **notificação** na loja física (via integração futura) sobre o preço atualizado/desconto. | Colaborador |
| **RF11** | **Dashboard/Indicadores** | Exibir um **Dashboard Geral** para o Gerente com estatísticas consolidadas (vendas, estoque, aluguel, contas a pagar). | Gerente |
| **RF12** | **Dashboard/Indicadores** | Exibir um **Dashboard Pessoal** para o Colaborador com suas métricas e resultados. | Colaborador |
| **RF13** | **Dashboard/Indicadores** | Permitir ao Colaborador **escolher e personalizar** os indicadores que deseja acompanhar (faturamento, ticket médio, etc.). | Colaborador |
| **RF14** | **Espaços/Aluguel** | Permitir ao Gerente **cadastrar** e **definir valores de aluguel** dos espaços/stands/prateleiras. | Gerente |
| **RF15** | **Espaços/Aluguel** | Permitir ao Gerente **associar** um espaço a um Colaborador. | Gerente |
| **RF16** | **Financeiro/Aluguel** | Permitir ao Colaborador **visualizar** e gerir os pagamentos de aluguel do seu espaço. | Colaborador |
| **RF17** | **Financeiro/Comissões** | Calcular **automaticamente** as comissões dos Colaboradores com base nas vendas e taxas predefinidas. | Gerente |
| **RF18** | **Financeiro/Contas** | Gerar **alertas** ao Gerente sobre contas a pagar (ex: aluguel geral, impostos) e contas a receber. | Gerente |
| **RF19** | **CRM** | Fornecer um módulo **CRM** (Customer Relationship Management) para o Gerente gerenciar os clientes e facilitar a comunicação. | Gerente |
| **RF20** | **Feedback** | Permitir o registro e acompanhamento do **feedback do cliente** (avaliação de atendimento, logística e produtos). | Colaborador |

## Requisitos Não Funcionais

| ID | Categoria | Requisito Não Funcional |
| :---: | :---: | :--- |
| **RNF01** | **Usabilidade** | A interface do sistema (web e mobile) deve ser **intuitiva** e de **fácil aprendizado**, com um design **responsivo** e **acessível**. |
| **RNF02** | **Desempenho** | O tempo de carregamento das páginas e dashboards não deve exceder **3 segundos**, mesmo com um alto volume de dados. |
| **RNF03** | **Disponibilidade** | O sistema deve estar **disponível 24 horas por dia, 7 dias por semana (99,9% de *uptime*)**. |
| **RNF04** | **Segurança (Dados)** | Todos os dados sensíveis (financeiros, pessoais de colaboradores e clientes) devem ser **criptografados** (em trânsito - SSL/TLS - e em repouso). |
| **RNF05** | **Segurança (Acesso)** | Deve haver **perfis de acesso** bem definidos (Gestor e Colaborador), garantindo que cada usuário acesse apenas as informações e funcionalidades de sua responsabilidade (isolamento de dados dos colaboradores). |
| **RNF06** | **Escalabilidade** | A arquitetura do sistema deve ser capaz de suportar o **crescimento** no número de lojas, colaboradores e volume de transações **sem degradação significativa de desempenho**. |
| **RNF07** | **Portabilidade** | O sistema deve ser acessível via **Web** e estar preparado para o desenvolvimento futuro de um **Aplicativo Mobile (iOS e Android)**. |
| **RNF08** | **Privacidade** | O sistema deve estar em conformidade com as regulamentações de **proteção de dados (LGPD no Brasil)**, garantindo a transparência e consentimento no tratamento das informações dos clientes. |
| **RNF09** | **Confiabilidade** | O sistema deve possuir um mecanismo robusto de **backup e recuperação de desastres** para garantir a integridade e disponibilidade dos dados. |

### Métricas de Avaliação de Desempenho (KPIs)

| Categoria | Métrica (KPI) | Objetivo |
| :--- | :--- | :--- |
| **Financeiro** | **Taxa de Comissão Média** | Monitorar o percentual médio de repasse e custo de serviço sobre as vendas. |
| **Estoque** | **Acuracidade do Estoque (Real vs. Sistema)** | Medir a diferença entre o estoque físico e o registrado, indicando a confiabilidade do sistema. |
| **Usabilidade** | **Taxa de Conclusão de Tarefas (Ex: Cadastrar Produto)** | Medir o quão fácil e rápido um Colaborador realiza tarefas-chave. |
| **Vendas** | **Ticket Médio por Colaborador** | Avaliar o valor médio de vendas por empreendedor, ajudando o Gerente a identificar *gaps* e sucessos. |
| **Desempenho** | **Tempo de Resposta da API** | Monitorar o tempo que o sistema leva para processar requisições (crucial para o **RNF02**). |
| **Adoção** | **Frequência de Acesso ao Dashboard** | Medir o engajamento dos Colaboradores com o sistema. |

## Caso de Uso
![Diagrama Caso de Uso](<assets/imgs/casosdeuso.png>)

### Documentação dos Casos de Uso

#### Atores

1. **Colaborador:** Usuário que gerencia seus produtos e visualiza suas vendas.
2. **Gerente:** Responsável por gerenciar colaboradores, clientes e ter visão geral da loja.
3. **Cliente:** Usuário que participa apenas quando compra um produto e para seu próprio cadastro no sistema.
4. **Sistema de Pagamento:** Sistema externo para processamento de pagamentos.

#### Tabela dos Casos de uso

| ID | Nome do Caso de Uso | Descrição | Requisito(s) Associado(s) |
| :---: | :--- | :--- | :--- |
| **CU01** | **Manter Loja e Ramo de Negócio** | Permite o cadastro, consulta e gestão de múltiplas lojas e dos ramos de negócio de atuação dos Colaboradores. | RF02 |
| **CU02** | **Manter Colaborador e Acesso** | Permite o cadastro, consulta, edição e remoção (desativação) de Colaboradores e a gestão de suas permissões de acesso ao sistema. | RF01 |
| **CU03** | **Manter Espaços de Aluguel** | Permite o cadastro de espaços físicos (stands, prateleiras), a definição de seus valores de aluguel e a associação a um Colaborador. | RF14, RF15 |
| **CU04** | **Manter Produto e Estoque** | Permite ao Colaborador cadastrar, editar (incluindo fotos e preço) e remover seus produtos, além de consultar o estoque atual. | RF03, RF04 |
| **CU05** | **Acompanhar Estoque em Tempo Real** | Monitora os níveis de estoque e gera notificações automáticas para o Colaborador e o Gerente quando o ponto de reposição é atingido. | RF04, RF05 |
| **CU06** | **Gerenciar Promoções** | Permite ao Colaborador aplicar descontos (promoções) em seus produtos e notificar o sistema da loja física sobre a alteração de preço. | RF09, RF10 |
| **CU07** | **Gerenciar Clientes (CRM)** | Permite o cadastro, visualização, edição e desativação de dados dos clientes para facilitar a comunicação e o rastreamento (CRM). | RF19 |
| **CU08** | **Realizar Venda** | Inicia o processo de venda, associa os produtos ao(s) Colaborador(es) correto(s) e calcula o valor total da transação. | RF06 |
| **CU09** | **Realizar Pagamento** | Finaliza a transação da venda, registra a forma de pagamento, e obtém as taxas de serviço (cartão, PIX, etc.) envolvidas. | RF06, RF07 |
| **CU10** | **Gerenciar Financeiro Geral** | Permite ao Gerente registrar e receber alertas sobre Contas a Pagar e Contas a Receber da loja (ex: aluguel geral, impostos, aluguéis de espaços). | RF18 |
| **CU11** | **Calcular Repasses e Comissões** | Processo interno que calcula automaticamente a comissão da loja e o valor líquido (repasse) devido ao Colaborador após cada venda. | RF07, RF17 |
| **CU12** | **Visualizar Finanças e Repasses** | Permite ao Colaborador visualizar o detalhe de suas vendas, as taxas descontadas e o valor final (repasse) que irá receber (seu lucro). | RF07 |
| **CU13** | **Visualizar Aluguel de Espaço** | Permite ao Colaborador acompanhar o valor, vencimento e status de pagamento do aluguel de seu box/stand na loja. | RF16 |
| **CU14** | **Visualizar Feedback de Clientes** | Permite ao Colaborador acompanhar as avaliações e *feedback* dos clientes sobre seus produtos e atendimento logístico. | RF20 |
| **CU15** | **Visualizar Dashboard Geral** | Apresenta ao Gerente um painel consolidado com as estatísticas gerais de vendas, estoque, finanças e aluguéis de todos os colaboradores. | RF11 |
| **CU16** | **Visualizar Dashboard Pessoal** | Apresenta ao Colaborador um painel com suas métricas de desempenho e resultados pessoais (vendas, faturamento, etc.). | RF12, RF13 |
| **CU17** | **Gerar Relatórios Pessoais de Venda** | Permite ao Colaborador gerar relatórios periódicos (semanais/mensais) de suas vendas, destacando os produtos de maior e menor saída. | RF08 |

### Especificações dos casos de uso

### Especificação do Caso de Uso CU01 - Manter Loja e Ramo de Negócio

#### 1 Resumo
Este caso de uso permite ao Gestor Principal cadastrar, consultar, editar e remover (desativar) múltiplas lojas e os ramos de negócio que elas comercializam.

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.
3.2 Para a edição/remoção, a Loja ou Ramo de Negócio deve estar previamente cadastrado.

#### 4 Pós-condições
4.1 A Loja é cadastrada e identificada no sistema (suporte a *multi-loja*).
4.2 O Ramo de Negócio é cadastrado e pode ser associado a um Colaborador.

#### 5 Fluxos de evento
5.1 Fluxo básico (Cadastrar Loja/Ramo) 
1. O Gerente acessa o módulo de Gestão de Lojas/Ramos.
2. O Gerente insere os dados da nova Loja ou Ramo de Negócio (ex: nome, CNPJ, etc.).
3. O sistema valida os dados inseridos.
4. O sistema salva o registro no banco de dados.

5.2 Fluxo alternativo - A (Editar Registro) 
1. O Gerente seleciona uma Loja ou Ramo de Negócio existente.
2. O sistema exibe os dados atuais.
3. O Gerente modifica as informações desejadas.
4. O sistema valida e atualiza o registro.

5.3 Fluxo de exceção - A (Nome/CNPJ Duplicado) 
1. No passo 3 do fluxo básico, o sistema identifica que o nome da Loja ou Ramo de Negócio já existe.
2. O sistema exibe uma mensagem de erro indicando a duplicidade.
3. O Gerente deve corrigir ou encerrar a operação.

---

### Especificação do Caso de Uso CU02 - Manter Colaborador e Acesso

#### 1 Resumo
Este caso de uso permite ao Gerente cadastrar, consultar, editar e remover (desativar) os perfis dos Colaboradores, garantindo a associação correta ao Ramo de Negócio.

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.
3.2 Para cadastro, o CPF do Colaborador não deve estar ativo no sistema.
3.3 O Ramo de Negócio (se exigido) deve estar previamente cadastrado (CU01).

#### 4 Pós-condições
4.1 O Colaborador é cadastrado com um perfil de acesso e associado a uma Loja e Ramo de Negócio.
4.2 Um Colaborador existente tem seus dados atualizados ou é desativado.

#### 5 Fluxos de evento
5.1 Fluxo básico (Cadastrar Colaborador) 
1. O Gerente acessa o módulo de Gestão de Colaboradores.
2. O Gerente preenche os dados do Colaborador (nome, CPF, contato, Loja, Ramo de Negócio).
3. O sistema valida os dados e a unicidade do CPF.
4. O sistema cria o perfil de usuário e envia credenciais de acesso (via e-mail, por exemplo).

5.2 Fluxo alternativo - A (Consultar/Editar) 
1. O Gerente busca o Colaborador por CPF ou nome.
2. O sistema exibe os dados atuais.
3. O Gerente pode modificar o Ramo de Negócio, informações de contato ou desativar o acesso.
4. O sistema valida e atualiza o registro.

5.3 Fluxo de exceção - A (CPF Inválido ou Duplicado) 
1. No passo 3 do fluxo básico, o sistema detecta que o CPF é inválido ou já está ativo.
2. O sistema exibe a mensagem de erro.
3. O Gerente deve corrigir ou verificar a existência do cadastro.

---

### Especificação do Caso de Uso CU03 - Manter Espaços de Aluguel

#### 1 Resumo
Permite ao Gerente cadastrar e configurar os espaços físicos disponíveis na loja (stands, prateleiras), definir seus valores de aluguel e associá-los aos Colaboradores.

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.
3.2 O Colaborador deve estar ativo no sistema (para associação).

#### 4 Pós-condições
4.1 O Espaço é cadastrado com valor de aluguel e status ("Disponível" ou "Alugado").
4.2 Ao associar um Colaborador, é gerado um registro de Conta a Receber (Gerente) e a Pagar (Colaborador).

#### 5 Fluxos de evento
5.1 Fluxo básico (Cadastrar Espaço e Associar) 
1. O Gerente acessa o módulo de Gestão de Espaços.
2. O Gerente cadastra o Espaço, definindo nome, tipo e **Valor de Aluguel**.
3. O Gerente seleciona a opção de associar o Espaço a um **Colaborador** ativo.
4. O sistema atualiza o status do Espaço para "Alugado" e cria o registro financeiro de aluguel.

5.2 Fluxo alternativo - A (Desassociar Espaço) 
1. O Gerente seleciona um Espaço alugado.
2. O Gerente solicita a desassociação do Colaborador.
3. O sistema remove a associação, atualiza o status do Espaço para "Disponível" e registra o encerramento do contrato de aluguel.

5.3 Fluxo de exceção - A (Valor de Aluguel Inválido) 
1. No passo 2 do fluxo básico, o Gerente tenta salvar um Valor de Aluguel negativo ou nulo.
2. O sistema bloqueia a ação e exige um valor válido (maior que zero).
3. O Gerente corrige o valor e tenta salvar novamente.

---

### Especificação do Caso de Uso CU04 - Manter Produto e Estoque

#### 1 Resumo
Permite ao Colaborador cadastrar, editar, excluir e consultar seus produtos, incluindo informações como preço, descrição, fotos e quantidade em estoque.

#### 2 Atores
Colaborador, Gerente (apenas consulta e remoção)

#### 3 Precondições
3.1 O Colaborador deve estar logado no sistema.
3.2 Para edição/exclusão, o produto deve estar previamente cadastrado.

#### 4 Pós-condições
4.1 O Produto é registrado e associado unicamente ao Colaborador.
4.2 O estoque inicial é definido.
4.3 Um produto existente tem seus dados atualizados ou é desativado.

#### 5 Fluxos de evento
5.1 Fluxo básico (Cadastrar Produto) 
1. O Colaborador acessa o módulo de Gestão de Produtos.
2. O Colaborador insere nome, descrição, **preço**, **quantidade inicial** e **faz upload de fotos**.
3. O sistema valida os campos obrigatórios (RF03).
4. O sistema registra o produto, associando-o ao Colaborador.

5.2 Fluxo alternativo - A (Editar Preço/Estoque) 
1. O Colaborador seleciona um produto para edição.
2. O Colaborador altera o preço e/ou a quantidade em estoque.
3. O sistema valida a alteração e atualiza o registro.

5.3 Fluxo de exceção - A (Dados Incompletos) 
1. No passo 3 do fluxo básico, o sistema identifica que campos obrigatórios (ex: preço ou quantidade inicial) estão vazios.
2. O sistema exige o preenchimento dos campos em falta.
3. O Colaborador fornece os dados e tenta salvar novamente.

---

### Especificação do Caso de Uso CU05 - Acompanhar Estoque em Tempo Real

#### 1 Resumo
Monitora os níveis de estoque dos produtos do Colaborador e gera alertas automáticos para informar sobre a necessidade de reposição.

#### 2 Atores
Colaborador, Gerente (apenas recebe notificação)

#### 3 Precondições
3.1 O produto deve estar cadastrado com uma quantidade mínima de estoque definida (ponto de reposição).
3.2 Deve ocorrer uma venda ou ajuste que altere o estoque.

#### 4 Pós-condições
4.1 Um alerta de "Estoque Baixo" é gerado e exibido nos dashboards do Colaborador e do Gerente.

#### 5 Fluxos de evento
5.1 Fluxo básico (Geração de Alerta) 
1. Ocorre um evento (venda ou ajuste) que altera a quantidade em estoque de um produto (RF04).
2. O sistema verifica se a nova quantidade é igual ou inferior ao ponto de reposição configurado.
3. Se for, o sistema gera uma notificação e a exibe no Dashboard do Colaborador e do Gerente (RF05).

5.2 Fluxo alternativo - A (Visualização Manual) 
1. O Colaborador ou Gerente acessa o módulo de Estoque.
2. O sistema exibe a lista de produtos, destacando aqueles com o status "Estoque Baixo".

5.3 Fluxo de exceção - A (Falha na Notificação) 
1. No passo 3 do fluxo básico, há uma falha na entrega da notificação (ex: erro de servidor).
2. O sistema registra a falha em um log de eventos e a tenta novamente em um período de tempo.

---

### Especificação do Caso de Uso CU06 - Gerenciar Promoções

#### 1 Resumo
Permite ao Colaborador definir e aplicar descontos em seus produtos por um período determinado e, futuramente, notificar a loja física sobre a alteração de preço.

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado no sistema.
3.2 O produto deve estar ativo.

#### 4 Pós-condições
4.1 O preço do produto é atualizado com o valor promocional e o status "Em Promoção" é aplicado.

#### 5 Fluxos de evento
5.1 Fluxo básico (Aplicar Promoção) 
1. O Colaborador seleciona o(s) produto(s) a serem promovidos.
2. O Colaborador define os parâmetros: tipo (percentual/fixo), valor do desconto/novo preço, e **data de validade**.
3. O sistema valida os dados e calcula o novo preço final.
4. O sistema atualiza o preço do produto no cadastro.
5. O sistema gera uma notificação (RF10) para o sistema de display da loja (integração futura).

5.2 Fluxo alternativo - A (Remover Promoção) 
1. O Colaborador seleciona um produto com promoção ativa.
2. O Colaborador solicita a remoção da promoção.
3. O sistema reverte o preço para o valor original e remove o status "Em Promoção".

5.3 Fluxo de exceção - A (Promoção Inválida) 
1. No passo 3 do fluxo básico, o valor do desconto faz com que o preço final seja igual ou menor que zero.
2. O sistema **alerta** o Colaborador e não aplica a promoção.
3. O Colaborador corrige o valor e tenta novamente.

---

### Especificação do Caso de Uso CU07 - Gerenciar Clientes (CRM)

#### 1 Resumo
Permite ao Gerente cadastrar e gerenciar as informações dos clientes para construir um banco de dados (CRM) e facilitar a comunicação.

#### 2 Atores
Gerente, Cliente (apenas fornece dados durante a venda)

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.

#### 4 Pós-condições
4.1 O Cliente é registrado no banco de dados para fins de CRM.

#### 5 Fluxos de evento
5.1 Fluxo básico (Cadastrar Cliente) 
1. O Gerente acessa o módulo CRM.
2. O Gerente insere nome, CPF, endereço e contato do Cliente.
3. O sistema valida os dados (ex: unicidade do CPF).
4. O sistema salva o registro (RF19).

5.2 Fluxo alternativo - A (Consulta/Edição) 
1. O Gerente busca o Cliente por CPF ou nome.
2. O Gerente pode atualizar o endereço ou contato.
3. O sistema valida e atualiza o registro.

5.3 Fluxo de exceção - A (CPF Inválido ou Duplicado) 
1. No passo 3 do fluxo básico, o sistema detecta um CPF inválido ou já cadastrado.
2. O sistema informa o erro.
3. O Gerente corrige os dados ou encerra o cadastro se o Cliente já existir.

---

### Especificação do Caso de Uso CU08 - Realizar Venda

#### 1 Resumo
Inicia o processo de venda. O Gerente insere os produtos, calcula o total e associa a transação ao(s) Colaborador(es) dono(s) do(s) item(ns).

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.
3.2 Os produtos devem estar cadastrados e com estoque disponível.

#### 4 Pós-condições
4.1 Uma transação de venda é registrada, associada ao Cliente (opcional) e ao(s) Colaborador(es).
4.2 O estoque é reservado (ou baixado no final do fluxo).

#### 5 Fluxos de evento
5.1 Fluxo básico (Registro de Venda) 
1. O Gerente acessa a interface de Venda.
2. O Gerente informa o(s) produto(s) e a quantidade.
3. O sistema **valida a disponibilidade do estoque** e **identifica o Colaborador** dono de cada item (RF06).
4. O sistema calcula o subtotal da venda, incluindo o preço promocional (se aplicável).
5. O Gerente informa o CPF do Cliente (opcional) e confirma a venda.

5.2 Fluxo alternativo - A (Venda com Cliente) 
1. No passo 5 do fluxo básico, o Gerente informa o CPF do Cliente.
2. O sistema verifica o cadastro (CU07).
3. A venda é registrada com o vínculo ao Cliente.

5.3 Fluxo de exceção - A (Quantidade Insuficiente) 
1. No passo 3 do fluxo básico, a quantidade solicitada excede o estoque disponível.
2. O sistema **alerta** a indisponibilidade.
3. O Gerente ajusta a quantidade ou remove o item da venda.

---

### Especificação do Caso de Uso CU09 - Realizar Pagamento

#### 1 Resumo
Finaliza a transação da venda, registrando a forma de pagamento e obtendo as taxas de serviço (maquininha, PIX) necessárias para o cálculo de repasse.

#### 2 Atores
Gerente, Cliente, Sistema de Pagamento (Externo)

#### 3 Precondições
3.1 O Caso de Uso "Realizar Venda" deve ter sido concluído.
3.2 O valor total da venda deve estar calculado.

#### 4 Pós-condições
4.1 O pagamento é registrado com sucesso.
4.2 O estoque dos produtos vendidos é definitivamente baixado.
4.3 A taxa de serviço aplicada é registrada na transação (RF07).
4.4 O CU11 é disparado para o cálculo financeiro.

#### 5 Fluxos de evento
5.1 Fluxo básico (Pagamento e Baixa) 
1. O Gerente informa a forma de pagamento (Dinheiro, Cartão, PIX, etc.).
2. Para pagamentos eletrônicos, o sistema se comunica com o **Sistema de Pagamento** para processar a transação.
3. O **Sistema de Pagamento** retorna a confirmação e a **Taxa de Serviço** aplicada (RF07).
4. O sistema registra o pagamento e dá a **baixa final no estoque** (RF06).
5. O sistema dispara o CU11 para calcular os repasses.

5.2 Fluxo alternativo - A (Pagamento Negado) 
1. No passo 3 do fluxo básico, o Sistema de Pagamento retorna a negação (ex: cartão recusado).
2. O Gerente solicita uma nova forma de pagamento ou o Cliente cancela a compra.

5.3 Fluxo de exceção - A (Falha na Integração de Taxas) 
1. No passo 3 do fluxo básico, o sistema de pagamento falha ao retornar a taxa.
2. O sistema solicita que o **Gerente insira a taxa manualmente** e registra um alerta de inconsistência.
3. O processo de pagamento continua no passo 4.

---

### Especificação do Caso de Uso CU10 - Gerenciar Financeiro Geral

#### 1 Resumo
Permite ao Gerente registrar, visualizar e receber alertas sobre Contas a Pagar (custos da loja) e Contas a Receber (aluguéis de espaços) para o controle financeiro geral.

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado no sistema.
3.2 O CU03 deve ter gerado registros de aluguel.

#### 4 Pós-condições
4.1 As contas da loja são registradas e monitoradas.
4.2 Alertas sobre vencimentos são gerados.

#### 5 Fluxos de evento
5.1 Fluxo básico (Registro e Alerta) 
1. O Gerente acessa o módulo Financeiro Geral.
2. O Gerente registra uma Conta a Pagar (ex: aluguel do imóvel, impostos) ou acompanha as Contas a Receber (aluguéis de espaços).
3. O Gerente define a data de vencimento.
4. O sistema verifica periodicamente as datas e **gera alertas** sobre vencimentos próximos (RF18).

5.2 Fluxo alternativo - A (Marcação de Pagamento) 
1. O Gerente seleciona uma Conta a Pagar/Receber.
2. O Gerente marca a conta como paga/recebida.
3. O sistema atualiza o status no extrato financeiro.

5.3 Fluxo de exceção - A (Data Inválida) 
1. No passo 3 do fluxo básico, o Gerente tenta registrar uma data de vencimento retroativa ou inválida.
2. O sistema exige uma data válida para o registro.
3. O Gerente corrige a data e tenta salvar.

---

### Especificação do Caso de Uso CU11 - Calcular Repasses e Comissões

#### 1 Resumo
Processo interno e automatizado, disparado pela finalização da venda (CU09), que calcula a comissão da loja, as taxas de serviço e o valor líquido (repasse) a ser pago ao Colaborador.

#### 2 Atores
Sistema (disparado pelo Gerente no CU09)

#### 3 Precondições
3.1 O CU09 (Realizar Pagamento) foi concluído.
3.2 A transação de venda e a taxa de serviço estão registradas.

#### 4 Pós-condições
4.1 O valor da comissão da loja é registrado.
4.2 O valor exato do repasse (lucro) do Colaborador é registrado na transação.

#### 5 Fluxos de evento
5.1 Fluxo básico (Cálculo Automático) 
1. Após a conclusão do pagamento (CU09), o sistema é acionado.
2. O sistema pega o valor total da venda e as taxas de serviço registradas (RF07).
3. O sistema aplica a regra de comissão da loja (percentual fixo ou variável).
4. O sistema calcula: **Preço Bruto - Taxa de Maquininha - Taxa de Serviço - Comissão da Loja = Repasse Líquido** (RF17).
5. O sistema registra o valor do repasse para que o Colaborador possa visualizá-lo (CU12).

5.2 Fluxo alternativo - A (Venda com Múltiplos Colaboradores) 
1. No passo 2, a venda envolve produtos de diferentes Colaboradores.
2. O sistema executa o cálculo do repasse e comissão **separadamente** para cada item/Colaborador.

5.3 Fluxo de exceção - A (Regra de Comissão Não Encontrada) 
1. No passo 3 do fluxo básico, o sistema não encontra a regra de comissão para a loja/ramo de negócio.
2. O sistema registra a transação com status "Pendente de Cálculo" e **alerta** o Gerente.
3. O Gerente deve definir a regra para que o cálculo seja reprocessado.

---

### Especificação do Caso de Uso CU12 - Visualizar Finanças e Repasses

#### 1 Resumo
Permite ao Colaborador visualizar o extrato de suas vendas, incluindo o detalhe das deduções (taxas e comissão) para verificar o valor líquido (lucro/repasse).

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado.
3.2 Devem existir transações processadas pelo CU11.

#### 4 Pós-condições
4.1 N/A.

#### 5 Fluxos de evento
5.1 Fluxo básico (Visualização Detalhada) 
1. O Colaborador acessa o módulo de Finanças Pessoais.
2. O sistema exibe o resumo financeiro (Dashboard Pessoal).
3. O Colaborador seleciona um período e/ou uma venda específica.
4. O sistema exibe o detalhe da transação, incluindo o valor da venda, as deduções (taxas, comissão) e o **Repasse Líquido** (RF07).

5.2 Fluxo alternativo - A (Exportação de Extrato) 
1. O Colaborador solicita a exportação do extrato financeiro do período.
2. O sistema gera um arquivo (Ex: CSV ou PDF) com os dados detalhados.

5.3 Fluxo de exceção - A (Nenhuma Venda) 
1. No passo 2 do fluxo básico, não há vendas no período selecionado.
2. O sistema exibe uma mensagem informativa ("Nenhuma transação registrada").

---

### Especificação do Caso de Uso CU13 - Visualizar Aluguel de Espaço

#### 1 Resumo
Permite ao Colaborador acompanhar os detalhes do aluguel de seu espaço na loja, incluindo valor, vencimento e status de pagamento.

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado.
3.2 O CU03 deve ter associado um espaço ao Colaborador.

#### 4 Pós-condições
4.1 N/A.

#### 5 Fluxos de evento
5.1 Fluxo básico (Consulta de Aluguel) 
1. O Colaborador acessa a área de Gestão de Pagamentos de Aluguel.
2. O sistema exibe o Espaço alugado, o **Valor do Aluguel** e a **Data de Vencimento** (RF16).
3. O sistema exibe o status dos últimos pagamentos ("Pago", "Pendente" ou "Vencido").

5.2 Fluxo alternativo - A (Visualizar Histórico) 
1. O Colaborador solicita o histórico de pagamentos de aluguel.
2. O sistema exibe as transações anteriores com datas de pagamento e *status*.

5.3 Fluxo de exceção - A (Nenhum Espaço Alugado) 
1. No passo 2 do fluxo básico, o Colaborador não está associado a nenhum espaço ativo.
2. O sistema exibe a mensagem "Nenhum espaço alugado registrado".

---

### Especificação do Caso de Uso CU14 - Visualizar Feedback de Clientes

#### 1 Resumo
Permite ao Colaborador visualizar e acompanhar as avaliações de clientes sobre seus produtos e a qualidade do atendimento/logística associada à venda.

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado.
3.2 Deve haver um mecanismo para registrar o feedback do cliente (interface externa ou *link* pós-venda).

#### 4 Pós-condições
4.1 N/A.

#### 5 Fluxos de evento
5.1 Fluxo básico (Acompanhamento de Avaliações) 
1. O Colaborador acessa o módulo de Feedback/Avaliações.
2. O sistema exibe as avaliações recebidas, filtradas por produto ou atendimento.
3. O sistema permite que o Colaborador visualize o detalhe do feedback (nota e comentário) (RF20).

5.2 Fluxo alternativo - A (Filtrar por Nota) 
1. O Colaborador aplica um filtro para ver apenas notas abaixo de um certo valor (ex: "Ver todos os 1 e 2 estrelas").
2. O sistema exibe a lista filtrada.

5.3 Fluxo de exceção - A (Nenhum Feedback) 
1. No passo 2 do fluxo básico, o sistema não encontra nenhum feedback no período.
2. O sistema exibe a mensagem "Nenhuma avaliação de cliente recebida".

---

### Especificação do Caso de Uso CU15 - Visualizar Dashboard Geral

#### 1 Resumo
Apresenta ao Gerente um painel consolidado com estatísticas críticas de todas as lojas, vendas, estoque, aluguéis e finanças.

#### 2 Atores
Gerente

#### 3 Precondições
3.1 O Gerente deve estar logado.
3.2 Devem existir dados registrados (vendas, estoque, etc.).

#### 4 Pós-condições
4.1 N/A.

#### 5 Fluxos de evento
5.1 Fluxo básico (Consulta Geral) 
1. O Gerente faz o login.
2. O sistema exibe o **Dashboard Geral** (RF11) com KPIs consolidados (ex: Vendas Totais, Total de Estoque, Aluguéis Pendentes, Contas a Pagar).
3. O Gerente pode filtrar os dados por Loja ou Período.

5.2 Fluxo alternativo - A (Drill-Down) 
1. O Gerente clica em um KPI no dashboard (ex: "Vendas Totais").
2. O sistema leva o Gerente para uma tela de detalhamento ou relatório para análise mais profunda.

5.3 Fluxo de exceção - A (Dados Inconsistentes) 
1. Ao carregar o painel, o sistema detecta inconsistências em alguma métrica (ex: valor total de comissão negativo).
2. O sistema exibe um **alerta visual** no respectivo KPI e notifica a equipe de TI.

---

### Especificação do Caso de Uso CU16 - Visualizar Dashboard Pessoal

#### 1 Resumo
Permite ao Colaborador visualizar seu painel de desempenho pessoal (vendas, faturamento) e personalizar os Indicadores-Chave de Desempenho (KPIs) exibidos.

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado.
3.2 Devem existir vendas registradas para o Colaborador.

#### 4 Pós-condições
4.1 As configurações de visualização do Colaborador são salvas.

#### 5 Fluxos de evento
5.1 Fluxo básico (Visualização Pessoal) 
1. O Colaborador faz o login.
2. O sistema exibe o **Dashboard Pessoal** (RF12) com os KPIs configurados (ex: Faturamento, Ticket Médio, Produtos Mais Vendidos).
3. O Colaborador pode filtrar os dados por Período.

5.2 Fluxo alternativo - A (Personalizar KPIs) 
1. O Colaborador acessa a área de configuração do Dashboard.
2. O Colaborador **seleciona/desmarca** os indicadores que deseja acompanhar (RF13).
3. O sistema salva as preferências e recarrega o Dashboard.

5.3 Fluxo de exceção - A (Falha no Cálculo do KPI) 
1. Ao carregar o painel, o sistema falha ao calcular um KPI (ex: Ticket Médio).
2. O sistema exibe o erro no widget do KPI e notifica o Colaborador para tentar mais tarde.

---

### Especificação do Caso de Uso CU17 - Gerar Relatórios Pessoais de Venda

#### 1 Resumo
Permite ao Colaborador gerar relatórios de suas vendas em períodos específicos, identificando os produtos com maior e menor saída (desempenho).

#### 2 Atores
Colaborador

#### 3 Precondições
3.1 O Colaborador deve estar logado.
3.2 Devem existir vendas registradas no período solicitado.

#### 4 Pós-condições
4.1 O relatório solicitado é gerado (na tela ou para exportação).

#### 5 Fluxos de evento
5.1 Fluxo básico (Geração do Relatório) 
1. O Colaborador acessa o módulo de Relatórios Pessoais.
2. O Colaborador seleciona o tipo de relatório (semanal/mensal) e o período.
3. O sistema processa os dados de vendas e exibe o relatório na tela, destacando os produtos com mais saídas (RF08).

5.2 Fluxo alternativo - A (Exportação) 
1. O Colaborador clica no botão "Exportar".
2. O sistema gera um arquivo do relatório (Ex: PDF, Excel) e inicia o download.

5.3 Fluxo de exceção - A (Tempo de Processamento Excedido) 
1. O volume de dados no período solicitado é muito grande e o tempo de geração excede o limite.
2. O sistema informa que o relatório será processado em *background* e enviado por e-mail quando concluído.
