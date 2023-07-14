https://www.youtube.com/shorts/Fk-xqmUtYQk - add smooth container appear

---
set env within package.json \
"start": "set PROXY=localhost:3001 && react-scripts start",

---
use proxy  \
const {createProxyMiddleware} = require('http-proxy-middleware'); \
module.exports = function (app) { \
    app.use( \
        '/endpointName', \
        createProxyMiddleware({ \
            target: process.env.PROXY ?? 'http://localhost:5000', \
            secure: false, \
            changeOrigin: true, \
        }) \
    ); \
    app.use( \
        '/endpointName', \
        createProxyMiddleware({ \
            target: process.env.PROXY ?? 'http://localhost:5000', \
            secure: false, \
            changeOrigin: true, \
        }) \
    ); \
};

---
flex container: 

.form { \
display: flex; \
flex: wrap; \
} \
.name { \
flex: 1 0 140px; \
} \
.email { \
flex: 1 0 140px; \
} \
.submit { \
flex: 1 0 50px; \
}

---
controlled scroll: 

.parent { \
    height: 100vh; \
    overflow: hidden; \
    position: relative; \
}

.child { \
    height: 100%; \
    width: 100%; \
    overflow: auto; \
    scrollbar-width: thin; \
    scrollbar-gutter: stable; \
}

---

