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

| Requisito | Descrição                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------|
| RF01      | Adicionar os produtos dentro do sistema com suas informações [COD, NOME, PREÇO, DESCRIÇÃO].    |
| RF02      | Solicitar a baixa, em quantidade, de algum produto em específico.                             |
| RF03      | Visualizar vendas e produtos da sua loja.                                                    |
| RF04      | Alterar informações do produto.                                                              |
| RF05      | Visualizar relatórios de vendas.                                                             |
| RF06      | Cadastrar o usuário com todas suas informações pessoais e seu ramo de venda [DADOS PESSOAIS, RAMO DO NEGÓCIO]. |
| RF07      | Notificar sobre a falta de estoque aos colaboradores.                                        |
| RF08      | Visualizar todos os colaboradores da loja.                                                  |
| RF09      | Visualizar o estoque dos colaboradores.                                                     |
| RF10      | Visualizar todas as vendas do sistema.                                                      |


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


# Caso de Uso
![Diagrama Caso de Uso](<assets/imgs/OSM-CASO DE USO.jpg>)

# Documentação dos Atores e Casos de Uso

# Atores

1. **Colaborador:** Usuário que gerencia seus produtos e visualiza suas vendas.
2. **Gerente:** Responsável por gerenciar colaboradores, clientes e ter visão geral da loja.
3. **Cliente:** Usuário que participa apenas quando compra um produto e para seu próprio cadastro no sistema.
4. **Sistema de Pagamento:** Sistema externo para processamento de pagamentos.

# Casos de uso

## Manter Colaborador

**Nome:** Cadastrar Colaborador  
**Descrição:** Este caso de uso permite o cadastro de colaboradores no sistema. As informações exigidas são: *nome, data de nascimento, CPF e ramo de negócio*.  
**Atores:** *Gerente e Colaborador*  
**Pré-condição:** O colaborador e o ramo de negócio não devem estar previamente cadastrados no sistema.  
**Pós-condição:** Um ID único é gerado e associado ao colaborador.  

**Fluxo Principal**  
1. O gerente preenche os dados do colaborador e clica em *Salvar*.  
2. O sistema valida os dados.  
3. O sistema salva o colaborador no banco de dados.  
4. O sistema retorna os dados do novo colaborador.  

**Fluxo Alternativo - A (CPF inválido)**  
- 2a. O CPF informado é inválido.  
  1. O gerente corrige os dados preenchidos.  
  2. Retorna ao passo 2 do fluxo principal.  

**Fluxo Alternativo - B (Ramo de negócio já existente)**  
- 2b. O sistema informa que o ramo de negócio já está cadastrado.  
  1. O sistema encerra o caso de uso.  

**Fluxo Alternativo - C (Colaborador já cadastrado)**  
- 2c. O CPF informado já existe no sistema.  
  1. O sistema informa que o colaborador já está cadastrado.  
  2. O sistema encerra o caso de uso.  

---

**Nome:** Consultar Colaborador  
**Descrição:** Este caso de uso permite que o gerente visualize os dados de um colaborador previamente cadastrado no sistema.  
**Ator:** *Gerente*  
**Pré-condição:** O colaborador deve estar cadastrado no sistema.  
**Pós-condição:** N/A  

**Fluxo Principal**  
1. O gerente informa o CPF do colaborador.  
2. O sistema retorna os dados do colaborador.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O CPF informado não existe no sistema.  
  1. O sistema informa que o CPF não foi encontrado.  
  2. O gerente digita novamente o CPF.  
  3. Retorna ao passo 2 do fluxo principal.  

---

**Nome:** Editar Colaborador  
**Descrição:** Este caso de uso permite que o gerente edite os dados de um colaborador cadastrado.  
**Ator:** *Gerente*  
**Pré-condição:** O colaborador deve estar cadastrado no sistema.  
**Pós-condição:** Os dados do colaborador são atualizados.  

**Fluxo Principal**  
1. O gerente informa o CPF do colaborador.  
2. O sistema retorna os dados do colaborador.  
3. O gerente realiza as modificações necessárias.  
4. O sistema valida os novos dados.  
5. O sistema atualiza os dados no banco de dados.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O CPF informado não existe no sistema.  
  1. O sistema informa que o CPF não foi encontrado.  
  2. O gerente digita novamente o CPF.  
  3. Retorna ao passo 2 do fluxo principal.  

**Fluxo Alternativo - B (Dados inválidos)**  
- 4b. Os dados informados são inválidos.  
  1. O sistema informa que os dados são inconsistentes.  
  2. O sistema encerra o caso de uso.  

