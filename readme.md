https://www.youtube.com/shorts/Fk-xqmUtYQk - add smooth container appear

set env within package.json
"start": "set PROXY=localhost:3001 && react-scripts start",

use proxy
const {createProxyMiddleware} = require('http-proxy-middleware');
module.exports = function (app) {
    app.use(
        '/endpointName',
        createProxyMiddleware({
            target: process.env.PROXY ?? 'http://localhost:5000',
            secure: false,
            changeOrigin: true,
        })
    );
    app.use(
        '/endpointName',
        createProxyMiddleware({
            target: process.env.PROXY ?? 'http://localhost:5000',
            secure: false,
            changeOrigin: true,
        })
    );
};
