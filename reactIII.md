# Assets, Metadata, and CSS

first sterp we shoul install `npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/assets-metadata-css-starter"`


# **Assets**


* Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

* The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.


**Download Your Profile Picture**

`<img src="/images/profile.jpg" alt="Your Name" />`


**Image Component and Image Optimization**


* next/image is an extension of the HTML `<img>` element, evolved for the modern web.

Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.


**Using the Image Component**

* Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.

```
import Image from 'next/image'

const YourComponent = () => (
  <Image
    src="/images/profile.jpg" // Route of the image file
    height={144} // Desired size with correct aspect ratio
    width={144} // Desired size with correct aspect ratio
    alt="Your Name"
  />
)
```

***************

# **Metadata**

```
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```



**Adding Head to first-post.js**

We haven't added a `<title> to our /posts/first-post` route. Let's add one.

Open the pages/posts/first-post.js file and add an import for Head from next/head at the beginning of the file:

`import Head from 'next/head'`

```

Assets, Metadata, and CSS
Metadata
What if we wanted to modify the metadata of the page, such as the <title> HTML tag?

<title> is part of the <head> HTML tag, so let's dive into how we can modify the <head> tag in a Next.js page.

Open pages/index.js in your editor and find the following lines:

<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
Notice that <Head> is used instead of the lowercase <head>. <Head> is a React Component that is built into Next.js. It allows you to modify the <head> of a page.

You can import the Head component from the next/head module.

Adding Head to first-post.js
We haven't added a <title> to our /posts/first-post route. Let's add one.

Open the pages/posts/first-post.js file and add an import for Head from next/head at the beginning of the file:

import Head from 'next/head'
Then, update the exported FirstPost component to include the Head component. For now, we‘ll add just the title tag:

export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}
```


***

 # **CSS Styling**

```
<style jsx>{`
  …
`}</style>
```

*  styled-jsx. => It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).


**Writing and Importing CSS**

* Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.

* Using popular CSS libraries like Tailwind CSS is also supported.

* In this lesson, we’ll talk about how to write and import CSS files in Next.js. We’ll also talk about Next.js’s built-in support for CSS Modules and Sass. Let’s dive in!





**Layout Component**

* First, Let’s create a Layout component which will be shared across all pages.

Create a top-level directory called components.
Inside components, create a file called layout.js with the following content:


```
export default function Layout({ children }) {
  return <div>{children}</div>
}
```



```
import styles from './layout.module.css'

export default function Layout({ children }) {
  return <div className={styles.container}>{children}</div>
}
```


**Adding CSS**

* Now, let’s add some styles to the Layout component. To do so, we’ll use CSS Modules, which lets you import CSS files in a React component.

Create a file called components/layout.module.css with the following content:

```
.container {
  max-width: 36rem;
  padding: 0 1rem;
  margin: 3rem auto 6rem;
}
```

**Global Styles**

* CSS Modules are useful for component-level styles. But if you want some CSS to be loaded by every page, Next.js has support for that as well.

- To load global CSS files, create a file called pages/_app.js with the following content:

```
export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```


**Adding Global CSS**
In Next.js, you can add global CSS files by importing them from pages/_app.js. You cannot import global CSS anywhere else.

The reason that global CSS can't be imported outside of pages/_app.js is that global CSS affects all elements on the page.

If you were to navigate from the homepage to the /posts/first-post page, global styles from the homepage would affect /posts/first-post unintentionally.

You can place the global CSS file anywhere and use any name. So let’s do the following:

Create a top-level styles directory and create global.css inside.
Add the following content to styles/global.css. It resets some styles and changes the color of the a tag:

```
html,
body {
  padding: 0;
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu,
    Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif;
  line-height: 1.6;
  font-size: 18px;
}

* {
  box-sizing: border-box;
}

a {
  color: #0070f3;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

img {
  max-width: 100%;
  display: block;
}
```


***Polishing Layout**

* So far, we’ve only added minimal React and CSS code just to illustrate concepts such as CSS Modules. Before we move on to our next lesson about data fetching, let’s polish our page styling and code.

Update components/layout.module.css


```
.container {
  max-width: 36rem;
  padding: 0 1rem;
  margin: 3rem auto 6rem;
}

.header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.backToHome {
  margin: 3rem 0 0;
}
```