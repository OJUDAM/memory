# Spring Security 설정
## Index
- [ddl-auto](#ddl-auto)

----

## ddl-auto
```
spring.jpa.hibernate.ddl-auto: create / create-drop / update / validate / none
```
 - create : 기존 테이블 삭제 후 다시 생성
 - create-drop : 기존 테이블 삭제 후 다시 생성. 종료시점에 테이블 삭제
 - update : 변경된 것만 반영
 - validate : 엔티티와 테이블이 정상 매핑되었는지만 확인
 - none : 사용하지 않음
###### [참조]https://smpark1020.tistory.com/140
