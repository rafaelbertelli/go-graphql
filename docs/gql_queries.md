## Mutations

```graphql
mutation createCategory {
  createCategory(input: { name: "JavaScript", description: "JS is awsome" }) {
    id
    name
    description
  }
}
```

## Queries

```graphql
query findCategories {
  categories {
    id
    name
    description
    courses {
      id
      name
      description
    }
  }
}
```
