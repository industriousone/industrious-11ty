# industrious-11ty

Shared configuration &amp; templates for the Industrious [Eleventy](https://www.11ty.dev/)-based websites. Provides a stock configuration and a shared set of templates to speed up development of new sites.

## Usage

Add the contents of this repository to an Eleventy project at `src/_includes/shared`. I do this using Git submodules to make versioning and fixes easier.

Initialize things by calling into the shared configuration from the root-level `.eleventy.js`.

```js
const sharedConfig = require('./src/_includes/shared/config.js');

module.exports = function(eleventyConfig) {
	let exports = sharedConfig(eleventyConfig);

	// add site-specific configuration here

	return exports;
};
```

## Shared Configuration

- Sets the [input directory](https://www.11ty.dev/docs/config/#input-directory) to `src`.
- Sets the [output directory](https://www.11ty.dev/docs/config/#output-directory) to `_site`.
