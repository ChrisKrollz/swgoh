[changelog](#changelog)

## Synopsis

Node library to get information of **swgoh** parsing [swgoh.gg][swgoh], you can get **profile**, **characters**, **guild members** and **ships**.

## Code Example

### import
```javascript
const swgoh = require("swgoh").swgoh
//or
import {swgoh} from 'swgoh';
```


```javascript
const username= "pikax";
swgoh.profile(username).then(function (p) {
  console.log(p);

  return swgoh.guild(p.guildUrl);
}).then(console.log);
swgoh.collection(username).then(console.log);
swgoh.ship(username).then(console.log);
```

## Motivation

With TB just released, this library provides easy way to get data from [swgoh.gg][swgoh]

## Installation

```bash
yarn add swgoh
```
```bash
npm i swgoh
```


# Changelog
All notable changes to this project will be documented in this file.

## [Unreleased]

# [0.1.3] - 2017-09-20
- Fix "Profile Data undefined" when not showing AllyCode on Swgoh ([#2][i2])

# [0.1.2] - 2017-09-20
- Added support for ships

# [0.1.1] - 2017-08-19
- Fixed issue with stars when getting collection

# [0.1.0] - 2017-08-19
- First release, support collection (toons), player info and guild info.



## License

MIT

## Disclaimer

The developer of this application does not have any affiliation with the Capital Games, Disney, Lucasfilm Limited or swgoh.gg.

[swgoh]: https://swgoh.gg
[i2]: https://github.com/pikax/swgoh/issues/2