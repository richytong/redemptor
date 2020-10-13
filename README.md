# redemptor
> contractor, undertaker, purveyor ([wiktionary](https://en.wiktionary.org/wiki/redemptor))

Generate native HTML, CSS, and JavaScript web applications with React.

Features:
 * History-based routing
 * Hot-reloading dev server
 * Simple, powerful, and extensible application architecture
 * Fill-in-the-blank Search Engine Optimization (SEO)
 * Painless deployment to Amazon S3
 * Component library

Requires:
 * AWS Command Line Interface `aws` authorized to create buckets and objects

Create a new project and bucket in S3.
```sh
redemptor create ./path/to/your.hostname.com
# bucket name will be your.hostname.com
```

Set up a local development server.
```sh
redemptor serve ./path/to/your.hostname.com
```

Deploy to Amazon S3
```sh
redemptor publish ./your.hostname.com
```

# Installation
Install global executable with `npm`.
```sh
npm i -g redemptor
```
