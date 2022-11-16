# Vue setting

## (1) start

- cd desktop

- npm init vue@latest

- 파일 이름 정하기

- Add Eslint for code quality? 부터 Yes

- cd 파일명

- npm install

- code . -y (open)

## (2) vite setup

- .eslintrc.cjs 작성
```js
/* eslint-env node */
require('@rushstack/eslint-patch/modern-module-resolution');

module.exports = {
    root: true,
    extends: [
        'plugin:vue/vue3-essential',
        'eslint:recommended',
        '@vue/eslint-config-prettier',
    ],
    parserOptions: {
        ecmaVersion: 'latest',
    },
    rules: {
        'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
        'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
        'prettier/prettier': [
            'error',
            {
                singleQuote: true,
                semi: true,
                useTabs: true,
                tabWidth: 2,
                trailingComma: 'all',
                printWidth: 80,
                bracketSpacing: true,
                arrowParens: 'avoid',
            },
        ],
    },
};
```
- eslint로 규칙만들기

- 설정, lint 검색, 작업영억: settings.js에서 편집, 다 삭제

- settings.js에서 입력
```js
{
    "eslint.validate": [
        
        "javascript",
        "javascriptreact",
        "typescript",
        "typescriptreact",
        "html",
        "vue",
        "markdown"
        ],
        "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
        },
        "editor.tabSize": 2,
        "eslint.rules.customizations": [
        
        ],
}
``` 
## (3) 설정하기

- 설정: save on format 미체크
- vs code 다시 실행
- npm run lint 실행

## (4) 불필요한 파일 삭제
- asserts
- compoments
- App.vue 정리
- main.js 수정

## (5) App.vue 정리
- 옵션방식 (vbase)
- 컴포지션 방식 (vbase -3) :차이점 알기

## (6) main.js 수정
```js
import { createApp } from 'vue';
import App from './App.vue';

createApp(App).mount('#app');
````


## (7) npm run dev