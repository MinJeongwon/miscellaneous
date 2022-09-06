## ssh 외부접속 세팅

1. 현재 포트 확인
   ```console
   sudo netstat -anp | grep LISTEN | grep sshd

   >>>
   tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      6509/sshd: /usr/sbi 
   tcp6       0      0 :::22                   :::*                    LISTEN      6509/sshd: /usr/sbi 
   ```

2. ssh 서버 설치
   ```console
   sudo apt-get install ssh
   ```

3. ssh 서버 설정 파일 들어가기
   ```console
   sudo vim /etc/ssh/sshd_config

   or

   sudo nano /etc/ssh/sshd_config
   ```

4. Port 22부분을 원하는 포트 넘버로 바꾸어주기
   ```console
   #Port 22
   부분을 주석 해제하고 Port 1111 등으로 바꾼 후
   <ESC> :wq!
   ```
   
5. ssh 재시작
   ```console
   sudo service ssh restart
   ```

6. 변경된 포트 확인
   ```console
   sudo netstat -anp | grep LISTEN | grep sshd 

   >>>
   tcp        0      0 0.0.0.0:1111            0.0.0.0:*               LISTEN      7497/sshd: /usr/sbi 
   tcp6       0      0 :::1111                 :::*                    LISTEN      7497/sshd: /usr/sbi 
   ```
