## 회고

- 이번 챌린지를 통해 awesome icons를 사용하지 않고 직접 이미지들을 불러와 hover 적용을 경험했다.
- background-image의 활용이 손에 익었다.
- horizontal scrollbar에 대해 새로 알게 되었다.
    - **horizontal scrollbar 구현하기**
    - 해당 list의 부모 요소에 `overflow: auto;` 속성과 `white-space: nowrap` 속성을 추가

## 아쉬운 점
- HTML을 조금 더 구조적으로 짜야겠다는 생각을 하게 되었다.
- button tag와 a tag를 적절하게 이용하지 못한 것 같다.
    - button tag는 CRUD 작업에서 사용
    - a tag는 링크를 걸어 다른 페이지로 이동할 때 사용
    - 일단은 이렇게 정리하고 차차 알아가자
- 태그의 class 속성을 많이 남발했던 것이 마음에 걸린다.
    - icon에 대해서 처리할 때 `icon`, `OOO-icon` 이렇게 두개의 클래스로 다루었는데 다음에는 css selecter에 대해 학습하여 한 개의 태그에 class 속성을 남발하는 일을 줄여야겠다.