# Documentação - COLAB

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
| RNF01 | Impedir que dois colabores vendão o mesmo produto |
| RNF02 | Impedir que tenha mais de dois ramo iguais na mesma loja |
| RNF03 | O sistema deve fazer o backup das informações pelo menos uma vez ao dia |
| RNF04 | O sistema deve ser web |
| RNF05 | As credenciais dos colabores e informações pessoais sensíveis devem ser criptografadas |
| RNF06 | A UI deve ser de fácil acesso aos usuários que são leigos em informática|
| RNF07 | A UI deve possuir cores que cumpram os requisitos determinandos pelos padrões WCAG em exigências com **POUR** |
| RNF08 | O sistema deve ser escalável com o tempo |

# Diagrama de Caso de Uso

<center>

[Link para o diagrama](https://lucid.app/lucidchart/22ee5153-410f-48be-9e4b-42a95e3f0678/edit?invitationId=inv_d4deb7ed-0afc-4be2-b5cc-7448a8a57ab8&page=0_0#)

</center>

![alt text](assets/imgs/DiagramaCasoDeUso.png)

# Documentação

## Manter Colaborador
**Nome:** Manter Colaborador <br>
**Descrição:** Este caso de uso permite que sejam cadastrados, editados e excluído os colabores pelos gerentes. As informações para os cadastros: `Nome, data de nascimento, cpf, e ramo do negócio`. _Autores_: Gerente<br>
**Pré-Condição:** Se a marca do ramo do negócio já existir na loja, será impossível cadastrar. <br>
**Pós-Condições:** NA

### Cenário Principal
***

**Inclusão:** 
> a. O gerente insere o nome, data de nascimento, cpf, e ramo do negócio do novo colaborador e clicar em salvar.
> b. O sistema salva as informações no sistema. 

**Remoção:** 
> a. O gerente informa o CPF do usuário e clica em remover do sistema.
> b. O sistema oculta as informações do colaborador.

**Consulta:**
> a. O gerente informa o CPF do colaborador e clica em buscar.
> b. O sistema retorna os dados do usuário.

**Edição:**
> a. O gerente informa o CPF do usuário e pode atualizar os dados do colaborador e clicar em salvar.
> b. O sistema salva as informações no sistema.

### Cenário Alternativo:

***
**Inclusão:**
> 1a. O ramo do negócio do colaborador já existe no sistema.
*  O sistema exibe que é impossível cadastrar mais de um colaborador com mesmo ramo de negócio e retorna ao sistema.

**Remoção, Consulta e Edição:**
> 2a. O gerente pode digitar o CPF incorreto ou o CPF pode não existir.
* O gerente digita novamente o CPF e clica em buscar.
* O sistema retorna os dados do colaborador se esse existir.

## Manter Cliente
**Nome:** Manter Cliente <br>
**Descrição:** Este caso de uso permite que sejam cadastrados, editados e excluidos os clientes pelos gerentes. As informações para os cadastros: `Nome, cpf, endereço e contato`. _Autores_: Gerente<br>
**Pré-Condição:** O Cliente ainda não está cadastrado no sistema.
**Pós-Condição:** Um ID único foi gerado e associado ao cliente.

### Cenário Principal
***

**Inclusão:**
> 1. O gerente preenche os dados do cliente clica em “Salvar”. <br>
> 2. O sistema armazena as informações no banco de dados e confirma a inclusão.

**Consulta:**
> 1. O gerente informa o CPF do cliente e clica em “Buscar”.<br>
> 2. O sistema exibe os dados do cliente, se encontrados.

**Edição:**
> 1. O gerente informa o CPF do cliente (include Consulta).<br>
> 2. O gerente atualiza os dados desejados e clica em “Atualizar”.<br>
> 3. O sistema salva as novas informações no banco de dados.

**Remoção:**
> 1. O gerente informa o CPF do cliente (include Consulta).<br>
> 2. O gerente clica em “Remover”.<br>
> 3. O sistema oculta as informações pessoais do cliente e marca o status como inativo.

### Cenário Alternativo:
***

**Inclusão ou Edição:**
> 1a. O gerente informou um CPF inválido.
  - 1. O sistema informará que o CPF é inválido.
  - 2. O gerente digita um novo CPF válido e clica em "Salvar".
  - 3. O sistema salva os dados do cliente no banco de dados.

**Consulta ou Remoção:**
> 1a. O cliente não está cadastrado no sistema.
  - 1. O sistema exibe uma mensagem de cliente não cadastrado.