---

**Nome:** Remover Colaborador  
**Descrição:** Este caso de uso permite que o gerente remova um colaborador do sistema.  
**Ator:** *Gerente*  
**Pré-condição:** O colaborador deve estar cadastrado no sistema.  
**Pós-condição:** O colaborador é desativado no sistema.  

**Fluxo Principal**  
1. O gerente informa o CPF do colaborador.  
2. O sistema retorna os dados do colaborador.  
3. O gerente confirma a remoção.  
4. O sistema desativa o colaborador no sistema.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O CPF informado não existe no sistema.  
  1. O sistema informa que o CPF não foi encontrado.  
  2. O gerente digita novamente o CPF.  
  3. Retorna ao passo 2 do fluxo principal.  


## Manter Cliente

**Nome:** Cadastrar Cliente  
**Descrição:** Este caso de uso permite que os gerentes cadastrem clientes no sistema. As informações para o cadastro incluem: *nome, CPF, endereço e contato*.  
**Autores:** *Gerente e Cliente*  
**Pré-condição:** O cliente ainda não está cadastrado no sistema.  
**Pós-condição:** Um ID único é gerado e associado ao cliente.  

**Fluxo Principal**  
1. O gerente preenche os dados do cliente.  
2. O sistema valida os dados.  
3. O sistema salva os dados no banco de dados.  

**Fluxo Alternativo - A (CPF inválido)**  
- 2a. O sistema informa que o CPF é inválido.  
  1. O gerente corrige o CPF do cliente.  
  2. Retorna ao passo 2 do fluxo principal.  

**Fluxo Alternativo - B (CPF já existente)**  
- 2a. O sistema informa que o CPF já está cadastrado.  
  1. O sistema retorna os dados do cliente correspondente.  
  2. O sistema encerra o caso de uso.  

---

**Nome:** Visualizar Cliente  
**Descrição:** Este caso de uso permite que os gerentes visualizem os dados dos clientes.  
**Autores:** *Gerente*  
**Pré-condição:** O cliente deve estar cadastrado no sistema.  
**Pós-condição:** N/A  

**Fluxo Principal**  
1. O gerente digita o CPF do cliente.  
2. O sistema retorna os dados do cliente.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O sistema informa que o CPF não foi encontrado.  
  1. O gerente digita novamente o CPF do cliente.  
  2. Retorna ao passo 2 do fluxo principal.  

---

**Nome:** Editar e Excluir Cliente  
**Descrição:** Este caso de uso permite que os gerentes editem ou excluam os dados dos clientes.  
**Autores:** *Gerente*  
**Pré-condição:** O cliente deve estar cadastrado no sistema.  
**Pós-condição:** Os dados do cliente são atualizados ou o cliente é desativado no sistema.  

**Fluxo Principal - Editar Cliente**  
1. O gerente digita o CPF do cliente.  
2. O sistema retorna os dados do cliente.  
3. O gerente escolhe os campos a serem modificados.  
4. O sistema valida os dados.  
5. O sistema atualiza os dados no banco de dados.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O sistema informa que o CPF não foi encontrado.  
  1. O gerente digita novamente o CPF do cliente.  
  2. Retorna ao passo 2 do fluxo principal.  

**Fluxo Alternativo - B (CPF inválido)**  
- 4b. O sistema informa que o CPF é inválido.  
  1. O gerente digita novamente o CPF do cliente.  
  2. Retorna ao passo 2 do fluxo principal.  

---

**Fluxo Principal - Excluir Cliente**  
1. O gerente digita o CPF do cliente.  
2. O sistema retorna os dados do cliente.  
3. O gerente confirma a exclusão do cliente.  
4. O sistema desativa o cliente no banco de dados.  

**Fluxo Alternativo - A (CPF não encontrado)**  
- 2a. O sistema informa que o CPF não foi encontrado.  
  1. O gerente digita novamente o CPF do cliente.  
  2. Retorna ao passo 2 do fluxo principal.


## Manter Ramo de Negócio

**Nome:** Cadastrar Ramo de Negócio  
**Descrição:** Este caso de uso permite que os gerentes cadastrem os ramos de negócio dos colaboradores. As informações para o cadastro incluem: *nome*.  
**Autores:** *Gerente*  
**Pré-condição:** O ramo de negócio ainda não está cadastrado no sistema.  
**Pós-condição:** Um ID único é gerado e associado ao novo ramo de negócio.  

