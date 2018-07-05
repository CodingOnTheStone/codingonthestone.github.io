---
layout: post
---

오늘은 미쿡 독립기념일이라 쉬는 날이다.  
요즘 정체된 기분이 들어서 공부를 조금 했다.  

## Rust language

java를 회사에서 쓰는데 당장 큰 불편함을 느끼지 못해서 새로운 걸 공부하고 싶었고  
이것 저것 기웃거리긴 했지만 이거다! 하는 느낌을 받는 건 없었다.  

사실 backend나 좀 더 core한 영역... 그러니까 os 근처 영역에 관심이 많았다.  
생산성이나 개발론이나 이런 것 보단 빠르고 아름다운 코드!!! 여기에 더 끌려서 더 그런 것 같다.  
아니면 내가 아직 프로젝트를 리드 하는 위치가 아니라 저런 부분에 관심이 없는 것 일 수도 있고  

무튼 코어한 무언가를 하려면 C나 C++를 해야 하는데  
진입장벽이 높은 것은 둘째 치고 취미로 무언가를 하는데  
재미있어도 할까 말까한데 온갖 짜증나는 문제들과 씨름하고 싶지 않았다.  

무슨 글을 읽다가 우연히 Rust에 대한 내용을 봤다.  
내가 찾던 core 한 곳에 접근 가능하면서도 짜증나는 문제에 크게 시달리지 않을 것 같고  
성능 또한 보장해 주는, 내가 찾던 언어였다.  
그래서 바로 열심히 자료들을 보았다. 아래 영상은 조금 길긴 한데 rust 소개 영상으로 나쁘지 않았다.  
<https://www.youtube.com/watch?v=_jMSrMex6R0>

변수에 쓰는 권한을 borrow 하는 구조는 메모리 관리를 compile time에 할 수 있게 해 주며
concurrency에서 race codition을 없앴다고 한다.  
race condition이 구체적으로 어떻게 해결되는지는 개념만 보고 직접 코딩을 해보지 않아서 감이 안잡힌다.  

튜토리얼은 공식 책자를 읽고 있다. 현재 1장까지 읽었고 2장 부터 하면 될 것 같다.  
<https://doc.rust-lang.org/book/second-edition/foreword.html>  

아직 성정중인 언어고 열심히 공부한다면 내가 기여 할 수 있지 않을까 하는 막연한 기대감도 크다.  

## O'Relly Web Newsletter

기록을 검색해 보니 6월 6일부터 오는 메일인데 오늘 눈에 띄었다.  
관심 가는 몇 가지를 읽었다.

### Switching from React to Vue

[Vue.js: the good, the meh, and the ugly](https://medium.com/@Pier/vue-js-the-good-the-meh-and-the-ugly-82800bbe6684)

오라일리 쪽에서 메일제목을 좀 더 자극적으로 잡은 것 같다.  
React.js 쓰다가 Vue를 2년간 쓴 사람의 후기인데 Vue.js를 써보지 않은 나로서는 흥미로웠다.  
(React는 router 기능을 기본적으로 안넣어서 정말 여기저기서 많이 까이는 것 같다. 이 글에서도 그 내용이...)  

### REST vs. GraphQL: Should you make the switch?

[REST vs GraphQL APIs, the Good, the Bad, the Ugly](https://www.moesif.com/blog/technical/graphql/REST-vs-GraphQL-APIs-the-good-the-bad-the-ugly/)

GraphQL에 대해 괜찮다고만 들었지 공부해 본적이 없는데  
글에서 REST와 비교해서 장단점을 구체적으로 정말 잘 설명해 주었다.  
사용자가 다양한 조건을 넣을 수 있는 복잡한 검색 결과를 주는 API는  
GraphQL을 고려 해 보는 것이 좋을 것 같다.  

### Fibonacci hashing: What it is and how it works

[Fibonacci Hashing: The Optimization that the World Forgot (or: a Better Alternative to Integer Modulo)](https://probablydance.com/2018/06/16/fibonacci-hashing-the-optimization-that-the-world-forgot-or-a-better-alternative-to-integer-modulo/)

자료구조에 대해 빠삭하진 않는데 그럼에도 불구하고 재미있게 읽었다.  
정말 쉽고 좋은 건데 왜 아무도 쓰지 않는거냐며 혹시 이유가 있으면 알려달라는, 매우 상식적인 이의제기를 하는 글이다.  
짧은 나의 지식으로는 collision을 최소화 하면서 아주 빠른, 매우 이상적인 알고리즘으로 보인다.  
아래쪽 hash function의 정의 부터 해서 꼼꼼하게 따지는 부분은  
학술적인 깊이가 없는 나로서는 쉽게 읽히진 않았다.

결론은 modulo 해서 뿌릴 바에는 피보나치로 곱해서 shift 합시당.
