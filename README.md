# api documentation for  [pegjs (v0.10.0)](http://pegjs.org/)  [![npm package](https://img.shields.io/npm/v/npmdoc-pegjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pegjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pegjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pegjs)
#### Parser generator for JavaScript

[![NPM](https://nodei.co/npm/pegjs.png?downloads=true)](https://www.npmjs.com/package/pegjs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pegjs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pegjs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pegjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pegjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pegjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "David Majda",
        "email": "david@majda.cz",
        "url": "http://majda.cz/"
    },
    "bin": {
        "pegjs": "bin/pegjs"
    },
    "bugs": {
        "url": "https://github.com/pegjs/pegjs/issues"
    },
    "dependencies": {},
    "description": "Parser generator for JavaScript",
    "devDependencies": {
        "browserify": "13.1.0",
        "eslint": "2.13.1",
        "http-server": "0.9.0",
        "jasmine-node": "1.14.5",
        "uglify-js": "2.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "cf8bafae6eddff4b5a7efb185269eaaf4610ddbd",
        "tarball": "https://registry.npmjs.org/pegjs/-/pegjs-0.10.0.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "files": [
        "CHANGELOG.md",
        "LICENSE",
        "README.md",
        "VERSION",
        "bin/pegjs",
        "examples/arithmetics.pegjs",
        "examples/css.pegjs",
        "examples/javascript.pegjs",
        "examples/json.pegjs",
        "lib/compiler/asts.js",
        "lib/compiler/index.js",
        "lib/compiler/js.js",
        "lib/compiler/opcodes.js",
        "lib/compiler/passes/generate-bytecode.js",
        "lib/compiler/passes/generate-js.js",
        "lib/compiler/passes/remove-proxy-rules.js",
        "lib/compiler/passes/report-duplicate-labels.js",
        "lib/compiler/passes/report-duplicate-rules.js",
        "lib/compiler/passes/report-infinite-recursion.js",
        "lib/compiler/passes/report-infinite-repetition.js",
        "lib/compiler/passes/report-undefined-rules.js",
        "lib/compiler/visitor.js",
        "lib/grammar-error.js",
        "lib/parser.js",
        "lib/peg.js",
        "lib/utils/arrays.js",
        "lib/utils/classes.js",
        "lib/utils/objects.js",
        "package.json"
    ],
    "gitHead": "671166bbe82150042b71d5756405c0ee067df961",
    "homepage": "http://pegjs.org/",
    "keywords": [
        "parser generator",
        "PEG"
    ],
    "license": "MIT",
    "main": "lib/peg",
    "maintainers": [
        {
            "name": "dmajda",
            "email": "david@majda.cz"
        }
    ],
    "name": "pegjs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pegjs/pegjs.git"
    },
    "scripts": {
        "test": "make lint && make spec"
    },
    "version": "0.10.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pegjs](#apidoc.module.pegjs)
