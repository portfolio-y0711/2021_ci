## 🐚️ **_Database_**

목록  

* Mysql

    * 설치 후 root 비번 변경하기 

    * 사용자 생성하기 

    * 원격 접속 허용하기 

    * 설치 전 utf-8를 설정하지 못했을 경우 

<br/>

### Mysql

* 설치 후 root 비번 변경하기 

    <details>
    <summary>..(열기)</summary>

    ```bash
    # 관리자로 접속하기 (sudo apt install mysql-server로 설치한 경우)
    $ sudo mysql

    # 비번 변경하기 
    mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

    # 변경 적용하기 
    mysql> FLUSH PRIVILEGES;

    # 확인 
    mysql> SELECT user,authentication_string,plugin,host FROM mysql.user;

    ```

    </details> <br/>

* 사용자 생성하기 

    <details>
    <summary>..(열기)</summary>

    ```bash

    # 사용자 생성 
    mysql> CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';

    # 모든 권한 부여하기
    mysql> GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost' WITH GRANT OPTION;

    # 확인 
    mysql> SELECT user,authentication_string,plugin,host FROM mysql.user;

    ```

    </details>


<br/>

* 원격 접속 허용하기 

    * [링크 바로가기 >>>](https://zetawiki.com/wiki/MySQL_%EC%9B%90%EA%B2%A9_%EC%A0%91%EC%86%8D_%ED%97%88%EC%9A%A9)

<br/>

* 설치 전 utf-8를 설정하지 못했을 경우 

    <details>
    <summary>..(열기)</summary>

    ```bash
    # 파일경로 /etc/mysql/mysql.cnf

    [client]
    default-character-set=utf8

    [mysql]
    default-character-set=utf8

    [mysqld]
    collation-server = utf8_unicode_ci
    init-connect='SET NAMES utf8'
    character-set-server = utf8

    # 설정 내용 확인 
    mysql> status

    ```

    </details>

<br/>
