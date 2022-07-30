# 문서화 템플릿

이 페이지는 새로운 키맵과 키보드를 QMK에 제출할 때 사용할 템플릿에 대해 문서화합니다.

## 키맵 `readme.md` 템플릿 :id=keyboard-readmemd-template

대부분의 키맵은 레이아웃을 설명하는 이미지를 가지고 있습니다. 이미지 생성에는 [Keyboard Layout Editor](https://keyboard-layout-editor.com)를 이용할 수 있습니다. [Imgur](https://imgur.com) 등 타 호스팅 서비스에 이미지를 업로드하고, Pull Request에 이미지를 포함하지 마십시오.

이미지 아래 사람들이 이해할 수 있도록 짧은 설명을 작성하십시오.

```
![Clueboard 레이아웃 이미지](https://i.imgur.com/7Capi8W.png)

# 기본 Clueboard Layout

이것은 모든 Clueboard에 플래싱되는 기본 레이아웃입니다. 대부분은 직관적이고 쓰기 좋은 레이아웃입니다. 유일하게 일반적이지 않은 키는 좌상단 키 스위치로, 평상시에는 ESC 키로 동작하며, Ctrl / Alt / GUI 모디키와 결합하면 Grave(\`) 키로 동작합니다.
```

## 키보드 `readme.md` 템플릿

```
# 플랭크

![플랭크](https://i.imgur.com/q2M3uEU.jpg)

OLKB와 Massdrop이 판매하는 40%(12x4) 컴팩트 오쏘리니어 키보드 킷. [추가적인 정보는 qmk.fm에서 확인하세요](https://qmk.fm/planck/)

* 키보드 유지·보수: [Jack Humbert](https://github.com/jackhumbert)
* 하드웨어 지원: Planck PCB rev1, rev2, rev3, rev4, Teensy 2.0
* 하드웨어 재고: [OLKB.com](https://olkb.com), [Massdrop](https://www.massdrop.com/buy/planck-mechanical-keyboard?mode=guest_open)

이 키보드의 예시 생성하기 (빌드 환경 설정 이후):

    make planck/rev4:default

더 많은 정보는 [빌드 환경 설정하기](https://docs.qmk.fm/#/getting_started_build_tools)와 [make 안내](https://docs.qmk.fm/#/getting_started_make_guide)를 참조하세요. QMK를 처음 써보시나요? [완전 초보 가이드](https://docs.qmk.fm/#/newbs)로 시작하세요.
```
