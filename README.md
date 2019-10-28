*Psst — looking for a shareable component template? Go here --> [sveltejs/component-template](https://github.com/sveltejs/component-template)*

---

# svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.


## Scripts

explanations of package.json scripts

### npm run ```build```

runs ```rollup -c```

```-c``` - use config. If no path is specified it defaults to ```config.rollup.js```

### npm run ```dev```

runs ```rollup -c -w```

As above plus ```-w``` - watches files in bundle and rebuild on change

### npm run ```start```

runs ```sirv public --single``` - serves from public dir, ```--single``` flag is to serve SPAs.

### npm run ```start:dev```

runs ```sirv public --single --dev``` - as above plus ```--dev``` which runs it in dev mode(?)