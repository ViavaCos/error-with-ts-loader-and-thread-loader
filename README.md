# Getting Started with Create React App

This is a repo for shown issue with `webpack` + `ts-loader` + `thread-loader`

## How to shown ? (npm)
```
npm install

npm run start
```

## How to shown ? (yarn)
```
yarn

start start
```

## After running above command and then you will get some error as below:

```
Failed to compile.

./src/components/TestDemo.tsx
Thread Loader (Worker 0)
Cannot read properties of undefined (reading 'hooks')
```

## If you delete `thread-loader` in `webpack.config.js` and erverything will be fine.

```diff
    oneOf: [
-     {
-       test: /\.tsx?$/,
-       use: [
-         {
-             loader: "thread-loader"
-         },
-         {
-             loader: "ts-loader",
-         },
-       ]
-     },
```


## Dependencies
```
"webpack": "4.28.4",
"webpack-cli": "3.1.2",
"thread-loader": "2.1.3",
"ts-loader": "5.2.2",
"typescript": "^4.2.3",
```