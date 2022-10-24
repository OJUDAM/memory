# Lombok 관련 어노테이션
## Index
- [bootWar](#bootWar)
- [war](#war)

## bootWar
```aidl
 bootWar (내/외장 톰캣) 
  ㅏ-META-INF
  ㅏ-org
  ㅏ-WEB-INF
```
- war 패키지에 톰캣이 내장되어있어 별도의 톰캣 설치없이 단독으로 실행 가능하다.
- 외장 톰캣 환경에서 실행하려면 별도의 설정이 필요하다.

## war
```aidl
  war (외장 톰캣 서버 배포, 단독 실행 불가능)
  ㅏ-META-INF
  ㅏ-WEB-INF
```
- 톰캣 설치 후에 webapps 폴더 내에 war 파일 위치 후에 톰캣 실행해야한다.
- ROOT.war 파일명이면 별도의 설정 안해도됨
- bin > shutdown.bat, start.bat 돌려서 리부팅

