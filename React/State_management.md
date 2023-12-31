# 상태 관리
- React는 요소의 변경된 요소만 요청
- 상태를 변경할 때 useState 같은 것들을 한 번만 호출할 수 있도록 해야 함


- 객채의 가변성, 불변성
    - 객체를 만들면 고유한 참조값이 형성됨 
    - react의 모든 state는 불변성을 유지해야 함
    - 새로운 객체를 만들어서 변경해야 함
    - 참조값이 동일한 상태에서 업데이트를 하면 업데이트가 안되기 때문에 참조값이 변경되는 상태 관리 tool을 활용해야 함


## useState
- 객체의 참조값 
- import {userState} from 'react'
- useState는 묶어서 관리 가능
    - setPosition({x: 아무거나 , y: 아무거나  })


## useReducer
- 다시 공부해야 함


## immer
- "..." spread 연산자를 사용하지 않고 가변성 객체를 사용하는 것처럼 사용가능
- useImmer
    - yarn add immer use-immer
    - package.json -> dependencies -> 확인
    - 상태를 자동으로 업데이트해줌


## Context
- 두 컴포넌트의 상태값을 공유해야 할 때, state를 가장 근접한 부모 컴포넌트로 올려서 props로 전달하면 상태값 공유 가능

- 하지만 컴포넌트가 말단에 있다면? -> context API를 사용하면 됨 
    - ex) 언어, 언어(다크모드), 로그인

- 데이터가 변경되면, 모든 자식 컴포넌트는 상태가 변경되기 때문에 rerendering이 됨
- 원하는 컴포넌트 트리 중간에 사용한다면, context API를 사용할 때 바뀔때마다 업데이트가 되기 때문에 최소한의 컴포넌트 공유가 될 수 있도록 해야 함


## 성능 개선
- 함수의 인자가 변경될때마다 호출됨
- 최상위 컴포넌트 업데이트 -> 자식 컴포넌트 모두 업데이트 되기 때문에, 매번 호출되지 않을수 있도록 useMemo등을 써야 함