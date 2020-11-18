# manual-shell

### 정의
```bash
쉘이란?
사용자와 커널간에 인터페이스 역활을 하는 프로그램

쉘 스크립트란?
텍스트 또는 프로그램
리눅스/유닉스 쉘에 의해 실행되도록 설계된 프로그램

인터프리터에 의해 해석되고, 쉘에 의해 실행

#! : 샤뱅,해쉬뱅 /bin/bash, /bin/perl
#
# 주석

함수() {

}

시스템 관리작업의 단순화, 자동화
###

### Hello World
export 

set | grep -E '[A-C]1'
evn | grep -E '[A-C]1'

echo $$
ps -f | grep "bash"

echo $$
ps -f | grep "bash"

a1=3
a2=3
a3=3
set | grep -E 'a[1-3]'

vi .bash_profile
source ./.bash_profile
echo $PATH

vi name.sh
chmod +x name.sh
./name.sh
```

### 별칭 설정
```
vi .bashrc
alias day='date;echo;cal'
unalias day
```

### cat << 멀티라인구분자
```
cat << __EOF__
> i
> am
> who
> iam
> __EOF__
i
am
who
iam

```