1.  [function <span class="apidocSignatureSpan">pegjs.</span>GrammarError (message, location)](#apidoc.element.pegjs.GrammarError)
1.  [function <span class="apidocSignatureSpan">pegjs.</span>generate (grammar, options)](#apidoc.element.pegjs.generate)
1.  [function <span class="apidocSignatureSpan">pegjs.</span>parser.SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError)
1.  object <span class="apidocSignatureSpan">pegjs.</span>GrammarError.prototype
1.  object <span class="apidocSignatureSpan">pegjs.</span>compiler
1.  object <span class="apidocSignatureSpan">pegjs.</span>compiler.visitor
1.  object <span class="apidocSignatureSpan">pegjs.</span>parser
1.  object <span class="apidocSignatureSpan">pegjs.</span>parser.SyntaxError.prototype
1.  string <span class="apidocSignatureSpan">pegjs.</span>VERSION

#### [module pegjs.GrammarError](#apidoc.module.pegjs.GrammarError)
1.  [function <span class="apidocSignatureSpan">pegjs.</span>GrammarError (message, location)](#apidoc.element.pegjs.GrammarError.GrammarError)

#### [module pegjs.GrammarError.prototype](#apidoc.module.pegjs.GrammarError.prototype)
1.  [function <span class="apidocSignatureSpan">pegjs.GrammarError.prototype.</span>constructor (message, location)](#apidoc.element.pegjs.GrammarError.prototype.constructor)

#### [module pegjs.compiler](#apidoc.module.pegjs.compiler)
1.  [function <span class="apidocSignatureSpan">pegjs.compiler.</span>compile (ast, passes, options)](#apidoc.element.pegjs.compiler.compile)
1.  object <span class="apidocSignatureSpan">pegjs.compiler.</span>passes
1.  object <span class="apidocSignatureSpan">pegjs.compiler.</span>visitor

#### [module pegjs.compiler.visitor](#apidoc.module.pegjs.compiler.visitor)
1.  [function <span class="apidocSignatureSpan">pegjs.compiler.visitor.</span>build (functions)](#apidoc.element.pegjs.compiler.visitor.build)

#### [module pegjs.parser](#apidoc.module.pegjs.parser)
1.  [function <span class="apidocSignatureSpan">pegjs.parser.</span>SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError)
1.  [function <span class="apidocSignatureSpan">pegjs.parser.</span>parse (input, options)](#apidoc.element.pegjs.parser.parse)

#### [module pegjs.parser.SyntaxError](#apidoc.module.pegjs.parser.SyntaxError)
1.  [function <span class="apidocSignatureSpan">pegjs.parser.</span>SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError.SyntaxError)
1.  [function <span class="apidocSignatureSpan">pegjs.parser.SyntaxError.</span>buildMessage (expected, found)](#apidoc.element.pegjs.parser.SyntaxError.buildMessage)

#### [module pegjs.parser.SyntaxError.prototype](#apidoc.module.pegjs.parser.SyntaxError.prototype)
1.  [function <span class="apidocSignatureSpan">pegjs.parser.SyntaxError.prototype.</span>constructor (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError.prototype.constructor)



# <a name="apidoc.module.pegjs"></a>[module pegjs](#apidoc.module.pegjs)

#### <a name="apidoc.element.pegjs.GrammarError"></a>[function <span class="apidocSignatureSpan">pegjs.</span>GrammarError (message, location)](#apidoc.element.pegjs.GrammarError)
- description and source-code
```javascript
function GrammarError(message, location) {
  this.name = "GrammarError";
  this.message = message;
  this.location = location;

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, GrammarError);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pegjs.generate"></a>[function <span class="apidocSignatureSpan">pegjs.</span>generate (grammar, options)](#apidoc.element.pegjs.generate)
- description and source-code
```javascript
generate = function (grammar, options) {
  options = options !== void 0 ? options : {};

  function convertPasses(passes) {
    var converted = {}, stage;

    for (stage in passes) {
      if (passes.hasOwnProperty(stage)) {
        converted[stage] = objects.values(passes[stage]);
      }
    }

    return converted;
  }

  options = objects.clone(options);

  var plugins = "plugins" in options ? options.plugins : [],
      config  = {
        parser: peg.parser,
        passes: convertPasses(peg.compiler.passes)
      };

  arrays.each(plugins, function(p) { p.use(config, options); });

  return peg.compiler.compile(
    config.parser.parse(grammar),
    config.passes,
    options
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pegjs.parser.SyntaxError"></a>[function <span class="apidocSignatureSpan">pegjs.</span>parser.SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError)
- description and source-code
```javascript
function peg$SyntaxError(message, expected, found, location) {
  this.message  = message;
  this.expected = expected;
  this.found    = found;
  this.location = location;
  this.name     = "SyntaxError";

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, peg$SyntaxError);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.GrammarError"></a>[module pegjs.GrammarError](#apidoc.module.pegjs.GrammarError)

#### <a name="apidoc.element.pegjs.GrammarError.GrammarError"></a>[function <span class="apidocSignatureSpan">pegjs.</span>GrammarError (message, location)](#apidoc.element.pegjs.GrammarError.GrammarError)
- description and source-code
```javascript
function GrammarError(message, location) {
  this.name = "GrammarError";
  this.message = message;
  this.location = location;

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, GrammarError);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.GrammarError.prototype"></a>[module pegjs.GrammarError.prototype](#apidoc.module.pegjs.GrammarError.prototype)

#### <a name="apidoc.element.pegjs.GrammarError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">pegjs.GrammarError.prototype.</span>constructor (message, location)](#apidoc.element.pegjs.GrammarError.prototype.constructor)
- description and source-code
```javascript
function GrammarError(message, location) {
  this.name = "GrammarError";
  this.message = message;
  this.location = location;

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, GrammarError);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.compiler"></a>[module pegjs.compiler](#apidoc.module.pegjs.compiler)

#### <a name="apidoc.element.pegjs.compiler.compile"></a>[function <span class="apidocSignatureSpan">pegjs.compiler.</span>compile (ast, passes, options)](#apidoc.element.pegjs.compiler.compile)
- description and source-code
```javascript
compile = function (ast, passes, options) {
  options = options !== void 0 ? options : {};

  var stage;

  options = objects.clone(options);
  objects.defaults(options, {
    allowedStartRules: [ast.rules[0].name],
    cache:             false,
    dependencies:      {},
    exportVar:         null,
    format:            "bare",
    optimize:          "speed",
    output:            "parser",
    trace:             false
  });

  for (stage in passes) {
    if (passes.hasOwnProperty(stage)) {
      arrays.each(passes[stage], function(p) { p(ast, options); });
    }
  }

  switch (options.output) {
    case "parser": return eval(ast.code);
    case "source": return ast.code;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.compiler.visitor"></a>[module pegjs.compiler.visitor](#apidoc.module.pegjs.compiler.visitor)

#### <a name="apidoc.element.pegjs.compiler.visitor.build"></a>[function <span class="apidocSignatureSpan">pegjs.compiler.visitor.</span>build (functions)](#apidoc.element.pegjs.compiler.visitor.build)
- description and source-code
```javascript
build = function (functions) {
  function visit(node) {
    return functions[node.type].apply(null, arguments);
  }

  function visitNop() { }

  function visitExpression(node) {
    var extraArgs = Array.prototype.slice.call(arguments, 1);

    visit.apply(null, [node.expression].concat(extraArgs));
  }

  function visitChildren(property) {
    return function(node) {
      var extraArgs = Array.prototype.slice.call(arguments, 1);

      arrays.each(node[property], function(child) {
        visit.apply(null, [child].concat(extraArgs));
      });
    };
  }

  var DEFAULT_FUNCTIONS = {
        grammar: function(node) {
          var extraArgs = Array.prototype.slice.call(arguments, 1);

          if (node.initializer) {
            visit.apply(null, [node.initializer].concat(extraArgs));
          }

          arrays.each(node.rules, function(rule) {
            visit.apply(null, [rule].concat(extraArgs));
          });
        },

        initializer:  visitNop,
        rule:         visitExpression,
        named:        visitExpression,
        choice:       visitChildren("alternatives"),
        action:       visitExpression,
        sequence:     visitChildren("elements"),
        labeled:      visitExpression,
        text:         visitExpression,
        simple_and:   visitExpression,
        simple_not:   visitExpression,
        optional:     visitExpression,
        zero_or_more: visitExpression,
        one_or_more:  visitExpression,
        group:        visitExpression,
        semantic_and: visitNop,
        semantic_not: visitNop,
        rule_ref:     visitNop,
        literal:      visitNop,
        "class":      visitNop,
        any:          visitNop
      };

  objects.defaults(functions, DEFAULT_FUNCTIONS);

  return visit;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.parser"></a>[module pegjs.parser](#apidoc.module.pegjs.parser)

#### <a name="apidoc.element.pegjs.parser.SyntaxError"></a>[function <span class="apidocSignatureSpan">pegjs.parser.</span>SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError)
- description and source-code
```javascript
function peg$SyntaxError(message, expected, found, location) {
  this.message  = message;
  this.expected = expected;
  this.found    = found;
  this.location = location;
  this.name     = "SyntaxError";

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, peg$SyntaxError);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pegjs.parser.parse"></a>[function <span class="apidocSignatureSpan">pegjs.parser.</span>parse (input, options)](#apidoc.element.pegjs.parser.parse)
- description and source-code
```javascript
function peg$parse(input, options) {
  options = options !== void 0 ? options : {};

  var peg$FAILED = {},

      peg$startRuleFunctions = { Grammar: peg$parseGrammar },
      peg$startRuleFunction  = peg$parseGrammar,

      peg$c0 = function(initializer, rules) {
            return {
              type:        "grammar",
              initializer: extractOptional(initializer, 0),
              rules:       extractList(rules, 0),
              location:    location()
            };
          },
      peg$c1 = function(code) {
            return { type: "initializer", code: code, location: location() };
          },
      peg$c2 = "=",
      peg$c3 = peg$literalExpectation("=", false),
      peg$c4 = function(name, displayName, expression) {
            return {
              type:        "rule",
              name:        name,
              expression:  displayName !== null
                ? {
                    type:       "named",
                    name:       displayName[0],
                    expression: expression,
                    location:   location()
                  }
                : expression,
              location:    location()
            };
          },
      peg$c5 = "/",
      peg$c6 = peg$literalExpectation("/", false),
      peg$c7 = function(head, tail) {
            return tail.length > 0
              ? {
                  type:         "choice",
                  alternatives: buildList(head, tail, 3),
                  location:     location()
                }
              : head;
          },
      peg$c8 = function(expression, code) {
            return code !== null
              ? {
                  type:       "action",
                  expression: expression,
                  code:       code[1],
                  location:   location()
                }
              : expression;
          },
      peg$c9 = function(head, tail) {
            return tail.length > 0
              ? {
                  type:     "sequence",
                  elements: buildList(head, tail, 1),
                  location: location()
                }
              : head;
          },
      peg$c10 = ":",
      peg$c11 = peg$literalExpectation(":", false),
      peg$c12 = function(label, expression) {
            return {
              type:       "labeled",
              label:      label,
              expression: expression,
              location:   location()
            };
          },
      peg$c13 = function(operator, expression) {
            return {
              type:       OPS_TO_PREFIXED_TYPES[operator],
              expression: expression,
              location:   location()
            };
          },
      peg$c14 = "$",
      peg$c15 = peg$literalExpectation("$", false),
      peg$c16 = "&",
      peg$c17 = peg$literalExpectation("&", false),
      peg$c18 = "!",
      peg$c19 = peg$literalExpectation("!", false),
      peg$c20 = function(expression, operator) {
            return {
              type:       OPS_TO_SUFFIXED_TYPES[operator],
              expression: expression,
              location:   location()
            };
          },
      peg$c21 = "?",
      peg$c22 = peg$literalExpectation("?", false),
      peg$c23 = "*",
      peg$c24 = peg$literalExpectation("*", false),
      peg$c25 = "+",
      peg$c26 = peg$literalExpectation("+", false),
      peg$c27 = "(",
      peg$c28 = peg$literalExpectation("(", false),
      peg$c29 = ")",
      peg$c30 = peg$literalExpectation(")", false),
      peg$c31 = function(expression) {
<span class="apidocCodeCommentSpan">            /*
             * The purpose of the "group" AST node is just to isolate label scope. We
             * don't need to put it around nodes that can't contain any labels or
             * nodes that already isolate label scope themselves. This leaves us with
             * "labeled" and "sequence".
             */
</span>            return expression.type === 'labeled' || expression.type === 'sequence'
                ? { type: "group", expression: expression }
                : expression;
          },
      peg$c32 = function(name) ...
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.parser.SyntaxError"></a>[module pegjs.parser.SyntaxError](#apidoc.module.pegjs.parser.SyntaxError)

#### <a name="apidoc.element.pegjs.parser.SyntaxError.SyntaxError"></a>[function <span class="apidocSignatureSpan">pegjs.parser.</span>SyntaxError (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError.SyntaxError)
- description and source-code
```javascript
function peg$SyntaxError(message, expected, found, location) {
  this.message  = message;
  this.expected = expected;
  this.found    = found;
  this.location = location;
  this.name     = "SyntaxError";

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, peg$SyntaxError);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pegjs.parser.SyntaxError.buildMessage"></a>[function <span class="apidocSignatureSpan">pegjs.parser.SyntaxError.</span>buildMessage (expected, found)](#apidoc.element.pegjs.parser.SyntaxError.buildMessage)
- description and source-code
```javascript
buildMessage = function (expected, found) {
  var DESCRIBE_EXPECTATION_FNS = {
        literal: function(expectation) {
          return "\"" + literalEscape(expectation.text) + "\"";
        },

        "class": function(expectation) {
          var escapedParts = "",
              i;

          for (i = 0; i < expectation.parts.length; i++) {
            escapedParts += expectation.parts[i] instanceof Array
              ? classEscape(expectation.parts[i][0]) + "-" + classEscape(expectation.parts[i][1])
              : classEscape(expectation.parts[i]);
          }

          return "[" + (expectation.inverted ? "^" : "") + escapedParts + "]";
        },

        any: function(expectation) {
          return "any character";
        },

        end: function(expectation) {
          return "end of input";
        },

        other: function(expectation) {
          return expectation.description;
        }
      };

  function hex(ch) {
    return ch.charCodeAt(0).toString(16).toUpperCase();
  }

  function literalEscape(s) {
    return s
      .replace(/\\/g, '\\\\')
      .replace(/"/g,  '\\"')
      .replace(/\0/g, '\\0')
      .replace(/\t/g, '\\t')
      .replace(/\n/g, '\\n')
      .replace(/\r/g, '\\r')
      .replace(/[\x00-\x0F]/g,          function(ch) { return '\\x0' + hex(ch); })
      .replace(/[\x10-\x1F\x7F-\x9F]/g, function(ch) { return '\\x'  + hex(ch); });
  }

  function classEscape(s) {
    return s
      .replace(/\\/g, '\\\\')
      .replace(/\]/g, '\\]')
      .replace(/\^/g, '\\^')
      .replace(/-/g,  '\\-')
      .replace(/\0/g, '\\0')
      .replace(/\t/g, '\\t')
      .replace(/\n/g, '\\n')
      .replace(/\r/g, '\\r')
      .replace(/[\x00-\x0F]/g,          function(ch) { return '\\x0' + hex(ch); })
      .replace(/[\x10-\x1F\x7F-\x9F]/g, function(ch) { return '\\x'  + hex(ch); });
  }

  function describeExpectation(expectation) {
    return DESCRIBE_EXPECTATION_FNS[expectation.type](expectation);
  }

  function describeExpected(expected) {
    var descriptions = new Array(expected.length),
        i, j;

    for (i = 0; i < expected.length; i++) {
      descriptions[i] = describeExpectation(expected[i]);
    }

    descriptions.sort();

    if (descriptions.length > 0) {
      for (i = 1, j = 1; i < descriptions.length; i++) {
        if (descriptions[i - 1] !== descriptions[i]) {
          descriptions[j] = descriptions[i];
          j++;
        }
      }
      descriptions.length = j;
    }

    switch (descriptions.length) {
      case 1:
        return descriptions[0];

      case 2:
        return descriptions[0] + " or " + descriptions[1];

      default:
        return descriptions.slice(0, -1).join(", ")
          + ", or "
          + descriptions[descriptions.length - 1];
    }
  }

  function describeFound(found) {
    return found ? "\"" + literalEscape(found) + "\"" : "end of input";
  }

  return "Expected " + describeExpected(expected) + " but " + describeFound(found) + " found.";
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pegjs.parser.SyntaxError.prototype"></a>[module pegjs.parser.SyntaxError.prototype](#apidoc.module.pegjs.parser.SyntaxError.prototype)

#### <a name="apidoc.element.pegjs.parser.SyntaxError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">pegjs.parser.SyntaxError.prototype.</span>constructor (message, expected, found, location)](#apidoc.element.pegjs.parser.SyntaxError.prototype.constructor)
- description and source-code
```javascript
function peg$SyntaxError(message, expected, found, location) {
  this.message  = message;
  this.expected = expected;
  this.found    = found;
  this.location = location;
  this.name     = "SyntaxError";

  if (typeof Error.captureStackTrace === "function") {
    Error.captureStackTrace(this, peg$SyntaxError);
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
