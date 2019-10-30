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
--문제 1. 
/*
    이번 태풍으로 인해 일본 후쿠시마 지역에 있던 방사능 폐기물이 퍼지게 되었습니다.
    따라서 본사는 일본 지사에 있는 모든 직원들을 한국으로 귀국 조치 시키고자 합니다. 
    근무지역 코드가 'L2'인 직원의 사번, 사원명, 부서명, 직급코드, 연락처, 이메일, 
    근무지역을 조회하시오.
*/
```

```sql
SELECT EMP_ID 사번, EMP_NAME 사원명, DEPT_TITLE 부서명, JOB_CODE 직급코드, 
       PHONE 연락처, EMAIL 이메일, LOCAL_CODE 위치코드, NATIONAL_CODE 근무지역코드,
       NATIONAL_NAME 근무지역
FROM EMPLOYEE
JOIN DEPARTMENT ON(DEPT_CODE = DEPT_ID)
JOIN LOCATION ON(LOCAL_CODE = LOCATION_ID)
JOIN NATIONAL USING(NATIONAL_CODE)
WHERE LOCAL_CODE = 'L2';                                  
```

> 문제 2.

```text
--문제 2. 
/*
    개발팀의 실수로 사원들의 연락처가 유출되었습니다. 
    모든 사원들의 연락처 뒤 4자리를 '*'로 채우고 
    (연락처가 없는 사람들은 고려하지 않음)
    사번, 사원이름, 연락처, 부서명을 조회하는 쿼리문을 작성하시오. 
*/
```

```sql
SELECT EMP_ID 사번, EMP_NAME 사원명, 
       RPAD(SUBSTR(PHONE, 1, 7), 11,'*') 연락처수정, 
       DEPT_TITLE 부서명
FROM EMPLOYEE
JOIN DEPARTMENT ON(DEPT_CODE = DEPT_ID);
```

> 문제 3.

```text
--문제 3. 
/*
    연락처를 수정하다 보니, 011, 017 번호를 쓰는 직원들을 위해 
    최신 갤럭시 노트 10+를 회사 복지 차원으로 지급하기로 했다. 
    연락처가 '011', '017'로 시작하는 직원들의 사번, 사원명, 연락처, 부서명, 
    직급명을 조회하고 연락처를 '010'으로 시작하는 번호로 수정하는 
    쿼리문을 작성하시오. 
*/
```

```sql
SELECT EMP_ID 사번, EMP_NAME 사원명, PHONE 연락처, DEPT_TITLE 부서명, 
        JOB_NAME 직급명
FROM EMPLOYEE
JOIN DEPARTMENT ON(DEPT_CODE = DEPT_ID)
JOIN JOB USING(JOB_CODE)
WHERE SUBSTR(PHONE, 1, 3) IN('011', '017');

UPDATE EMPLOYEE
SET PHONE = '01047365678'
WHERE SUBSTR(PHONE, 1, 3) = ('011');
UPDATE EMPLOYEE
SET PHONE = '01012839065'
WHERE SUBSTR(PHONE, 1, 3) = ('017');

ROLLBACK;

SELECT EMP_ID, EMP_NAME, PHONE
FROM EMPLOYEE
WHERE EMP_NAME IN('윤은해', '심봉선');
```

> 문제 4.

```text
--문제 4.
/*
  본사는 근무년수가 5년 이상인 사람들에게 장기 근속 수당(월급의 20%)과 함께 
  3일간의 휴가를 주기로 했습니다. 
  근무년수가 5년 이상 29년 미만(대표 제외)인 
  사원들의 사번, 사원명, 부서코드, 직급코드, 직급명, 장기근속수당을 조회하시오. 
*/
```

```sql
SELECT EMP_ID 사번, EMP_NAME 사원명, DEPT_CODE 부서코드, JOB_CODE 직급코드,
    JOB_NAME 직급명, 
    TO_CHAR(TRUNC(SALARY*0.2, -4), 'L999,999,999') 장기근속수당    
FROM EMPLOYEE
JOIN JOB USING(JOB_CODE)
WHERE TRUNC(MONTHS_BETWEEN(SYSDATE, HIRE_DATE)/12) BETWEEN 5 AND 28;
```

> 문제 5.

```text
--문제 5.
/*
    본사에 위기가 닥쳐 급히 구조조정 공문이 내려왔습니다. 
    입사년도가 2000년 이전인 직원이거나 부서별 가장 높은 월급을
    받는 직원들부터 1순위로 명예퇴직 대상자입니다. 
    해당 조건에 맞는 직원들의 사번, 사원명, 부서코드, 직급코드, 월급, 
    입사일을 조회하시오.
    (단, 월급은 TO_CHAR 이용하여 형식 표기(좌우 공백제거)/
    부서코드가 null일 경우 '없음' 표기)
*/
```

```sql
SELECT EMP_ID 사번, EMP_NAME 사원명, NVL(DEPT_CODE,'없음') 부서코드, 
        JOB_CODE 직급코드, TRIM(TO_CHAR(SALARY, 'L999,999,999')) 월급, 
        HIRE_DATE 입사일
FROM EMPLOYEE
WHERE (DEPT_CODE, SALARY) IN(SELECT DEPT_CODE, MAX(SALARY) 
FROM EMPLOYEE GROUP BY DEPT_CODE)
    OR HIRE_DATE < TO_DATE('00/01/01');
```

