# Documento Lista de User Stories

## Descrição

Este documento descreve os User Stories criados a partir da Lista de Casos de Uso. Modelo de documento baseado nas características do processo easYProcess (YP).

### Tabelas de Users Stories
| Nome | Título |
|------|-----------|
| US01 | Manter Loja e Ramo de Negócio      |
| US02 | Manter Colaborador e Acesso        |
| US03 | Manter Espaços de Aluguel          |
| US04 | Manter Produto e Estoque           |
| US05 | Acompanhar Estoque em Tempo Real   |
| US06 | Gerenciar Promoções                |
| US07 | Gerenciar Clientes (CRM)           |
| US08 | Realizar Venda                     |
| US09 | Realizar Pagamento                 |
| US10 | Gerenciar Financeiro Geral         |
| US11 | Calcular Repasses e Comissões      |
| US12 | Visualizar Finanças e Repasses     |
| US13 | Visualizar Aluguel de Espaço       |
| US14 | Visualizar Feedback de Clientes    |
| US15 | Visualizar Dashboard Geral         |
| US16 | Visualizar Dashboard Pessoal       |
| US17 | Gerar Relatórios Pessoais de Venda |

## Especificação de User Stories em Markdown

### User Story US01 - Manter Loja e Ramo de Negócio (CU01)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Cadastrar e Gerenciar Múltiplas Lojas e Ramos de Negócio |
| **Story** | Como **Gerente**, eu quero **cadastrar e gerenciar múltiplas lojas e seus respectivos ramos de negócio**, para **poder utilizar a mesma plataforma para administrar diferentes unidades e segmentos (Multi-Loja)**. |
| **Requisitos Relacionados** | RF02 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir o cadastro de dados essenciais da Loja (Nome, CNPJ, Endereço). <br> CA02: O sistema deve permitir o cadastro e a edição do Ramo de Negócio (ex: Vestuário, Alimentação). <br> CA03: O sistema deve garantir que o CNPJ da Loja seja único. |
| **Testes de Aceitação** | TA01.01: Tentar cadastrar uma nova loja e verificar se o sistema a registra corretamente (RF02). <br> TA01.02: Tentar cadastrar um Ramo de Negócio e associá-lo a uma loja existente. <br> TA01.03: Tentar cadastrar uma loja com um CNPJ já existente e verificar se o sistema emite erro. |
| **Estimativa** | 8h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Essencial |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US02 - Manter Colaborador e Acesso (CU02)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Cadastrar e Gerenciar Colaboradores e seus Acessos |
| **Story** | Como **Gerente**, eu quero **cadastrar, associar a uma loja/ramo e gerenciar o acesso dos Colaboradores (Empreendedores)**, para **controlar quem pode usar o sistema e garantir que cada um acesse apenas seus próprios dados**. |
| **Requisitos Relacionados** | RF01, RNF05 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir o cadastro de informações pessoais e de contato do Colaborador. <br> CA02: O sistema deve associar o Colaborador a uma Loja e um Ramo de Negócio. <br> CA03: O sistema deve validar o CPF como único no cadastro. <br> CA04: O Colaborador deve receber credenciais para realizar o primeiro login com o perfil "Colaborador" (RNF05). |
| **Testes de Aceitação** | TA02.01: Cadastrar um novo colaborador e tentar logar com as credenciais geradas. <br> TA02.02: Tentar editar um colaborador e desativar seu acesso. <br> TA02.03: Tentar cadastrar um colaborador com um CPF já existente e verificar o erro. |
| **Estimativa** | 10h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Essencial |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US03 - Manter Espaços de Aluguel (CU03)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Cadastrar e Associar Espaços/Stands aos Colaboradores |
| **Story** | Como **Gerente**, eu quero **cadastrar os espaços disponíveis (prateleiras, stands) e definir seus valores de aluguel**, para **associar esses espaços a um Colaborador e controlar as Contas a Receber da Loja**. |
| **Requisitos Relacionados** | RF14, RF15, RF18 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir o cadastro do Espaço com nome, tipo e **Valor de Aluguel** (RF14). <br> CA02: O Gerente deve conseguir associar um Espaço cadastrado a um Colaborador (RF15). <br> CA03: Ao associar, o sistema deve registrar a data de início e gerar um registro automático de Conta a Receber (RF18). <br> CA04: O valor do aluguel deve ser maior que zero. |
| **Testes de Aceitação** | TA03.01: Cadastrar um novo espaço com seu valor de aluguel. <br> TA03.02: Associar o espaço a um colaborador e verificar se o status muda para "Alugado". <br> TA03.03: Verificar se o registro de Conta a Receber é gerado no financeiro. |
| **Estimativa** | 12h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Essencial |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US04 - Manter Produto e Estoque (CU04)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Cadastrar, Gerenciar Produtos e Consultar Estoque |
| **Story** | Como **Colaborador**, eu quero **cadastrar, editar meus produtos (incluindo fotos e preço) e consultar meu estoque**, para **ter controle total sobre meus itens e garantir que as vendas sejam precisas**. |
| **Requisitos Relacionados** | RF03, RF04 |
| **Critérios de Aceitação** | CA01: O Colaborador deve conseguir cadastrar o produto com Nome, Descrição, Preço, **Estoque Inicial** e **Fotos** (RF03). <br> CA02: O produto deve ser registrado com vínculo direto e exclusivo ao Colaborador. <br> CA03: O sistema deve exibir o **Estoque em tempo real** do produto na tela de gestão (RF04). <br> CA04: O Colaborador deve conseguir editar o preço e a quantidade de estoque. |
| **Testes de Aceitação** | TA04.01: Cadastrar um produto com todos os campos obrigatórios e verificar a associação ao Colaborador. <br> TA04.02: Tentar editar o produto de outro colaborador (Gerente ou Colaborador) e verificar se o acesso é negado. <br> TA04.03: Editar a quantidade em estoque e verificar se o valor é atualizado imediatamente. |
| **Estimativa** | 14h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Essencial |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US05 - Acompanhar Estoque em Tempo Real (CU05)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Receber Alerta de Estoque Baixo para Reposição |
| **Story** | Como **Colaborador e Gerente**, eu quero **receber notificações em tempo real quando o estoque de um produto atingir um nível mínimo**, para **saber exatamente quando devo fazer a reposição de itens e evitar a perda de vendas (ruptura de estoque)**. |
| **Requisitos Relacionados** | RF04, RF05 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir configurar um **ponto de reposição** (estoque mínimo) para cada produto. <br> CA02: O sistema deve disparar uma notificação (visual no Dashboard) para o Colaborador e o Gerente quando o estoque for igual ou inferior ao ponto de reposição (RF05). <br> CA03: O Dashboard do Colaborador deve destacar os produtos com estoque baixo. |
| **Testes de Aceitação** | TA05.01: Configurar um ponto de reposição e simular uma venda que o atinja. Verificar se a notificação é gerada. <br> TA05.02: Verificar se a notificação é exibida para o Gerente e apenas para o Colaborador responsável pelo produto. |
| **Estimativa** | 10h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Essencial |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US06 - Gerenciar Promoções (CU06)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Aplicar e Gerenciar Promoções em Produtos |
| **Story** | Como **Colaborador**, eu quero **aplicar descontos nos meus produtos, definindo o novo preço e o período de validade**, para **aumentar as vendas de itens específicos e ter autonomia sobre minhas estratégias de preço**. |
| **Requisitos Relacionados** | RF09, RF10 |
| **Critérios de Aceitação** | CA01: O Colaborador deve conseguir definir o desconto por valor fixo ou percentual (RF09). <br> CA02: O sistema deve validar que o preço final seja maior que zero. <br> CA03: O sistema deve registrar a data de início e fim da promoção e aplicar o novo preço no sistema de vendas. <br> CA04: O sistema deve emitir uma **notificação de atualização de preço** (digital ou para integração futura com display da loja) (RF10). |
| **Testes de Aceitação** | TA06.01: Aplicar uma promoção por percentual e verificar se o preço é corretamente atualizado no cadastro. <br> TA06.02: Simular uma venda durante a vigência da promoção e verificar se o preço com desconto é aplicado. <br> TA06.03: Tentar aplicar um desconto que zere o preço e verificar se o sistema bloqueia. |
| **Estimativa** | 8h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US07 - Gerenciar Clientes (CRM) (CU07)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Manter Cadastro de Clientes para CRM |
| **Story** | Como **Gerente**, eu quero **cadastrar e gerenciar as informações de contato dos clientes da loja**, para **construir um banco de dados (CRM) e facilitar a comunicação e fidelização** (RF19). |
| **Requisitos Relacionados** | RF19 |
| **Critérios de Aceitação** | CA01: O Gerente deve conseguir cadastrar o Cliente com Nome, CPF e Contato. <br> CA02: O sistema deve verificar a unicidade do CPF para evitar duplicidade. <br> CA03: O Gerente deve conseguir consultar e editar os dados do Cliente. |
| **Testes de Aceitação** | TA07.01: Cadastrar um novo cliente e verificar se o registro é salvo no CRM. <br> TA07.02: Tentar cadastrar um cliente com CPF já existente e verificar o erro de duplicidade. |
| **Estimativa** | 6h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Média |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US08 - Realizar Venda (CU08)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Registrar Venda com Associação Correta de Produtos/Colaboradores |
| **Story** | Como **Gerente**, eu quero **registrar os itens de uma venda, identificando o Colaborador dono de cada produto**, para **garantir que a transação seja rastreável e que o repasse de comissão seja feito corretamente**. |
| **Requisitos Relacionados** | RF06 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir a inclusão de múltiplos produtos de diferentes colaboradores na mesma venda. <br> CA02: O sistema deve calcular o total da venda, aplicando automaticamente preços promocionais se houver. <br> CA03: O sistema deve identificar e registrar o **ID do Colaborador** associado a cada produto vendido (RF06). |
| **Testes de Aceitação** | TA08.01: Registrar uma venda com dois produtos de diferentes colaboradores e verificar se a associação correta é registrada. <br> TA08.02: Tentar registrar uma venda com quantidade maior que o estoque e verificar se o sistema emite o alerta. |
| **Estimativa** | 16h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Crítica |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US09 - Realizar Pagamento (CU09)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Finalizar Pagamento e Registrar Taxas de Serviço |
| **Story** | Como **Gerente**, eu quero **registrar a forma de pagamento e obter a taxa de serviço (maquininha/PIX) da transação**, para **concluir a venda, dar baixa no estoque e fornecer os dados para o cálculo financeiro preciso**. |
| **Requisitos Relacionados** | RF06, RF07 |
| **Critérios de Aceitação** | CA01: O sistema deve registrar a forma de pagamento (Dinheiro, Cartão, PIX). <br> CA02: O sistema deve receber (via integração ou input manual) e registrar o valor da **taxa de serviço** para pagamentos eletrônicos (RF07). <br> CA03: Após o pagamento, o sistema deve dar a **baixa definitiva no estoque**. |
| **Testes de Aceitação** | TA09.01: Registrar um pagamento em cartão e verificar se a taxa é registrada junto à transação. <br> TA09.02: Verificar se a quantidade do produto é reduzida no estoque após a conclusão. |
| **Estimativa** | 18h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Crítica |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US10 - Gerenciar Financeiro Geral (CU10)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Gerenciar e Receber Alertas de Contas a Pagar/Receber |
| **Story** | Como **Gerente**, eu quero **registrar os custos fixos e os aluguéis a receber da loja e ser alertado sobre os vencimentos**, para **manter o controle financeiro geral e evitar multas/atrasos**. |
| **Requisitos Relacionados** | RF18 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir o registro de Contas a Pagar (custos) e Contas a Receber (aluguéis). <br> CA02: O sistema deve emitir **alertas** visuais (no Dashboard Geral) sobre contas com vencimento nos próximos dias (RF18). <br> CA03: O Gerente deve conseguir marcar uma conta como paga ou recebida. |
| **Testes de Aceitação** | TA10.01: Registrar uma Conta a Pagar com vencimento para amanhã e verificar se o alerta aparece no Dashboard Geral. <br> TA10.02: Marcar uma Conta a Receber (aluguel) como recebida e verificar se o status é atualizado. |
| **Estimativa** | 12h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US11 - Calcular Repasses e Comissões (CU11)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Cálculo Automático de Repasses e Comissões (Regra de Negócio) |
| **Story** | Como **Sistema**, eu quero **calcular automaticamente o valor líquido (repasse) de cada venda para o Colaborador**, para **garantir a precisão e a transparência financeira, deduzindo taxas de serviço e a comissão da loja**. |
| **Requisitos Relacionados** | RF07, RF17 |
| **Critérios de Aceitação** | CA01: O cálculo deve ser disparado automaticamente após a conclusão do pagamento (CU09). <br> CA02: O cálculo deve seguir a fórmula: **Preço Bruto - Taxas de Serviço - Comissão da Loja = Repasse Líquido** (RF07, RF17). <br> CA03: O sistema deve conseguir calcular o repasse separadamente quando a venda envolver produtos de diferentes colaboradores. <br> CA04: O resultado do repasse deve ser armazenado na transação para ser visualizado pelo Colaborador (CU12). |
| **Testes de Aceitação** | TA11.01: Simular uma venda de R$100 com 5% de taxa de serviço e 10% de comissão da loja. Verificar se o Repasse Líquido é R$85,00. <br> TA11.02: Simular uma venda com 2 itens de 2 colaboradores diferentes e verificar se 2 repasses separados são calculados. |
| **Estimativa** | 20h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Crítica |
| **Protótipo** | *(Não se aplica, é um processo de *backend*)* |

