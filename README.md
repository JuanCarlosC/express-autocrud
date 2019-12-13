# Express AutoCRUD

Automate creating a CRUD backend using a config file to auto generate mongoose models, express routes, controllers, and documentation for your resources.

The perfect prototyping tool.

### Create express app and use the auotCRUD util:

```

const resources = [
  { 
    name: 'Users',
    properties: {
      name: {
        type: String 
      }
    }
  }
]

const app = express()

autoCRUD.create({
    expressApp: app,
    resources: resources,
    route: '/api/v1/'
})

app.listen(8888, (err) => ...

```

### Generates the following routes for you


#### GET
`/api/v1/users`

#### POST
`/api/v1/users`

body:
`{ name: 'John Doe' }`

#### PUT
`/api/v1/users/{id}`

body: `{ name: 'Jane Doe' }`

#### DELETE
`/api/v1/users/{id}`


## TO DO

- [] Add the `index.html` for display the UI for the documentation
- [] Automate creating the UI for the CRUD routes
