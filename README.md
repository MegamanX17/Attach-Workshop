# | attach |

Attach is a contact sharing website that anyone can fork and customize for their own. Fork this project and set up your own! Here is my personal [demo](https://attach.fly.dev)

-   [Installation](#installation)
-   [Development](#development)
-   [Deployment](#deployment)
    -   [Fly](#fly)
    -   [Locally](#locally)
-   [Runtime and Tools](#runtime-and-tools)
-   [Technologies](#technologies)
    -   [Frontend](#frontend)
    -   [Backend](#backend)

## Installation

Install [pre-reqs](#runtime-and-tools)

Then:

Run

```
git clone https://github.com/ZackarySantana/Attach.git attach
```

If it doesn't work, run

```
git clone git@github.com:ZackarySantana/Attach.git attach
```

Then make sure to cd (change directory) in to the attach folder

```
cd attach
```

Install the [technologies](#technologies) by running

```
npm install
```

And deploy to the web with

```
fly launch
```

For more info on deploying, head to [deploy with fly](#fly)

## Development

### Customization

Most of the customization will happen in [config.ts](./src/config.ts). This has the list of easily customizable things (all colors and gradients). I've made some themes at [color_schemes.ts](./src/color_schemes.ts). By default, the theme is randomly chosen each time the user accesses the website. You can change this functionality in the config!

If you would like to not randomize color schemes, edit the config.ts to directly export the scheme you want (copy and paste from the color_schemes.ts or create your own in config.ts). As well, change [tailwind.config.js](./tailwind.config.js) to \_not\* include the line with `"./src/color_schemes.ts",` so tailwind doesn't compile useless themes

You can also force a theme (if using the random option) by adding a search parameter (e.g. [https://attach.fly.dev/?scheme=dracula](https://attach.fly.dev/?scheme=dracula))

### `npm dev` or `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>

## Deployment

### Fly

Make sure to install [Fly.io](https://fly.io) (You don't need Docker to deploy this project!). You'll need to setup Fly by following their [docs](https://fly.io/docs/speedrun/), and then run `fly launch`. You should select yes to copy the existing fly.toml (configuration file) to this project, and give it any name you want!

### Locally

#### `npm run build`

Builds the app for production to the `dist` folder.<br>
It correctly bundles Solid in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

#### `npm run deploy`

Runs the app generated in the `dist` folder. This script uses the [host.js](./host.js) file to host all static files in dist on port `4173`.

## Runtime and Tools:

To install:

-   [Node](https://nodejs.org/en/) v18.4.0
-   NPM v8.12.1
-   [Flyctl](https://fly.io/) (Deployment)
-   [Docker](https://www.docker.com/) (The project just uses this tool but you don't need it installed locally)

## Technologies:

No need to try installing these, these are installed automatically when running `npm install`

### Frontend:

-   [Solid.js](https://solidjs.com) - Main Framework
-   [TypeScript](https://www.typescriptlang.org/docs/) - Main language
-   [Tailwind](https://tailwindcss.com/) - Used in all components

### Backend:

-   [Express](https://expressjs.com/) - Main server that handles all requests to the website

```

```

```

```
