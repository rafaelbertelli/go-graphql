## Mutations

```graphql
mutation createCategory {
  createCategory(input: { name: "JavaScript", description: "JS is awsome" }) {
    id
    name
    description
  }
}

mutation createCourse {
  createCourse(input: { name: "JavaScript ninja", description: "Se torne um ninja em JS", categoryId: "" }) {
    id
    name
    description
    category {
      id
      name
    }
  }
}

mutation createChapter {
  createChapter(input: { name: "Capítulo 1", courseId: "C8674665223082153551" }) {
    id
    name
    course {
      id
      name
      description
      category {
        id
        name
        description
      }
    }
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

query findCourses {
  courses {
    id
    name
    description
    category {
      id
      name
    }
    chapters {
      id
      name
    }
  }
}

query findChapter {
  chapters {
    id
    name
    course {
      id
      name
      description
      category {
        id
        name
        description
      }
    }
  }
}
```
