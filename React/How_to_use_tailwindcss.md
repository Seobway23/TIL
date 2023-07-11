# Tailwindcss 사용 방법
https://tailwindcss.com/docs/installation
yarn, npm 상관X

## 1. Install
- npm install -D tailwindcss (D=> developer 약자)
- npm tailwindcss init
    - tailwind.config.js 파일 생성 

## 2. Configure
- tailwind.config.js 경로에 content -> ["./src/**/*.{html,js}"], 추가
```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

## 3. Add 
- root의 css에 파일 추가
- react의 경우 index.css 에 추가
```
// 이 내용 추가
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## 4. 사용하면 끝!