# 20191031

```
 org.apache.tiles.template.NoSuchAttributeException: Attribute 'body' not found
```

- 이슈 상황: tiles.xml에 index를 정의함. 그리고 index.jsp에서 
<definition name="index"><put-attribute name="body"></definition>정의 후,
<tiles:insertAtribution name="body">를 불렀는데 해당 에러 메시지가 뜸.
- 메시지 내용 : tiles.xml에 정의한 속성명 'body'를 찾을 수 없다.
- 해결한 방법 : 
``` html
<definition name="index"> 최상위 타일즈를 호출해서 난 오류.
<definition name="base.definitions">로 최상위 타일즈를 정의한 후 <definition name="index" extends="base.definitions">와 같이 최상위 타일즈를 상속받은 index 타일즈를 정의한다. 그리고 jsp에서 이전과 같이 호출한다.
```
참고 : https://www.codepedia.org/ama/spring-mvc-and-apache-tiles-integration-example/