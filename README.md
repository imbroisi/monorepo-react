# Monorepo React
Utilização:

```
git clone git@github.com:imbroisi/monorepo-react.git
cd monorepo-react
npm install
npm run start:my-react-app
```
Ao alterar ou criar shared component/function:

```
npx lerna bootstrap
```


## Referência
[The Multi CRA Lerna Monorepo](https://itnext.io/guide-react-app-monorepo-with-lerna-d932afb2e875)

Correções necessárias no artigo acima (já corrigidas neste repositório):

- Em ```packages/comp-button/package.json```, corrigir

  1)  ```
      "name": "@project/comp-button",
      ```
      por:
      ```
      "name": "@my-project/comp-button",
      ```

  2) Inverter nomes abaixo:
      ```
      "main": "dist/index.js",
      "module": "src/index.js",
      ```
      para:
      ```
      "main": "src/index.js",
      "module": "dist/index.js",
      ```

- O *hack* indicado (utilização de ```babel-loader-lerna-cra```) não é necessário para CRA atual (hoje: 23/02/2020).
