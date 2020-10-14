# redemptor
> contractor, undertaker, purveyor ([wiki](https://en.wiktionary.org/wiki/redemptor))

Create dynamic web applications with HTML, CSS, and JavaScript.

### Features
 * Single Page Application with proper (not hash-based) urls
 * Hot-reloading dev server
 * First class [JavaScript (ES) modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)
 * Simple, extensible, and buildless [Arche(React)](https://github.com/richytong/Arche) application architecture
 * Pipeline-based state management with [rubico](https://rubico.land/)
 * Fill-in-the-blank meta tags for search engine optimization (SEO)
 * Painless deployment to Amazon S3
 * Fully featured component library

### System Requirements
 * Node.js `node` v10.3.x
 * AWS Command Line Interface `aws` v2.x, authorized to create buckets and upload files

# Getting Started
Install globally with `npm`.
```sh
npm i -g redemptor
```

Create a new project.
```sh
redemptor create ./path/to/your.hostname.com
# bucket name will be your.hostname.com
```

This generates a project with the following file structure at `./path/to/your.hostname.com/`
```
README.md - # your.hostname.com
index.html - site entrypoint + dependencies, defaults to empty metadata
index.js - JavaScript entrypoint. This renders to a div with id="root"
style.css - site-wide styles with some defaults
routes.js - exports a JavaScript array of all the paths you want to serve. Starts as `['/']`
site.webmanifest - json metadata for progressive web apps, defaults to empty fields
```

Start the hot-reloading development server.
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
# default file writing concurrency limit 10

redemptor publish --concurrency 20 ./path/to/your.hostname.com
# bump the concurrency limit to 20
```
