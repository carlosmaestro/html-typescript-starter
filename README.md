# Initial project HTML & Typescript based on node, webpack, typescript e html
### Iniciar o projeto node
```bash
$ npm init -y
```
### Instalar o Typescript
```bash
$ npm i typescript -D
```
### Configurar o Typescript
```bash
$ npx tsc --init
```
### Configurar `tsconfig.json`
```json
...
// habilitar
"module": "ES6",
...
// configurar pasta de saida
"outDir": "./dist", 
...
```
### Instalar ts-loader
```bash
npm install --save-dev ts-loader
```
### Criar webpack.config.js
```javascript
const path = require('path');

module.exports = {
  entry: './src/index.ts',
  module: {
    rules: [
      {
        test: /\.tsx?$/,
        use: 'ts-loader',
        exclude: /node_modules/,
      },
    ],
  },
  resolve: {
    extensions: ['.tsx', '.ts', '.js'],
  },
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```
### Instalar webpack-cli
```bash
npm i webpack-cli
```

### Adicionar Tailwindcss
```bash
npm install tailwindcss @tailwindcss/cli
```