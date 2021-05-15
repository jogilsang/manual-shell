
# 1. cli


## POC
- Hello World
- curl
    - [curl 날리기](#curl-날리기)
    - [curl 호출 시, $변수사용하기](#curl-호출-시,-$변수사용하기)
    - [curl로 쿠키 저장 및 조회전송](#curl로-쿠키-저장-및-조회전송)
    - [curl-health-check](#curl-health-check)
- awk
- sed
    - [SED 정의 및 구성요소](#SED-정의-및-구성요소)
- grep
- alias
    - [별칭 설정](#별칭-설정)
- cat
    - [cat << 멀티라인구분자](#cat-<<-멀티라인구분자)
- tcpdump
    - [tcpdump](#tcpdump)

---

## awk 구분자
```bash
result=`echo CV_0060_NAVER | awk -F'_' '{print $1}'`
```

## curl
### curl 호출 시, $변수사용하기
```
$site_no => (X)
${site_no} => (X)
"$site_no" => (X)
\"$site_no\" => (X)
"$((site_no))" => (X)
'"$site_no"' => (O)

Reference :
https://pythonq.com/so/bash/812964
```

### curl로 쿠키 저장 및 조회전송
```
쿠키를 파일로 저장
curl -v -I  -c cookiejar.txt https://www.example.com

파일 또는 문자열에서 쿠키 읽기
curl -v -I  -b cookiejar.txt https://www.example.com

reference :
https://www.lesstif.com/software-architect/curl-http-get-post-rest-api-14745703.html
```

### curl-health-check
```
curl --write-out %{http_code} --silent --output /dev/null -L ${website}
```

### curl 날리기
curl -s -d "payload={\"text\":\"Hello, World\"}" "URL"

---

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

### SED 정의 및 구성요소
- 정의 : streamlined editor(능률적인 에디터)   
- 내용 : 명령행에서 파일을 인자로 받아서, 명령어로 작업한 뒤 결과를 화면으로 출력함
- 패턴 스페이스(pattern space) : 파일을 라인단위로 읽을 때, 라인이 저장되는 임시공간
- 홀드 스페이스(hold space) : 다음행을 읽더라도 이전에 저장된 행이 남아있어서, 불러와서 사용가능한 공간

### list 보기
 systemctl list-units --type service

### tcpdump
```
tcpdump -vvvs 1024 -l -A host www.naver.com
```
