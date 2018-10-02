# webpack-hot-koa-middleware

> The hot middleware from webpack 4.x

How to use ?

```
const koaHotMiddleware = require('webpack-hot-koa-middleware')

const config = {...} // your's webpack config

clientConfig.entry.app = [
  'webpack-hot-middleware/client?noInfo=true',
  clientConfig.entry.app
]

const compiler = webpack(config)

const hotMiddleware = koaHotMiddleware(clientCompiler, {
  heartbeat: 5000,
  log: false
})

app.use(hotMiddleware)
```