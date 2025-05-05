# Documentação - COLAB

> Como colaboradora eu quero poder controlar o estoque dos meus produtos e ser notificada quando um produto acabou, ver minhas vendas e poder alterar o preço dos produtos,  ter um relatório de quais produtos vendem mais, assim como o valor médio dos produtos comprados, editar as informações dos produtos, ter uma madeira de pagar o aluguel da loja, ser uma interface fácil de usada.N
Como gerente dos colaboradores eu quero poder notificar os colabores de falta de produto, às vezes uma pessoa vem atrás de algo e não tem. Não quero ter acesso à edição, apenas ver as informações como estoque; vendas; pagamento de aluguel; os outros colaboradores não podem ver as informações um dos outros. O sistema deve ter um backup das informações, na web e local, ser uma interface fácil de usar., ser web

## Descrição do Projeto

### Definição dos usuários

| Número | Perfil | Descrição |
| ---------- | ------- | ------|
| 1 | Colaborador | Usuário do sistema o qual tem função de colabor na loja, ele pode adicionar, solicitar a baixa e alterar produtos. Ele pode visualizar apenas seus próprios produtos dentro do sistema. |
| 2 | Gerente | Usuário do sistema o qual gerencia os colabores, possui a visão geral dos colabores, como estoque, vendas e pagamentos de aluguel.|
| 3 | Sistema de Pagamento | Sistema externo de pagamento |

### Requisitos Funcionais
| Requisito | Descrição | Ator |
| - | - | - |
| RF01 | Adicionar os produtos dentro do sistema com suas informações [COD, NOME, PREÇO, DESCRIÇÃO] | Colaborador |
| RF02 | Solicitar a baixa, em quantidade, de algum produto em específico | Colaborador |
| RF03 | Visualizar vendas e produtos da sua loja | Colaborador |
| RF04 | Alterar informações do produto | Colabodrador |
| RF05 | Visualizar relatórios de vendas | Colaborador |
| RF06 | Cadastrar o usuário com todas suas informações pessoais e seu ramo de venda [DADOS PESSOAIS, RAMO DO NEGÓCIO] | Gerente |
| RF07 | Notificar sobre a falta de estoque aos colaboradore| Gerente |
| RF08 | Visualizar todos os colabores da loja | Gerente |
| RF09 | Visualizar o estoque dos colaboradores | Gerente |
| RF10 | Visualizar todas as vendas do sistema | Gerente |

### Requisitos Não Funcionais
| Requisito | Descrição |
| - | - |
| RNF01 | Impedir que dois colabores vendem o mesmo produto |
| RNF02 | Impedir que tenha mais de dois ramo iguais na mesma loja |
| RNF03 | O sistema deve fazer o backup das informações pelo menos uma vez ao dia |
| RNF04 | O sistema deve ser web |
| RNF05 | As credenciais dos colabores e informações pessoais sensíveis devem ser criptografadas |
| RNF06 | A UI deve ser de fácil acesso aos usuários que são leigos em informática|
| RNF07 | A UI deve possuir cores que cumpram os requisitos determinandos pelos padrões WCAG em exigências com **POUR** |
| RNF08 | O sistema deve ser escalável com o tempo |
