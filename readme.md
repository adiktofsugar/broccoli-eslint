Broccoli-eslint-alt
===

Plugin for broccoli to use eslint [http://eslint.org/].
You need a `.eslintrc.json` file to use this, and also `babel-eslint` installed on your project.

(I couldn't figure out how to use https://www.npmjs.com/package/broccoli-lint-eslint)

`npm install broccoli-eslint-alt`

tldr
===
```
(in your project's directory)
npm install --save-dev babel-eslint
(if you're using react, then also install eslint-plugin-react)
```

Sample .eslintrc.json file
===
```
{
    "parser": "babel-eslint",
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module"
    },
    "env": {
        "browser": true
    },

    "extends": [
        "eslint:recommended",
        "plugin:react/recommended"
    ],

    "rules": {
        "no-unused-vars": 0,
        "curly": [1, "multi-line"],
        "no-bitwise": 1
    },

    "ecmaFeatures": {
        "jsx": true
    },

    "plugins": [ "react" ]
}
```

Issues
===
This plugin doesn't do anything different per error levels.
