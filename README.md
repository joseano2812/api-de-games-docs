# API de Games
Esta API é utilizada para criação, edição e deleção de jogos.
## Endpoints
### GET /Games
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parâmetros
Nenhum
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.

Exemplo de resposta:
```

[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 65,
        "title": "Sea of dieve",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]
```
##### Falha na autenticação! 401
Caso essa reposta acontença, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido e Token expirado.

Exemplo de reposta:
```
{
    "err": "Token inválido!"
}

```

### POST /auth
Esse endpoint é responsável por fazer o processo de login.
#### Parâmetros
email: E-mail do usuário cadastrado no sistema.

password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail.

Exemplo:
```
{
    "email": "victordevtb@guiadoprogramador.com",
    "password": "nodejs<3"
}
```
#### Respostas
##### OK! 200
Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:
```

{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJ2aWN0b3JkZXZ0YkBndWlhZG9wcm9ncmFtYWRvci5jb20iLCJpYXQiOjE2MzQwNjkyODMsImV4cCI6MTYzNDI0MjA4M30.5rpGvihfiuZNnvzdm3IttYm0cYjtW7wGilrRAZhrgkI"
}
```
##### Falha na autenticação! 401
Caso essa reposta acontença, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Senha ou e-mail incorretos.

Exemplo de reposta:
```
{err: "Credenciais inválidas!"}
```

