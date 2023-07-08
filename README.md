<p align="center">
  <a href="https://www.npmjs.com/package/@sl-code-lords/project-obfuscator" rel="noopener">
 <img width=130px height=100px src="https://raw.githubusercontent.com/javascript-obfuscator/javascript-obfuscator/master/images/logo.png" alt="SL Code LORDS"></a>
</p>

<h2 align="center">Project-Obfuscator</h2>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/SL-CODE-LORDS/Project-Obfuscator.svg)](https://github.com/SL-CODE-LORDS/Project-Obfuscator/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/SL-CODE-LORDS/Project-Obfuscator.svg)](https://github.com/SL-CODE-LORDS/Project-Obfuscator/pulls)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> Obfuscate an entire JS project with a single click.
    <br> 
</p>

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Obfuscate an entire JS project with a single click.

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes

### Installing


```sh
yarn add @sl-code-lords/project-obfuscator
```

or

```sh
npm i @sl-code-lords/project-obfuscator
```

## 🎈 Usage <a name="usage"></a>

```ts
const { obfuscate, BEST_NODE_HIGH_PERFORMANCE_CONFIG } = require('@sl-code-lords/project-obfuscator')
const Source_Folder = '/example/folder/'
const Store_Folder = '/example/obstore/'
const Bin_Path = '/example/.bin/' // its helps to ob only changed files
const Comment = {
	top: 'Javascript Project Obfuscator \n Coded By Ravindu Manoj\n\nModified File : #filename#\nModified Date : #date#\nModified Time : #time#',
	bottom: 'Powered By https://www.npmjs.com/package/@sl-code-lords/project-obfuscator',
	dont_set : false,
	timeZone : 'Asia/Colombo', // Time Zone For #time# && #date#
	deactive : false //set value as true to deactive comments 
}
// keywords == #filename# && #date# && #time# 


function obfuscateFolder() {
	console.log('starting...')
	obfuscate(Source_Folder, Store_Folder, BEST_NODE_HIGH_PERFORMANCE_CONFIG, Comment, Bin_Path)
	console.log(Source_Folder + 'Folder Successfull Obfuscated To ' + Store_Folder)
}

obfuscateFolder()

```

***

## Obfuscate Configs 

### You Can Use
```ts
const {
	BEST_NODE_HIGH_PERFORMANCE_CONFIG,
	HIGH_OB_LOW_PERFORMANCE_CONFIG,
	MEDIUM_OB_OPTIMAL_PERFORMANCE_CONFIG,
	LOW_OB_HIGH_PERFORMANCE_CONFIG,
	DEFAULT_PRESET_HIGH_PERFORMANCE_CONFIG
} = require('@ravindu01manoj/obfuscator')

```
## or

```ts
const config = {
		compact: true,
		controlFlowFlattening: true,
		controlFlowFlatteningThreshold: 0.75,
		deadCodeInjection: true,
		deadCodeInjectionThreshold: 0.4,
		debugProtection: false,
		debugProtectionInterval: 0,
		disableConsoleOutput: false,
		domainLock: [],
		domainLockRedirectUrl: 'about:blank',
		forceTransformStrings: [],
		identifierNamesCache: null,
		identifierNamesGenerator: 'hexadecimal',
		identifiersDictionary: [],
		identifiersPrefix: '',
		ignoreRequireImports: false,
		inputFileName: '',
		log: false,
		numbersToExpressions: true,
		optionsPreset: 'default',
		renameGlobals: false,
		renameProperties: false,
		renamePropertiesMode: 'safe',
		reservedNames: [],
		reservedStrings: [],
		seed: 0,
		selfDefending: false,
		simplify: true,
		sourceMap: false,
		sourceMapBaseUrl: '',
		sourceMapFileName: '',
		sourceMapMode: 'separate',
		sourceMapSourcesMode: 'sources-content',
		splitStrings: true,
		splitStringsChunkLength: 10,
		stringArray: true,
		stringArrayCallsTransform: true,
		stringArrayCallsTransformThreshold: 0.5,
		stringArrayEncoding: [],
		stringArrayIndexesType: [
			'hexadecimal-number'
		],
		stringArrayIndexShift: true,
		stringArrayRotate: true,
		stringArrayShuffle: true,
		stringArrayWrappersCount: 1,
		stringArrayWrappersChainedCalls: true,
		stringArrayWrappersParametersMaxCount: 2,
		stringArrayWrappersType: 'variable',
		stringArrayThreshold: 0.75,
		target: 'node',
		transformObjectKeys: true,
		unicodeEscapeSequence: true
	}

```

## ✍️ Authors <a name = "authors"></a>

- [@ravindu01manoj](https://github.com/ravindu01manoj) Project Author

See also the list of [contributors](https://github.com/SL-CODE-LORDS/Esana-News/contributors) who participated in this project.