## ️🕸 **_Web Server_**

목록  

* Nginx

    * Ubuntu에서 Nginx 삭제하기(설정파일 포함)

    * Tomcat 서버 앞단에 proxy 서버 설정하기 

<br/>

### Nginx

* Nginx

    * Ubuntu에서 Nginx 삭제하기(설정파일 포함)

        <details>
        <summary>..(열기)</summary>

        ```bash
        # 아래 명령어는 설정 파일을 삭제하지 않음 
        $ sudo apt-get remove nginx nginx-common

        # 아래 명령어는 설정 파일까지 삭제함
        $ sudo apt-get purge nginx nginx-common

        # 아래 명령어는 nginx의 dependencies를 삭제함
        $ sudo apt-get autoremove
        ```

        </details><br/> 

    * Tomcat 서버 앞단에 proxy 서버 설정하기 

        * [링크 바로가기 >>>](https://www.nginx.com/resources/wiki/start/topics/examples/javaservers/)

    <br/>
