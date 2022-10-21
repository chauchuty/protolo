## Login:
##### Cliente
```json
{
    "operacao": "login",
    "parametros": {
        "ra": "2098270",
        "senha": "010203"
    }
}
```
### Servidor:
```json
{
    "status": 200,
    "mensagem": "Usuário logado com sucesso!",
    "dados": {
        "operacao": "login"
    }
}

{
    "status": 404,
    "mensagem": "Usuário não encontrado / Usuário ou senha inválido!",
    "dados": {
        "operacao": "login"
    }
}

{
    "status": 403,
    "mensagem": "Usuário já encontra-se conectado!",
    "dados": {}
}

{
    "status": 500,
    "mensagem": "Erro interno do servidor",
    "dados": {
        "operacao": "login"
    }
}
```

## Cadastro:
##### Cliente
```json
{
    "operacao": "cadastrar",
    "parametros": {
        "nome": "Jacúncio José",
        "ra": "2098270",
        "senha": "010203",
        "categoria_id": 3,
        "descricao": "Estudante de Engenharia de Software"
    }
}

```
### Servidor:
```json
{
    "status": 201,
    "mensagem": "Usuário cadastrado com sucesso!",
    "dados": {
        "operacao": "cadastrar"
    }
}

{
    "status": 400,
    "mensagem": "Parâmetros enviados não correspondem à operação!",
    "dados": {
        "operacao": "cadastrar"
    }
}

{
    "status": 202,
    "mensagem": "Usuário já encontra-se cadastrado!",
    "dados": {
        "operacao": "cadastrar"
    }
}

{
    "status": 500,
    "mensagem": "Erro interno do servidor",
    "dados": {
        "operacao": "cadastrar"
    }
}
```

## Logout:
##### Cliente
```json
{
    "operacao": "logout",
    "parametros": {
        "ra": "2098270",
        "senha": "010203",
    }
}

```
### Servidor:
```json
{
    "status": 600,
    "mensagem": "Usuário desconectado com sucesso!",
    "dados": {
        "operacao": "logout"
    }
}

{
    "status": 404,
    "mensagem": "Usuário não encontrado!",
    "dados": {
        "operacao": "logout"
    }
}

{
    "status": 202,
    "mensagem": "Usuário já  encontra-se desconectado!",
    "dados": {
        "operacao": "logout"
    }
}

{
    "status": 500,
    "mensagem": "Erro interno do servidor",
    "dados": {
        "operacao": "logout"
    }
}
```

## Obter Usuários:
##### Cliente
```json
{
    "operacao": "obter_usuarios",
    "parametros": {
        "ra": "2098270",
        "senha": "010203",
    }
}

```
### Servidor:
```json
{
    "status": 200,
    "mensagem": "Lista de Usuários",
    "dados": {
        "operacao": "obter_usuarios",
        "usuarios": [
            { "id": 1, "nome": "Jacúcio José", "descricao": "Lorem Ipsum...", "disponivel": 1, "categoria_id": 1 },
            { "id": 2, "nome": "Maria João", "descricao": "Lorem Ipsum...", "disponivel": 0, "categoria_id": 2 },
            { "id": 3, "nome": "João Silva", "descricao": "Lorem Ipsum...", "disponivel": 1, "categoria_id": 3 }
        ]
    }
}

{
    "status": 401,
    "mensagem": "Não foi possível retornar usuários",
    "dados": {
        "operacao": "obter_usuarios"
    }
}

{
    "status": 500,
    "mensagem": "Erro interno do servidor",
    "dados": {
        "operacao": "obter_usuarios"
    }
}
```
