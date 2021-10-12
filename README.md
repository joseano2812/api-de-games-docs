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
##### Falha na autenticação! 401
Caso essa reposta acontença, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido e token expirado.

