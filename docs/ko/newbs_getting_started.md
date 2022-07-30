# QMK 환경 설정하기

여러분의 키맵을 빌드할수 있게 되기 전에, 몇 가지 소프트웨어를 설치하고 빌드 환경을 설정해야 합니다. 얼마나 많은 키보드 펌웨어를 컴파일 하려는지는 모르지만, 이 과정은 단 한번만 하시면 됩니다.

## 1. 전제 조건

시작하려면 몇 가지 소프트웨어가 필요합니다.There are a few pieces of software you'll need to get started.

* [텍스트 에디터](newbs_learn_more_resources.md#text-editor-resources)
  * 일반 텍스트 파일을 수정하고 저장할 수 있는 프로그램이 필요합니다. 많은 OS에 딸려오는 기본 에디터는 일반 텍스트 파일을 저장하지 않기 때문에, 선택할때 어떤 에디터가 지원되는지 확인하십시오.
* [툴박스 (선택사항)](https://github.com/qmk/qmk_toolbox)
  * 윈도우와 맥에서 사용가능한 GUI 프로그램. 커스텀 키보드를 프로그램하고 디버그 할 수 있게 해줍니다.

?> Linux/Unix 커맨드라인으로 작업해보지 않았다면, 몇 가지 기본 개념과 명령어를 익히셔야 합니다. [이 리소스들](newbs_learn_more_resources.md#command-line-resources)은 QMK를 작업하기에 충분히 가르쳐줄 것입니다.

## 2. 빌드 환경을 준비하세요 :id=set-up-your-environment

우리는 QMK를 가능한 한 쉽게 설치할 수 있도록 노력해왔습니다. 여러분이 Linux/Unix 환경만 준비하시면, QMK가 나머지 것들을 설치할 것입니다.

<!-- tabs:start -->

### ** 윈도우 **

QMK는 CLI와 다른 필요한 플러그인과 같이, MSYS2와 관련된 것들을 관리하고 있습니다. 또한, 현재 환경에서 바로 띄울수 있는 'QMK MSYS' 터미널 숏컷이 제공됩니다.

#### 전제 조건

[QMK MSYS](https://msys.qmk.fm/)를 설치하셔야 합니다. 최신 버전은 [여기](https://github.com/qmk/qmk_distro_msys/releases/latest)에서 구하실 수 있습니다.

아니면, 수동으로 MSYS2를 설치하시고 싶다면, 다음 섹션의 절차를 따르십시오.

<details>
  <summary>수동 설치</summary>

?> 'QMK MSYS'를 사용하시면, 이 과정을 무시하십시오.

#### 전제 조건

MSYS2, Git, Python을 설치하셔야 합니다. https://www.msys2.org에서 설치 과정을 따르십시오.

MSYS2가 설치되면, 모든 열려있는 MSYS 터미널을 닫고, 새로운 MinGW 64비트 터미널을 여십시오.

!> **알림:** MinDW 64bit 터미널은 설치가 끝날때 열리는 MSYS 터미널과는 *다릅니다*. 프롬프트에는 "MSYS"가 아니고, 보라색 글자로 "MINGW64"라고 써있어야 합니다. 차이점에 대해 더 많은 정보는 [이 페이지](https://www.msys2.org/wiki/MSYS2-introduction/#subsystems)를 보십시오.

그리고 아래와 같은 명령을 실행하십시오:

    pacman --needed --noconfirm --disable-download-timeout -S git mingw-w64-x86_64-toolchain mingw-w64-x86_64-python3-pip mingw-w64-x86_64-python-pillow

#### 설치

아래의 명령어를 실행해 QMK CLI를 설치하십시오:

    python3 -m pip install qmk

</details>

### ** 맥 OS **

QMK는 CLI와 다른 모든 필요한 부속 프로그램을 자동적으로 설치하는 홈브류와 포뮬라를 유지하고 있습니다.

#### 전제 건조건

홈브류를 설치하셔야 합니다. https://brew.sh 에서 설명을 따르십시오.

#### 설치

아래 명령어를 실행하여 QMK CLI를 설치하십시오. :

    brew install qmk/qmk/qmk

### ** 리눅스/WSL **

?> **WSL 사용자들에게 알림**: 기본적으로, 설치 과정은 QMK 리포지토리를 여러분의 WSL 홈 디렉터리에 복사할 것입니다. 하지만 여러분이 수동으로 복사했다면, 윈도우즈 파일시스템이 *아니라* WSL 인스턴스에 있는지 확인하십시오(예: '/mnt' 안에 있지 않음). 거기에 접속하는 것이 현재는 [매우 느리기](https://github.com/microsoft/WSL/issues/4197) 때문입니다.

#### 전제 조건

Git과 Python을 설치하셔야 합니다. 아마 두 가지 모두 설치가 돼있겠지만, 만약 아니라면, 다음 명령어가 그것들을 설치할 것입니다.:

* Debian / Ubuntu / Devuan: `sudo apt install -y git python3-pip`
* Fedora / Red Hat / CentOS: `sudo yum -y install git python3-pip`
* Arch / Manjaro: `sudo pacman --needed --noconfirm -S git python-pip libffi`
* Void: `sudo xbps-install -y git python3-pip`
* Solus: `sudo eopkg -y install git python3`
* Sabayon: `sudo equo install dev-vcs/git dev-python/pip`
* Gentoo: `sudo emerge dev-vcs/git dev-python/pip`

#### 설치

다음 명령어를 실행하여 QMK CLI를 설치하십시오. :

    python3 -m pip install --user qmk

#### 커뮤니티 지패키지

이 패키지들은 커뮤니티 멤버들에 의해 유지됩니다. 따라서, 최신이 아니거나 완전히 작동하지 않을수 있습니다. 문제가 발생한다면, 각각의 보수자에게 알려주십시오.

Arch 기반의 배포판에서, 공식 리포지토리로부터 CLI를 설치하실수 있습니다. (알림: 이것을 작성중인 현재, 이 패키지는 필수적인 종속물을 선택적인 것으로 표시하고 있습니다.):

    sudo pacman -S qmk

또한 `qmk-git` 패키지를 시도해 보실수다있습니다 from AUR:

    yay -S qmk-git

###  ** FreeBSD **

#### 설치

아래의 명령어를 실행하여 QMK CLI의 FreeBSD 패키지를 설치하십시오 :

    pkg install -g "py*-qmk"

알림: 설치 마지막에 적힌 설명을 따라야 합니다. (다시 보려면 `pkg info -Dg "py*-qmk"` 를오사용하십시오).

<!-- tabs:end -->

## 3. QMK Setup 실행하기 :id=set-up-qmk

<!-- tabs:start -->

### ** 윈도우즈 **

QMK를 설치(인스톨)한 후, 다음 명령어로 셋업 할 수 있습니다. :

    qmk setup

대부분의 경우, 모든 프롬프트에 'y'로 대답할 것입니다.

### ** 맥OS **

QMK를 설치(인스톨)한 후, 다음 명령어로 셋업 할 수 있습니다. :

    qmk setup

대부분의 경우, 모든 프롬프트에 'y'로 대답할 것입니다.

### **SL **

QMK를 설치(인스톨)한 후, 다음 명령어로 셋업 할 수 있습니다. :

    qmk setup

대부분의 경우, 모든 프롬프트에 'y'로 대답할 것입니다.

?>**Note on Debian, Ubuntu and their derivatives**:
It's possible, that you will get an error saying something like: `bash: qmk: command not found`.
This is due to a [bug](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=839155) Debian introduced with their Bash 4.4 release, which removed `$HOME/.local/bin` from the PATH. This bug was later fixed on Debian and Ubuntu.
Sadly, Ubuntu reintroduced this bug and is [yet to fix it](https://bugs.launchpad.net/ubuntu/+source/bash/+bug/1588562).
Luckily, the fix is easy. Run this as your user: `echo 'PATH="$HOME/.local/bin:$PATH"' >> $HOME/.bashrc && source $HOME/.bashrc`

###  ** FreeBSD **

QMK를 설치(인스톨)한 후, 다음 명령어로 셋업 할 수 있습니다. :

    qmk setup

대부분의 경우, 모든 프롬프트에 'y'로 대답할 것입니다.

<!-- tabs:end -->

?> 셋업 할 때, `qmk setup -H <path>`으로 QMK 홈 폴더를 설정할 수 있습니다. 혹은 설치 후에, [cli configuration](cli_configuration.md?id=single-key-example)과 `user.qmk_home`을 사용하여 설정 할 수 있습니다. 모든 가능한 옵션은 `qmk setup --help`으로 확인하십시오.

?> 깃헙을 어떻게 사용하는지 아신다면, [이 설명을 따르기를 권장합니다.](getting_started_github.md) 그리고 당신의 개인 포크를 복사하려면 `qmk setup <github_username>/qmk_firmware` 을 사용하십시오. 무슨 뜻인지 모르겠다면, 이 메시지를 무시하셔도 괜찮습니다.

## 4. 빌드 환경 테스트하기

QMK 빌드 환경이 설정되었으ㅡㅁ로, 여러분의 키보드 펌웨어를 빌드하실수 있습니다. 키보드의 기본 키맵을 빌드하는 것으로 시작해보세요. 다음의 형식과 같은 명령어로 할 수 있습니다.:

    qmk compile -kb <keyboard> -km default

예를 들어, Clueboard 66%의 펌웨어를 빌드하려면, 이렇게 써야 합니다.:

    qmk compile -kb clueboard/66/rev3 -km default

이것이 실행되면, 아래와 비슷하게 끝나는 많은 결과를 얻을 것입니다.:

```
Linking: .build/clueboard_66_rev3_default.elf                                                       [OK]
Creating load file for flashing: .build/clueboard_66_rev3_default.hex                               [OK]
Copying clueboard_66_rev3_default.hex to qmk_firmware folder                                        [OK]
Checking file size of clueboard_66_rev3_default.hex                                                 [OK]
 * The firmware size is fine - 26356/28672 (2316 bytes free)
```

# 여러분의 키맵을 생성하세요

여러분은 자신만의 키맵을 만들 준비가 됐습니다! [첫 펌웨어 만들기](newbs_building_firmware.md)에서 진행해보세요.
