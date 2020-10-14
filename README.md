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
```

This generates a project with the following file structure at `./path/to/your.hostname.com/`.
```
index.html
index.js
style.css
routes.js
site.webmanifest
README.md
LICENSE
package.json
```

 * `index.html` - the entrypoint to your website. Contains blank metadata fields.
 * `index.js` - JavaScript entrypoint for your application. Contains a minimal Arche(React) application
 * `style.css` - CSS entrypoint for your application. Contains default, site-wide CSS.
 * `routes.js` - `export default` a single array of paths. Starts as `['/']`
 * `site.webmanifest` - mostly blank configuration for supporting [PWAs](https://web.dev/progressive-web-apps/)
 * `README.md` - readme with just the header # your.hostname.come
 * `LICENSE` - an MIT license with blank name and year
 * `package.json` - a mostly blank project configuration file

Start the hot-reloading development server.
```sh
redemptor serve ./path/to/your.hostname.com
# serve port 8000 by default

redemptor serve -p 3000 ./path/to/your.hostname.com
redemptor serve --port 3000 ./path/to/your.hostname.com
# specify the port as 3000
```

Author your site and deploy to Amazon S3.
```sh
redemptor publish ./path/to/your.hostname.com
# default file writing concurrency limit 10

redemptor publish --concurrency 20 ./path/to/your.hostname.com
# bump the concurrency limit to 20
```
