# REF
The React Engine Framework for Express

> ***NOTE:*** This framework is not ready for production and for now, is just a Proof of Concept. Soon it will be ready for production

## About
REF is a template engine for Express, making Express able to provide server-side rendered React.

Features:
- Server-side rendering

## Installing
> npm i the-ref-framework

## Example
> Model-View-Controller using Express and REF (Github repo [here](https://github.com/Zlynt/the-ref-framework-examples))

## How to connect REF to Express server
```
import express from "express";
import RenderEngine from "the-ref-framework";
import path from "path";

const app = express();
const PORT = 3000;

const viewsFolderPath: string = __dirname + "/views";

new RenderEngine({
  viewsPath: viewsFolderPath,
  errorMessage: "An error happened while loading this page.",
  jsxOrTsx: "TypeScript XML",
  expressApp: app,
});

app.get("/", function (req, res) {
  res.render("root");
});

app.listen(PORT, () => console.log(`Server listening on port: ${PORT}`));
```

