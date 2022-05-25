## Creaet React App

- npm started : react-scripts start / Starting the development server
- npm run build : react-scripts build / Creating an optimized production build
- npm test : react-scripts test / Jest를 통해 test code 를 실행한다.
- npm run eject : react-scripts eject -> CRA과 관계 없이 빼서 여러 설정들을 커스텀할 수 있게 된다. (돌이킬 수 없다. 신중히)
- npm install serve -g : serve라는 패키지를 전역으로 설치한다.
- serve -s build : serve 명령어를 -s 옵션으로 build 폴더를 지정하여 실행한다. (-s는 어떤 요청을 해도 index.html로)

## lint-staged

Run linters on git staged files
ESLint, prettier, husky를 연결
커밋 직전에 staged된 파일을 점검

```bash
npm i husky -D
npx husky install
npx husky add .husky/pre-commit "lint-staged"
npm i lint-staged -D
npm i prettier -D
```

- package.json 코드 추가

```js
  "lint-staged": {
    "**/*.js": [
      "eslint --fix",
      "prettier --write",
      "git add"
    ]
  },
```
