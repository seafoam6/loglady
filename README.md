[![view on npm](http://img.shields.io/npm/v/loglady.svg)](https://www.npmjs.org/package/loglady)
[![Dependency Status](https://david-dm.org/alexanderwallin/loglady.svg)](https://david-dm.org/alexanderwallin/loglady)

# loglady

![](https://s-media-cache-ak0.pinimg.com/736x/42/db/aa/42dbaad8be6ffbc091b323770f6a0944.jpg)

*One Day the Sadness Will End - Log Lady - Art Print - 8x10, by [DecisionandRevision](https://www.etsy.com/se-en/shop/DecisionandRevision?ref=unav_listing-r) at Etsy*

Utility for logging categorized and formatted output in cli apps or when debugging.

* [Installation](#Installation)
* [Usage](#Usage)
* [Examples](#Examples)
* [Roadmap](#Roadmap)

<a name="Installation"></a>
## Installation

```bash
npm install loglady
```

<a name="Usage"></a>
## Usage

```javascript
const loglady = require('loglady');

loglady.setMuted(isMuted);
loglady.setVerbose(isVerbose);
loglady.setLogFunc(logFunc);
loglady.setIgnoreFuncRegex(regex);
loglady.clearHistory();
loglady.log(...args);
loglady.logVerbose(...args);
loglady.json(json);
loglady.error(err);
loglady.pipeStdout(data);
loglady.section(heading);
loglady.action(heading);
loglady.command(cmd);
loglady.fncall(fn);
loglady.intermediate(message);
loglady.showIntroHeader(title, barChar = '#');
loglady.endWithABang(msg);
loglady.endInTotalDespair(err);
loglady.spyOn(obj, name = null);
```

<a name="Examples"></a>
## Examples

Get a taste of loglady by running `node examples/log-all-the-things.js` and you'll see something like:

![](examples/example-output.png)

<a name="Roadmap"></a>
## Roadmap

- [x] Some sort of (configurable) timestamps
- [ ] Log data sets as ascii tables
- [ ] Customizable styling (colors and text-decoration)
- [ ] Customizable ascii images
- [ ] Browser support
- [x] Log history
- [ ] Saving log history to a file
- [ ] Option to buffer output and log later
- [ ] Smart logging based on type of input (string, error etc)
- [x] Spy on an object and log all its function calls
- [x] Styled boolean logging
- [ ] Ability to theme output using TextMate/Sublime/Atom color schemes

## Developing

### Tasks

**Building the distributed version**
```bash
npm run dist
```

**Releasing a new version**
```bash
npm run release -- (major|minor|patch|x.x.x)
```

### Todo

- [ ] Watch -> build
- [ ] JS linting
- [ ] Visual examples in README
- [ ] Interactive tryout
