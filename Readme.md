# TypeScript project structure

This repo gets a typescript structure including eslint and prettier

```
├── .eslintignore		//Eslintignore file
├── .eslintrc			//estlin rules
├── .gitignore			//gitignore file
├── .prettierrc			//Prettier rules
├── Readme.md
├── dist			//Output Folder
├── package.json
├── src				//TS code Folder
│   └── index.ts		//Index File
└── tsconfig.json		//TS Config file
```

### Dev-Dependencies

| Dependencie                      | Version |
| -------------------------------- | ------- |
| @types/node                      | 18.6.3  |
| @typescript-eslint/eslint-plugin | 5.32.0  |
| @typescript-eslint/parser        | 5.32.0  |
| eslint                           | 8.21.0  |
| eslint-config-airbnb-base        | 15.0.0  |
| eslint-config-prettier           | 8.5.0   |
| eslint-plugin-import             | 2.26.0  |
| eslint-plugin-prettier           | 4.2.1   |
| onchange                         | 7.1.0   |
| prettier                         | 2.7.1   |
| ts-node                          | 10.9.1  |
| typescript                       | 4.7.4   |

### Scripts

| Script        | Code                                                   | Description                                                          |
| ------------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| *build*      | npx tsc                                                | Build TS code to JS in `./dist` folder                             |
| *lint*       | eslint . --ext .ts                                     | Lint code with `eslint` rules                                      |
| *prettier-f* | prettier --config .prettierrc 'src/**/*.ts' --write    | Prettier TS files in `./src` folder                                |
| *prettier-w* | onchange 'src/**/*.ts' -- prettier --write {{changed}} | Prettier TS files in `./src` folder inmediatly when file changes  |
| *fbuild*     | npm run prettier-f && npm run lint && npx tsc          | Run all command at once                                              |
