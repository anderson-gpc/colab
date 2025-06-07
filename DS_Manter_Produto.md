```mermaid
sequenceDiagram
    box Consultar Produto
        actor Colaborador
        participant Interface
        participant Produto
    end

    Colaborador->>Interface: Consultar Produto
    Interface->>Produto: consultar(p: Produto): Produto
   
    alt Consultar Produto
        Produto-->>Interface: Dados do Produto
    else false
        Produto-->>Interface: Produto não existe
    end
```
```mermaid
sequenceDiagram
    box Adicionar Produto
        actor Colaborador
        participant Interface
        participant Produto
    end
    opt
        note over Colaborador, Produto: Consultar Produto
    end
    Colaborador->>Interface: Adicionar Produto
    Interface->>Produto: adicionar(p: Produto): booleano
    alt Adicionar Produto
        Produto-->>Interface: Produto Adicionado
    else false
        Produto-->>Interface: Erro ao adicionar
    end
```

```mermaid
sequenceDiagram
    box Excluir Produto
        actor Colaborador
        participant Interface
        participant Produto
    end
    opt
        note over Colaborador, Produto: Consultar Produto
    end
    Colaborador->>Interface: Excluir Produto
    Interface->>Produto: excluir(p: Produto): void
```


```mermaid
sequenceDiagram
    box Editar Produto
        actor Colaborador
        participant Interface
        participant Produto
    end
    opt
        note over Colaborador, Produto: Consultar Produto
    end
    Colaborador->>Interface: Editar Produto
    Interface->>Produto: editar(p: Produto): void
```
