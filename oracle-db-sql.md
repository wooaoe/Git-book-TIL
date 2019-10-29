---
description: "\U0001F469\U0001F3FC‍\U0001F4BB문제 5개 만들기 챌린지\U0001F469\U0001F3FC‍\U0001F4BB"
---

# ORACLE DB SQL

## 쿼리문 짜기 

🔗 **사용할 계정** : Homework  
**사용할 TABLE** : EMPLOYEE, DEPARTMENT, LOCATION, JOB, NATIONAL, SAL\_GRADE  
**조건** : SELECT문을 활용한 그 어느 쿼리라도 가능 

```graphql
SELECT * FROM EMPLOYEE;
SELECT * FROM DEPARTMENT;
SELECT * FROM LOCATION;
SELECT * FROM JOB;
SELECT * FROM NATIONAL;
SELECT * FROM SAL_GRADE;
```

{% hint style="info" %}
 Story를 통한 SQL 문제 만들기 

* 모든 테이블 JOIN해서 전체보기 
* 수업 때 배운 내용을 적절하게 섞어서 만들기 
* 문제 꼬아서 내지 않기 - 내가 어려우면 남들도 어려워 
* 26일 23:59분까지 15문제 제출\(이메일 제출\)
* 1-2 DB\_HW\(조원이름\).sql
{% endhint %}

📌 JOIN을 통한 전체 사원의 정보 조회해보기 

```
SELECT * FROM EMPLOYEE 
JOIN JOB USING(JOB_CODE) 
LEFT JOIN DEPARTMENT ON(DEPT_CODE = DEPT_ID) 
LEFT JOIN LOCATION ON(LOCATION_ID = LOCAL_CODE) 
JOIN NATIONAL USING(NATIONAL_CODE) 
LEFT JOIN SAL_GRADE USING(SAL_LEVEL) 
ORDER BY EMP_ID, EMP_NAME;
```

> 문제 1.

```text
/*
    이번 태풍으로 인해 일본 후쿠시마 지역에 있던 방사능 폐기물이 퍼지게 되었습니다.
    따라서 본사는 일본 지사에 있는 모든 직원들을 한국으로 귀국 조치 시키고자 합니다. 
    근무지역이 '일본'인 직원의 사번, 사원명, 부서명, 직급코드, 연락처, 이메일, 
    근무지역을 조회하는 뷰(V_INFO)를 생성하고, 근무지역을 '한국'으로 수정하세요.     
*/
```

```text
일부 오류가 나는 지점이 있어 내일 다시 수정해서 올려야겠다                                    
```













