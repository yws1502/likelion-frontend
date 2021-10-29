## HTML과 CSS를 활용한 이력서 만들기
![image](https://user-images.githubusercontent.com/77317312/139446243-8b3aac48-56ae-4f00-a101-2cfc945a28cf.png)

- `border: 두께 방식 색깔`
  - content의 경계를 그릴 때 사용
  - 방식의 경우 다양하게 존재 [여기](https://developer.mozilla.org/ko/docs/Web/CSS/border)참고
  - 실선의 경우 `solid`

- `text-align: [location]`
  - 박스(태그) 안에서 Content의 위치를 결정
```css
/*가운데 정렬 ex/*
text-align: center;
```

- `margin`
  - 박스(태그)의 위치 조정 ~~박스의 바깥쪽의 여유라고 생각~~
  - `margin`만 설정할 경우 전부, 위치를 설정하면 그 위치면 적용
```css
/*박스를 가운데 정렬하기 위해 auto 사용/*
margin-left: auto;
margin-right: auto;
```

#### Margin, Border, Padding 정리 이미지
![image](https://user-images.githubusercontent.com/77317312/139395088-0d455442-4204-44ba-bbcf-0234dc79c199.png)

- `box-shadow: x축 y축 blur(흐림정도) spread(퍼짐도) 색상`
  | 위치 | 음수 or 0 | 양수 or 증가 |
  | -- | -- | -- |
  | x축 | 왼쪽 | 오른쪽 |
  | y축 | 위쪽 | 아래쪽 |
  | blur | 명확해짐 | 흐려짐 |
  | spread | 조금 퍼짐 | 많이 퍼짐 |
  | -- | -- | -- |
  | 색상 | rgb(색상) | a(투명도)
> ```css
> box-shadow: 0 1px 20px 0 rgba(0,0,0,0.1);
> ```

- `float: [location]`
  - 한줄에 오른쪽, 왼쪽 정렬하고 싶은 경우 클래스에 float 추가
  - float -> 둥둥 떠다닌다는 뜻
  - But `float` 때문에 **다음 태그들과 겹칠 수 있다.**
> ![image](https://user-images.githubusercontent.com/77317312/139450540-8a77a685-ee1d-4059-87df-402c450c0ff5.png)
> - 요렇게 되기 때문에 아래 친구를 이용해 조치를 취해야함

- `overflow: hidden;` <- 위의 둥둥이 조치 사항!
  - `float`속성을 갖은 친구들을 div로 묶어주고 div에 style속성으로 `overflow` 지정!
  - 이렇게 P태그를 감싸는 wrapper에 `overflow` 속성을 추가해준다.!
> ```html
> <div style'overflow: hidden;'>
>   <p style='float: left;'>안녕</p>
>   <p style='float: right;'>Hello World</p>
> </div>
> ```


#### 폰트 설정은?!! 구글 웹 폰트 사용하기
- 구글에 검색하면 나옴 [여기](https://fonts.google.com/)
- css 상단에 이거 넣기
> ```css
> @import url('https://fonts.googleapis.com/css?family=Montserrat:100,200,300,400,500,600,700,> 800&display=swap');
> ```
- 우리 문서의 폰트 적용
> ```css
> * {
>   font-family: 'Montserrat';
> }
> ```

- 브라우저 마다 margin, padding이 다를 수 있으니 초기화 해주기
> ```css
> body,h1,h2 {
>   margin: 0px;
>   padding: 0px;
> }
> ```

- div만 쓰지 말고 상황에 맞게 section, article도 같이 쓰자 ~~(다 같은)~~
- 줄간 간격을 넓히기 위해 `line-height` 사용 ~~(제일 보기 편한거는 16px)~~
- 검은 색은 쨍한 검은색 보다는 `#282828`이 마음에 듬
