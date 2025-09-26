# Documentação - COLAB

## Descrição do Projeto

### Definição dos usuários

| Número | Perfil              | Descrição                                                                                                  |
|--------|---------------------|------------------------------------------------------------------------------------------------------------|
| 1      | Colaborador         | Usuário do sistema com função de colaborador na loja. Pode adicionar, solicitar baixa e alterar produtos. Pode visualizar apenas seus próprios produtos no sistema. |
| 2      | Gerente             | Usuário do sistema que gerencia os colaboradores, possuindo visão geral dos colaboradores, estoque, vendas e pagamentos de aluguel.                          |
| 3      | Cliente             | Ator passivo que participa das vendas, tendo seus dados registrados no sistema, mas sem acesso direto ao sistema.                                            |
| 4      | Sistema de Pagamento | Sistema externo de pagamento.                                                                          |

### Requisitos Funcionais

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

### Requisitos Não Funcionais

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

# Caso de Uso
![Diagrama Caso de Uso](<assets/imgs/casosdeuso.png>)

# Documentação dos Atores e Casos de Uso

# Atores

1. **Colaborador:** Usuário que gerencia seus produtos e visualiza suas vendas.
2. **Gerente:** Responsável por gerenciar colaboradores, clientes e ter visão geral da loja.
3. **Cliente:** Usuário que participa apenas quando compra um produto e para seu próprio cadastro no sistema.
4. **Sistema de Pagamento:** Sistema externo para processamento de pagamentos.

# Casos de uso

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


