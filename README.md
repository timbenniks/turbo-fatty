# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install the dependencies:

```bash
yarn install
```

## Add GraphQL and Hygraph connections

Install `nuxt-graphql-client`

```bash
yarn add nuxt-graphql-client
```

In `.env` add and make sure to add content viewing permissions in Hygraph API settings

```
GQL_HOST=https://<HYGRAPH_CDN_LOCATION>.cdn.hygraph.com/content/<ID>/master
```

In Nuxt Config add

```js
export default defineNuxtConfig({
  modules: ["nuxt-graphql-client"],
});
```

Add `.gql` query files in the `./queries` folder and use them like this:

```js
const { data } = await useAsyncGql("<QUERY_NAME>", { foo: "bar" });
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
yarn dev
```

## Production

Build the application for production:

```bash
yarn build
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
