### 상태 관리 function

1. useState
- React의 상태관리 함수
    
    ```jsx
    import React, { useState } from 'react';
    
    function Counter() {
      const [number, setNumber] = useState(0);
    			// 변수, 변수를 바꾸는 함수 // useState ('초기값')
      ...
    }
    ```
    

1. useRecoilState
- Recoil에서 사용되는 상태관리 함수
    - atom or selector의 값을 읽고 쓰려고 할 때 사용
    
    ```jsx
    import {useRecoilState} from 'recoil';
    
    const [count, setCount] = useRecoilState(countState)
    // [get, set]으로 useState와 동일
    
    const increaseCount = () => {
    	setCount(count + 1)}
    ...
    ```
    

1. useRecoilValue
- Recoil 상태의 값을 반환 → 읽기만
    
    ```jsx
    import {useRecoilValue} from 'recoil';
    const count = useRecoilValue(countState)
    ```
    

1. useSetRecoilState
- Recoil 상태의 값을 업데이트하기 위한 setter 함수를 반환
    
    ```jsx
    import {useSetRecoilState} from 'recoil';
    const count = useRecoilValue(countState)
    ```
    

1. **useResetRecoilState**
- 이 함수를 사용하면 atom, selector 초기화 가능