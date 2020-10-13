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
# serve port 8000 by default

redemptor serve -p 3000 ./path/to/your.hostname.com
redemptor serve --port 3000 ./path/to/your.hostname.com
# specify the port as 3000
```

Deploy to Amazon S3
```sh
redemptor publish ./path/to/your.hostname.com
# default file writing concurrency limit 10 (recommended)

redemptor publish --concurrency 20 ./path/to/your.hostname.com
# bump the concurrency limit to 20
```

# Installation
Install global executable with `npm`.
```sh
npm i -g redemptor
```
