---
Title : SSAFY Start Camp 챗봇 퀘스트
---

서울_7_이한규  
 github url : https://github.com/Rapha0814/chatbot_test

# I. 스펙(Specification)
### 구현된 어플리케이션의 주요 기능
#### (1) 별자리 운세를 알려준다.
사용자가 '오늘의 *별자리* 운세 알려줘' 라고 입력하면 YTN에서 제공하는 자료를 크롤링해서 모든 별자리 운세를 알려준다.
이때 오늘의 자리에 예를 들어 11월 20일 이라고 특정 날짜를 입력하면 해당 달짜의 별자리 운세를 알려준다.
#### (2) 띠별 운세를 알려준다.
사용자가 '오늘의 *띠별* 운세 알려줘' 라고 입력하면 YTN에서 제공하는 자료를 크롤링해서 모든 띠의 운세를 알려준다.
이때 오늘의 자리에 예를 들어 11월 20일 이라고 특정 날짜를 입력하면 해당 달짜의 띠별 운세를 알려준다.
#### (3) 특정 띠, 별자리의 운세만 알려줄 수 있다.
사용자가 '오늘의 *사자자리* 운세 알려줘 혹은 오늘의 *닭띠* 운세 알려줘'라고 입력하면 해당 별자리와 띠의 운세만 알려준다.

# II. 회고(Retrospective)
### 어플리케이션 구현 과정에서의 어려움과 문제점
1. 데이터를 크롤링 할 때 특정 날짜의 운세도 알려주려고 하니까 여러 페이지를 크롤링 해야하는 문제가 있었다.
각 페이지 별로 운세를 알려주는 페이지 href 주소를 크롤링한 뒤 2차로 해당 주소를 이용해서 운세를 크롤링하였다.
나중에 확인해보니 url 주소에서 날짜부분과 별자리운세인지 띠별운세인지 구분하는 부분을 찾아서 해당 부분만 변경하는
것으로 코드를 수정하여 가독성과 성능을 향상 시켰다. 
2. 별자리 운세인지, 띠별 운세인지, 어떤 별자리, 띠 인지, 어느 날짜인지에 대해 분기를 만드는 과정에서 어려움이 있었다.
분기할 사항이 많아 지다보니 생각할 부분이 많았다.
# III. 보완 계획(Feedback)
### 현재 미완성이지만 추가로 구현할 기능 및 기존 문제점 보완 계획
#### (1) 필터링 기능
현재는 '오늘' 이나 특정날짜 예를 들어 '12월 31일' 같은 날짜가 입력이 없으면 돌아가지 않습니다.
해당 부분에 대한 분기를 또 작성해야 되는데 기존에 분기점이 많아서 어떻게 해야 간결하게 예외 사항을 처리할 수
있을지 고민중입니다.
#### (2) 행운의 아이템만 보여주는 기능
별자리 운세를 검색해보면 각 별자리 마다 그날의 행운의 아이템을 알려줍니다.
현재는 운세를 검색하면 한번에 같이 보여주는데 행운의 아이템만 알려줄 수 있는 기능을 추가할 예정입니다.
