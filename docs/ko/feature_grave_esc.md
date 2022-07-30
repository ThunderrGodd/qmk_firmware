# 그레이브 ESC

60% 키보드, 혹은 펑션열이 없는 다른 레이아웃을 사용한다면, 지정된 ESC 키가 없다는걸 파악하셨을 것입니다. 그레이브 ESC는 그레이브 키(<code>&#96;</code> 와 `~`)를 ESC와 공유하게 하는 특징입니다.

## 사용

키맵 안의 `KC_GRV`키(보통 '1'키 왼쪽에 있는)를 `QK_GESC`로 바꾸십시오. 대부분의 경우, 이 키는 눌리면 'KC_ESC'를 출력할 것입니다. 하지만, Shift 혹은 Gui를 누른 채로 누른다면, 그 키는 대신 'KC_GRV'를 출력할 것입니다.

## 당신의 OS가 보는 것

만약 Mary가 그녀의 키보드의 `QK_GESC`를 누르면, OS는 KC_ESC 글자를 볼 것입니다. 이제, 만약 Mary가 Shift를 누른 채로 `QK_GESC`를 누르면,`~`혹은 shift가 눌린 <code>&#96;</code>를 출력할 것입니다. 이제 그녀가 GUI/CMD/WIN을 누른 채로 한다면, 그냥 간단히 <code>&#96;</code> 문자를 출력할 것입니다.

## 키코드

|Key              |Aliases  |설명                                                     |
|-----------------|---------|------------------------------------------------------------------|
|`QK_GRAVE_ESCAPE`|`QK_GESC`|눌리면 ESC, Shift나 GUI가 눌린채로는 <code>&#96;</code>|

### 주의사항

macOS에서, 커맨드+<code>&#96;</code>는 기본적으로 "다음 창으로 포커스 이동"에 맵 되어 있기 때문에, <code>&#96;</code>를 출력하지 않습니다. 추가로, 터미널은 항상 이 단축키를 창들 사이의 순환으로 인식하며, 키보드 우선순위에서 바꿔도 마찬가지입니다.

## 설정

There are several possible key combinations this will break, among them Control+Shift+Escape on Windows and Command+Option+Escape on macOS. To work around this, you can `#define` these options in your `config.h`:

|Define                    |Description                              |
|--------------------------|-----------------------------------------|
|`GRAVE_ESC_ALT_OVERRIDE`  |Always send Escape if Alt is pressed     |
|`GRAVE_ESC_CTRL_OVERRIDE` |Always send Escape if Control is pressed |
|`GRAVE_ESC_GUI_OVERRIDE`  |Always send Escape if GUI is pressed     |
|`GRAVE_ESC_SHIFT_OVERRIDE`|Always send Escape if Shift is pressed   |
