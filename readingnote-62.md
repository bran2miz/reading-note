# Reading 40 - React 4

## Dynamic Routes

Steps to create Pages with Dynamic Routes

Create a page under `pages/posts`.

then add:

```js script
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}
```

export async function called `getStaticPaths`:

```js script
export async function getStaticPaths() {
  // Return a list of possible value for id
}
```

implement `getStaticProps`; it is given `params` which contains `id`.

```js script
export async function getStaticProps({ params }) {
  const postData = getPostData(params.id)
  return {
    props: {
      postData
    }
  }
```

## Dynamic Routes Details

`getStaticPaths` can fetch data from any source.

### Development vs. Production

**development** - `getStaticpaths` runs on every request.

**production** - `getStaticPaths` runs at build time.

## Fallback

`fallback` is `false`= paths not returned by `getStaticPaths` will result in a 404 page.

`fallback` is `true` = `getStaticProps` changes:

-paths returned from `getStaticPaths` will be rendered to HTML at build time.

-paths that aren't build at the right time will not result in a 404 page. Next.js will be the fallback of the page on the first request.

-In background, Next.js will generate the requested path.

`fallback` is `blocking`= new paths will be server-side rendered with `getStaticProps`.

## Deployment via Vercel

1. Push to GitHub
2. Deployment within Vercel:
    -first create a Vercel Account
    -give permission for Vercel to access your GitHub
    -deployment urls will be given up building completion.
3. Next.js can be deployed to any hosting provide that supports Node.js.

[<==BACK](README.md)
