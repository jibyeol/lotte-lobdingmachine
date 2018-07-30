# lotte-lobdingmachine

http://lempedu.ldcc.co.kr/square
그때 만들었던 계정임 (10자리이상, 특수문자포함)

http://lempedu.ldcc.co.kr/EDU02.zip
http://lempedu.ldcc.co.kr/EDU03.zip
http://lempedu.ldcc.co.kr/전문테스트.zip
http://lempedu.ldcc.co.kr/SMART_HOME.zip

Window -> Preference -> General/workspace -> Text file encoding을 Other에 UTF-8로 설정

Help -> Install New Software -> Add -> http://propedit.sourceforge.jp/eclipse/updates 에서 PropertiesEditor/Properties Editor 체크 후 Next -> Next -> 동의함 -> Finish
 http://lempqa.ldcc.co.kr/adt/update

Window -> Preference -> LEMP 에서
builder URL : https://lempqa.ldcc.co.kr/builder
id : edu001
pw : edu0101!
인증받기!

server.xml에
<Connector URIEncoding="UTF-8" connectionTimeout="20000" port="8080" protocol="HTTP/1.1" redirectPort="8443"/>
URLEncoding 프로퍼티 추가

EDU02안에 context.xml파일을 server에 덮어쓰기함

일반 Project를 생성한다. SMART_HOME으로 그리고 SMART_HOME에 있는 폴더 복사 붙여넣기함
(원래는 SMART_HOME 프로젝트로 생성하는데 방화벽때문)

LEMP WebServer Project 생성 (lemp-server)
여기서 Dynamic web module version은 2.5까지밖에 지원안되므로 2.5로 할것!
Configuration에 LEMP Server Project를 선택하고 생성

lemp-server/WebContent/WEB-INF

LEMP MODEL과 LEMP ADAPTER 프로젝트 생성



lemp-server 우클릭 properties -> Java Build Path -> Libraries -> lemp1.0 -> edit -> user libraries -> import -> workspace3/lib/lemp1.0.userlibraries를 임포트시킴
Libraries에서 Projects에서 lemp-adapter 프로젝트 추가
왼쪽에 Deployment Assembly Add Java Build Path Entiryes에 lemp~~ 2개 넣고, Project에서 model과 adapter 프로젝트 추가


SMART_HOME/lib/ex/limpEx.userlibraries에 이외에 필요한 jar파일들을 정의해주면 됨


lemp-adapter의 properties에서 Java Build Path -> Proejct 에서 lemp-model 프로젝트 추가


lemp-server/WebContent/config/lemp_configuration.xml
에서 baseConfig의 customHome에 SMART_HOME경로로 바꿔주기 \를 /로 바꾸기

lemp-server/WebContent/config/sql/journalDB~~~랑LEMPDB~~~에서 MSSQL을 MYSQL로 바꿈

SMART_HOME/conf/properties/lemp.properties에 프로퍼티 설정하면됨
SMART_HOME/conf/server/display_message~~.xml은 메세지들,,,
SMART_HOME/conf/server/log4j2.xml은 log4j



