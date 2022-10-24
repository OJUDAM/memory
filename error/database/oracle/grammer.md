# ORACLE 문법 정리

## Index
 - [DECODE](#DECODE)
 - [NVL](#NVL)
 - [SYSDATE](#SYSDATE)
 - [INSERT SELECT](#INSERT-SELECT)
 - [BackUp](#BackUp)
-----

## DECODE
```
DECODE(필드이름,(1),(2),(3),(4))
```
- 해당필드 조회 후 ① 값일 경우 ② 로 변환, 마찬가지로 ③ 값일 경우 ④ 로 변환...
- ex) `SELECT DECODE(동의,'0','미동의', '1', '동의') FROM TABLE`

## NVL
```
NVL(필드이름,(1))
```
- 해당 필드 조회 시 NULL 일 경우 ① 값으로 변환
- ex) `nvl(동의, '0')`

## SYSDATE
```
SYSDATE
```
- 오라클의 현재 시간을 반환하는 함수이다.
- ex) `SELECT SYSDATE FROM DUAL` return : `2022-10-24 11:04:42.0'
- TO_CHAR 함수로 포맷 설정할 수 있다.
- ex) `SELECT TO_CHAR(SYSDATE, 'yyyy-MM-dd') FROM DUAL` return : 2022-10-24

## INSERT-SELECT
```
INSERT INTO TABLE1
SELECT * FROM TABLE2
```
- 테이블 백업 시 주로 사용

## BackUp
```
AS OF TIMESTAMP(SYSTIMESTAMP-INTERVAL '100' MINUTE) 
```
- 일정 시간 전의 데이터를 조회한다.
- ex) SELECT * FROM TABLE1 S OF TIMESTAMP(SYSTIMESTAMP-INTERVAL '100' MINUTE) --1시간 전의 TABLE1 데이터 조회
- 테이블 삭제 후 동일한 이름으로 컬럼이 일치하지 않는 경우 조회되지 않는다.

