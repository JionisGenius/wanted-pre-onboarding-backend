# wanted-pre-onboarding-backend
wanted-pre-onboarding-backend internship selection assignment





- 지원자 : 송지원
- 애플리케이션의 실행 방법 (엔드포인트 호출 방법 포함)
  -  
- 데이터베이스 테이블 구조
  -  
- 구현한 API의 동작을 촬영한 데모 영상 링크
  -  
- 구현 방법 및 이유에 대한 간략한 설명
  -  AWS 클라우드 환경에서 구축을 했습니다. 그 이유는 클라우드로 개발환경을 설정하면 어디에서나 동일한 환경에서 개발할수 있는점이 용이해서 사용했습니다.
  -  
- API명세(request/response포함)



- 트러블슈팅 모음
  - 억울해서 적어둔 트러블슈팅
    - 환경
      window local
      eclipse temurin : 11 version 11.0.9
      intellij : community
      tomcat  : 8 version
      docker





- java 환경변수 오류

```bash
java -version
# 'javac'은(는) 내부 또는 외부 명령 실행할 수 있는 프로그램 또는 배치 파일이 아닙니다

set PATH=%PATH%;"C:\\Program Files\\Eclipse Adoptium\\jdk-11.0.19.7-hotspot\\bin"

# cmd 껏다 다시 킨다
```

고급시스템 설정변경 > 환경변수 > 시스템변수 > path 편집 > (설치된jdk 경로 맨위로)

<img src="https://github.com/JionisGenius/wanted-pre-onboarding-backend/assets/98302106/48b400cd-1fac-4d23-807e-ca989d89b9b4.png" width="300" height="300"/>

Cmd 끄고 다시 실행하면 java version 확인이 된다.



- Git 서브 모듈 에러

중복된 .git file때문에 git push 가 안되었다.

`rm -rf .git`으로 .git 을 지워 하나로 만들어준다

(내 경우 master brach .git을 지우고  main brach 에 .git 파일을 남겨두었다)



- 톰캣 한글깨짐

톰캣경로 > conf> logging.properties 메모장으로 열기 UTF-8 → **EUC-KR 변경**



- 톰캣 엑세스 거부 로그

start up.bat 파일을 관리자 권한으로 실행



- 도커 데스크탑 이미지 받기 에러

cmd 관리자 모드로 열기

https://lsjsj92.tistory.com/527 ← 참고하여 해결

docker desktop> setting> general > Expose daemon on tcp://localhost:2375 without TLS 체크박스

```jsx
docker --install

docker --update

docker -v

docker pull mysql:latest # 아래와 같은 에러내용

C:\\WINDOWS\\system32>docker ps # 도커 상태확인
error during connect: in the default daemon configuration on Windows, the docker client must be run with elevated privileges to connect: Get "http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.24/containers/json": open //./pipe/docker_engine: The system cannot find the file specified.
#에러내용
```

<img src="https://github.com/JionisGenius/wanted-pre-onboarding-backend/assets/98302106/a0ff6755-a080-4b56-9691-f8502b517746.png" width="350" height="230"/>

→ 해결된 화면
