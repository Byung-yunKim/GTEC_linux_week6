# GTEC_linux_week6
2022.04.08.Fri

root (유저 사용자 홈 디렉토리)
bin (실행 명령어)
dev (디바이스 제어)
lib (라이브러리)
etc (시스템 설정)

cd / -> root로 갈 수 있음

apt-get (패키지명): 패키지 다운로드

sudo(super user do): 일시적인 root권한(해당 명령어만 root 권한)

apt-get update (버전 업데이트)

passwd root (root계정 비밀번호 설정)

su(switch user): 유저 변경

cd ./dir1
cd ~/dir1
cd dir1
-> 상대경로

cd /home/ubuntu/dir1 -> 절대경로

exit (계정 로그아웃)

-rw-rw-r-- 1 ubuntu ubuntu    0 Apr  8 05:00 file1
-rw-rw-r-- 1 ubuntu ubuntu    0 Apr  8 05:00 file2
-rw-rw-r-- 1 ubuntu ubuntu    0 Apr  8 05:00 file3
-rw-r--r-- 1 root   root      0 Apr  8 05:49 rfile
-> rfile은 root 계정에서 만들어서 ubuntu 계정에는 write 권한이 없음
-> 처음이 user, 두 번째가 group, 세 번째가 other

r = read -> 4
w= write -> 2
x = execute -> 1

-rw-r--r-- 1 root   root      0 Apr  8 05:49 rfile
-> rfile의 파일 권한은 user 6, group 4, other 4

chmod 646 rfile -> rfile의 접근 권한을 rw-r--rw-로 변경
chmod u+x rfile -> rfile에 접근하는 user 권한에 실행 권한을 추가
u = user
g = group
o = other
a = all

ls -l f* -> f로 시작하는 파일만을 자세하게 보여줌

chown(change owner): 파일의 사용자를 변경
-> chown (바꿀 사용자) (파일 이름)

chgrp(change group): 파일의 그룹을 변경
-> chgrop (바꿀 그룹) (파일 이름)
