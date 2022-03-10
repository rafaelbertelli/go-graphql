# Mutations

```graphql
mutation createCategory {
  createCategory(input: { name: "JavaScript", description: "JS is awsome" }) {
    id
    name
    description
  }
}

mutation createCourse {
  createCourse(input: { 
    name: "JavaScript ninja", 
    description: "Se torne um ninja em JS", 
    categoryId: "T5577006791947779410" 
  }) {
    id
    name
    description
    category {
      id
      name
    }
  }
}

mutation createChapter1 {
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

mutation createChapter2 {
  createChapter(input: { name: "Capítulo 2", courseId: "C8674665223082153551" }) {
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
