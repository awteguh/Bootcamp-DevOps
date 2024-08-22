# Tutorial Instal Multipass Linux 24.04 LTS

Hal pertama yang harus di lakuan adalah masuk ke terminal

## Install

using sudo:

```bash
sudo apt update
```
```bash
sudo apt upgrade
```

using multipass:

```bash
sudo snap install multipass
```

## Usage

cek version multipass:

```bash
multipass version
```

### Usage with `app/layout.js` for `app` folder structure

For rendering add `<NextTopLoader />` to your `return()` inside the `<body></body>` of `RootLayout()`:

```js
import NextTopLoader from 'nextjs-toploader';

export default function RootLayout({ children }) {
  return (
    <html lang="en">
      <body>
        <NextTopLoader />
        {children}
      </body>
    </html>
  );
}
```

### Usage with `pages/_app.js` for `pages` folder structure

For rendering add `<NextTopLoader />` to your `return()` in `MyApp()`:

```js
import NextTopLoader from 'nextjs-toploader';

export default function MyApp({ Component, pageProps }) {
  return (
    <>
      <NextTopLoader />
      <Component {...pageProps} />;
    </>
  );
}
```

### Usage with React, Vite React or any other React Based Framework

