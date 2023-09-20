# cdk-sample
CDK sample project in typescript with eslint prettier and husky dependencies 

# Steps :
# 1. Initialize the CDK project:
    mkdir cdk-sample && cd my-sample
    cdk init app --language=typescript
# 2 Install ESLint and Prettier:
    npm install --save-dev eslint prettier @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-config-prettier eslint-plugin-prettier

# 3 Create ESLint configuration:
Create a new file named .eslintrc.js in the root of your project, and add the following content:

    {
        "root": true,
        "parser": "@typescript-eslint/parser",
        "plugins": ["@typescript-eslint", "prettier"],
        "extends": [
            "eslint:recommended",
            "plugin:@typescript-eslint/eslint-recommended",
            "plugin:@typescript-eslint/recommended",
            "prettier",
            "plugin:prettier/recommended",
        ],
        "rules": {
            "@typescript-eslint/no-explicit-any": "off"
        }
    }
# 4 Create Prettier configuration:
Create a new file named .prettierrc in the root of your project and configure Prettier settings:

    # Ignore:
    node_modules
    
    # ingore build output
    cdk.out
    ts.out
    
    #Ignore Coverate
    coverage

# 5 Add lint and format scripts to package.json:
Open your package.json file and add the following scripts:

    "lint": "eslint .",
    "lint-and-fix": "eslint . --ext .ts --fix",

# 6 Run lint and format:
Now you can run the linting and formatting checks on your CDK project:

    npm run lint
    npm run lint-and-fix


