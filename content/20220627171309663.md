---
title: "옵시디언 지킬 디지털 가든을 이용한 웹 퍼블리싱에서 Facebook 댓글 달기"
alias: "옵시디언 지킬 디지털 가든을 이용한 웹 퍼블리싱에서 Facebook 댓글 달기"
---
FACEBOOK 에서는 댓글 플러그인을 제공한다. 다양한 댓글 서비스가 있지만 페이스북 댓글을 다는 방법을 정리해본다.

## 코드 생성
먼저 [facebook 댓글 플러그인](https://developers.facebook.com/docs/plugins/comments) 에 들어가서 코드를 생성한다.


![[attachments/Pasted image 20220616010029.png]]

댓글을 남길 URL을 입력하고, 코드받기를 실행한다.

![[attachments/Pasted image 20220616010159.png]]

## default.html 수정
`_layouts` 아래 `default.html`을 수정한다. 

`<body>` 바로 아래에 2단계에 나와있는 코드를 추가한다.

## 개별 layout 수정
가령 `_note` 레이아웃에서만 댓글을 사용하겠다 할 경우. 댓글을 달고자 하는 위치에 코드를 추가한다. 이 페이지의 경우에는 아래와 같이 추가할 수 있다.

```
{% if page.comments %}
<div    class="fb-comments" 
        data-href="메인주소{{ site.url | append: page.url }}"
        data-width="100%" 
        data-numposts="5">
</div>
{% endif %}
```

## 개별 포스팅 프론트매터 추가
댓글을 사용하고자 할 경우 프론트매터에 `comments: true` 를 작성한다.