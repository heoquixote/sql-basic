# 2-1. DBeaver 다운로드

## 1. MySQL 설치

MySQL을 설치하는 것은 설치파일을 실행한 뒤 "다음", "다음"의 연속입니다.
중요한 점은 중간에 MySQL 접속을 위한 비밀번호 설정과 MySQL 포트(지하철로 따지면 출구번호)가 `3306`으로 사전 지정이 잘 되어있는지 확인하는 것입니다.

이를 통해 MySQL을 로컬 컴퓨터에 설치할 수 있고,
추후 Database에 접속할 수 있는 Command Line 혹은 DBeaver와 같은 Application을 통해 테이블을 생성하고 SQL 쿼리를 실행할 수 있게 됩니다.

[MySQL Community Server 다운로드](https://dev.mysql.com/downloads/mysql/)

여기서 본인 운영체제에 따라 Windows 혹은 macOS를 선택해줍니다.

2023년 12월 기준 ver 8이 최신이네요.
`Download`를 눌러서 설치파일을 받고 실행하겠습니다.

두 파일의 차이는 설치 시 인터넷이 필요한가 아닌가의 유무여서 별다른 차이는 없습니다.

- `mysql-installer-web-community-8.0.35.0.msi`: 인터넷 연결을 통해 다운로드 받는 설치
- `mysql-installer-community-8.0.35.0.msi`: 인터넷 연결 없이 설치하는 full package

로그인이나 회원가입을 하지 않고 `No thanks, just start my download`를 누르겠습니다.

실습이나 과제를 위해서는 `Server only`를 사용하는 걸 권장합니다.

※ 이 부분은 기존 23년 1월 배포버전만 해도 `Develop only` 항목이 있었는데 최근되어서 삭제되었습니다.

### Server only 방법

`Server only`로 진행하여도 크게 문제는 없습니다.
오히려 `Full`은 설치하는 것이 많아서 많이 무거워집니다.
본인이 사용하려는 Application에 따라 선택하면 됩니다.

- 방법 1: `Server Only` + DBeaver 와 같은 Application 따로 사용
- 방법 2: `Full` 설치하여 Workbench Application 이용

### Custom 방법

Product를 구체적으로 다음을 추가합니다.

- `[MySQL Servers] - [MySQL Server] - [MySQL Server 8.0] - [MySQL Server 8.0.21 - X64]`
- `[Applications] - [MySQL Workbench] - [MySQL Workbench 8.0] - [MySQL Workbench 8.0.21 - X64]`
- `[Documentation] - [Samples and Examples] - [Samples and Examples 8.0] - [Samples and Examples 8.0.21 - X86]`

### Custom 이용방법

MySQL을 설치하기 위한 Microsoft Visual이 필요하여 `Execute` 버튼을 눌러줍니다.

설정한 비밀번호를 넣고 check 합니다.

설치 완료 후 위 `start ~~` 항목은 모두 해제해주도록 합시다.

## 2. MySQL 실행하기

MySQL 설치가 완료되었으니 잘 실행되는지 확인해 봅시다.
사전에 설정한 비밀번호를 입력한 뒤, 아래 코드를 이용해서 데이터베이스의 종류, 데이터베이스 선택, 테이블 종류를 확인해볼 수 있습니다.

```sql
-- 설치된 데이터 베이스 조회
show databases;

-- 데이터베이스 중 mysql 선택
use mysql;

-- 선택한 mysql 데이터베이스의 테이블 조회하기
show tables;
```

## 3. Application을 통해 MySQL 접속하기 - DBeaver

Command Line을 통해 쿼리를 날릴 수 있지만 인터페이스가 불편하기 때문에 DBeaver라는 어플리케이션을 이용하여 연결해보겠습니다.
DBeaver가 설치되어 있지 않다면 다음 글을 참조해주세요.

[dbeaver 설치 및 설정](https://velog.io/@yongseok0419/dbeaver-%EC%84%A4%EC%B9%98-%EB%B0%8F-%EC%84%A4%EC%A0%95)

SQL Workbench 등의 다른 Tool을 이용하여 연결할 수도 있습니다.

- 새 데이터베이스 연결 클릭
- 연결할 수 있는 다양한 Database를 지원합니다. 우리는 MySQL을 설치했기 때문에 해당하는 것을 클릭합니다.
- MySQL 설치 시 설정한 Password를 넣어줍니다.
- Username은 기본적으로 `root`로 설정되어 있어서 변경하지 않아도 됩니다.
- `3306` 포트의 `localhost`가 연결된 것을 확인할 수 있습니다.
