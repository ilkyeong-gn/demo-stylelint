# 스타일린트 데모

## 1. 설치하기

인기있는 스타일링 선택지를 대부분 지원하지만 설정이 다소 복잡해지는 경우도 있다.

1.1 기본 설정으로 설치하기

```bash
npm init stylelint
```

1.2 scss 설정으로 설치하기

```bash
npm install --save-dev stylelint stylelint-config-standard-scss
```

1.3 postcss(css-in-js) 설정으로 설치하기

```bash
npm install --save-dev stylelint stylelint-config postcss-styled-syntax
```

데모는 일반 css 설정으로 진행한다.

## 2. 검사하기

프로젝트 내 css 파일을 검사하기

```bash
npx stylelint "**/*.css"
```