-----

### User Story US12 - Visualizar Finanças e Repasses (CU12)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Visualizar Detalhe de Repasses, Comissões e Custos |
| **Story** | Como **Colaborador**, eu quero **visualizar o detalhe de cada venda, vendo exatamente o valor da comissão e das taxas descontadas**, para **ter total transparência e acompanhar meu lucro (Repasse Líquido) a qualquer momento**. |
| **Requisitos Relacionados** | RF07 |
| **Critérios de Aceitação** | CA01: O sistema deve exibir um extrato de vendas com o valor bruto e o Repasse Líquido total. <br> CA02: Ao detalhar a transação, o sistema deve mostrar os valores exatos de **Taxa da Maquininha**, **Comissão da Loja** e o **Repasse Líquido** (RF07). <br> CA03: O Colaborador deve conseguir filtrar a visualização por período (ex: mensal, semanal). |
| **Testes de Aceitação** | TA12.01: Acessar o detalhe de uma venda calculada (TA11.01) e verificar se todos os valores de deduções e o lucro (R$85,00) são exibidos corretamente. <br> TA12.02: Tentar acessar o detalhe de venda de outro colaborador e verificar se o acesso é bloqueado. |
| **Estimativa** | 10h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US13 - Visualizar Aluguel de Espaço (CU13)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Gerir Pagamentos de Aluguel do Espaço |
| **Story** | Como **Colaborador**, eu quero **visualizar o valor, a data de vencimento e o status de pagamento do aluguel do meu stand/prateleira**, para **organizar minhas finanças e garantir que estou em dia com a Loja**. |
| **Requisitos Relacionados** | RF16 |
| **Critérios de Aceitação** | CA01: O sistema deve exibir o valor e a descrição do Espaço alugado. <br> CA02: O sistema deve mostrar a **data de vencimento** e o **status** (Pago/Pendente/Vencido) da mensalidade (RF16). <br> CA03: O Colaborador deve conseguir visualizar o histórico de pagamentos de aluguel. |
| **Testes de Aceitação** | TA13.01: Acessar o módulo e verificar se o valor e o status do aluguel atual são exibidos corretamente. <br> TA13.02: Simular a marcação de pagamento do aluguel pelo Gerente (CU10) e verificar se o status do Colaborador muda para "Pago". |
| **Estimativa** | 6h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Média |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US14 - Visualizar Feedback de Clientes (CU14)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Acompanhar Avaliações de Clientes |
| **Story** | Como **Colaborador**, eu quero **acompanhar o feedback e a nota de avaliação dos clientes sobre meus produtos e o atendimento logístico**, para **identificar áreas de melhoria e medir a satisfação dos meus clientes**. |
| **Requisitos Relacionados** | RF20 |
| **Critérios de Aceitação** | CA01: O sistema deve exibir uma lista de avaliações recebidas. <br> CA02: O feedback deve ser associado ao produto e/ou ao serviço de atendimento/logística (RF20). <br> CA03: O Colaborador deve conseguir filtrar os feedbacks (ex: por nota ou data). |
| **Testes de Aceitação** | TA14.01: Simular a inserção de um feedback (externo) e verificar se ele é exibido no Dashboard do Colaborador. <br> TA14.02: Filtrar apenas as avaliações com nota baixa e verificar se a lista é correta. |
| **Estimativa** | 8h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Média |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US15 - Visualizar Dashboard Geral (CU15)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Visualizar Estatísticas e Dashboard Geral da Loja |
| **Story** | Como **Gerente**, eu quero **acessar um painel consolidado com estatísticas sobre vendas, estoque e finanças de todas as lojas/colaboradores**, para **ter uma visão geral do desempenho do negócio e tomar decisões estratégicas**. |
| **Requisitos Relacionados** | RF11 |
| **Critérios de Aceitação** | CA01: O Dashboard deve carregar rapidamente (RNF02) após o login. <br> CA02: O sistema deve exibir KPIs sobre **Vendas Totais**, **Estoque Geral**, **Aluguéis Pendentes** e **Contas a Pagar/Receber** (RF11). <br> CA03: O Gerente deve conseguir filtrar os dados por período (ex: Mês, Semana). |
| **Testes de Aceitação** | TA15.01: Acessar o Dashboard Geral e verificar se todos os KPIs listados são exibidos. <br> TA15.02: Filtrar por um mês anterior e verificar se os dados de vendas se alteram corretamente. |
| **Estimativa** | 12h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US16 - Visualizar Dashboard Pessoal (CU16)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Personalizar e Acessar Dashboard Pessoal de Métricas |
| **Story** | Como **Colaborador**, eu quero **acessar meu painel pessoal de desempenho e escolher os indicadores (KPIs) que desejo acompanhar**, para **focar nas métricas mais importantes para o meu negócio (faturamento, ticket médio, etc.)**. |
| **Requisitos Relacionados** | RF12, RF13 |
| **Critérios de Aceitação** | CA01: O Dashboard Pessoal deve carregar ao fazer o login (RF12). <br> CA02: O Colaborador deve ter uma interface para **selecionar/remover** os KPIs que deseja exibir (RF13). <br> CA03: Os KPIs devem refletir apenas os dados de vendas e estoque do próprio Colaborador. |
| **Testes de Aceitação** | TA16.01: Acessar a tela de configuração e adicionar/remover um KPI (ex: Ticket Médio). Verificar se o Dashboard é atualizado. <br> TA16.02: Verificar se os dados exibidos são consistentes com os Relatórios de Vendas (CU17). |
| **Estimativa** | 10h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |

