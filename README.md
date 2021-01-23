# dev-concepts-backend

# command

> yarn init -y
> yarn add express
> yarn add nodemon -D
> yarn add uuidv4

# Métodos HTTP

- GET: Buscar informações do back-end
- POST: Criar uma informação no back-end
- PUT/PATCH: Alterar uma informação no back-end
- DELETE: Deletar uma informação no back-end

# Tipos de Parâmetros

- Query params: Filtros e paginação
    Exemplo 1
      const query = request.query
      console.log(query)
      Resultado = { title: 'React', owner: 'Diego' }
    Exemplo 2 (Desestruturando)
      const { title, owner } = request.query
      console.log(title)
      console.log(owner)
      Resultado = React
                  Diego

- Route params: Identificar recursos (Atualizar/Deletar)
    Exemplo 1
      const params = request.params
      console.log(params)
      Resultado = { id: '1' }
    Exemplo 2
      const { id } = request.params
      console.log(id)
      Resultado = 1

- Request body: Conteúdo na hora criar ou editar um recurso (JSON)
    Exemplo 1
      const body = request.body
      console.log(body)
      Resultado = undefined
                  { title: 'Aplicativo React Native', owner: 'Marcelo Basílio'} -> app.use(express.json())  para o express enviar JSON
    Exemplo 2 (Desestruturando)
      const { title, owner } = request.body
      console.log(title)
      console.log(owner)
      Resultado = Aplicativo React Native
