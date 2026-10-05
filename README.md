# JSON Server Mock API

Small mock-data repository intended to expose posts and comments through JSON Server.

## How it works

`db.json` contains `posts` and `comments` collections. `server.js` attempts to create a JSON Server router and listen on port `3000`.

## Usage

Requires Node.js and npm. Install dependencies with `npm install`. With the declared JSON Server 1.x CLI, serve the data directly:

```sh
npx json-server db.json --port 3000
```

Resources are available at `http://localhost:3000/posts` and `http://localhost:3000/comments`.

## Notes

The custom `server.js` uses the older `create()`, `router()` and `defaults()` API, while `package.json` declares JSON Server 1.x beta. The custom server therefore needs a compatible dependency version or an API update. No start script or implemented test suite is included.
