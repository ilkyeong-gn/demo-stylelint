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

## 3. stylelint-order 플러그인 설치하기

> 플러그인은 특정 용도로 사용하는 커스텀 규칙의 집합
> https://stylelint.io/user-guide/configure#plugins

3.1 플러그인 설치하기

```bash
npm install --save-dev stylelint-order
```

3.2 설정 파일 수정하기(.stylelintrc.json)

```json
{
  "plugins": ["stylelint-order"],
  "rules": {}
}
```

3.3 순서 규칙 커스텀하기

~~세가지~~ 두가지 옵션을 제공한다.

- ~~properties-alphabetical-order: 속성을 알파벳 순서로 정렬~~ (알파벳 순서는 해로운 정렬 방식으로 간주)
- [order: 스타일 블록 안의 구성 요소에 순서를 부여](https://github.com/hudochenkov/stylelint-order/blob/master/rules/order/README.md)
- [properties-order: 스타일 블록 안의 속성을 정의한 순서대로 정렬](https://github.com/hudochenkov/stylelint-order/blob/master/rules/properties-order/README.md)

### 우리는 우리가 정한 기준으로 속성을 모아서 보고 싶다

```json
{
  "order/properties-order": [
    {
      "groupName": "dimensions",
      "emptyLineBefore": "always",
      "properties": ["height", "width"]
    },
    {
      "groupName": "font",
      "emptyLineBefore": "always",
      "properties": ["font-size", "font-weight"]
    }
  ]
}
```