### Fluxo Principal
1. O gerente insere o nome do novo ramo de negócio.
2. O sistema valida se o nome é válido e se não há duplicidade.
3. O sistema salva o ramo de negócio no banco de dados.

### Fluxo Alternativo - A (Nome inválido)
- 2a. O sistema informa que o nome inserido é inválido.
  1. O gerente corrige o nome.
  2. Retorna ao passo 2 do fluxo principal.

### Fluxo Alternativo - B (Ramo já existente)
- 2b. O sistema informa que o ramo de negócio já está cadastrado.
  1. O sistema retorna os dados do ramo já existente.
  2. O sistema encerra o caso de uso.

---

**Nome:** Visualizar Ramo de Negócio  
**Descrição:** Este caso de uso permite que os gerentes visualizem os ramos de negócio cadastrados no sistema.  
**Autores:** *Gerente*  
**Pré-condição:** Deve haver pelo menos um ramo de negócio cadastrado.  
**Pós-condição:** N/A  

### Fluxo Principal
1. O gerente solicita a visualização dos ramos de negócio.
2. O sistema exibe a lista de ramos cadastrados.

### Fluxo Alternativo - A (Nenhum ramo cadastrado)
- 2a. O sistema informa que não há ramos de negócio cadastrados.

---

**Nome:** Editar e Excluir Ramo de Negócio  
**Descrição:** Este caso de uso permite que os gerentes editem ou excluam ramos de negócio cadastrados.  
**Autores:** *Gerente*  
**Pré-condição:** O ramo de negócio deve estar cadastrado no sistema.  
**Pós-condição:** Os dados do ramo de negócio são atualizados ou o ramo é desativado no sistema.  

### Fluxo Principal - Editar Ramo de Negócio
1. O gerente seleciona o ramo de negócio por meio de uma lista ou digita o ID correspondente.
2. O sistema exibe os dados atuais do ramo.
3. O gerente edita o nome do ramo de negócio.
4. O sistema valida o novo nome.
5. O sistema atualiza os dados no banco de dados.

### Fluxo Alternativo - A (Ramo não encontrado)
- 2a. O sistema informa que o ID informado ou a seleção não corresponde a nenhum ramo de negócio cadastrado.
  1. O gerente tenta novamente, escolhendo da lista ou digitando um novo ID.
  2. Retorna ao passo 2 do fluxo principal.

### Fluxo Principal - Excluir Ramo de Negócio
1. O gerente seleciona o ramo de negócio por meio de uma lista ou digita o ID correspondente.
2. O sistema exibe os dados do ramo.
3. O gerente confirma a exclusão.
4. O sistema desativa o ramo de negócio no banco de dados.

### Fluxo Alternativo - B (Ramo não encontrado)
- 2a. O sistema informa que o ID informado ou a seleção não corresponde a nenhum ramo de negócio cadastrado.
  1. O gerente tenta novamente, escolhendo da lista ou digitando um novo ID.
  2. Retorna ao passo 2 do fluxo principal.

---

## Manter Produto

**Nome:** Cadastrar Produto  
**Descrição:** Este caso de uso permite que produtos sejam cadastrados no sistema. As informações exigidas são: *Nome, Descrição, Quantidade e Valor Unitário*.  
**Atores:** *Colaborador e Gerente*  
**Pré-condição:** O produto não deve estar cadastrado no sistema.  
**Pós-condição:** Um ID único é gerado e associado ao produto.  

### Fluxo Principal
1. O autor (colaborador ou gerente) clica para adicionar produto.
2. O autor preenche os dados do produto.
3. O sistema valida os dados.
4. O sistema salva os dados no banco de dados.

### Fluxo Alternativo - A (Produto já cadastrado)
- 3a. O sistema identifica que o produto já está cadastrado.
  1. O sistema informa que o produto já existe.
  2. O autor pode encerrar o caso de uso ou reiniciar o cadastro.

---

**Nome:** Visualizar Produto  
**Descrição:** Este caso de uso permite que produtos cadastrados sejam visualizados.  
**Atores:** *Colaborador e Gerente*  
**Pré-condição:** O produto deve estar cadastrado no sistema.  
**Pós-condição:** N/A  

### Fluxo Principal
1. O autor busca o produto pelo ID.
2. O sistema retorna os dados do produto.

### Fluxo Alternativo - A (ID não encontrado)
- 2a. O sistema não encontra o ID informado.
  1. O sistema informa que o ID não foi encontrado.
  2. O autor digita o ID novamente.
  3. Retorna ao passo 2 do fluxo principal.

