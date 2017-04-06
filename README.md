# api documentation for  [drakov (v1.0.3)](https://github.com/aconex/drakov)  [![npm package](https://img.shields.io/npm/v/npmdoc-drakov.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-drakov) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-drakov.svg)](https://travis-ci.org/npmdoc/node-npmdoc-drakov)
#### Mock server that implements the API Blueprint specification

[![NPM](https://nodei.co/npm/drakov.png?downloads=true)](https://www.npmjs.com/package/drakov)

[![apidoc](https://npmdoc.github.io/node-npmdoc-drakov/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-drakov_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-drakov/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-drakov/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-drakov/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Yakov Khalinsky",
        "email": "ykhalinsky@aconex.com"
    },
    "bin": {
        "drakov": "drakov"
    },
    "bugs": {
        "url": "https://github.com/aconex/drakov/issues"
    },
    "dependencies": {
        "async": "^2.1.4",
        "chokidar": "^1.6.1",
        "colors": "^1.1.0",
        "drafter": "^1.2.0",
        "express": "^4.14.1",
        "glob": "^7.1.1",
        "jade": "^1.11.0",
        "lodash": "^4.17.4",
        "path-to-regexp": "^1.7.0",
        "qs": "^6.3.0",
        "tv4": "^1.1.9",
        "yargs": "^6.6.0"
    },
    "description": "Mock server that implements the API Blueprint specification",
    "devDependencies": {
        "grunt": "^0.4.5",
        "grunt-blueprint-validator": "^3.1.0",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-jshint": "^1.1.0",
        "grunt-simple-mocha": "^0.4.0",
        "supertest": "^3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "57b0fa4d4ebd27f2c9c28bce30343ad447bce1f2",
        "tarball": "https://registry.npmjs.org/drakov/-/drakov-1.0.3.tgz"
    },
    "engines": {
        "node": ">= 0.12"
    },
    "gitHead": "d8fdeda555bd1020c7257cc1353c3bd7f5d80799",
    "homepage": "https://github.com/aconex/drakov",
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "russianator",
            "email": "yakov@ninebyt.es"
        },
        {
            "name": "mobz",
            "email": "ben@mobz.org"
        },
        {
            "name": "marcelogo",
            "email": "marcelo.mgo@gmail.com"
        }
    ],
    "name": "drakov",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Aconex/drakov.git"
    },
    "scripts": {
        "test": "grunt"
    },
    "version": "1.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module drakov](#apidoc.module.drakov)
