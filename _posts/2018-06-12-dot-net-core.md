---
layout: post
---

bay area에 출장 온지 어느덧 4개월이 지났다.  
여기에 오면 보고 느낀 것들을 적어야지 라고 생각하고 있었는데  
이전 부터 하고 싶었던 github pages를 이용해 보려고 한다.

게을러서 루비 깔고 한참 쉬다가  
jekyll 설정하고 쉬다가  
드디어 theme을 설정하고 첫 글을 쓴다.

오늘은 회의가 좀 있어서 회사에서 배운 건 크게 없고 저녁에 집에서 잠깐 찾아본 내용들

## Unity3d와 dotnet core

[unity3d 블로그 글](https://blogs.unity3d.com/2018/03/28/updated-scripting-runtime-in-unity-2018-1-what-does-the-future-hold/)  
그냥 막연히 서로 협력하면 시너지가 좋지 않을까 했는데  
2016년에 .net foundation에 들어가서 이미 하고 있었고  
dotnet core가 업데이트 하면 나름 열심히 잘 따라가는 듯 하다.  
이렇게 서로 협력하는 모습이 너무나 보기 좋다.

덧글을 보면 mono의 새 GC인 SGen로 안바꾸냐고 물어보는데  
memory access를 막 할 수가 없어져서  
성능이 좋음에도 불구하고 아직 도입 못했고  
아에 자체적으로 나아갈 것 처럼 보임

>Plenty of native code in Unity Engine has unfettered access to managed memory. This is fine for a conservative, non-moving GC. A moving GC could cause problems for that code. We’re actively working on locking down access to managed memory from our native code so that we can support a different GC in the future.  


## Orleans 2.0

[무엇이 달라졌나?](https://dotnet.github.io/orleans/Documentation/2.0/New.html)  
한 때 product에 도입해 보겠다고 정말 열심히 공부했었는데 어느세 2.0이 나왔다.  
dotnet core를 정식으로 지원한다는 점이 가장 큰 변경점 같다.  
validation logic 같은 건 서버와 클라 모두가 가지는 경우가 많은데  
Unity로 개발 한 게임의 서버로 쓰면 좋을 것 같다.
