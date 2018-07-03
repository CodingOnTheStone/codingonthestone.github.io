---
layout: post
---

암복호화 관련해서 bouncycastle을 써야 하는데 자꾸 오류가 났다.  
bouncycastle 안에 있는 constant를 못찾는다고 하는데... 이게 못찾을 이유가 없는데...  

이것이 오류 메세지  
>Caused by: java.lang.NoSuchFieldError: data

구글링을 해 보면 여러 버전의 bouncycastle이 있어서 나는 오류라고 한결 같이 말하는데  
pom.xml에 직접적으로 적은 적이 없기 때문에 더 당황 스러웠다.  
pom.xml에 명시적으로 dependency를 적어 보았지만 소용 없었다.  

dependency tree를 뒤져서 오래된 버전을 찾았는데  
오래된 버전에는 해당 constant가 있는 package 자체가 없었다.  
나는 당연히 없으면 다른 곳을 찾겠지? 라고 생각했다.  
왜냐하면 org.abcd.ef.g 라는 것이 A.jar 안에 있다고 해서  
org.abcd.ef.b 또한 A.jar안에 반드시 있어야 하는 법은 없기 때문이다.  
그래서 org.abcd.ef.b가 A.jar 안에 없으면  
다른 jar를 뒤질 거라 생각을 했다.  

그렇게 삽질을 더 하다가...  
다른 분의 과감한(?) 결단으로 저 오래된 것을 exclude 해보자 했고  
결과는 에러없이 매우 잘 돌아가게 되었다고 한다.  

도데체 왜 찾다가 마는 건지 이해 할 수가 없고  
내가 명시적으로 dependency 적어놨으면 그걸 따라야 하는거 아니냐 정말 -_-...  