1.  [function <span class="apidocSignatureSpan">drakov.</span>run (argv, cb)](#apidoc.element.drakov.run)
1.  [function <span class="apidocSignatureSpan">drakov.</span>stop (cb)](#apidoc.element.drakov.stop)
1.  object <span class="apidocSignatureSpan"></span>drakov
1.  object <span class="apidocSignatureSpan">drakov.</span>content
1.  object <span class="apidocSignatureSpan">drakov.</span>content_type
1.  object <span class="apidocSignatureSpan">drakov.</span>debugRequest
1.  object <span class="apidocSignatureSpan">drakov.</span>handler_filter
1.  object <span class="apidocSignatureSpan">drakov.</span>logger
1.  object <span class="apidocSignatureSpan">drakov.</span>middleware
1.  object <span class="apidocSignatureSpan">drakov.</span>query_comparator
1.  object <span class="apidocSignatureSpan">drakov.</span>route
1.  object <span class="apidocSignatureSpan">drakov.</span>setup
1.  object <span class="apidocSignatureSpan">drakov.</span>spec_schema

#### [module drakov.content](#apidoc.module.drakov.content)
1.  [function <span class="apidocSignatureSpan">drakov.content.</span>areContentTypesSame (httpReq, specReq)](#apidoc.element.drakov.content.areContentTypesSame)
1.  [function <span class="apidocSignatureSpan">drakov.content.</span>contentTypeComparator (specA)](#apidoc.element.drakov.content.contentTypeComparator)
1.  [function <span class="apidocSignatureSpan">drakov.content.</span>matchesBody (httpReq, specReq)](#apidoc.element.drakov.content.matchesBody)
1.  [function <span class="apidocSignatureSpan">drakov.content.</span>matchesHeader (httpReq, specReq)](#apidoc.element.drakov.content.matchesHeader)
1.  [function <span class="apidocSignatureSpan">drakov.content.</span>matchesSchema (httpReq, specReq)](#apidoc.element.drakov.content.matchesSchema)

#### [module drakov.content_type](#apidoc.module.drakov.content_type)
1.  [function <span class="apidocSignatureSpan">drakov.content_type.</span>isFormUrlEncoded (contentType)](#apidoc.element.drakov.content_type.isFormUrlEncoded)
1.  [function <span class="apidocSignatureSpan">drakov.content_type.</span>isJson (contentType)](#apidoc.element.drakov.content_type.isJson)
1.  [function <span class="apidocSignatureSpan">drakov.content_type.</span>isMultipart (contentType)](#apidoc.element.drakov.content_type.isMultipart)

#### [module drakov.debugRequest](#apidoc.module.drakov.debugRequest)
1.  [function <span class="apidocSignatureSpan">drakov.debugRequest.</span>notFoundHandler (argv)](#apidoc.element.drakov.debugRequest.notFoundHandler)

#### [module drakov.drakov](#apidoc.module.drakov.drakov)
1.  [function <span class="apidocSignatureSpan">drakov.drakov.</span>run (argv, cb)](#apidoc.element.drakov.drakov.run)
1.  [function <span class="apidocSignatureSpan">drakov.drakov.</span>stop (cb)](#apidoc.element.drakov.drakov.stop)

#### [module drakov.handler_filter](#apidoc.module.drakov.handler_filter)
1.  [function <span class="apidocSignatureSpan">drakov.handler_filter.</span>filterHandlers (req, handlers)](#apidoc.element.drakov.handler_filter.filterHandlers)

#### [module drakov.logger](#apidoc.module.drakov.logger)
1.  [function <span class="apidocSignatureSpan">drakov.logger.</span>log ()](#apidoc.element.drakov.logger.log)
1.  [function <span class="apidocSignatureSpan">drakov.logger.</span>setStealthMode (isStealthMode)](#apidoc.element.drakov.logger.setStealthMode)
1.  [function <span class="apidocSignatureSpan">drakov.logger.</span>stringfy (matched)](#apidoc.element.drakov.logger.stringfy)

#### [module drakov.middleware](#apidoc.module.drakov.middleware)
1.  [function <span class="apidocSignatureSpan">drakov.middleware.</span>init (app, argv, cb)](#apidoc.element.drakov.middleware.init)

#### [module drakov.query_comparator](#apidoc.module.drakov.query_comparator)
1.  [function <span class="apidocSignatureSpan">drakov.query_comparator.</span>countMatchingQueryParms (handlers, reqQueryParams)](#apidoc.element.drakov.query_comparator.countMatchingQueryParms)
1.  [function <span class="apidocSignatureSpan">drakov.query_comparator.</span>noParamComparator (a, b)](#apidoc.element.drakov.query_comparator.noParamComparator)
1.  [function <span class="apidocSignatureSpan">drakov.query_comparator.</span>queryParameterComparator (a, b)](#apidoc.element.drakov.query_comparator.queryParameterComparator)

#### [module drakov.route](#apidoc.module.drakov.route)
1.  [function <span class="apidocSignatureSpan">drakov.route.</span>getRouteHandlers (method, parsedUrl, action)](#apidoc.element.drakov.route.getRouteHandlers)

#### [module drakov.setup](#apidoc.module.drakov.setup)
1.  boolean <span class="apidocSignatureSpan">drakov.setup.</span>isSSL
1.  [function <span class="apidocSignatureSpan">drakov.setup.</span>startServer (argv, app, cb)](#apidoc.element.drakov.setup.startServer)

#### [module drakov.spec_schema](#apidoc.module.drakov.spec_schema)
1.  [function <span class="apidocSignatureSpan">drakov.spec_schema.</span>hasSchema (spec)](#apidoc.element.drakov.spec_schema.hasSchema)
1.  [function <span class="apidocSignatureSpan">drakov.spec_schema.</span>matchWithSchema (json, schema)](#apidoc.element.drakov.spec_schema.matchWithSchema)
1.  [function <span class="apidocSignatureSpan">drakov.spec_schema.</span>validateAndParseSchema (spec)](#apidoc.element.drakov.spec_schema.validateAndParseSchema)



# <a name="apidoc.module.drakov"></a>[module drakov](#apidoc.module.drakov)

#### <a name="apidoc.element.drakov.run"></a>[function <span class="apidocSignatureSpan">drakov.</span>run (argv, cb)](#apidoc.element.drakov.run)
- description and source-code
```javascript
run = function (argv, cb) {

    logger.setStealthMode(argv.stealthmode);

    console.log('   DRAKOV STARTED   '.green.bold.inverse);

    var app = express();

    // REQUEST MIDDLEWARE
    app.use(requestUtils.logger);
    app.use(requestUtils.getBody);

    // SETUP RESPONSE MIDDLEWARE
    argv.drakovHeader = true;
    middleware.init(app, argv, function(err, middlewareFunction) {
        if (err) {
            throw err;
        }

        var discoverabilityModule;

        app.use(middlewareFunction);
        server = setup.startServer(argv, app, cb);
        if (argv.discover && typeof argv.discover === 'string') {
            discoverabilityModule = require(argv.discover);
        } else {
            app.set('views', path.join(__dirname, '..', 'views'));
            app.set('view engine', 'jade');
            discoverabilityModule = require('./middleware/discover');
        }
        if (argv.discover) {
            app.get('/drakov', discoverabilityModule(argv));
        }

        //404
        app.use(debugRequest.notFoundHandler(argv));
    });
}
```
- example usage
```shell
...
    disableCORS: true,
    sslKeyFile: '/path/to/ssl/key.key',
    sslCrtFile: '/path/to/ssl/cert.crt',
    delay: 2000,
    method: ['DELETE','OPTIONS']
};

drakov.run(argv, function(){
    // started Drakov
    drakov.stop(function() {
        // stopped Drakov
    });
});
...
```

#### <a name="apidoc.element.drakov.stop"></a>[function <span class="apidocSignatureSpan">drakov.</span>stop (cb)](#apidoc.element.drakov.stop)
- description and source-code
```javascript
stop = function (cb) {
    var runCb = function() {
        if (cb) {
            cb();
        }
    };
    try {
        server.close(function() {
            console.log('   DRAKOV STOPPED   '.red.bold.inverse);
            runCb();
        });
    } catch (e) {
        runCb();
    }
}
```
- example usage
```shell
...
        sslCrtFile: '/path/to/ssl/cert.crt',
        delay: 2000,
        method: ['DELETE','OPTIONS']
    };

    drakov.run(argv, function(){
        // started Drakov
        drakov.stop(function() {
            // stopped Drakov
        });
    });


## Using as an Express middleware
...
```



# <a name="apidoc.module.drakov.content"></a>[module drakov.content](#apidoc.module.drakov.content)

#### <a name="apidoc.element.drakov.content.areContentTypesSame"></a>[function <span class="apidocSignatureSpan">drakov.content.</span>areContentTypesSame (httpReq, specReq)](#apidoc.element.drakov.content.areContentTypesSame)
- description and source-code
```javascript
areContentTypesSame = function (httpReq, specReq) {
    var actual = getMediaTypeFromHttpReq(httpReq);
    var expected = getMediaTypeFromSpecReq(specReq);

    var result = !expected || actual === expected;
    logger.log('[MATCHING]'.yellow,'by request content type:', expected, 'actual:', actual, logger.stringfy(result));
    return result;
}
```
- example usage
```shell
...


var content = require('./content');
var queryComparator = require('./query-comparator');

var filterContentType = function (req) {
return function (handler) {
    return content.areContentTypesSame(req, handler.request);
};
};

var filterRequestHeader = function (req) {
return function (handler) {
    return content.matchesHeader(req, handler.request);
};
...
```

#### <a name="apidoc.element.drakov.content.contentTypeComparator"></a>[function <span class="apidocSignatureSpan">drakov.content.</span>contentTypeComparator (specA)](#apidoc.element.drakov.content.contentTypeComparator)
- description and source-code
```javascript
contentTypeComparator = function (specA) {

    function hasContentTypeHeader(spec){
        if (spec.request && spec.request.headers){
            return spec.request.headers.filter(function(header){ return header.name.toLowerCase() === 'content-type';}).length >
0;
        }
        return false;
    }

    return !hasContentTypeHeader(specA)? 1 : -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.drakov.content.matchesBody"></a>[function <span class="apidocSignatureSpan">drakov.content.</span>matchesBody (httpReq, specReq)](#apidoc.element.drakov.content.matchesBody)
- description and source-code
```javascript
matchesBody = function (httpReq, specReq) {
    if (!specReq) {
        return true;
    }

    var contentType = getMediaTypeFromHttpReq(httpReq);

    if (contentTypeChecker.isMultipart(contentType)) {
        return true;
    }

    var reqBody = getBodyContent(httpReq, isJson(contentType));
    var specBody = getBodyContent(specReq, isJson(contentType));
    var result = lodash.isEqual(reqBody, specBody);

    logger.log('[MATCHING]'.yellow,'by request body content', logger.stringfy(result));
    return result;
}
```
- example usage
```shell
...
return function (handler) {
    return content.matchesHeader(req, handler.request);
};
};

var filterRequestBody = function (req) {
return function (handler) {
    return content.matchesBody(req, handler.request);
};
};

var filterSchema = function (req) {
return function (handler) {
    return content.matchesSchema(req, handler.request);
};
...
```

#### <a name="apidoc.element.drakov.content.matchesHeader"></a>[function <span class="apidocSignatureSpan">drakov.content.</span>matchesHeader (httpReq, specReq)](#apidoc.element.drakov.content.matchesHeader)
- description and source-code
```javascript
matchesHeader = function (httpReq, specReq) {
    if (!specReq || !specReq.headers){
        return true;
    }

    function removeContentTypeHeader(header){
        return header.name.toLowerCase() !== 'content-type';
    }

    function containsHeader( header ){
        var httpReqHeader = header.name.toLowerCase();
        var result = httpReq.headers.hasOwnProperty(httpReqHeader) &&
          httpReq.headers[httpReqHeader] === header.value;

        logger.log('[MATCHING]'.yellow,'by request header', httpReqHeader, '=', header.value, logger.stringfy(result));
        return result;
    }

    return specReq.headers.filter(removeContentTypeHeader).every(containsHeader);
}
```
- example usage
```shell
...
return function (handler) {
    return content.areContentTypesSame(req, handler.request);
};
};

var filterRequestHeader = function (req) {
return function (handler) {
    return content.matchesHeader(req, handler.request);
};
};

var filterRequestBody = function (req) {
return function (handler) {
    return content.matchesBody(req, handler.request);
};
...
```

#### <a name="apidoc.element.drakov.content.matchesSchema"></a>[function <span class="apidocSignatureSpan">drakov.content.</span>matchesSchema (httpReq, specReq)](#apidoc.element.drakov.content.matchesSchema)
- description and source-code
```javascript
matchesSchema = function (httpReq, specReq) {
    if (!specReq){
        return true;
    }

    var contentType = getMediaTypeFromHttpReq(httpReq);
    var reqBody = getBodyContent(httpReq, isJson(contentType));
    var result =  specSchema.matchWithSchema(reqBody, specReq.schema);
    logger.log('[MATCHING]'.yellow,'by request body schema', logger.stringfy(result));
    return result;
}
```
- example usage
```shell
...
return function (handler) {
    return content.matchesBody(req, handler.request);
};
};

var filterSchema = function (req) {
return function (handler) {
    return content.matchesSchema(req, handler.request);
};
};

exports.filterHandlers = function (req, handlers) {
if (handlers) {
    var filteredHandlers;
...
```



# <a name="apidoc.module.drakov.content_type"></a>[module drakov.content_type](#apidoc.module.drakov.content_type)

#### <a name="apidoc.element.drakov.content_type.isFormUrlEncoded"></a>[function <span class="apidocSignatureSpan">drakov.content_type.</span>isFormUrlEncoded (contentType)](#apidoc.element.drakov.content_type.isFormUrlEncoded)
- description and source-code
```javascript
isFormUrlEncoded = function (contentType) {
    return match(/application\/x-www-form-urlencoded/i, contentType);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.drakov.content_type.isJson"></a>[function <span class="apidocSignatureSpan">drakov.content_type.</span>isJson (contentType)](#apidoc.element.drakov.content_type.isJson)
- description and source-code
```javascript
isJson = function (contentType) {
    return match(/json/i, contentType);
}
```
- example usage
```shell
...
var contentTypeChecker = require('./content-type');

exports.notFoundHandler = function(argv) {

    function debug(req){

function getBody(req) {
    if (contentTypeChecker.isJson(req.get('Content-Type'))){
        try {
            return JSON.parse(req.body);
        } catch (e) {
            return req.body;
        }
    }
    return req.body;
...
```

#### <a name="apidoc.element.drakov.content_type.isMultipart"></a>[function <span class="apidocSignatureSpan">drakov.content_type.</span>isMultipart (contentType)](#apidoc.element.drakov.content_type.isMultipart)
- description and source-code
```javascript
isMultipart = function (contentType) {
    return match(/multipart\/form-data/i, contentType);
}
```
- example usage
```shell
...
exports.matchesBody = function(httpReq, specReq) {
if (!specReq) {
    return true;
}

var contentType = getMediaTypeFromHttpReq(httpReq);

if (contentTypeChecker.isMultipart(contentType)) {
    return true;
}

var reqBody = getBodyContent(httpReq, isJson(contentType));
var specBody = getBodyContent(specReq, isJson(contentType));
var result = lodash.isEqual(reqBody, specBody);
...
```



# <a name="apidoc.module.drakov.debugRequest"></a>[module drakov.debugRequest](#apidoc.module.drakov.debugRequest)

#### <a name="apidoc.element.drakov.debugRequest.notFoundHandler"></a>[function <span class="apidocSignatureSpan">drakov.debugRequest.</span>notFoundHandler (argv)](#apidoc.element.drakov.debugRequest.notFoundHandler)
- description and source-code
```javascript
notFoundHandler = function (argv) {

    function debug(req){

        function getBody(req) {
            if (contentTypeChecker.isJson(req.get('Content-Type'))){
                try {
                    return JSON.parse(req.body);
                } catch (e) {
                    return req.body;
                }
            }
            return req.body;
        }

        var debugObj = {
            originalUrl: req.originalUrl,
            body: getBody(req),
            method: req.method,
            headers: req.headers,
            query: req.query
        };

        return debugObj;

    }

    return function (req, res) {
        if (!res.headersSent){
            if (argv.debugMode) {
                var debugRequest = debug(req);
                logger.log('[DEBUG]'.yellow, 'mismatching request:', JSON.stringify(debugRequest));
                res.status(404).json(debugRequest);
                return;
            }
            res.status(404).send('Endpoint not found');
        }
    };

}
```
- example usage
```shell
...
        discoverabilityModule = require('./middleware/discover');
    }
    if (argv.discover) {
        app.get('/drakov', discoverabilityModule(argv));
    }

    //404
    app.use(debugRequest.notFoundHandler(argv));
});
};

exports.stop = function(cb) {
var runCb = function() {
    if (cb) {
        cb();
...
```



# <a name="apidoc.module.drakov.drakov"></a>[module drakov.drakov](#apidoc.module.drakov.drakov)

#### <a name="apidoc.element.drakov.drakov.run"></a>[function <span class="apidocSignatureSpan">drakov.drakov.</span>run (argv, cb)](#apidoc.element.drakov.drakov.run)
- description and source-code
```javascript
run = function (argv, cb) {

    logger.setStealthMode(argv.stealthmode);

    console.log('   DRAKOV STARTED   '.green.bold.inverse);

    var app = express();

    // REQUEST MIDDLEWARE
    app.use(requestUtils.logger);
    app.use(requestUtils.getBody);

    // SETUP RESPONSE MIDDLEWARE
    argv.drakovHeader = true;
    middleware.init(app, argv, function(err, middlewareFunction) {
        if (err) {
            throw err;
        }

        var discoverabilityModule;

        app.use(middlewareFunction);
        server = setup.startServer(argv, app, cb);
        if (argv.discover && typeof argv.discover === 'string') {
            discoverabilityModule = require(argv.discover);
        } else {
            app.set('views', path.join(__dirname, '..', 'views'));
            app.set('view engine', 'jade');
            discoverabilityModule = require('./middleware/discover');
        }
        if (argv.discover) {
            app.get('/drakov', discoverabilityModule(argv));
        }

        //404
        app.use(debugRequest.notFoundHandler(argv));
    });
}
```
- example usage
```shell
...
    disableCORS: true,
    sslKeyFile: '/path/to/ssl/key.key',
    sslCrtFile: '/path/to/ssl/cert.crt',
    delay: 2000,
    method: ['DELETE','OPTIONS']
};

drakov.run(argv, function(){
    // started Drakov
    drakov.stop(function() {
        // stopped Drakov
    });
});
...
```

#### <a name="apidoc.element.drakov.drakov.stop"></a>[function <span class="apidocSignatureSpan">drakov.drakov.</span>stop (cb)](#apidoc.element.drakov.drakov.stop)
- description and source-code
```javascript
stop = function (cb) {
    var runCb = function() {
        if (cb) {
            cb();
        }
    };
    try {
        server.close(function() {
            console.log('   DRAKOV STOPPED   '.red.bold.inverse);
            runCb();
        });
    } catch (e) {
        runCb();
    }
}
```
- example usage
```shell
...
        sslCrtFile: '/path/to/ssl/cert.crt',
        delay: 2000,
        method: ['DELETE','OPTIONS']
    };

    drakov.run(argv, function(){
        // started Drakov
        drakov.stop(function() {
            // stopped Drakov
        });
    });


## Using as an Express middleware
...
```



# <a name="apidoc.module.drakov.handler_filter"></a>[module drakov.handler_filter](#apidoc.module.drakov.handler_filter)

#### <a name="apidoc.element.drakov.handler_filter.filterHandlers"></a>[function <span class="apidocSignatureSpan">drakov.handler_filter.</span>filterHandlers (req, handlers)](#apidoc.element.drakov.handler_filter.filterHandlers)
- description and source-code
```javascript
filterHandlers = function (req, handlers) {
    if (handlers) {
        var filteredHandlers;

        handlers.sort(content.contentTypeComparator);

        var queryParams = req.query;
        if (Object.keys(queryParams).length === 0) {
            handlers.sort(queryComparator.noParamComparator);
        } else {
            queryComparator.countMatchingQueryParms(handlers, queryParams);
            handlers.sort(queryComparator.queryParameterComparator);
        }

        filteredHandlers = handlers
            .filter(filterRequestHeader(req))
            .filter(filterContentType(req));

        var matchRequestBodyHandlers = filteredHandlers.filter(filterRequestBody(req));

        if (matchRequestBodyHandlers.length > 0) {
            return matchRequestBodyHandlers[0];
        }

        var matchSchemaHandlers = filteredHandlers.filter(filterSchema(req));

        if (matchSchemaHandlers.length > 0) {
            return matchSchemaHandlers[0];
        }
    }

    return null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.drakov.logger"></a>[module drakov.logger](#apidoc.module.drakov.logger)

#### <a name="apidoc.element.drakov.logger.log"></a>[function <span class="apidocSignatureSpan">drakov.logger.</span>log ()](#apidoc.element.drakov.logger.log)
- description and source-code
```javascript
log = function () {
    if (stealthMode) {
        return;
    }
    console.log(Array.prototype.slice.call(arguments).join(' '));
}
```
- example usage
```shell
...
### Code conventions
* Setup your editor to use the '.editorconfig' and '.jshintrc' files included in the project
* We use 4 spaces for tabs
* Most of the style issues should be resolve as long as you run 'npm test' and run against the jshinting rules
* We prefer readability over compact code

### Logging in your code
* Include the 'lib/logger' module and use 'logger.log()', this allows your logging be properly disabled in Drakov's stealth mode
* Always have a type qualifier in square brackets in from of your message in white, 'logger.log('[TYPE]'.white', 'Something is happening
');'
* We don't have any guidelines for how to log, except that you should have your type a different colour from your actual message
 (better logging is in our roadmap)

### Functionality that adds CLI arguments
* Make sure you add the new argument property to the 'yargsConfigOptions' object in the [arguments module](https://github.com/Aconex
/drakov/blob/master/lib/arguments.js#L3)

### Middleware functionality
...
```

#### <a name="apidoc.element.drakov.logger.setStealthMode"></a>[function <span class="apidocSignatureSpan">drakov.logger.</span>setStealthMode (isStealthMode)](#apidoc.element.drakov.logger.setStealthMode)
- description and source-code
```javascript
setStealthMode = function (isStealthMode) {
    stealthMode = isStealthMode;
}
```
- example usage
```shell
...
var middleware = require('./middleware');
var debugRequest = require('./debugRequest');

var server = null;

exports.run = function(argv, cb) {

logger.setStealthMode(argv.stealthmode);

console.log('   DRAKOV STARTED   '.green.bold.inverse);

var app = express();

// REQUEST MIDDLEWARE
app.use(requestUtils.logger);
...
```

#### <a name="apidoc.element.drakov.logger.stringfy"></a>[function <span class="apidocSignatureSpan">drakov.logger.</span>stringfy (matched)](#apidoc.element.drakov.logger.stringfy)
- description and source-code
```javascript
stringfy = function (matched) {
  return matched ? 'MATCHED'.green : 'NOT_MATCHED'.red;
}
```
- example usage
```shell
...
};

exports.areContentTypesSame = function(httpReq, specReq) {
var actual = getMediaTypeFromHttpReq(httpReq);
var expected = getMediaTypeFromSpecReq(specReq);

var result = !expected || actual === expected;
logger.log('[MATCHING]'.yellow,'by request content type:', expected, 'actual:', actual, logger.stringfy(result));
return result;
};

exports.matchesBody = function(httpReq, specReq) {
if (!specReq) {
    return true;
}
...
```



# <a name="apidoc.module.drakov.middleware"></a>[module drakov.middleware](#apidoc.module.drakov.middleware)

#### <a name="apidoc.element.drakov.middleware.init"></a>[function <span class="apidocSignatureSpan">drakov.middleware.</span>init (app, argv, cb)](#apidoc.element.drakov.middleware.init)
- description and source-code
```javascript
init = function (app, argv, cb) {
    bootstrapMiddleware(app, argv);
    var options = {sourceFiles: argv.sourceFiles, autoOptions: argv.autoOptions};
    routeHandlers(options, function(err, middleware) {
        cb(err, middleware);
    });
}
```
- example usage
```shell
...
    sslKeyFile: '/path/to/ssl/key.key',
    sslCrtFile: '/path/to/ssl/cert.crt',
    delay: 2000,
    method: ['DELETE','OPTIONS']
};

var app = express();
drakovMiddleware.init(app, argv, function(err, middlewareFunction) {
    if (err) {
        throw err;
    }
    app.use(middlewareFunction);
    app.listen(argv.serverPort);
});
...
```



# <a name="apidoc.module.drakov.query_comparator"></a>[module drakov.query_comparator](#apidoc.module.drakov.query_comparator)

#### <a name="apidoc.element.drakov.query_comparator.countMatchingQueryParms"></a>[function <span class="apidocSignatureSpan">drakov.query_comparator.</span>countMatchingQueryParms (handlers, reqQueryParams)](#apidoc.element.drakov.query_comparator.countMatchingQueryParms)
- description and source-code
```javascript
countMatchingQueryParms = function (handlers, reqQueryParams){
    handlers.forEach(function(handler){
        handler.matchingQueryParams = 0;
        handler.exactMatchingQueryParams = 0;
        handler.nonMatchingQueryParams = 0;
        var specQueryParams = handler.parsedUrl.queryParams;
        for(var param in specQueryParams){
            var value = specQueryParams[param];
            if (reqQueryParams.hasOwnProperty(param)){
                var reqValue = reqQueryParams[param];
                if (_.isEqual(value, reqValue)){
                    handler.matchingQueryParams += 1;
                    handler.exactMatchingQueryParams += 1;
                }else if (value === ''){
                    handler.matchingQueryParams += 1;
                }
            }else{
                handler.nonMatchingQueryParams +=1;
            }
        }
    });
}
```
- example usage
```shell
...

handlers.sort(content.contentTypeComparator);

var queryParams = req.query;
if (Object.keys(queryParams).length === 0) {
    handlers.sort(queryComparator.noParamComparator);
} else {
    queryComparator.countMatchingQueryParms(handlers, queryParams);
    handlers.sort(queryComparator.queryParameterComparator);
}

filteredHandlers = handlers
    .filter(filterRequestHeader(req))
    .filter(filterContentType(req));
...
```

#### <a name="apidoc.element.drakov.query_comparator.noParamComparator"></a>[function <span class="apidocSignatureSpan">drakov.query_comparator.</span>noParamComparator (a, b)](#apidoc.element.drakov.query_comparator.noParamComparator)
- description and source-code
```javascript
noParamComparator = function (a, b){
    return (Object.keys(a.parsedUrl.queryParams).length - Object.keys(b.parsedUrl.queryParams).length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.drakov.query_comparator.queryParameterComparator"></a>[function <span class="apidocSignatureSpan">drakov.query_comparator.</span>queryParameterComparator (a, b)](#apidoc.element.drakov.query_comparator.queryParameterComparator)
- description and source-code
```javascript
queryParameterComparator = function (a, b){
    if (b.matchingQueryParams === a.matchingQueryParams){
        if (b.exactMatchingQueryParams === a.exactMatchingQueryParams){
            return (a.nonMatchingQueryParams - b.nonMatchingQueryParams);
        }
        return (b.exactMatchingQueryParams - a.exactMatchingQueryParams);
    }
    return (b.matchingQueryParams - a.matchingQueryParams);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.drakov.route"></a>[module drakov.route](#apidoc.module.drakov.route)

#### <a name="apidoc.element.drakov.route.getRouteHandlers"></a>[function <span class="apidocSignatureSpan">drakov.route.</span>getRouteHandlers (method, parsedUrl, action)](#apidoc.element.drakov.route.getRouteHandlers)
- description and source-code
```javascript
getRouteHandlers = function (method, parsedUrl, action) {
     return action.examples.map(function (example) {
        return {
            action: action,
            parsedUrl: parsedUrl,
            response: example.responses[0],
            request: 'undefined' === typeof example.requests[0] ? null : specSchema.validateAndParseSchema(example.requests[0]),
            execute: function (req, res) {
                var buildResponseBody = function(specBody){
                    switch (typeof specBody) {
                        case 'boolean':
                        case 'number':
                        case 'string':
                            return new Buffer(specBody);
                        case 'object':
                            return new Buffer(JSON.stringify(specBody));
                        default:
                            return specBody;
                    }
                };

                logger.log('[DRAKOV]'.red, action.method.green, parsedUrl.uriTemplate.yellow,
                    (this.request && this.request.description ? this.request.description : action.name).blue);

                this.response.headers.forEach(function (header) {
                    res.set(header.name, header.value);
                });

                res.status(+this.response.name);
                res.send(buildResponseBody(this.response.body));
            }
        };
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.drakov.setup"></a>[module drakov.setup](#apidoc.module.drakov.setup)

#### <a name="apidoc.element.drakov.setup.startServer"></a>[function <span class="apidocSignatureSpan">drakov.setup.</span>startServer (argv, app, cb)](#apidoc.element.drakov.setup.startServer)
- description and source-code
```javascript
startServer = function (argv, app, cb) {

    var startCb = function() {
        console.log(('   Drakov ' + version + '     ').bold.inverse, 'Listening on port ' + argv.serverPort.toString().bold.red);
        if (argv.stealthmode) {
            console.log('   STEALTH MODE     '.grey.bold.inverse, 'running silently'.grey);
        }

        if (argv.public) {
            console.log('   PUBLIC MODE     '.grey.bold.inverse, 'running publicly'.grey);
        }

        if (cb) {
          cb();
        }
    };

    var server = null;
    if (argv.sslKeyFile && argv.sslCrtFile) {
        exports.isSSL = true;
        var sslOptions = {
            key: fs.readFileSync(argv.sslKeyFile, 'utf8' ),
            cert: fs.readFileSync(argv.sslCrtFile, 'utf8' ),
            rejectUnauthorized: false
        };
        server = https.createServer(sslOptions, app);
    } else {
        server = app;
    }

    if (argv.public) {
        return server.listen(argv.serverPort, startCb);
    }
    return server.listen(argv.serverPort, 'localhost', startCb);

}
```
- example usage
```shell
...
if (err) {
    throw err;
}

var discoverabilityModule;

app.use(middlewareFunction);
server = setup.startServer(argv, app, cb);
if (argv.discover && typeof argv.discover === 'string') {
    discoverabilityModule = require(argv.discover);
} else {
    app.set('views', path.join(__dirname, '..', 'views'));
    app.set('view engine', 'jade');
    discoverabilityModule = require('./middleware/discover');
}
...
```



# <a name="apidoc.module.drakov.spec_schema"></a>[module drakov.spec_schema](#apidoc.module.drakov.spec_schema)

#### <a name="apidoc.element.drakov.spec_schema.hasSchema"></a>[function <span class="apidocSignatureSpan">drakov.spec_schema.</span>hasSchema (spec)](#apidoc.element.drakov.spec_schema.hasSchema)
- description and source-code
```javascript
hasSchema = function (spec){
    return !!spec.schema;
}
```
- example usage
```shell
...
};

exports.matchWithSchema = function (json, schema){
    return tv4.validate(json, schema);
};

exports.validateAndParseSchema = function (spec){
    if (this.hasSchema(spec)){
        spec.schema = JSON.parse(spec.schema);
        validateSchema(spec.schema);
    }
    return spec;
};
...
```

#### <a name="apidoc.element.drakov.spec_schema.matchWithSchema"></a>[function <span class="apidocSignatureSpan">drakov.spec_schema.</span>matchWithSchema (json, schema)](#apidoc.element.drakov.spec_schema.matchWithSchema)
- description and source-code
```javascript
matchWithSchema = function (json, schema){
    return tv4.validate(json, schema);
}
```
- example usage
```shell
...
exports.matchesSchema = function(httpReq, specReq) {
if (!specReq){
    return true;
}

var contentType = getMediaTypeFromHttpReq(httpReq);
var reqBody = getBodyContent(httpReq, isJson(contentType));
var result =  specSchema.matchWithSchema(reqBody, specReq.schema);
logger.log('[MATCHING]'.yellow,'by request body schema', logger.stringfy(result));
return result;
};

exports.matchesHeader = function(httpReq, specReq) {
if (!specReq || !specReq.headers){
    return true;
...
```

#### <a name="apidoc.element.drakov.spec_schema.validateAndParseSchema"></a>[function <span class="apidocSignatureSpan">drakov.spec_schema.</span>validateAndParseSchema (spec)](#apidoc.element.drakov.spec_schema.validateAndParseSchema)
- description and source-code
```javascript
validateAndParseSchema = function (spec){
    if (this.hasSchema(spec)){
        spec.schema = JSON.parse(spec.schema);
        validateSchema(spec.schema);
    }
    return spec;
}
```
- example usage
```shell
...

exports.getRouteHandlers = function (method, parsedUrl, action) {
return action.examples.map(function (example) {
   return {
       action: action,
       parsedUrl: parsedUrl,
       response: example.responses[0],
       request: 'undefined' === typeof example.requests[0] ? null : specSchema.validateAndParseSchema(example.requests[0]),
       execute: function (req, res) {
           var buildResponseBody = function(specBody){
               switch (typeof specBody) {
                   case 'boolean':
                   case 'number':
                   case 'string':
                       return new Buffer(specBody);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
