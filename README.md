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

- `6. Query books in authors `

    ```
    {
      authors {
        id,
        name, 
        books {
          name
        }
      }
    }
    ```
- `7. Query a single book by id `

    ```
    {
      book(id: 1) {
        name
      }
    }
    ```

- `8. Query a single author by id `

    ```
    {
      author(id: 1) {
        name
      }
    }
    ```

- `9. Add a book` 
    
    add a new book

    ```
    mutation {
      addBook(name: "New Name", authorId: 1) {
        id
        name
      }
    }
    ```
    
    check the new book is added    

    ```
    {
        books {
            id
            name
        }
    }
  ```  

- `10. Add an author`

  add a new author

    ```
    mutation {
      addAuthor(name: "New Author") {
        name
      }
    }
    ```

  check the new book is added

    ```
    {
        authors {
            id
            name
        }
    }
  ```  
  