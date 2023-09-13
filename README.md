# Prepare project
- npm init
- npm i express express-graphql graphql
- npm i --save-dev nodemon

# Commits info

- `server is running` - blank express template
- `2. GraphQL HelloWorld` 

    open localhost:5000/graphql in the browser. You should see graphql UI.
    You can query:
    ```
    query {
      message
    } 
    ```

    or
    ```
    {
      message
    } 
    ```

    It should return 
    ```json
    {
      "data": {
        "message": "Hello World"
      }
    }
    ```

- `3. Query books info` 

    use query to get only names of the books:
    ```
    {
        books {
            name
        }
    }
    ```
  The same way you can query id and authodId

- `4. Query authors inside books`

    ```
    {
        books {
            id
            author {
              name
            }
        }
    }
    ```

- `5. Query authors list`

    ```
    {
      authors {
        id,
        name
      }
    }
    ```