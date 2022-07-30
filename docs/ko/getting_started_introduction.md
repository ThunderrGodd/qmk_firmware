# 들어가며

이 페이지에서는 여러분이 QMK 프로젝트를 작업하기에 필요한 정보를 설명한다. 여러분이 Unix 쉘을 다루는 데에 익숙하다고 가정할 것이지만, C나 'make'로 컴파일하는 데에는 익숙하지 않다고 가정할 것이다.

## 기본적인 QMK 구조

QMK는 [Jun Wako](https://github.com/tmk)의 [tmk_keyboard](https://github.com/tmk/tmk_keyboard) 프로젝트의 포크이다. 원본 TMK 코드와 수정본은 `tmk_core` 폴더에서 찾을 수 있다. QMK가 추가된 버전은`quantum` 폴더에서 찾을 수 있다. 키보드 프로젝트들은 `handwired` 와 `keyboard` 폴더에서 찾을 수 있다.

### 사용자 공간 구조

`users` 폴더와 그 안에 있는 폴더들은 각 유저를 위한 곳이다. 이곳은 유저들이 키보드들 사이에서 쓰일 코드를 두는 곳이다. [Userspace feature](feature_userspace.md)에서 더 많은 정보를 얻을 수 있다.

### 키보드 프로젝트 구조
`keyboards` 폴더와 그 안에 있는 `handwired`의 하위폴더들, 그리고 벤더와 제작자의 하위 폴더들. 예를들어, `clueboard`에는 각 키보드 프로젝트 폴더가 들어있다. (예시: `qmk_firmware/keyboards/clueboard/2x1800`. 그 안에서, 다음과 같은 구조를 찾을 수 있다:

* `keymaps/`: 빌드될수 있는 다른 키맵들Different keymaps that can be built
* `rules.mk`: 기본 "make" 옵션을 설정하는 파일. 이 파일을 바로 수정하지 말고, 대신 각 키맵 고유의 `rules.mk`를 사용할 것.
* `config.h`: 기본 컴파일 옵션을 설정하는 파일. 이 파일을 바로 수정하지 말고, 대신 각 키맵 고유의 `config.h`를 사용할 것.
* `info.json`: QMK Configurator에서 레이아웃을 설정하는데 사용된다. [Configurator Support](reference_configurator_support.md)에서 더 많은 정보를 볼것.
* `readme.md`: 키보드에 대한 짧은 요약.
* `<keyboardName>.h`: 키보드 스위치 매트릭스에 대해 키보드 레이아웃을 규정하는 파일.
* `<keyboardName>.c`: 키보드의 커스텀 코드가 적힌 파일.  

프로젝트 구조에 대해 더 많은 정보를 보려면 [QMK Keyboard Guidelines](hardware_keyboard_guidelines.md)에서 확인할것.

### 키맵 구조

모든 키맵 폴더에서, 다음 파일들을 찾을 수 있다. `keymap.c` 파일만 필수이며, 다른 파일들이 없으면 기본 옵션이 사용된다.

* `config.h`: 키맵을 설정하기 위한 옵션
* `keymap.c`: 키맵 코드, 필수적
* `rules.mk`: QMK가 이용가능한 특색들
* `readme.md`: 키맵에 대한 설명과 다른 사람을 위한 사용법, 그리고 특색들에 대한 설명. imgur과 같은 서비스에 이미지를 업로드할것.

# `config.h` 파일

`config.h` 파일이 있을 수 있는 3가지 위치들:

* 키보드 (`/keyboards/<keyboard>/config.h`)
* 유저 공간 (`/users/<user>/config.h`)
* 키맵 (`/keyboards/<keyboard>/keymaps/<keymap>/config.h`)

빌드 시스템은 위 순서대로 config 파일을 가져올 것이다. 이전의 `config.h`에 적힌 세팅을 덮어씌우려고 한다면, 수정하려는 설정 앞에 가장 먼저 표준 형식을 포함시켜야 한다

```
#pragma once
```

그리고 이전의 `config.h` 파일의 설정을 덮어씌우려고 한다면, `#undef`하고 다시 `#define`하여 설정해야 한다.

표준 형식 코드와 설정은 다음과 같다:

```
#pragma once

// overrides go here!
#undef MY_SETTING
#define MY_SETTING 4
```
