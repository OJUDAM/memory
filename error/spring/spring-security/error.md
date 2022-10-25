# Anotation 관련 에러

## Index
- [NoSuchBeanDefinition](#NoSuchBeanDefinition)

---

## NoSuchBeanDefinition
```
NoSuchBeanDefinitionException: No qualifying bean of type 'repository.SubjectRepository' 
available: expected at least 1 bean which qualifies as autowire candidate. 
Dependency annotations: {@org.springframework.beans.factory.annotation.Autowired(required=true)}
```
`com.excel.csv 폴더 아래 존재했어야할 repository가 java 밑에 있었다...`

- SpringBoot는 root package(main 메소드 있는 폴더) 기준으로 하위에 존재하는 파일들을 탐색 
- @Configuration, @Component, @Service, @Repository, @Controller 등을 찾아 Bean 으로 등록

