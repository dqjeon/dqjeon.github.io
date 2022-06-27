---
title: "GoogleAnalytics 적용하기"
alias: "GoogleAnalytics 적용하기"
---
[Googole Analytics](https://analytics.google.com/analytics/web/provision/?authuser=1#/provision) 는 구글에서 제공하는 웹사이트 통계 프로그램이다. Jekyll에서 방문자 통계를 낼 수 있는 방법 중의 하나이다.


![[images/Pasted image 20220622005455.png]]
측정시작

![[images/Pasted image 20220622005528.png]]
계정설정 및 속성설정을 모두 해주자.

* `웹 스트림 세부정보` 
* `새로운 온페이지 태그 추가`

![[images/Pasted image 20220622005739.png]]

* `<head>` 아래에 구글에서 제공하는 태그를 입력해야 한다.
* 디지털가든 지킬 템플릿의 경우에는 `_includes`아래에 `head.html` 파일을 수정해 주면 된다.

GoogleAnalytics 적용은 검색만 해봐도 방법이 쉽게 나온다.