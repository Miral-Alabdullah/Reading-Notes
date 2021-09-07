# GraphQL @connection

## Add relationships between types

- The `@connection` directive enables you to specify relationships between `@model` types.

```
directive @connection(keyName: String, fields: [String!]) on FIELD_DEFINITION
```

## Usage

- Relationships between types are specified by annotating fields on an `@model` object type with the `@connection` directive.

## Has one

```
type Project @model {
  id: ID!
  name: String
  team: Team @connection
}

type Team @model {
  id: ID!
  name: String!
}

**********************

type Project @model {
  id: ID!
  name: String
  teamID: ID!
  team: Team @connection(fields: ["teamID"])
}

type Team @model {
  id: ID!
  name: String!
}
```

## Has many

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
}

type Comment @model
  @key(name: "byPost", fields: ["postID", "content"]) {
  id: ID!
  postID: ID!
  content: String!
}

*******************

mutation CreatePost {
  createPost(input: { id: "a-post-id", title: "Post Title" } ) {
    id
    title
  }
}

mutation CreateCommentOnPost {
  createComment(input: { id: "a-comment-id", content: "A comment", postID: "a-post-id"}) {
    id
    content
  }
}
```