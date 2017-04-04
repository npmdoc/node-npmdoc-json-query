# api documentation for  [json-query (v2.2.0)](http://github.com/mmckegg/json-query)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-query.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-query) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-query.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-query)
#### Retrieves values from JSON objects for data binding. Offers params, nested queries, deep queries, custom reduce/filter functions and simple boolean logic. Browserify compatible.

[![NPM](https://nodei.co/npm/json-query.png?downloads=true)](https://www.npmjs.com/package/json-query)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-query/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-json-query_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-query/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-json-query/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-json-query/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matt McKegg",
        "email": "matt@wetsand.co.nz",
        "url": "http://twitter.com/MattMcKegg"
    },
    "bugs": {
        "url": "https://github.com/mmckegg/json-query/issues"
    },
    "dependencies": {},
    "description": "Retrieves values from JSON objects for data binding. Offers params, nested queries, deep queries, custom reduce/filter functions and simple boolean logic. Browserify compatible.",
    "devDependencies": {
        "ava": "^0.14.0",
        "es5-shim": "~2.1.0",
        "tape": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "750bb1750f0f985a9ae267906a2d25754d529852",
        "tarball": "https://registry.npmjs.org/json-query/-/json-query-2.2.0.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "f15ff9bbae337f4ae936e6fd2280c56d1132ae3a",
    "homepage": "http://github.com/mmckegg/json-query",
    "keywords": [
        "data binding",
        "filter",
        "json",
        "query"
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "mmckegg",
            "email": "matt@wetsand.co.nz"
        }
    ],
    "name": "json-query",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/mmckegg/json-query.git"
    },
    "scripts": {
        "test": "tape test/*.js --tap"
    },
    "testling": {
        "files": "test/*.js",
        "browsers": [
            "chrome/20.0",
            "chrome/25.0",
            "chrome/latest",
            "chrome/canary",
            "firefox/3.6",
            "firefox/20.0",
            "firefox/latest",
            "firefox/nightly",
            "opera/12.0",
            "opera/latest",
            "safari/4.0",
            "safari/latest",
            "opera/next",
            "iphone/6.0..latest",
            "ipad/6.0..latest",
            "safari/6.0..latest",
            "android-browser/4.2..latest",
            "iexplore/6.0",
            "iexplore/9.0..latest"
        ]
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module json-query](#apidoc.module.json-query)
1.  [function <span class="apidocSignatureSpan">json-query.</span>lastParent (query)](#apidoc.element.json-query.lastParent)
1.  [function <span class="apidocSignatureSpan">json-query.</span>state (options, params, handleQuery)](#apidoc.element.json-query.state)
1.  object <span class="apidocSignatureSpan">json-query.</span>state.prototype

#### [module json-query.state](#apidoc.module.json-query.state)
1.  [function <span class="apidocSignatureSpan">json-query.</span>state (options, params, handleQuery)](#apidoc.element.json-query.state.state)

#### [module json-query.state.prototype](#apidoc.module.json-query.state.prototype)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>addReference (ref)](#apidoc.element.json-query.state.prototype.addReference)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>addReferences (references)](#apidoc.element.json-query.state.prototype.addReferences)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>deepQuery (source, tokens, options, callback)](#apidoc.element.json-query.state.prototype.deepQuery)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>force (def)](#apidoc.element.json-query.state.prototype.force)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getFilter (filterName)](#apidoc.element.json-query.state.prototype.getFilter)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getGlobal (globalName)](#apidoc.element.json-query.state.prototype.getGlobal)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getLocal (localName)](#apidoc.element.json-query.state.prototype.getLocal)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValue (value)](#apidoc.element.json-query.state.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValueFrom (value, item)](#apidoc.element.json-query.state.prototype.getValueFrom)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValues (values, callback)](#apidoc.element.json-query.state.prototype.getValues)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>resetCurrent ()](#apidoc.element.json-query.state.prototype.resetCurrent)
1.  [function <span class="apidocSignatureSpan">json-query.state.prototype.</span>setCurrent (key, value)](#apidoc.element.json-query.state.prototype.setCurrent)



# <a name="apidoc.module.json-query"></a>[module json-query](#apidoc.module.json-query)

#### <a name="apidoc.element.json-query.lastParent"></a>[function <span class="apidocSignatureSpan">json-query.</span>lastParent (query)](#apidoc.element.json-query.lastParent)
- description and source-code
```javascript
lastParent = function (query) {
  var last = query.parents[query.parents.length - 1]
  if (last) {
    return last.value
  } else {
    return null
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-query.state"></a>[function <span class="apidocSignatureSpan">json-query.</span>state (options, params, handleQuery)](#apidoc.element.json-query.state)
- description and source-code
```javascript
function State(options, params, handleQuery){

  options = options || {}

  //this.options = options
  this.handleQuery = handleQuery
  this.options = options
  this.locals = this.options.locals || {}
  this.globals = this.options.globals || {}
  this.rootContext = firstNonNull(options.data, options.rootContext, options.context, options.source)
  this.parent = options.parent
  this.override = options.override
  this.filters = options.filters || {}
  this.params = params || options.params || []
  this.context = firstNonNull(options.currentItem, options.context, options.source)
  this.currentItem = firstNonNull(this.context, options.rootContext, options.data)
  this.currentKey = null
  this.currentReferences = []
  this.currentParents = []
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-query.state"></a>[module json-query.state](#apidoc.module.json-query.state)

#### <a name="apidoc.element.json-query.state.state"></a>[function <span class="apidocSignatureSpan">json-query.</span>state (options, params, handleQuery)](#apidoc.element.json-query.state.state)
- description and source-code
```javascript
function State(options, params, handleQuery){

  options = options || {}

  //this.options = options
  this.handleQuery = handleQuery
  this.options = options
  this.locals = this.options.locals || {}
  this.globals = this.options.globals || {}
  this.rootContext = firstNonNull(options.data, options.rootContext, options.context, options.source)
  this.parent = options.parent
  this.override = options.override
  this.filters = options.filters || {}
  this.params = params || options.params || []
  this.context = firstNonNull(options.currentItem, options.context, options.source)
  this.currentItem = firstNonNull(this.context, options.rootContext, options.data)
  this.currentKey = null
  this.currentReferences = []
  this.currentParents = []
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-query.state.prototype"></a>[module json-query.state.prototype](#apidoc.module.json-query.state.prototype)

#### <a name="apidoc.element.json-query.state.prototype.addReference"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>addReference (ref)](#apidoc.element.json-query.state.prototype.addReference)
- description and source-code
```javascript
addReference = function (ref){
  if (ref instanceof Object && !~this.currentReferences.indexOf(ref)){
    this.currentReferences.push(ref)
  }
}
```
- example usage
```shell
...
}

// flush
handleToken(null, state)

// set databind hooks
if (state.currentItem instanceof Object) {
  state.addReference(state.currentItem)
} else {
  var parentObject = getLastParentObject(state.currentParents)
  if (parentObject) {
    state.addReference(parentObject)
  }
}
...
```

#### <a name="apidoc.element.json-query.state.prototype.addReferences"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>addReferences (references)](#apidoc.element.json-query.state.prototype.addReferences)
- description and source-code
```javascript
addReferences = function (references){
  if (references){
    references.forEach(this.addReference, this)
  }
}
```
- example usage
```shell
...
  } else if (value._sub){

    var options = copy(this.options)
    options.force = null
    options.currentItem = item

    var result = this.handleQuery(value._sub, options, this.params)
    this.addReferences(result.references)
    return result.value

  } else {
    return value
  }
},
...
```

#### <a name="apidoc.element.json-query.state.prototype.deepQuery"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>deepQuery (source, tokens, options, callback)](#apidoc.element.json-query.state.prototype.deepQuery)
- description and source-code
```javascript
deepQuery = function (source, tokens, options, callback){
  var keys = Object.keys(source)

  for (var key in source){
    if (key in source){

      var options = copy(this.options)
      options.currentItem = source[key]

      var result = this.handleQuery(tokens, options, this.params)

      if (result.value){
        return result
      }
    }
  }

  return null
}
```
- example usage
```shell
...
    }
  } else if (token.deep) {
    if (state.currentItem) {
if (token.deep.length === 0) {
  return
}

var result = state.deepQuery(state.currentItem, token.deep, state.options)
if (result) {
  state.setCurrent(result.key, result.value)
  for (var i = 0; i < result.parents.length; i++) {
    state.currentParents.push(result.parents[i])
  }
} else {
  state.setCurrent(null, null)
...
```

#### <a name="apidoc.element.json-query.state.prototype.force"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>force (def)](#apidoc.element.json-query.state.prototype.force)
- description and source-code
```javascript
force = function (def){
  var parent = this.currentParents[this.currentParents.length-1]
  if (!this.currentItem && parent && (this.currentKey != null)){
    this.currentItem = def || {}
    parent.value[this.currentKey] = this.currentItem
  }
  return !!this.currentItem
}
```
- example usage
```shell
...

function handleToken (token, state) {
// state: setCurrent, getValue, getValues, resetCurrent, deepQuery, rootContext, currentItem, currentKey, options, filters

if (token == null) {
  // process end of query
  if (!state.currentItem && state.options.force) {
    state.force(state.options.force)
  }
} else if (token.values) {
  if (state.currentItem) {
    var keys = Object.keys(state.currentItem)
    var values = []
    keys.forEach(function (key) {
      if (token.deep && Array.isArray(state.currentItem[key])) {
...
```

#### <a name="apidoc.element.json-query.state.prototype.getFilter"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getFilter (filterName)](#apidoc.element.json-query.state.prototype.getFilter)
- description and source-code
```javascript
getFilter = function (filterName){
  if (~filterName.indexOf('/')){
    var result = null
    var filterParts = filterName.split('/')

    for (var i=0;i<filterParts.length;i++){
      var part = filterParts[i]
      if (i == 0){
        result = this.filters[part]
      } else if (result && result[part]){
        result = result[part]
      }
    }

    return result
  } else {
    return this.filters[filterName]
  }
}
```
- example usage
```shell
...
  if (typeof helper === 'function') {
    // function(input, args...)
    var values = state.getValues(token.args || [])
    var result = helper.apply(state.options, [state.currentItem].concat(values))
    state.setCurrent(null, result)
  } else {
    // fallback to old filters
    var filter = state.getFilter(token.filter)
    if (typeof filter === 'function') {
      var values = state.getValues(token.args || [])
      var result = filter.call(state.options, state.currentItem, {args: values, state: state, data: state.rootContext})
      state.setCurrent(null, result)
    }
  }
} else if (token.deep) {
...
```

#### <a name="apidoc.element.json-query.state.prototype.getGlobal"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getGlobal (globalName)](#apidoc.element.json-query.state.prototype.getGlobal)
- description and source-code
```javascript
getGlobal = function (globalName){
  if (~globalName.indexOf('/')){
    var result = null
    var parts = globalName.split('/')

    for (var i=0;i<parts.length;i++){
      var part = parts[i]
      if (i == 0){
        result = this.globals[part]
      } else if (result && result[part]){
        result = result[part]
      }
    }

    return result
  } else {
    return this.globals[globalName]
  }
}
```
- example usage
```shell
...
  if (state.currentItem) {
    return true
  } else {
    state.resetCurrent()
    state.setCurrent(null, state.context)
  }
} else if (token.filter) {
  var helper = state.getLocal(token.filter) || state.getGlobal(token.filter)
  if (typeof helper === 'function') {
    // function(input, args...)
    var values = state.getValues(token.args || [])
    var result = helper.apply(state.options, [state.currentItem].concat(values))
    state.setCurrent(null, result)
  } else {
    // fallback to old filters
...
```

#### <a name="apidoc.element.json-query.state.prototype.getLocal"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getLocal (localName)](#apidoc.element.json-query.state.prototype.getLocal)
- description and source-code
```javascript
getLocal = function (localName){
  if (~localName.indexOf('/')){
    var result = null
    var parts = localName.split('/')

    for (var i=0;i<parts.length;i++){
      var part = parts[i]
      if (i == 0){
        result = this.locals[part]
      } else if (result && result[part]){
        result = result[part]
      }
    }

    return result
  } else {
    return this.locals[localName]
  }
}
```
- example usage
```shell
...
  if (state.currentItem) {
    return true
  } else {
    state.resetCurrent()
    state.setCurrent(null, state.context)
  }
} else if (token.filter) {
  var helper = state.getLocal(token.filter) || state.getGlobal(token.filter)
  if (typeof helper === 'function') {
    // function(input, args...)
    var values = state.getValues(token.args || [])
    var result = helper.apply(state.options, [state.currentItem].concat(values))
    state.setCurrent(null, result)
  } else {
    // fallback to old filters
...
```

#### <a name="apidoc.element.json-query.state.prototype.getValue"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValue (value)](#apidoc.element.json-query.state.prototype.getValue)
- description and source-code
```javascript
getValue = function (value) {
  return this.getValueFrom(value, null)
}
```
- example usage
```shell
...
      }
    })
    state.setCurrent(keys, values)
  } else {
    state.setCurrent(keys, [])
  }
} else if (token.get) {
  var key = state.getValue(token.get)
  if (shouldOverride(state, key)) {
    state.setCurrent(key, state.override[key])
  } else {
    if (state.currentItem || (state.options.force && state.force({}))) {
      if (isDeepAccessor(state.currentItem, key) || token.multiple) {
        var values = state.currentItem.map(function (item) {
          return item[key]
...
```

#### <a name="apidoc.element.json-query.state.prototype.getValueFrom"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValueFrom (value, item)](#apidoc.element.json-query.state.prototype.getValueFrom)
- description and source-code
```javascript
getValueFrom = function (value, item) {
  if (value._param != null){
    return this.params[value._param]
  } else if (value._sub){

    var options = copy(this.options)
    options.force = null
    options.currentItem = item

    var result = this.handleQuery(value._sub, options, this.params)
    this.addReferences(result.references)
    return result.value

  } else {
    return value
  }
}
```
- example usage
```shell
...
if (part.op === ':') {
  var key = state.getValue(part.select[0])
  return {
    func: function (item) {
      if (key) {
        item = item[key]
      }
      return state.getValueFrom(part.select[1], item)
    },
    negate: part.negate,
    booleanOp: part.booleanOp
  }
} else {
  var selector = state.getValues(part.select)
  if (!state.options.allowRegexp && part.op === '~' && selector[1] instanceof RegExp) throw new Error('options.allowRegexp is not
 enabled.')
...
```

#### <a name="apidoc.element.json-query.state.prototype.getValues"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>getValues (values, callback)](#apidoc.element.json-query.state.prototype.getValues)
- description and source-code
```javascript
getValues = function (values, callback){
  return values.map(this.getValue, this)
}
```
- example usage
```shell
...
      }
      return state.getValueFrom(part.select[1], item)
    },
    negate: part.negate,
    booleanOp: part.booleanOp
  }
} else {
  var selector = state.getValues(part.select)
  if (!state.options.allowRegexp && part.op === '~' && selector[1] instanceof RegExp) throw new Error('options.allowRegexp is not
 enabled.')
  return {
    key: selector[0],
    value: selector[1],
    negate: part.negate,
    booleanOp: part.booleanOp,
    op: part.op
...
```

#### <a name="apidoc.element.json-query.state.prototype.resetCurrent"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>resetCurrent ()](#apidoc.element.json-query.state.prototype.resetCurrent)
- description and source-code
```javascript
resetCurrent = function (){
  this.currentItem = null
  this.currentKey = null
  this.currentParents = []
}
```
- example usage
```shell
...
        state.setCurrent(null, null)
      }
    }
  } else {
    state.setCurrent(null, null)
  }
} else if (token.root) {
  state.resetCurrent()
  if (token.args && token.args.length) {
    state.setCurrent(null, state.getValue(token.args[0]))
  } else {
    state.setCurrent(null, state.rootContext)
  }
} else if (token.parent) {
  state.resetCurrent()
...
```

#### <a name="apidoc.element.json-query.state.prototype.setCurrent"></a>[function <span class="apidocSignatureSpan">json-query.state.prototype.</span>setCurrent (key, value)](#apidoc.element.json-query.state.prototype.setCurrent)
- description and source-code
```javascript
setCurrent = function (key, value){
  if (this.currentItem || this.currentKey || this.currentParents.length>0){
    this.currentParents.push({key: this.currentKey, value: this.currentItem})
  }
  this.currentItem = value
  this.currentKey = key
}
```
- example usage
```shell
...
        state.currentItem[key].forEach(function (item) {
          values.push(item)
        })
      } else {
        values.push(state.currentItem[key])
      }
    })
    state.setCurrent(keys, values)
  } else {
    state.setCurrent(keys, [])
  }
} else if (token.get) {
  var key = state.getValue(token.get)
  if (shouldOverride(state, key)) {
    state.setCurrent(key, state.override[key])
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