---

**Nome:** Editar Produto  
**Descrição:** Este caso de uso permite que produtos cadastrados sejam editados.  
**Atores:** *Colaborador e Gerente*  
**Pré-condição:** O produto deve estar cadastrado no sistema.  
**Pós-condição:** Os dados do produto são atualizados no sistema.  

### Fluxo Principal
1. O autor busca o produto pelo ID.
2. O sistema retorna os dados do produto.
3. O autor informa os novos dados a serem alterados.
4. O sistema atualiza os dados no banco de dados.

### Fluxo Alternativo - A (ID não encontrado)
- 2a. O sistema não encontra o ID informado.
  1. O sistema informa que o ID não foi encontrado.
  2. O autor digita o ID novamente.
  3. Retorna ao passo 2 do fluxo principal.

---

**Nome:** Excluir Produto  
**Descrição:** Este caso de uso permite que produtos cadastrados sejam removidos do sistema.  
**Atores:** *Colaborador e Gerente*  
**Pré-condição:** O produto deve estar cadastrado no sistema.  
**Pós-condição:** O produto é desativado no sistema.  

### Fluxo Principal
1. O autor busca o produto pelo ID.
2. O sistema retorna os dados do produto.
3. O autor confirma a exclusão do produto.
4. O sistema desativa o produto no banco de dados.

### Fluxo Alternativo - A (ID não encontrado)
- 2a. O sistema não encontra o ID informado.
  1. O sistema informa que o ID não foi encontrado.
  2. O autor digita o ID novamente.
  3. Retorna ao passo 2 do fluxo principal.

---

## Realizar Pagamento

**Nome:** Realizar Pagamento  
**Descrição:** Este caso de uso permite a finalização de uma venda por meio de pagamento, realizado pelo cliente com mediação do gerente.  
**Atores:** *Gerente e Cliente*  
**Pré-condição:** A venda deve estar registrada com o valor total calculado.  
**Pós-condições:** O pagamento é registrado, o estoque é mantido atualizado e um ID único é associado ao pagamento.  

### Fluxo Principal
1. O sistema exibe o valor total da venda.
2. O gerente informa a forma de pagamento (dinheiro, cartão, pix, etc.).
3. O cliente realiza o pagamento.
4. O sistema valida e confirma o pagamento.
5. O sistema finaliza a venda e gera o comprovante.

### Fluxo Alternativo - A (Cliente desiste)
- 3a. O cliente desiste do pagamento.
  1. O gerente confirma o cancelamento.
  2. O sistema cancela a venda e encerra o caso de uso.

---

## Vender Produto

**Nome:** Vender Produto  
**Descrição:** Este caso de uso permite que uma venda seja realizada por um gerente.  
**Ator:** *Gerente e Cliente*  
**Pré-condição:** Os produtos envolvidos na venda devem estar cadastrados e disponíveis em estoque.  
**Pós-condições:** Venda registrada, estoque atualizado e um ID único associado à venda.  

### Fluxo Principal
1. O gerente informa os IDs dos produtos.
2. O gerente informa a quantidade de cada produto.
3. O sistema valida a existência e disponibilidade dos produtos.
4. O sistema calcula o total da venda.
5. O gerente confirma a venda.
6. O gerente solicita o CPF cliente na venda.
7. A venda é registrada.
8. O sistema dá baixa no estoque.
9. O sistema salva os dados da venda.

### Fluxo Alternativo - A (Produto não encontrado)
- 1a. O sistema não encontra um ou mais IDs informados.
  1. O sistema informa que o(s) produto(s) não foram encontrados.
  2. O gerente informa os IDs corretos.
  3. Retorna ao passo 2 do fluxo principal.

### Fluxo Alternativo - B (Quantidade insuficiente)
- 3b. A quantidade informada excede a disponível no estoque.
  1. O sistema informa a indisponibilidade.
  2. O gerente pode alterar a quantidade ou remover o produto da venda.
  3. Retorna ao passo 3 do fluxo principal.

### Fluxo Alternativo - C (Venda cancelada)
- 5c. O gerente opta por cancelar a venda antes da confirmação.
  1. O sistema encerra o caso de uso sem alterações no estoque.

### Fluxo Alternativo - D (Cliente não encontrado)
- 6d. O CPF do cliente não está no sistema.
  1. O sistema informa que o cliente não está cadastrado.
  2. O gerente cadastra o cliente.
  3. Retorna ao passo 6 do fluxo principal.
