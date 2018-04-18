# gatsby-source-prismic-field

Source plugin for pulling documents into Gatsby from prismic.io repositories. Forked from gatsby-source-prismic to permit json extraction and some other custom features.

## Install

`npm install --save gatsby-source-prismic-field`

## How to use

```javascript
// In your gatsby-config.js
plugins: [
  {
    resolve: `gatsby-source-prismic`,
    options: {
      repositoryName: `your_repository_name`,
      accessToken: `your_acces_token`
    }
  }
];
```

## How to query

You can query Document nodes created from prismic.io like the following:

```graphql
{
  allPrismicDocument {
    edges {
      node {
        id
        data {
          title {
            type
            text
          }
        }
      }
    }
  }
}
```