-----

### User Story US17 - Gerar Relatórios Pessoais de Venda (CU17)

| **Papeis** | |
| :--- | :--- |
| **Analista** | [A definir] |
| **Desenvolvedor** | [A definir] |
| **Revisor** | [A definir] |
| **Testador** | [A definir] |

| Campo | Descrição |
| :--- | :--- |
| **Título** | Gerar Relatório de Produtos Mais Vendidos |
| **Story** | Como **Colaborador**, eu quero **gerar um relatório semanal ou mensal das minhas vendas**, para **ver quais produtos tiveram mais saída e planejar minha produção e reposição de estoque**. |
| **Requisitos Relacionados** | RF08 |
| **Critérios de Aceitação** | CA01: O sistema deve permitir a seleção de períodos (semanal ou mensal) (RF08). <br> CA02: O relatório gerado deve listar os produtos e suas quantidades vendidas, **destacando os mais vendidos**. <br> CA03: O sistema deve permitir a exportação do relatório (Ex: PDF ou CSV). |
| **Testes de Aceitação** | TA17.01: Gerar um relatório mensal e verificar se os produtos com maior volume de vendas estão no topo. <br> TA17.02: Exportar o relatório e verificar se o arquivo gerado está completo e formatado. |
| **Estimativa** | 8h |
| **Tempo Real Gasto** | |
| **Tamanho Funcional** | x PF |
| **Prioridade** | Alta |
| **Protótipo** | *(inserir link ou imagem do protótipo)* |
