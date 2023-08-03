# 0803
- 행성 texture 입히기
- Constellation <=> response data 연동
    - 문제 발생
    - datatype 매칭 실패
    - 결국 하나하나 뜯어보면서 해결 


### 해야 할 것
0   1  2    3      4       5       6   
[x, y, z, index, title, content, image]
- Starposition  -> const로 return 전에 관리
- Starposition -> index, star title, content, image 저장