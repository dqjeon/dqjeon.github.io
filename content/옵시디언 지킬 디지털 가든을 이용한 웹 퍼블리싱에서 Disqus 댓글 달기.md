---
title: "옵시디언 지킬 디지털 가든을 이용한 웹 퍼블리싱에서 Disqus 댓글 달기"
alias: "옵시디언 지킬 디지털 가든을 이용한 웹 퍼블리싱에서 Disqus 댓글 달기"
---
Disqus 댓글을 다는 방법

1. `_note` 폴더 아래에 글을 쓸때 frontmatter에 `comments: true` 추가

2. 지킬 템플릿의 `_layouts` 폴더 아래의 `note.html` 아래에 `universal embed code`만 붙여넣으면 끝.

전체 코드는 아래와 같은 형식이 된다.

```
{% if page.comments %}
<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://각자 달리 부여되는 주소.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
```
