## SSH 접속(iterm 사용)
1) .ssh 폴더가 없으면 생성, Key파일 없으면 생성  
  cat ~/.ssh/

2) ssh-keygen 으로 위에 폴더랑 key가 없으면 생성 가능 (Enter 2번 클릭으로 생성)

3) ./ssh 폴더로 pem파일 복사 
cp <pem 파일 경로> ~/.ssh/

4) Key 파일 권한 변경 
chmod 600 ~/.ssh/<Key파일명>.pem

5) ~/.ssh에 config 파일 생성  
vi config  
[내용]
*#main  
Host lim  
HostName <IP 주소 입력>  
User ubuntu  
IdentityFile ~/.ssh/[key 파일명].pem*


6) config 파일 권한 변경  
chmod 700 ~/.ssh/config

7) 해당 네임으로 ssh 접속  
ssh lim
