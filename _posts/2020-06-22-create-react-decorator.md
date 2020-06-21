---
layout: post
title: "React - create-react-app with decorators"
categories: react
---

## Getting Started

```shell script
npx create-react-app my-app
cd my-app
yarn start
```

<br/>

### (Optional) babel-eslint version error

```shell script
cat > .env
SKIP_PREFLIGHT_CHECK=true 
^C
```

<br/>
<br/>

## Using Decorator

```shell script
yarn eject
```

```shell script
yarn add @babel/plugin-proposal-class-properties @babel/plugin-proposal-decorators
```

- package.json 수정 

```javascript
"babel": {
    "presets": [
      "react-app"
    ],
    "plugins": [
      [
        "@babel/plugin-proposal-decorators",
        {
          "legacy": true
        }
      ],
      [
        "@babel/plugin-proposal-class-properties",
        {
          "loose": true
        }
      ]
    ]
}
```
