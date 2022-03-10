# Queries

```graphql
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

query findAll {
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
