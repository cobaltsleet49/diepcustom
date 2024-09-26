<br><br>
<div align="center">
<img src="./icon.png" width="20%" />
<h3> diep custom </h3>
<p> An open source diep.io custom private-server template </p>
</div>
<br>

## Installation

You may need to install [Node.js](https://nodejs.org/), as well as the [Yarn Package Manager](https://classic.yarnpkg.com/en/docs/install).\
After doing so, download or clone this repository and install the dependencies with:
```bash
$ yarn install
```

## Running the Server

Run the server with:
```bash
$ yarn run server
```
This builds and runs the server.

After running the server, content will be served at `localhost:PORT` on your computer. The port will default to 8080, and you may override it with `process.env.PORT`.

To change the port number for a temporary session, you can prepend `PORT=PortNumber` to your start command. Replace `PortNumber` with the port number you want. For example, to set the port number to 3000:
```bash
PORT=3000 yarn run server
```

Alternatively, you could configure the port number permanently with a new .env file:
1. **Create a `.env` file** in your project's root directory.
   
2. **Open the `.env` file** and add the following line to specify the port:
```bash
PORT=PortNumber
```
Replace `PortNumber` with the port number you wish to use.

3. **Save the file.** Your application needs to read this `.env` file and use its values. Ensure your server’s startup script or configuration is set up to parse `.env` files. Usually, this is done with libraries like `dotenv` in Node.js applications.

4. **Install** `dotenv`. If it's not already installed, you can add it using [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm):
```bash
npm install dotenv
```

5. **Open the `index.js` File** and add the following line to the beginning of the file so that your project parses the environment variables before starting:
```bash
require('dotenv').config();
```
Once saved, this will parse and load the environment variables from the .env file and make them accessible via `process.env.PORT`.

Consult [`src/config.ts`](./src/config.ts) for configuration, and [`package.json`](./package.json) for more environment variable setup.

To close the server for local ports, you may press `Ctrl` + `C` in the command line.

## Discord Chat

For support or discussion, please join our [online Discord chat](https://discord.gg/SyxWdxgHnT).

## Contribution

Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for information on contributing.

## License

Please see [LICENSE](./LICENSE)
