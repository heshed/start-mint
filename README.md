# start-mint
----

가성비 갑 한성 u35s 3304 노트북 리눅스 셋팅기

## 좋은점
- 설치 괜찮음. 우분투 3번 설치 후 지움. 민트는 한번에 해결.
 - 우분투(15.04)는 네트워크 드라이버의 문제, 한글입력기 설정이 리붓 후 통째로 날라감. 리붓 후 기본 설정앱들이 없어지는 현상 등 몹쓸것!!
- 맥북 대신 사용해도 되겠...지?
- 화면 1600*900이라 나름 괜찮음
- HDMI 모니터 연결 잘됨

## 아쉬운점
- 사용할만하게 셋팅하려면 신경쓸게 많음.
- 셀러론이라 그런지 크롬창 여러개 많이 띄워놓으면 느려짐
 - 메모리 8기가로 업글했더니 많이 쾌적해짐. 4기가는 스왑을 사용..
- SourceTree 같은 훌륭한 git GUI클라이언트가 없음.
- vpn 설정을 못하고 있음.

### 한글입력기 : uim 벼루
- 전환 반응이 느려서 좀 답답.
- 설정 난이도가 높음. 노트북에서 alt키를 Hangul 키로 인식하게 하려면 별도의 작업이 필요함.
 - [우분투-한영키-누르면-hud-뜨는-문제-해결하기](http://blog.mezeet.com/2015/05/%EC%9A%B0%EB%B6%84%ED%88%AC-%ED%95%9C%EC%98%81%ED%82%A4-%EB%88%84%EB%A5%B4%EB%A9%B4-hud-%EB%9C%A8%EB%8A%94-%EB%AC%B8%EC%A0%9C-%ED%95%B4%EA%B2%B0%ED%95%98%EA%B8%B0/)
 - 주의! : 위 블로그에서 가이드하는 설정파일 문법을 실수했다가는 키보드 먹통현상이 발생.
 - 복구모드 들어가 / rw remount 후 해당 설정파일을 수정해야하는 불상사 발생 가능.
- 한영입력키를 alt-space, Hangul 키로 셋팅해놨는데, 특정 프로그램에서는 적용 안되는 경우.
 - wine으로 설치한 카톡에서 한글 입력 안됨
- 한글입력하다 백스페이스로 지울 때 자소입력중에는 두번을 입력해야 취소되고, 마지막으로 입력된 자소가 한번 더 복사되는 현상이 있음.

OSX 에서 사용하던 툴 대체 () 괄호는 OSX 앱

## Launcher : (Alfred)
- https://github.com/qdore/Mutate
```
sudo add-apt-repository ppa:mutate/ppa
sudo apt-get update
sudo apt-get install mutate
```

## slack client
- https://github.com/raelgc/scudcloud
```
sudo apt-add-repository -y ppa:rael-gc/scudcloud
sudo apt-get update
sudo apt-get install scudcloud
```
- icon
```
sudo dpkg-divert --add --rename --divert /opt/scudcloud/resources/scudcloud.png.real /opt/scudcloud/resources/scudcloud.png
sudo cp ~/scudcloud.png /opt/scudcloud/resources/
sudo chmod +r /opt/scudcloud/resources/scudcloud.png # ensure it's globally readable
```

 
## Screen Capture : (SnappyApp)
- shutter
 - http://lifehacker.com/5889994/the-best-screen-capture-tool-for-linux
 - http://shutter-project.org/
 - 단축키 설정 메뉴가 안보임..

```
sudo add-apt-repository ppa:shutter/ppa
sudo apt-get update && sudo apt-get install shutter
```

## Window Manager : (spectacle)
- 못찾음
- Super + 화살표 키로 창을 50% 사이즈로 이동할 수 있다.
- 아쉬운대로 키보드 설정에서 창 이동 단축키 설정 가능

## clipboard manager (ClipMenu)
- https://github.com/Keruspe/GPaste (안써봄)
- 쓸만한게 없어 보임

## Git Client
- sourcetree
 - 절규만 보일뿐
 - https://answers.atlassian.com/questions/149631/sourcetree-for-linux
 - https://blog.sourcetreeapp.com/2015/02/25/were-just-getting-started-with-sourcetree/
- http://www.syntevo.com/smartgit/
 - 유료..

## Chrome
- https://www.google.com/chrome/browser/desktop/

## Jebrains
- Intellij, PyCharm, Clion Linux 버전 받으면 됨

## KakaoTalk
- PlayOnLinux, wine 설치
- 카톡 설치는 구글신에게
- 뜬금없는 행업, 메시지 알람마다 포커스 이동 등 불편한 점이 많음


## MarkDown Editor : (MacDown)
- Intellij markdown plugin
- gitbook (online)
- Atom ...
- 적당한걸 못찾겠음..

## Memo
- http://getspringseed.com/
 - 마크다운을 지원하고 드랍박스와 동기화
 - libscript11? 디펜던시로 설치 안됨
- Atom 을 그냥.. ㅎ

## 팟캐스트
- 의존성 이슈로 설치 안됨.
- http://vocalproject.net/
```
sudo apt-add-repository ppa:nathandyer/vocal-stable
sudo apt-get update
sudo apt-get install vocal
```

## 동영상 플레이어 (XBMC)
- Bomi
 - https://bomi-player.github.io/
 - https://github.com/xylosper/bomi
- XBMC는 내 컴에서 실행 후 행업
```
sudo add-apt-repository ppa:darklin20/bomi
sudo apt-get update && sudo apt-get install bomi
```

## Google Drive
- https://github.com/odeke-em/drive (테스트 안해봄)
- 

## zsh
- 설치
 - https://github.com/sorin-ionescu/prezto
 - ~/.zpreztorc 에 git, fasd, python 추가
- 터미널 기본 셋팅
 - http://jr0cket.co.uk/2013/09/hey-prezto-zsh-for-command-line-heaven.html

## 시스템

### Time Machine
- TimeShift
 - http://www.teejeetech.in/p/timeshift.html
 - http://blog.daum.net/bagjunggyu/128
```
sudo add-apt-repository ppa:teejee2008/ppa
sudo apt-get update
sudo apt-get install timeshift
```

- https://www.code42.com/crashplan/


## Languages

### Java8
- http://tecadmin.net/install-oracle-java-8-jdk-8-ubuntu-via-ppa/
```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install oracle-java8-installer
$ sudo apt-get install oracle-java8-set-default
```

### Golang
- https://golang.org/dl/
```
wget https://storage.googleapis.com/golang/go1.5beta3.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.5beta3.linux-amd64.tar.gz
# PATH 설정은 알아서
export GOPATH=~/go
export PATH=/usr/local/go/bin:$GOPATH:$PATH
```

## VPN (작성중)

- 설치 가이드
 - 아래 작업 포함 단계는 http://support.purevpn.com/openvpn-configuration-guide-for-linux-mint
```
sudo apt-get install network-manager-openvpn-gnome
sudo restart network-manager
wget https://s3-us-west-1.amazonaws.com/heartbleed/linux/linux-files.zip
unzip linux-files.zip
```

## Docker
- source 저장소 추가 
```
deb https://apt.dockerproject.org/repo ubuntu-trusty main 

sudo apt-get install docker-engine
```


## ETC

```
sudo apt-get install git git-flow tig
sudo apt-get install ansible 
```

## 참고
- http://linuxmint.kr/
- http://m.blog.daum.net/bagjunggyu/193 이것저것 프로그램


### 단축키 익히기
- http://support.purevpn.com/openvpn-configuration-guide-for-linux-mint

## 바탕화면
- 설정-데스클릿
 - Weather Desklet
  - Data Service : yahoo
  - Location : 1132454 (제주). 야후 날씨 사이트에 들어가 자신이 원하는 지역의 id를 확인할 수 있다.

# Old Doc

## network driver (ubuntu-only)
- iwlwifi-3160-ucode-25.30.14.0
- https://wireless.wiki.kernel.org/en/users/drivers/iwlwifi
```
wget https://wireless.wiki.kernel.org/_media/en/users/drivers/iwlwifi-3160-ucode-25.30.14.0.tgz
tar xvfz iwlwifi-3160-ucode-25.30.14.0.tgz

cd iwlwifi-3160-ucode-25.30.14.0/
cp *ucode /lib/firmware/
# reboot or disable bluetooth
```

## 한글 디렉토리 영문명으로 변경
```
LANG=C xdg-user-dirs-gtk-update
```
