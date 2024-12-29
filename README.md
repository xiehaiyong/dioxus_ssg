# Development

Your new jumpstart project includes basic organization with an organized `assets` folder and a `components` folder. 
If you chose to develop with the router feature, you will also have a `views` folder.

### Tailwind
1. Install npm: https://docs.npmjs.com/downloading-and-installing-node-js-and-npm
2. Install the Tailwind CSS CLI: https://tailwindcss.com/docs/installation
3. Run the following command in the root of the project to start the Tailwind CSS compiler:

```bash
npx tailwindcss -i ./input.css -o ./assets/tailwind.css --watch
```

### Serving Your App

Run the following command in the root of your project to start developing with the default platform:

```bash
dx serve --platform web
```

To run for a different platform, use the `--platform platform` flag. E.g.
```bash
dx serve --platform desktop
```

## Usage

- To run it in your localhost browser
```
cd dioxus-ssg/

dx serve --platform web --open
```

- To deploy using static site generation (SSG)
```
cd dioxus-ssg/

rm -rf dist/

rm -rf static/

rm -rf target/dx/

dx build --platform web --release --ssg

mkdir dist/

cp -r target/dx/dioxus-ssg/release/web/public/* dist/

cp -r static/* dist/

cd dist/

http-server -c-1 -o
```
