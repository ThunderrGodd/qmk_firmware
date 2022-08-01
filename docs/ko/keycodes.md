# 키 코드 개론

[키맵](keymap.md) 을 정의할 때 각 키는 유효한 키 정의 값을 가져야 합니다. 이 페이지는 QMK에서 사용자가 사용할 수 있는 키 코드에 대응하는 심볼들을 문서화합니다.

이는 단순 참조용입니다. 각 키 그룹은 더 상세한 기능에 대해 문서화한 페이지로 연결됩니다.

## 기본 키 코드 :id=basic-keycodes

참조: [Basic Keycodes](keycodes_basic.md)

| Key                      | Aliases                         | Description                             | Windows       | macOS         | Linux<sup>1</sup> |
| ------------------------ | ------------------------------- | --------------------------------------- | ------------- | ------------- | ----------------- |
| `KC_NO`                  | `XXXXXXX`                       | 이 키를 무시 (NOOP)                          | *N/A*         | *N/A*         | *N/A*             |
| `KC_TRANSPARENT`         | `KC_TRNS`, `_______`            | Use the next lowest non-transparent key | *N/A*         | *N/A*         | *N/A*            |
| `KC_A`                   |                                 | `a` 및 `A`                               | ✔             | ✔             | ✔                 |
| `KC_B`                   |                                 | `b` 및 `B`                               | ✔             | ✔             | ✔                 |
| `KC_C`                   |                                 | `c` 및 `C`                               | ✔             | ✔             | ✔                 |
| `KC_D`                   |                                 | `d` 및 `D`                               | ✔             | ✔             | ✔                 |
| `KC_E`                   |                                 | `e` 및 `E`                               | ✔             | ✔             | ✔                 |
| `KC_F`                   |                                 | `f` 및 `F`                               | ✔             | ✔             | ✔                 |
| `KC_G`                   |                                 | `g` 및 `G`                               | ✔             | ✔             | ✔                 |
| `KC_H`                   |                                 | `h` 및 `H`                               | ✔             | ✔             | ✔                 |
| `KC_I`                   |                                 | `i` 및 `I`                               | ✔             | ✔             | ✔                 |
| `KC_J`                   |                                 | `j` 및 `J`                               | ✔             | ✔             | ✔                 |
| `KC_K`                   |                                 | `k` 및 `K`                               | ✔             | ✔             | ✔                 |
| `KC_L`                   |                                 | `l` 및 `L`                               | ✔             | ✔             | ✔                 |
| `KC_M`                   |                                 | `m` 및 `M`                               | ✔             | ✔             | ✔                 |
| `KC_N`                   |                                 | `n` 및 `N`                               | ✔             | ✔             | ✔                 |
| `KC_O`                   |                                 | `o` 및 `O`                               | ✔             | ✔             | ✔                 |
| `KC_P`                   |                                 | `p` 및 `P`                               | ✔             | ✔             | ✔                 |
| `KC_Q`                   |                                 | `q` 및 `Q`                               | ✔             | ✔             | ✔                 |
| `KC_R`                   |                                 | `r` 및 `R`                               | ✔             | ✔             | ✔                 |
| `KC_S`                   |                                 | `s` 및 `S`                               | ✔             | ✔             | ✔                 |
| `KC_T`                   |                                 | `t` 및 `T`                               | ✔             | ✔             | ✔                 |
| `KC_U`                   |                                 | `u` 및 `U`                               | ✔             | ✔             | ✔                 |
| `KC_V`                   |                                 | `v` 및 `V`                               | ✔             | ✔             | ✔                 |
| `KC_W`                   |                                 | `w` 및 `W`                               | ✔             | ✔             | ✔                 |
| `KC_X`                   |                                 | `x` 및 `X`                               | ✔             | ✔             | ✔                 |
| `KC_Y`                   |                                 | `y` 및 `Y`                               | ✔             | ✔             | ✔                 |
| `KC_Z`                   |                                 | `z` 및 `Z`                               | ✔             | ✔             | ✔                 |
| `KC_1`                   |                                 | `1` 및 `!`                               | ✔             | ✔             | ✔                 |
| `KC_2`                   |                                 | `2` 및 `@`                               | ✔             | ✔             | ✔                 |
| `KC_3`                   |                                 | `3` 및 `#`                               | ✔             | ✔             | ✔                 |
| `KC_4`                   |                                 | `4` 및 `$`                               | ✔             | ✔             | ✔                 |
| `KC_5`                   |                                 | `5` 및 `%`                               | ✔             | ✔             | ✔                 |
| `KC_6`                   |                                 | `6` 및 `^`                               | ✔             | ✔             | ✔                 |
| `KC_7`                   |                                 | `7` 및 `&`                               | ✔             | ✔             | ✔                 |
| `KC_8`                   |                                 | `8` 및 `*`                               | ✔             | ✔             | ✔                 |
| `KC_9`                   |                                 | `9` 및 `(`                               | ✔             | ✔             | ✔                 |
| `KC_0`                   |                                 | `0` 및 `)`                               | ✔             | ✔             | ✔                 |
| `KC_ENTER`               | `KC_ENT`                        | Return (엔터)                             | ✔             | ✔             | ✔                 |
| `KC_ESCAPE`              | `KC_ESC`                        | Esc                                     | ✔             | ✔             | ✔                 |
| `KC_BACKSPACE`           | `KC_BSPC`                       | Delete (백스페이스)                          | ✔             | ✔             | ✔                 |
| `KC_TAB`                 |                                 | 탭                                       | ✔             | ✔             | ✔                 |
| `KC_SPACE`               | `KC_SPC`                        | 스페이스                                    | ✔             | ✔             | ✔                 |
| `KC_MINUS`               | `KC_MINS`                       | `-` 및 `_`                               | ✔             | ✔             | ✔                 |
| `KC_EQUAL`               | `KC_EQL`                        | `=` 및 `+`                               | ✔             | ✔             | ✔                 |
| `KC_LEFT_BRACKET`        | `KC_LBRC`                       | `[` 및 `{`                               | ✔             | ✔             | ✔                 |
| `KC_RIGHT_BRACKET`       | `KC_RBRC`                       | `]` 및 `}`                               | ✔             | ✔             | ✔                 |
| `KC_BACKSLASH`           | `KC_BSLS`                       | `\` 및 `\|`                              | ✔             | ✔             | ✔                 |
| `KC_NONUS_HASH`          | `KC_NUHS`                       | Non-US `#` 및 `~`                        | ✔             | ✔             | ✔                 |
| `KC_SEMICOLON`           | `KC_SCLN`                       | `;` 및 `:`                               | ✔             | ✔             | ✔                 |
| `KC_QUOTE`               | `KC_QUOT`                       | `'` 및 `"`                               | ✔             | ✔             | ✔                 |
| `KC_GRAVE`               | `KC_GRV`                        | <code>&#96;</code> 및 `~`                | ✔             | ✔             | ✔                 |
| `KC_COMMA`               | `KC_COMM`                       | `,` 및 `<`                               | ✔             | ✔             | ✔                 |
| `KC_DOT`                 |                                 | `.` 및 `>`                               | ✔             | ✔             | ✔                 |
| `KC_SLASH`               | `KC_SLSH`                       | `/` 및 `?`                               | ✔             | ✔             | ✔                 |
| `KC_CAPS_LOCK`           | `KC_CAPS`                       | 캡스락                                     | ✔             | ✔             | ✔                 |
| `KC_F1`                  |                                 | F1                                      | ✔             | ✔             | ✔                 |
| `KC_F2`                  |                                 | F2                                      | ✔             | ✔             | ✔                 |
| `KC_F3`                  |                                 | F3                                      | ✔             | ✔             | ✔                 |
| `KC_F4`                  |                                 | F4                                      | ✔             | ✔             | ✔                 |
| `KC_F5`                  |                                 | F5                                      | ✔             | ✔             | ✔                 |
| `KC_F6`                  |                                 | F6                                      | ✔             | ✔             | ✔                 |
| `KC_F7`                  |                                 | F7                                      | ✔             | ✔             | ✔                 |
| `KC_F8`                  |                                 | F8                                      | ✔             | ✔             | ✔                 |
| `KC_F9`                  |                                 | F9                                      | ✔             | ✔             | ✔                 |
| `KC_F10`                 |                                 | F10                                     | ✔             | ✔             | ✔                 |
| `KC_F11`                 |                                 | F11                                     | ✔             | ✔             | ✔                 |
| `KC_F12`                 |                                 | F12                                     | ✔             | ✔             | ✔                 |
| `KC_PRINT_SCREEN`        | `KC_PSCR`                       | Print Screen                            | ✔             | ✔<sup>2</sup> | ✔                 |
| `KC_SCROLL_LOCK`         | `KC_SCRL`, `KC_BRMD`            | Scroll Lock, Brightness Down (macOS)    | ✔             | ✔<sup>2</sup> | ✔                 |
| `KC_PAUSE`               | `KC_PAUS`, `KC_BRK`, `KC_BRMU`  | Pause, Brightness Up (macOS)            | ✔             | ✔<sup>2</sup> | ✔                 |
| `KC_INSERT`              | `KC_INS`                        | Insert                                  | ✔             |               | ✔                 |
| `KC_HOME`                |                                 | Home                                    | ✔             | ✔             | ✔                 |
| `KC_PAGE_UP`             | `KC_PGUP`                       | Page Up                                 | ✔             | ✔             | ✔                 |
| `KC_DELETE`              | `KC_DEL`                        | Forward Delete                          | ✔             | ✔             | ✔                 |
| `KC_END`                 |                                 | End                                     | ✔             | ✔             | ✔                 |
| `KC_PAGE_DOWN`           | `KC_PGDN`                       | Page Down                               | ✔             | ✔             | ✔                 |
| `KC_RIGHT`               | `KC_RGHT`                       | 오른쪽 화살표                                 | ✔             | ✔             | ✔                 |
| `KC_LEFT`                |                                 | 왼쪽 화살표                                  | ✔             | ✔             | ✔                 |
| `KC_DOWN`                |                                 | 아래쪽 화살표                                 | ✔             | ✔             | ✔                 |
| `KC_UP`                  |                                 | 위쪽 화살표                                  | ✔             | ✔             | ✔                 |
| `KC_NUM_LOCK`            | `KC_NUM`                        | 키패드 NumLock 및 Clear                     | ✔             | ✔             | ✔                 |
| `KC_KP_SLASH`            | `KC_PSLS`                       | 키패드 `/`                                 | ✔             | ✔             | ✔                 |
| `KC_KP_ASTERISK`         | `KC_PAST`                       | 키패드 `*`                                 | ✔             | ✔             | ✔                 |
| `KC_KP_MINUS`            | `KC_PMNS`                       | 키패드 `-`                                 | ✔             | ✔             | ✔                 |
| `KC_KP_PLUS`             | `KC_PPLS`                       | 키패드 `+`                                 | ✔             | ✔             | ✔                 |
| `KC_KP_ENTER`            | `KC_PENT`                       | Keypad Enter                            | ✔             | ✔             | ✔                 |
| `KC_KP_1`                | `KC_P1`                         | 키패드 `1` 및 End                           | ✔             | ✔             | ✔                 |
| `KC_KP_2`                | `KC_P2`                         | 키패드 `2` 및 아래쪽 화살표 Arrow                 | ✔             | ✔             | ✔                 |
| `KC_KP_3`                | `KC_P3`                         | 키패드 `3` 및 Page Down                     | ✔             | ✔             | ✔                 |
| `KC_KP_4`                | `KC_P4`                         | 키패드 `4` 및 왼쪽 화살표                        | ✔             | ✔             | ✔                 |
| `KC_KP_5`                | `KC_P5`                         | 키패드 `5`                                 | ✔             | ✔             | ✔                 |
| `KC_KP_6`                | `KC_P6`                         | 키패드 `6` 및 오른쪽 화살표                       | ✔             | ✔             | ✔                 |
| `KC_KP_7`                | `KC_P7`                         | 키패드 `7` 및 Home                          | ✔             | ✔             | ✔                 |
| `KC_KP_8`                | `KC_P8`                         | 키패드 `8` 및 위쪽 화살표                        | ✔             | ✔             | ✔                 |
| `KC_KP_9`                | `KC_P9`                         | 키패드 `9` 및 Page Up                       | ✔             | ✔             | ✔                 |
| `KC_KP_0`                | `KC_P0`                         | 키패드 `0` 및 Insert                        | ✔             | ✔             | ✔                 |
| `KC_KP_DOT`              | `KC_PDOT`                       | 키패드 `.` 및 Delete                        | ✔             | ✔             | ✔                 |
| `KC_NONUS_BACKSLASH`     | `KC_NUBS`                       | Non-US `\` 및 `\|`                       | ✔             | ✔             | ✔                 |
| `KC_APPLICATION`         | `KC_APP`                        | 어플리케이션 (윈도우 컨텍스트 메뉴 키)                  | ✔             |               | ✔                 |
| `KC_KB_POWER`            |                                 | 시스템 전원                                  |               | ✔<sup>3</sup> | ✔                 |
| `KC_KP_EQUAL`            | `KC_PEQL`                       | 키패드 `=`                                 | ✔             | ✔             | ✔                 |
| `KC_F13`                 |                                 | F13                                     | ✔             | ✔             | ✔                 |
| `KC_F14`                 |                                 | F14                                     | ✔             | ✔             | ✔                 |
| `KC_F15`                 |                                 | F15                                     | ✔             | ✔             | ✔                 |
| `KC_F16`                 |                                 | F16                                     | ✔             | ✔             | ✔                 |
| `KC_F17`                 |                                 | F17                                     | ✔             | ✔             | ✔                 |
| `KC_F18`                 |                                 | F18                                     | ✔             | ✔             | ✔                 |
| `KC_F19`                 |                                 | F19                                     | ✔             | ✔             | ✔                 |
| `KC_F20`                 |                                 | F20                                     | ✔             |               | ✔                 |
| `KC_F21`                 |                                 | F21                                     | ✔             |               | ✔                 |
| `KC_F22`                 |                                 | F22                                     | ✔             |               | ✔                 |
| `KC_F23`                 |                                 | F23                                     | ✔             |               | ✔                 |
| `KC_F24`                 |                                 | F24                                     | ✔             |               | ✔                 |
| `KC_EXECUTE`             | `KC_EXEC`                       | Execute                                 |               |               | ✔                 |
| `KC_HELP`                |                                 | 도움말                                     |               |               | ✔                 |
| `KC_MENU`                |                                 | 메뉴                                      |               |               | ✔                 |
| `KC_SELECT`              | `KC_SLCT`                       | Select                                  |               |               | ✔                 |
| `KC_STOP`                |                                 | Stop                                    |               |               | ✔                 |
| `KC_AGAIN`               | `KC_AGIN`                       | Again                                   |               |               | ✔                 |
| `KC_UNDO`                |                                 | 실행취소                                    |               |               | ✔                 |
| `KC_CUT`                 |                                 | 잘라내기                                    |               |               | ✔                 |
| `KC_COPY`                |                                 | 복사                                      |               |               | ✔                 |
| `KC_PASTE`               | `KC_PSTE`                       | 붙여넣기                                    |               |               | ✔                 |
| `KC_FIND`                |                                 | 검색                                      |               |               | ✔                 |
| `KC_KB_MUTE`             |                                 | 음소거                                     |               | ✔             | ✔                 |
| `KC_KB_VOLUME_UP`        |                                 | 음량 키우기                                  |               | ✔             | ✔                 |
| `KC_KB_VOLUME_DOWN`      |                                 | 음량 줄이기                                  |               | ✔             | ✔                 |
| `KC_LOCKING_CAPS_LOCK`   | `KC_LCAP`                       | 캡스락 잠금                                  | ✔             | ✔             |                   |
| `KC_LOCKING_NUM_LOCK`    | `KC_LNUM`                       | Num Lock 잠금                             | ✔             | ✔             |                   |
| `KC_LOCKING_SCROLL_LOCK` | `KC_LSCR`                       | Scroll Lock 잠금                          | ✔             | ✔             |                   |
| `KC_KP_COMMA`            | `KC_PCMM`                       | 키패드 `,`                                 |               |               | ✔                 |
| `KC_KP_EQUAL_AS400`      |                                 | AS/400 키보드에서 키패드 `=`                    |               |               |                   |
| `KC_INTERNATIONAL_1`     | `KC_INT1`                       | International 1                         | ✔             |               | ✔                 |
| `KC_INTERNATIONAL_2`     | `KC_INT2`                       | International 2                         | ✔             |               | ✔                 |
| `KC_INTERNATIONAL_3`     | `KC_INT3`                       | International 3                         | ✔             |               | ✔                 |
| `KC_INTERNATIONAL_4`     | `KC_INT4`                       | International 4                         | ✔             |               | ✔                 |
| `KC_INTERNATIONAL_5`     | `KC_INT5`                       | International 5                         | ✔             |               | ✔                 |
| `KC_INTERNATIONAL_6`     | `KC_INT6`                       | International 6                         |               |               | ✔                 |
| `KC_INTERNATIONAL_7`     | `KC_INT7`                       | International 7                         |               |               |                   |
| `KC_INTERNATIONAL_8`     | `KC_INT8`                       | International 8                         |               |               |                   |
| `KC_INTERNATIONAL_9`     | `KC_INT9`                       | International 9                         |               |               |                   |
| `KC_LANGUAGE_1`          | `KC_LNG1`                       | Language 1                              |               |               | ✔                 |
| `KC_LANGUAGE_2`          | `KC_LNG2`                       | Language 2                              |               |               | ✔                 |
| `KC_LANGUAGE_3`          | `KC_LNG3`                       | Language 3                              |               |               | ✔                 |
| `KC_LANGUAGE_4`          | `KC_LNG4`                       | Language 4                              |               |               | ✔                 |
| `KC_LANGUAGE_5`          | `KC_LNG5`                       | Language 5                              |               |               | ✔                 |
| `KC_LANGUAGE_6`          | `KC_LNG6`                       | Language 6                              |               |               |                   |
| `KC_LANGUAGE_7`          | `KC_LNG7`                       | Language 7                              |               |               |                   |
| `KC_LANGUAGE_8`          | `KC_LNG8`                       | Language 8                              |               |               |                   |
| `KC_LANGUAGE_9`          | `KC_LNG9`                       | Language 9                              |               |               |                   |
| `KC_ALTERNATE_ERASE`     | `KC_ERAS`                       | Alternate Erase                         |               |               |                   |
| `KC_SYSTEM_REQUEST`      | `KC_SYRQ`                       | SysReq/Attention                        |               |               |                   |
| `KC_CANCEL`              | `KC_CNCL`                       | 취소                                      |               |               |                   |
| `KC_CLEAR`               | `KC_CLR`                        | 비우기                                     |               |               | ✔                 |
| `KC_PRIOR`               | `KC_PRIR`                       | Prior                                   |               |               |                   |
| `KC_RETURN`              | `KC_RETN`                       | 엔터                                      |               |               |                   |
| `KC_SEPARATOR`           | `KC_SEPR`                       | Separator                               |               |               |                   |
| `KC_OUT`                 |                                 | Out                                     |               |               |                   |
| `KC_OPER`                |                                 | Oper                                    |               |               |                   |
| `KC_CLEAR_AGAIN`         | `KC_CLAG`                       | Clear/Again                             |               |               |                   |
| `KC_CRSEL`               | `KC_CRSL`                       | CrSel/Props                             |               |               |                   |
| `KC_EXSEL`               | `KC_EXSL`                       | ExSel                                   |               |               |                   |
| `KC_LEFT_CTRL`           | `KC_LCTL`                       | 왼쪽 컨트롤                                  | ✔             | ✔             | ✔                 |
| `KC_LEFT_SHIFT`          | `KC_LSFT`                       | 왼쪽 시프트                                  | ✔             | ✔             | ✔                 |
| `KC_LEFT_ALT`            | `KC_LALT`, `KC_LOPT`            | 왼쪽 알트 (옵션)                              | ✔             | ✔             | ✔                 |
| `KC_LEFT_GUI`            | `KC_LGUI`, `KC_LCMD`, `KC_LWIN` | 왼쪽 GUI (윈도우키/커맨드키/메타 키)                 | ✔             | ✔             | ✔                 |
| `KC_RIGHT_CTRL`          | `KC_RCTL`                       | 오른쪽 컨트롤                                 | ✔             | ✔             | ✔                 |
| `KC_RIGHT_SHIFT`         | `KC_RSFT`                       | 오른쪽 시프트                                 | ✔             | ✔             | ✔                 |
| `KC_RIGHT_ALT`           | `KC_RALT`, `KC_ROPT`, `KC_ALGR` | 오른쪽 알트 (옵션/AltGr)                       | ✔             | ✔             | ✔                 |
| `KC_RIGHT_GUI`           | `KC_RGUI`, `KC_RCMD`, `KC_RWIN` | 오른쪽 GUI (윈도우키/커맨드키/메타키)                 | ✔             | ✔             | ✔                 |
| `KC_SYSTEM_POWER`        | `KC_PWR`                        | 시스템 전원 종료                               | ✔             | ✔<sup>3</sup> | ✔                 |
| `KC_SYSTEM_SLEEP`        | `KC_SLEP`                       | 시스템 잠자기                                 | ✔             | ✔<sup>3</sup> | ✔                 |
| `KC_SYSTEM_WAKE`         | `KC_WAKE`                       | 시스템 깨우기                                 |               | ✔<sup>3</sup> | ✔                 |
| `KC_AUDIO_MUTE`          | `KC_MUTE`                       | 음소거                                     | ✔             | ✔             | ✔                 |
| `KC_AUDIO_VOL_UP`        | `KC_VOLU`                       | 음량 키우기                                  | ✔             | ✔<sup>4</sup> | ✔                 |
| `KC_AUDIO_VOL_DOWN`      | `KC_VOLD`                       | 음량 줄이기                                  | ✔             | ✔<sup>4</sup> | ✔                 |
| `KC_MEDIA_NEXT_TRACK`    | `KC_MNXT`                       | 다음 트랙                                   | ✔             | ✔<sup>5</sup> | ✔                 |
| `KC_MEDIA_PREV_TRACK`    | `KC_MPRV`                       | 이전 트랙                                   | ✔             | ✔<sup>5</sup> | ✔                 |
| `KC_MEDIA_STOP`          | `KC_MSTP`                       | 트랙 중지                                   | ✔             |               | ✔                 |
| `KC_MEDIA_PLAY_PAUSE`    | `KC_MPLY`                       | 트랙 일시중지                                 | ✔             | ✔             | ✔                 |
| `KC_MEDIA_SELECT`        | `KC_MSEL`                       | 미디어 플레이어 열기                             | ✔             |               | ✔                 |
| `KC_MEDIA_EJECT`         | `KC_EJCT`                       | 꺼내기                                     |               | ✔             | ✔                 |
| `KC_MAIL`                |                                 | 메일 열기                                   | ✔             |               | ✔                 |
| `KC_CALCULATOR`          | `KC_CALC`                       | 계산기 열기                                  | ✔             |               | ✔                 |
| `KC_MY_COMPUTER`         | `KC_MYCM`                       | 내 컴퓨터 열기                                | ✔             |               | ✔                 |
| `KC_WWW_SEARCH`          | `KC_WSCH`                       | 브라우저 검색                                 | ✔             |               | ✔                 |
| `KC_WWW_HOME`            | `KC_WHOM`                       | 브라우저 홈                                  | ✔             |               | ✔                 |
| `KC_WWW_BACK`            | `KC_WBAK`                       | 브라우저 뒤로가기                               | ✔             |               | ✔                 |
| `KC_WWW_FORWARD`         | `KC_WFWD`                       | 브라우저 앞으로 가기                             | ✔             |               | ✔                 |
| `KC_WWW_STOP`            | `KC_WSTP`                       | 브라우저 멈추기                                | ✔             |               | ✔                 |
| `KC_WWW_REFRESH`         | `KC_WREF`                       | 브라우저 새로고침                               | ✔             |               | ✔                 |
| `KC_WWW_FAVORITES`       | `KC_WFAV`                       | 브라우저 즐겨찾기                               | ✔             |               | ✔                 |
| `KC_MEDIA_FAST_FORWARD`  | `KC_MFFD`                       | 다음 트랙                                   | ✔             | ✔<sup>5</sup> | ✔                 |
| `KC_MEDIA_REWIND`        | `KC_MRWD`                       | 이전 트랙                                   | ✔<sup>6</sup> | ✔<sup>5</sup> | ✔                 |
| `KC_BRIGHTNESS_UP`       | `KC_BRIU`                       | 밝기 키우기                                  | ✔             | ✔             | ✔                 |
| `KC_BRIGHTNESS_DOWN`     | `KC_BRID`                       | 밝기 줄이기                                  | ✔             | ✔             | ✔                 |

<sup>1. 리눅스 커널 HID 드라이버는[거의 모든 키코드](https://github.com/torvalds/linux/blob/master/drivers/hid/hid-input.c)를 인식하지만, 기본 바인딩은 데스크탑 환경(Desktop Environment)/윈도우 매니저(Window Manager)에 따라 다를 수 있습니다.</sup><br/>
<sup>2. F13-F15 로 취급합니다.</sup><br/>
<sup>3. 최소 3초 가량 누르고 있어야 하며, 프롬프트를 대신 엽니다.</sup><br/>
<sup>4. 시프트 + 옵션 키를 누르고 있으면 더 세밀한 조작이 가능합니다.</sup><br/>
<sup>5. 짧게 누르면 iTunes에서 전체 트랙을 건너뒤고, 누르고 있으면 현재 트랙 내에서 빨리감기/뒤로감기됩니다.</sup><br/>
<sup>6. 윈도우 미디어 플레이어는 뒤로감기 키를 인식하지 않지만, 둘 다 VLC에서 재생 속도를 조정합니다.</sup>

## 퀀텀 키 코드 :id=quantum-keycodes

참조: [퀀텀 키 코드](quantum_keycodes.md#qmk-keycodes)

| Key               | Aliases   | Description                                                                                |
| ----------------- | --------- | ------------------------------------------------------------------------------------------ |
| `QK_BOOTLOADER`   | `QK_BOOT` | 플래싱을 위해 키보드를 부트로더 모드로 진입시킵니다.                                                              |
| `QK_DEBUG_TOGGLE` | `DB_TOGG` | 디버그 모드를 켜거나 끕니다.                                                                           |
| `QK_CLEAR_EEPROM` | `EE_CLR`  | 키보드의 EEPROM(영구 메모리)를 재기동합니다.                                                               |
| `QK_MAKE`         |           | `qmk compile -kb (keyboard) -km (keymap)` 명령을 전송하거나, 시프트가 눌린 상태에서는 `qmk flash` 명령어를 전송합니다. |
| `QK_REBOOT`       | `QK_RBT`  | 키보드를 재설정합니다. 부트로더를 로드하지 않습니다.                                                              |

## 오디오 키 :id=audio-keys

참조: [오디오](feature_audio.md)

| Key             | Aliases   | Description          |
| --------------- | --------- | -------------------- |
| `AU_ON`         |           | 오디오 기능을 켭니다.         |
| `AU_OFF`        |           | 오디오 기능을 끕니다.         |
| `AU_TOG`        |           | 오디오 상태를 켜거나 끕니다.     |
| `CLICKY_TOGGLE` | `CK_TOGG` | 타건음 모드를 켜거나 끕니다.     |
| `CLICKY_UP`     | `CK_UP`   | 타건음 톤을 높입니다.         |
| `CLICKY_DOWN`   | `CK_DOWN` | 타건음 톤을 낮춥니다.         |
| `CLICKY_RESET`  | `CK_RST`  | 타건음 톤을 기본값으로 재설정합니다. |
| `MU_ON`         |           | 음악 모드를 켭니다.          |
| `MU_OFF`        |           | 음악 모드를 끕니다           |
| `MU_TOG`        |           | 음악 모드를 켜거나 끕니다.      |
| `MU_MOD`        |           | 음악 모드를 순차적으로 변경합니다.  |

## 백라이팅 :id=backlighting

참조: [백라이팅](feature_backlight.md)

| Key       | Description           |
| --------- | --------------------- |
| `BL_TOGG` | 백라이트를 켜거나 끕니다.        |
| `BL_STEP` | 백라이트 밝기를 순차적으로 변경합니다. |
| `BL_ON`   | 백라이트를 최대 밝기로 설정합니다.   |
| `BL_OFF`  | 백라이트를 끕니다.            |
| `BL_INC`  | 백라이트 밝기를 높입니다.        |
| `BL_DEC`  | 백라이트 밝기를 낮춥니다.        |
| `BL_BRTG` | 백라이트 숨쉬기 모드를 켜고 끕니다.  |

## 블루투스 :id=bluetooth

참조: [블루투스](feature_bluetooth.md)

| Key        | Description            |
| ---------- | ---------------------- |
| `OUT_AUTO` | USB 또는 Bluetooth 자동 설정 |
| `OUT_USB`  | USB 전용                 |
| `OUT_BT`   | Bluetooth 전용           |

## Caps Word :id=caps-word

See also: [Caps Word](feature_caps_word.md)

| Key         | Aliases   | Description      |
| ----------- | --------- | ---------------- |
| `CAPS_WORD` | `CAPSWRD` | 대문자 모드를 켜거나 끕니다. |

## 동적 매크로 :id=dynamic-macros

참조: [동적 매크로](feature_dynamic_macros.md)

| Key               | Aliases   | Description       |
| ----------------- | --------- | ----------------- |
| `DYN_REC_START1`  | `DM_REC1` | 매크로 1에 저장합니다.     |
| `DYN_REC_START2`  | `DM_REC2` | 매크로 2에 저장합니다.     |
| `DYN_MACRO_PLAY1` | `DM_PLY1` | 매크로 1을 재생합니다.     |
| `DYN_MACRO_PLAY2` | `DM_PLY2` | 매크로 2를 재생합니다.     |
| `DYN_REC_STOP`    | `DM_RSTP` | 저장 중인 매크로를 종료합니다. |

## 백틱 Esc :id=grave-escape

참조: [백틱 Esc](feature_grave_esc.md)

| Key               | Aliases   | Description                                                  |
| ----------------- | --------- | ------------------------------------------------------------ |
| `QK_GRAVE_ESCAPE` | `QK_GESC` | Esc 키로 동작하다가, 시프트나 GUI 키가 눌렸을 경우 <code>&#96;</code> 를 입력합니다. |

## 키 잠금 :id=key-lock

참조: [키 잠금](feature_key_lock.md)

| Key       | Description                 |
| --------- | --------------------------- |
| `KC_LOCK` | 새로운 키가 눌릴 때까지 다음 입력키를 반복 입력 |

## 레이어 변경 :id=layer-switching

참조: [레이어 변경](feature_layers.md#switching-and-toggling-layers)

| Key              | Description                                                                                                                   |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `DF(layer)`      | 기본 레이어로 설정                                                                                                                    |
| `MO(layer)`      | 임시적으로 `layer` 레이어를 활성 (도착 레이어에 키 위치에 `KC_TRNS` 키가 필요)                                                                         |
| `OSL(layer)`     | 키가 입력될 때까지 임시적으로 `layer` 레이어를 활성. 세부 사항은 [One Shot Keys](one_shot_keys.md) 문서를 참조.                                            |
| `LM(layer, mod)` | 임시적으로 `layer` 레이어를 활성하고(이 부분은 MO 키 코드와 동일), `mod` 모디키를 같이 활성. 모디키는 [여기](mod_tap.md)에서 확인할 수 있습니다. 예시: `LM(LAYER_1, MOD_LALT)` |
| `LT(layer, kc)`  | 길게 누르고 있을 때 `layer` 레이어를 활성, 짧게 누르면 `kc` 키를 입력                                                                                |
| `TG(layer)`      | `layer` 레이어를 켜거나 끔                                                                                                            |
| `TO(layer)`      | Turns on `layer` 레이어를 활성화하고 기본 레이어를 제외한 나머지 레이어를 모두 끔.                                                                        |
| `TT(layer)`      | 평상시에는 MO 키와 동일하게 동작하나 수차례 반복적으로 눌릴 경우 `layer` 레이어를 활성                                                                         |

## 리더 키 :id=leader-key

참조: [리더 키](feature_leader_key.md)

| Key       | Description     |
| --------- | --------------- |
| `KC_LEAD` | 리더키 시퀀스를 시작합니다. |

## 매직 키 코드 :id=magic-keycodes

참조: [매직 키 코드](keycodes_magic.md)

| Key                                | Aliases   | Description                                |
| ---------------------------------- | --------- | ------------------------------------------ |
| `MAGIC_SWAP_CONTROL_CAPSLOCK`      | `CL_SWAP` | 캡스락과 왼쪽 컨트롤 위치를 바꿉니다.                      |
| `MAGIC_UNSWAP_CONTROL_CAPSLOCK`    | `CL_NORM` | 캡스락과 왼쪽 컨트롤 위치 교환을 해제합니다.                  |
| `MAGIC_TOGGLE_CONTROL_CAPSLOCK`    | `CL_TOGG` | 캡스락과 왼쪽 컨트롤 위치 교환 상태를 전환합니다.               |
| `MAGIC_CAPSLOCK_TO_CONTROL`        | `CL_CTRL` | 캡스락을 컨트롤로 취급합니다.                           |
| `MAGIC_UNCAPSLOCK_TO_CONTROL`      | `CL_CAPS` | 캡스락을 컨트롤로 취급하지 않습니다.                       |
| `MAGIC_SWAP_LCTL_LGUI`             | `LCG_SWP` | 왼쪽 컨트롤과 GUI의 위치를 서로 바꿉니다.                  |
| `MAGIC_UNSWAP_LCTL_LGUI`           | `LCG_NRM` | 왼쪽 컨트롤과 GUI 위치 교환을 해제합니다.                  |
| `MAGIC_SWAP_RCTL_RGUI`             | `RCG_SWP` | 오른쪽 컨트롤과 GUI 위치를 서로 바꿉니다.                  |
| `MAGIC_UNSWAP_RCTL_RGUI`           | `RCG_NRM` | 오른쪽 컨트롤과 GUI 위치 교환을 해제합니다.                 |
| `MAGIC_SWAP_CTL_GUI`               | `CG_SWAP` | 양쪽 컨트롤과 GUI를 서로 바꿉니다.                      |
| `MAGIC_UNSWAP_CTL_GUI`             | `CG_NORM` | 양쪽 컨트롤과 GUI 위치 교환을 해제합니다.                  |
| `MAGIC_TOGGLE_CTL_GUI`             | `CG_TOGG` | 양쪽에서 컨트롤과 GUI 위치 교환 상태를 전환합니다.             |
| `MAGIC_SWAP_LALT_LGUI`             | `LAG_SWP` | 왼쪽 Alt와 GUI 위치를 서로 바꿉니다.                   |
| `MAGIC_UNSWAP_LALT_LGUI`           | `LAG_NRM` | 왼쪽 Alt와 GUI 위치 교환을 해제합니다.                  |
| `MAGIC_SWAP_RALT_RGUI`             | `RAG_SWP` | 오른쪽 Alt와 GUI 위치를 서로 바꿉니다.                  |
| `MAGIC_UNSWAP_RALT_RGUI`           | `RAG_NRM` | 오른쪽 Alt와 GUI 위치 교환을 해제합니다.                 |
| `MAGIC_SWAP_ALT_GUI`               | `AG_SWAP` | 양쪽 Alt와 GUI 위치를 서로 바꿉니다.                   |
| `MAGIC_UNSWAP_ALT_GUI`             | `AG_NORM` | 양쪽 Alt와 GUI 위치 교환을 해제합니다.                  |
| `MAGIC_TOGGLE_ALT_GUI`             | `AG_TOGG` | 양쪽 Alt와 GUI 키의 위치 교환 상태를 전환합니다.            |
| `MAGIC_NO_GUI`                     | `GUI_OFF` | GUI 키를 비활성화합니다.                            |
| `MAGIC_UNNO_GUI`                   | `GUI_ON`  | GUI 키를 활성화합니다.                             |
| `MAGIC_TOGGLE_GUI`                 | `GUI_TOG` | GUI 키의 활성화 상태를 전환합니다.                      |
| `MAGIC_SWAP_GRAVE_ESC`             | `GE_SWAP` | <code>&#96;</code>와 Esc 키의 위치를 서로 바꿉니다.    |
| `MAGIC_UNSWAP_GRAVE_ESC`           | `GE_NORM` | <code>&#96;</code>와 Esc 키의 위치 교환을 해제합니다.   |
| `MAGIC_SWAP_BACKSLASH_BACKSPACE`   | `BS_SWAP` | `\` 키와 백스페이스 위치를 서로 바꿉니다.                  |
| `MAGIC_UNSWAP_BACKSLASH_BACKSPACE` | `BS_NORM` | `\` 키와 백스페이스 위치 교환을 해제합니다.                 |
| `MAGIC_HOST_NKRO`                  | `NK_ON`   | N-key 롤오버를 활성화합니다.                         |
| `MAGIC_UNHOST_NKRO`                | `NK_OFF`  | N-key 롤오버를 비활성화합니다.                        |
| `MAGIC_TOGGLE_NKRO`                | `NK_TOGG` | N-key 롤오버 활성화 상태를 전환합니다.                   |
| `MAGIC_EE_HANDS_LEFT`              | `EH_LEFT` | ( `EE_HANDS`에 대해) 스플릿 보드의 왼쪽을 마스터로 설정합니다.  |
| `MAGIC_EE_HANDS_RIGHT`             | `EH_RGHT` | ( `EE_HANDS`에 대해) 스플릿 보드의 오른쪽을 마스터로 설정합니다. |

## MIDI :id=midi

See also: [MIDI](feature_midi.md)

| Key          | Aliases   | Description            |
| ------------ | --------- | ---------------------- |
| `MI_ON`      |           | MIDI 기능을 켭니다.          |
| `MI_OFF`     |           | MIDI 기능을 끕니다.          |
| `MI_TOG`     |           | MIDI 기능 활성화 상태를 전환합니다. |
| `MI_C`       |           | 0 옥타브 C                |
| `MI_Cs`      | `MI_Db`   | 0 옥타브 C♯/D♭            |
| `MI_D`       |           | 0 옥타브 D                |
| `MI_Ds`      | `MI_Eb`   | 0 옥타브 D♯/E♭            |
| `MI_E`       |           | 0 옥타브 E                |
| `MI_F`       |           | 0 옥타브 F                |
| `MI_Fs`      | `MI_Gb`   | 0 옥타브 F♯/G♭            |
| `MI_G`       |           | 0 옥타브 G                |
| `MI_Gs`      | `MI_Gs`   | 0 옥타브 G♯/A♭            |
| `MI_A`       |           | 0 옥타브 A                |
| `MI_As`      | `MI_Bb`   | 0 옥타브 A♯/B♭            |
| `MI_B`       |           | 0 옥타브 B                |
| `MI_C_1`     |           | 1 옥타브 C                |
| `MI_Cs_1`    | `MI_Db_1` | 1 옥타브 C♯/D♭            |
| `MI_D_1`     |           | 1 옥타브 D                |
| `MI_Ds_1`    | `MI_Eb_1` | 1 옥타브 D♯/E♭            |
| `MI_E_1`     |           | 1 옥타브 E                |
| `MI_F_1`     |           | 1 옥타브 F                |
| `MI_Fs_1`    | `MI_Gb_1` | 1 옥타브 F♯/G♭            |
| `MI_G_1`     |           | 1 옥타브 G                |
| `MI_Gs_1`    | `MI_Ab_1` | 1 옥타브 G♯/A♭            |
| `MI_A_1`     |           | 1 옥타브 A                |
| `MI_As_1`    | `MI_Bb_1` | 1 옥타브 A♯/B♭            |
| `MI_B_1`     |           | 1 옥타브 B                |
| `MI_C_2`     |           | 2 옥타브 C                |
| `MI_Cs_2`    | `MI_Db_2` | 2 옥타브 C♯/D♭            |
| `MI_D_2`     |           | 2 옥타브 D                |
| `MI_Ds_2`    | `MI_Eb_2` | 2 옥타브 D♯/E♭            |
| `MI_E_2`     |           | 2 옥타브 E                |
| `MI_F_2`     |           | 2 옥타브 F                |
| `MI_Fs_2`    | `MI_Gb_2` | 2 옥타브 F♯/G♭            |
| `MI_G_2`     |           | 2 옥타브 G                |
| `MI_Gs_2`    | `MI_Ab_2` | 2 옥타브 G♯/A♭            |
| `MI_A_2`     |           | 2 옥타브 A                |
| `MI_As_2`    | `MI_Bb_2` | 2 옥타브 A♯/B♭            |
| `MI_B_2`     |           | 2 옥타브 B                |
| `MI_C_3`     |           | 3 옥타브 C                |
| `MI_Cs_3`    | `MI_Db_3` | 3 옥타브 C♯/D♭            |
| `MI_D_3`     |           | 3 옥타브 D                |
| `MI_Ds_3`    | `MI_Eb_3` | 3 옥타브 D♯/E♭            |
| `MI_E_3`     |           | 3 옥타브 E                |
| `MI_F_3`     |           | 3 옥타브 F                |
| `MI_Fs_3`    | `MI_Gb_3` | 3 옥타브 F♯/G♭            |
| `MI_G_3`     |           | 3 옥타브 G                |
| `MI_Gs_3`    | `MI_Ab_3` | 3 옥타브 G♯/A♭            |
| `MI_A_3`     |           | 3 옥타브 A                |
| `MI_As_3`    | `MI_Bb_3` | 3 옥타브 A♯/B♭            |
| `MI_B_3`     |           | 3 옥타브 B                |
| `MI_C_4`     |           | 4 옥타브 C                |
| `MI_Cs_4`    | `MI_Db_4` | 4 옥타브 C♯/D♭            |
| `MI_D_4`     |           | 4 옥타브 D                |
| `MI_Ds_4`    | `MI_Eb_4` | 4 옥타브 D♯/E♭            |
| `MI_E_4`     |           | 4 옥타브 E                |
| `MI_F_4`     |           | 4 옥타브 F                |
| `MI_Fs_4`    | `MI_Gb_4` | 4 옥타브 F♯/G♭            |
| `MI_G_4`     |           | 4 옥타브 G                |
| `MI_Gs_4`    | `MI_Ab_4` | 4 옥타브 G♯/A♭            |
| `MI_A_4`     |           | 4 옥타브 A                |
| `MI_As_4`    | `MI_Bb_4` | 4 옥타브 A♯/B♭            |
| `MI_B_4`     |           | 4 옥타브 B                |
| `MI_C_5`     |           | 5 옥타브 C                |
| `MI_Cs_5`    | `MI_Db_5` | 5 옥타브 C♯/D♭            |
| `MI_D_5`     |           | 5 옥타브 D                |
| `MI_Ds_5`    | `MI_Eb_5` | 5 옥타브 D♯/E♭            |
| `MI_E_5`     |           | 5 옥타브 E                |
| `MI_F_5`     |           | 5 옥타브 F                |
| `MI_Fs_5`    | `MI_Gb_5` | 5 옥타브 F♯/G♭            |
| `MI_G_5`     |           | 5 옥타브 G                |
| `MI_Gs_5`    | `MI_Ab_5` | 5 옥타브 G♯/A♭            |
| `MI_A_5`     |           | 5 옥타브 A                |
| `MI_As_5`    | `MI_Bb_5` | 5 옥타브 A♯/B♭            |
| `MI_B_5`     |           | 5 옥타브 B                |
| `MI_OCT_N2`  |           | 옥타브를 -2로 설정            |
| `MI_OCT_N1`  |           | 옥타브를 -1로 설정            |
| `MI_OCT_0`   |           | 옥타브를 0으로 설정            |
| `MI_OCT_1`   |           | 옥타브를 1로 설정             |
| `MI_OCT_2`   |           | 옥타브를 2로 설정             |
| `MI_OCT_3`   |           | 옥타브를 3로 설정             |
| `MI_OCT_4`   |           | 옥타브를 4로 설정             |
| `MI_OCT_5`   |           | 옥타브를 5로 설정             |
| `MI_OCT_6`   |           | 옥타브를 6로 설정             |
| `MI_OCT_7`   |           | 옥타브를 7로 설정             |
| `MI_OCTD`    |           | 한 옥타브 내림               |
| `MI_OCTU`    |           | 한 옥타브 올림               |
| `MI_TRNS_N6` |           | 6반음 내림                 |
| `MI_TRNS_N5` |           | 5반음 내림                 |
| `MI_TRNS_N4` |           | 4반음 내림                 |
| `MI_TRNS_N3` |           | 3반음 내림                 |
| `MI_TRNS_N2` |           | 2반음 내림                 |
| `MI_TRNS_N1` |           | 1반음 내림                 |
| `MI_TRNS_0`  |           | 음정 원위치                 |
| `MI_TRNS_1`  |           | 1반음 올림                 |
| `MI_TRNS_2`  |           | 2반음 올림                 |
| `MI_TRNS_3`  |           | 3반음 올림                 |
| `MI_TRNS_4`  |           | 4반음 올림                 |
| `MI_TRNS_5`  |           | 5반음 올림                 |
| `MI_TRNS_6`  |           | 6반음 올림                 |
| `MI_TRNSD`   |           | 반음 내림                  |
| `MI_TRNSU`   |           | 반음 올림                  |
| `MI_VEL_0`   |           | 빠르기를 0으로 설정            |
| `MI_VEL_1`   |           | 빠르기를 12로 설정            |
| `MI_VEL_2`   |           | 빠르기를 25로 설정            |
| `MI_VEL_3`   |           | 빠르기를 38로 설정            |
| `MI_VEL_4`   |           | 빠르기를 51로 설정            |
| `MI_VEL_5`   |           | 빠르기를 64로 설정            |
| `MI_VEL_6`   |           | 빠르기를 76으로 설정           |
| `MI_VEL_7`   |           | 빠르기를 89로 설정            |
| `MI_VEL_8`   |           | 빠르기를 102로 설정           |
| `MI_VEL_9`   |           | 빠르기를 114로 설정           |
| `MI_VEL_10`  |           | 빠르기를 127로 설정           |
| `MI_VELD`    |           | 빠르기 낮추기                |
| `MI_VELU`    |           | 빠르기 높이기                |
| `MI_CH1`     |           | 채널을 1로 설정              |
| `MI_CH2`     |           | 채널을 2로 설정              |
| `MI_CH3`     |           | 채널을 3으로 설정             |
| `MI_CH4`     |           | 채널을 4로 설정              |
| `MI_CH5`     |           | 채널을 5로 설정              |
| `MI_CH6`     |           | 채널을 6으로 설정             |
| `MI_CH7`     |           | 채널을 7로 설정              |
| `MI_CH8`     |           | 채널을 8로 설정              |
| `MI_CH9`     |           | 채널을 9로 설정              |
| `MI_CH10`    |           | 채널을 10으로 설정            |
| `MI_CH11`    |           | 채널을 11로 설정             |
| `MI_CH12`    |           | 채널을 12로 설정             |
| `MI_CH13`    |           | 채널을 13으로 설정            |
| `MI_CH14`    |           | 채널을 14로 설정             |
| `MI_CH15`    |           | 채널을 15로 설정             |
| `MI_CH16`    |           | 채널을 16으로 설정            |
| `MI_CHD`     |           | 채널 감소                  |
| `MI_CHU`     |           | 채널 증가                  |
| `MI_ALLOFF`  |           | 모든 노트 중지               |
| `MI_SUS`     |           | 계속                     |
| `MI_PORT`    |           | 포르타멘토portamento        |
| `MI_SOST`    |           | 소스테누토Sostenuto         |
| `MI_SOFT`    |           | 부드러운 페달                |
| `MI_LEG`     |           | 레가토                    |
| `MI_MOD`     |           | 비브라토                   |
| `MI_MODSD`   |           | 비브라토 속도 낮춤             |
| `MI_MODSU`   |           | 비브라토 속도 높임             |
| `MI_BENDD`   |           | 음높이 꺾어내림               |
| `MI_BENDU`   |           | 음높이 꺾어올림               |

## 마우스 키 :id=mouse-keys

참조: [Mouse Keys](feature_mouse_keys.md)

| Key              | Aliases   | Description       |
| ---------------- | --------- | ----------------- |
| `KC_MS_UP`       | `KC_MS_U` | 마우스 커서 위로 이동      |
| `KC_MS_DOWN`     | `KC_MS_D` | 마우스 커서 아래로 이동     |
| `KC_MS_LEFT`     | `KC_MS_L` | 마우스 커서 왼쪽으로 이동    |
| `KC_MS_RIGHT`    | `KC_MS_R` | 마우스 커서 오른쪽으로 이동   |
| `KC_MS_BTN1`     | `KC_BTN1` | 마우스 버튼 1 (왼쪽 클릭)  |
| `KC_MS_BTN2`     | `KC_BTN2` | 마우스 버튼 2 (오른쪽 클릭) |
| `KC_MS_BTN3`     | `KC_BTN3` | 마우스 버튼 3          |
| `KC_MS_BTN4`     | `KC_BTN4` | 마우스 버튼 4          |
| `KC_MS_BTN5`     | `KC_BTN5` | 마우스 버튼 5          |
| `KC_MS_WH_UP`    | `KC_WH_U` | 마우스 휠 위로          |
| `KC_MS_WH_DOWN`  | `KC_WH_D` | 마우스 휠 아래로         |
| `KC_MS_WH_LEFT`  | `KC_WH_L` | 마우스 휠 왼쪽으로        |
| `KC_MS_WH_RIGHT` | `KC_WH_R` | 마우스 휠 오른쪽으로       |
| `KC_MS_ACCEL0`   | `KC_ACL0` | 마우스 가속을 0으로 설정    |
| `KC_MS_ACCEL1`   | `KC_ACL1` | 마우스 가속을 1로 설정     |
| `KC_MS_ACCEL2`   | `KC_ACL2` | 마우스 가속을 2로 설정     |

## 모디키 :id=modifiers

참조: [모디키](feature_advanced_keycodes.md#modifier-keys)

| Key        | Aliases                            | Description                          |
| ---------- | ---------------------------------- | ------------------------------------ |
| `LCTL(kc)` | `C(kc)`                            | 왼쪽 컨트롤을 누른 채로 `kc` 입력                |
| `LSFT(kc)` | `S(kc)`                            | 왼쪽 시프트를 누른 채로 `kc` 입력                |
| `LALT(kc)` | `A(kc)`, `LOPT(kc)`                | 왼쪽 Alt를 누른 채로 `kc` 입력                |
| `LGUI(kc)` | `G(kc)`, `LCMD(kc)`, `LWIN(kc)`    | 왼쪽 GUI를 누른 채로 `kc` 입력                |
| `RCTL(kc)` |                                    | 오른쪽 컨트롤을 누른 채로 `kc` 입력               |
| `RSFT(kc)` |                                    | 오른쪽 시프트를 누른 채로 `kc`입력                |
| `RALT(kc)` | `ROPT(kc)`, `ALGR(kc)`             | 오른쪽 Alt를 누른 채로 `kc` 입력               |
| `RGUI(kc)` | `RCMD(kc)`, `LWIN(kc)`             | 오른쪽 GUI를 누른 채로 `kc` 입력               |
| `LSG(kc)`  | `SGUI(kc)`, `SCMD(kc)`, `SWIN(kc)` | 왼쪽 시프트와 왼쪽 GUI를 누른 채로 `kc` 입력        |
| `LAG(kc)`  |                                    | 왼쪽 Alt와 왼쪽 GUI를 누른 채로 `kc` 입력        |
| `RSG(kc)`  |                                    | 오른쪽 시프트와 오른쪽 GUI를 누른 채로 `kc` 입력      |
| `RAG(kc)`  |                                    | 오른쪽 Alt와 오른쪽 GUI를 누른 채로 `kc` 입력      |
| `LCA(kc)`  |                                    | 왼쪽 컨트롤과 Alt를 누른 채로 `kc` 입력           |
| `LSA(kc)`  |                                    | 왼쪽 시프트와 왼쪽 Alt를 누른 채로 `kc` 입력        |
| `RSA(kc)`  | `SAGR(kc)`                         | 오른쪽 시프트와 오른쪽 Alt를 누른 채로 `kc` 입력      |
| `RCS(kc)`  |                                    | 오른쪽 컨트롤과 오른쪽 시프트를 누른 채로 `kc` 입력      |
| `LCAG(kc)` |                                    | 왼쪽 컨트롤, Alt, GUI를 누른 채로 `kc` 입력      |
| `MEH(kc)`  |                                    | 왼쪽 컨트롤, 시프트, Alt를 누른 채로 `kc` 입력      |
| `HYPR(kc)` |                                    | 왼쪽 컨트롤, 시프트, Alt, GUI를 누른 채로 `kc` 입력 |
| `KC_MEH`   |                                    | 왼쪽 컨트롤, 시프트, Alt                     |
| `KC_HYPR`  |                                    | 왼쪽 컨트롤, 시프트, Alt, GUI                |

## Mod-Tap Keys :id=mod-tap-keys

See also: [Mod-Tap](mod_tap.md)

| Key           | Aliases                                                           | Description                                                                                                                 |
| ------------- | ----------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| `MT(mod, kc)` |                                                                   | 누르고 있으면 `mod`, 짧게 누르면 `kc`                                                                                                  |
| `LCTL_T(kc)`  | `CTL_T(kc)`                                                       | 누르고 있으면 왼쪽 컨트롤, 짧게 누르면 `kc`                                                                                                 |
| `LSFT_T(kc)`  | `SFT_T(kc)`                                                       | 누르고 있으면 왼쪽 시프트, 짧게 누르면 `kc`                                                                                                 |
| `LALT_T(kc)`  | `LOPT_T(kc)`, `ALT_T(kc)`, `OPT_T(kc)`                            | 누르고 있으면 왼쪽 Alt, 짧게 누르면 `kc`                                                                                                 |
| `LGUI_T(kc)`  | `LCMD_T(kc)`, `LWIN_T(kc)`, `GUI_T(kc)`, `CMD_T(kc)`, `WIN_T(kc)` | 누르고 있으면 왼쪽 GUI, 짧게 누르면 `kc`                                                                                                 |
| `RCTL_T(kc)`  |                                                                   | 누르고 있으면 오른쪽 컨트롤, 짧게 누르면 `kc`                                                                                                |
| `RSFT_T(kc)`  |                                                                   | 누르고 있으면 오른쪽 시프트, 짧게 누르면 `kc`                                                                                                |
| `RALT_T(kc)`  | `ROPT_T(kc)`, `ALGR_T(kc)`                                        | 누르고 있으면 오른쪽 Alt, 짧게 누르면 `kc`                                                                                                |
| `RGUI_T(kc)`  | `RCMD_T(kc)`, `RWIN_T(kc)`                                        | 누르고 있으면 오른쪽 GUI, 짧게 누르면 `kc`                                                                                                |
| `LSG_T(kc)`   | `SGUI_T(kc)`, `SCMD_T(kc)`, `SWIN_T(kc)`                          | 누르고 있으면 왼쪽 시프트와 GUI, 짧게 누르면 `kc`                                                                                            |
| `LAG_T(kc)`   |                                                                   | 누르고 있으면 왼쪽 Alt와 GUI, 짧게 누르면 `kc`                                                                                            |
| `RSG_T(kc)`   |                                                                   | 누르고 있으면 오른쪽 시프트와 GUI, 짧게 누르면 `kc`                                                                                           |
| `RAG_T(kc)`   |                                                                   | 누르고 있으면 오른쪽 Alt와 GUI, 짧게 누르면 `kc`                                                                                           |
| `LCA_T(kc)`   |                                                                   | 누르고 있으면 왼쪽 컨트롤과 Alt, 짧게 누르면 `kc`                                                                                            |
| `LSA_T(kc)`   |                                                                   | 누르고 있으면 왼쪽 시프트와 Alt, 짧게 누르면 `kc`                                                                                            |
| `RSA_T(kc)`   | `SAGR_T(kc)`                                                      | 누르고 있으면 오른쪽 시프트와 Alt, 짧게 누르면 `kc`                                                                                           |
| `RCS_T(kc)`   |                                                                   | 누르고 있으면 오른쪽 컨트롤과 시프트, 짧게 누르면 `kc`                                                                                           |
| `LCAG_T(kc)`  |                                                                   | 누르고 있으면 왼쪽 컨트롤과 GUI, 짧게 누르면 `kc`                                                                                            |
| `RCAG_T(kc)`  |                                                                   | 누르고 있으면 오른쪽 컨트롤, Alt, GUI, 짧게 누르면 `kc`                                                                                      |
| `C_S_T(kc)`   |                                                                   | 누르고 있으면 왼쪽 컨트롤과 시프트, 짧게 누르면 `kc`                                                                                            |
| `MEH_T(kc)`   |                                                                   | 누르고 있으면 왼쪽 컨트롤, 시프트, Alt, 짧게 누르면 `kc`                                                                                       |
| `HYPR_T(kc)`  | `ALL_T(kc)`                                                       | 누르고 있으면 왼쪽 컨트롤, 시프트, Alt, GUI, 짧게 누르면 `kc`, 추가적인 정보는 [여기](https://brettterpstra.com/2012/12/08/a-useful-caps-lock-key/)를 참조 |

## 탭 간격 키 :id=tapping-term-keys

참조: [동적 탭 간격](tap_hold#dynamic-tapping-term)

| Key       | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| `DT_PRNT` | "동적 탭 간격 출력": 현재 탭 간격을 밀리초 기준으로 입력                                               |
| `DT_UP`   | "동적 탭 간격 증가": 현재 탭 간격을 기준으로 `DYNAMIC_TAPPING_TERM_INCREMENT`밀리초 만큼 증가 (기본값: 5ms) |
| `DT_DOWN` | "동적 탭 간격 감소": 현재 탭 간격을 기준으로 `DYNAMIC_TAPPING_TERM_INCREMENT`밀리초 만큼 감소 (기본값: 5ms) |

## RGB 조명 :id=rgb-lighting

참조: [RGB 조명](feature_rgblight.md)

| Key                 | Aliases    | Description                                     |
| ------------------- | ---------- | ----------------------------------------------- |
| `RGB_TOG`           |            | RGB 조명 켜고 끄기                                    |
| `RGB_MODE_FORWARD`  | `RGB_MOD`  | 모드를 순차적으로 적용하며, 시프트 키를 누르고 있을 경우 반대로 순회합니다.     |
| `RGB_MODE_REVERSE`  | `RGB_RMOD` | 모드를 역방향으로 순차적용하며, 시프트 키를 누르고 있을 경우 정방향으로 순회합니다. |
| `RGB_HUI`           |            | 색상 값을 증가시키며, 시프트 키를 누르고 있을 경우 색상 값을 낮춥니다.       |
| `RGB_HUD`           |            | 색상 값을 낮추며, 시프트 키를 누르고 있을 경우 색상 값을 높입니다.         |
| `RGB_SAI`           |            | 채도를 증가시키며, 시프트 키를 누르고 있을 경우 채도를 낮춥니다.           |
| `RGB_SAD`           |            | 채도를 낮추며, 시프트 키를 누르고 있을 경우 채도를 높입니다.             |
| `RGB_VAI`           |            | 명도를 증가시키며, 시프트 키를 누르고 있을 경우 명도를 낮춥니다.           |
| `RGB_VAD`           |            | 명도를 낮추며, 시프트 키를 누르고 있을 경우 명도를 높입니다.             |
| `RGB_MODE_PLAIN`    | `RGB_M_P`  | 정적 모드                                           |
| `RGB_MODE_BREATHE`  | `RGB_M_B`  | 숨쉬기 모드                                          |
| `RGB_MODE_RAINBOW`  | `RGB_M_R`  | 무지개 모드                                          |
| `RGB_MODE_SWIRL`    | `RGB_M_SW` | 소용돌이 모드                                         |
| `RGB_MODE_SNAKE`    | `RGB_M_SN` | 뱀 모드                                            |
| `RGB_MODE_KNIGHT`   | `RGB_M_K`  | "기사 라이더" 모드                                     |
| `RGB_MODE_XMAS`     | `RGB_M_X`  | 크리스마스 모드                                        |
| `RGB_MODE_GRADIENT` | `RGB_M_G`  | 정적 그라데이션 모드                                     |
| `RGB_MODE_RGBTEST`  | `RGB_M_T`  | 빨강, 녹색, 파랑 테스트 모드                               |

## RGB 매트릭스 조명 :id=rgb-matrix-lighting

참조: [RGB 매트릭스 조명](feature_rgb_matrix.md)

| Key                | Aliases    | Description                                                      |
| ------------------ | ---------- | ---------------------------------------------------------------- |
| `RGB_TOG`          |            | RGB 조명 켜고 끄기                                                     |
| `RGB_MODE_FORWARD` | `RGB_MOD`  | 모드를 순차적으로 적용하며, 시프트 키를 누르고 있을 경우 반대로 순회합니다.                      |
| `RGB_MODE_REVERSE` | `RGB_RMOD` | 모드를 역방향으로 순차적용하며, 시프트 키를 누르고 있을 경우 정방향으로 순회합니다.                  |
| `RGB_HUI`          |            | 색상 값을 증가시키며, 시프트 키를 누르고 있을 경우 색상 값을 낮춥니다.                        |
| `RGB_HUD`          |            | 색상 값을 낮추며, 시프트 키를 누르고 있을 경우 색상 값을 높입니다.                          |
| `RGB_SAI`          |            | 채도를 증가시키며, 시프트 키를 누르고 있을 경우 채도를 낮춥니다.                            |
| `RGB_SAD`          |            | 채도를 낮추며, 시프트 키를 누르고 있을 경우 채도를 높입니다.                              |
| `RGB_VAI`          |            | 명도를 증가시키며, 시프트 키를 누르고 있을 경우 명도를 낮춥니다.                            |
| `RGB_VAD`          |            | 명도를 낮추며, 시프트 키를 누르고 있을 경우 명도를 높입니다.                              |
| `RGB_SPI`          |            | 효과 속도를 증가시키며 (현재까지는 eeprom을 지원하지 않습니다), 시프트를 누르고 있을 경우 속도를 낮춥니다. |
| `RGB_SPD`          |            | 효과 속도를 낮추며(현재까지는 eeprom을 지원하지 않습니다), 시프트를 누르고 있을 경우 속도를 높입니다.    |

## 감열 프린터 :id=thermal-printer

참조: [감열 프린터](feature_thermal_printer.md)

| Key         | Description    |
| ----------- | -------------- |
| `PRINT_ON`  | 사용자 입력값을 모두 출력 |
| `PRINT_OFF` | 사용자 입력값 출력을 중지 |

## US ANSI Shifted 특수기호 :id=us-ansi-shifted-symbols

참조: [US ANSI Shifted 특수기호](keycodes_us_ansi_shifted.md)

| Key                      | Aliases             | Description |
| ------------------------ | ------------------- | ----------- |
| `KC_TILDE`               | `KC_TILD`           | `~`         |
| `KC_EXCLAIM`             | `KC_EXLM`           | `!`         |
| `KC_AT`                  |                     | `@`         |
| `KC_HASH`                |                     | `#`         |
| `KC_DOLLAR`              | `KC_DLR`            | `$`         |
| `KC_PERCENT`             | `KC_PERC`           | `%`         |
| `KC_CIRCUMFLEX`          | `KC_CIRC`           | `^`         |
| `KC_AMPERSAND`           | `KC_AMPR`           | `&`         |
| `KC_ASTERISK`            | `KC_ASTR`           | `*`         |
| `KC_LEFT_PAREN`          | `KC_LPRN`           | `(`         |
| `KC_RIGHT_PAREN`         | `KC_RPRN`           | `)`         |
| `KC_UNDERSCORE`          | `KC_UNDS`           | `_`         |
| `KC_PLUS`                |                     | `+`         |
| `KC_LEFT_CURLY_BRACE`    | `KC_LCBR`           | `{`         |
| `KC_RIGHT_CURLY_BRACE`   | `KC_RCBR`           | `}`         |
| `KC_PIPE`                |                     | `\|`        |
| `KC_COLON`               | `KC_COLN`           | `:`         |
| `KC_DOUBLE_QUOTE`        | `KC_DQUO`, `KC_DQT` | `"`         |
| `KC_LEFT_ANGLE_BRACKET`  | `KC_LABK`, `KC_LT`  | `<`         |
| `KC_RIGHT_ANGLE_BRACKET` | `KC_RABK`, `KC_GT`  | `>`         |
| `KC_QUESTION`            | `KC_QUES`           | `?`         |

## 원샷 키 :id=one-shot-keys

참조: [원샷 키](one_shot_keys.md)

| Key          | Description                          |
| ------------ | ------------------------------------ |
| `OSM(mod)`   | `mod` 모디키가 눌린 채로 한 키 입력              |
| `OSL(layer)` | 다음 한 키 입력에 대해서만 `layer` 레이어로 변경하여 입력 |
| `OS_ON`      | 원샷 키 활성화                             |
| `OS_OFF`     | 원샷 키 비활성화                            |
| `OS_TOGG`    | 원샷 키 활성화 여부 전환                       |

## 사용자 정의 버튼 지원 :id=programmable-button

참조: [사용자 정의 버튼](feature_programmable_button.md)

| Key                      | Description  |
| ------------------------ | ------------ |
| `PROGRAMMABLE_BUTTON_1`  | 사용자 정의 버튼 1  |
| `PROGRAMMABLE_BUTTON_2`  | 사용자 정의 버튼 2  |
| `PROGRAMMABLE_BUTTON_3`  | 사용자 정의 버튼 3  |
| `PROGRAMMABLE_BUTTON_4`  | 사용자 정의 버튼 4  |
| `PROGRAMMABLE_BUTTON_5`  | 사용자 정의 버튼 5  |
| `PROGRAMMABLE_BUTTON_6`  | 사용자 정의 버튼 6  |
| `PROGRAMMABLE_BUTTON_7`  | 사용자 정의 버튼 7  |
| `PROGRAMMABLE_BUTTON_8`  | 사용자 정의 버튼 8  |
| `PROGRAMMABLE_BUTTON_9`  | 사용자 정의 버튼 9  |
| `PROGRAMMABLE_BUTTON_10` | 사용자 정의 버튼 10 |
| `PROGRAMMABLE_BUTTON_11` | 사용자 정의 버튼 11 |
| `PROGRAMMABLE_BUTTON_12` | 사용자 정의 버튼 12 |
| `PROGRAMMABLE_BUTTON_13` | 사용자 정의 버튼 13 |
| `PROGRAMMABLE_BUTTON_14` | 사용자 정의 버튼 14 |
| `PROGRAMMABLE_BUTTON_15` | 사용자 정의 버튼 15 |
| `PROGRAMMABLE_BUTTON_16` | 사용자 정의 버튼 16 |
| `PROGRAMMABLE_BUTTON_17` | 사용자 정의 버튼 17 |
| `PROGRAMMABLE_BUTTON_18` | 사용자 정의 버튼 18 |
| `PROGRAMMABLE_BUTTON_19` | 사용자 정의 버튼 19 |
| `PROGRAMMABLE_BUTTON_20` | 사용자 정의 버튼 20 |
| `PROGRAMMABLE_BUTTON_21` | 사용자 정의 버튼 21 |
| `PROGRAMMABLE_BUTTON_22` | 사용자 정의 버튼 22 |
| `PROGRAMMABLE_BUTTON_23` | 사용자 정의 버튼 23 |
| `PROGRAMMABLE_BUTTON_24` | 사용자 정의 버튼 24 |
| `PROGRAMMABLE_BUTTON_25` | 사용자 정의 버튼 25 |
| `PROGRAMMABLE_BUTTON_26` | 사용자 정의 버튼 26 |
| `PROGRAMMABLE_BUTTON_27` | 사용자 정의 버튼 27 |
| `PROGRAMMABLE_BUTTON_28` | 사용자 정의 버튼 28 |
| `PROGRAMMABLE_BUTTON_29` | 사용자 정의 버튼 29 |
| `PROGRAMMABLE_BUTTON_30` | 사용자 정의 버튼 30 |
| `PROGRAMMABLE_BUTTON_31` | 사용자 정의 버튼 31 |
| `PROGRAMMABLE_BUTTON_32` | 사용자 정의 버튼 32 |
| `PB_1` to `PB_32`        | 키맵 바로가기      |

## 스페이스 카뎃 :id=space-cadet

참조: [스페이스 카뎃](feature_space_cadet.md)

| Key         | Description                  |
| ----------- | ---------------------------- |
| `KC_LCPO`   | 길게 누르면 왼쪽 컨트롤, 짧게 누르면 `(`    |
| `KC_RCPC`   | 길게 누르면 오른쪽 컨트롤, 짧게 누르면 `)`   |
| `KC_LSPO`   | 길게 누르면 왼쪽 시프트, 짧게 누르면 `(`    |
| `KC_RSPC`   | 길게 누르면 오른쪽 시프트, 짧게 누르면 `)`   |
| `KC_LAPO`   | 길게 누르면 왼쪽 Alt, 짧게 누르면 `(`    |
| `KC_RAPC`   | 길게 누르면 오른쪽 Alt, 짧게 누르면 `)`   |
| `KC_SFTENT` | 길게 누르면 오른쪽 시프트, 짧게 누르면 Enter |

## 손 바꾸기 :id=swap-hands

참조: [손 바꾸기](feature_swap_hands.md)

| Key         | Description                                    |
| ----------- | ---------------------------------------------- |
| `SH_T(key)` | 짧게 누르면 `key` 를 입력, 길게 누르면 임시로 손바꿈              |
| `SW_ON`     | 손바꿈을 활성화하고 유지                                  |
| `SW_OFF`    | 손바꿈을 비활성화하고 유지. 알려진 (일반적인) 상태로 복귀하기에 좋습니다.     |
| `SH_MON`    | 누르면 손바꿈, 손을 떼면 원래 상태로 복귀합니다(임시적).              |
| `SH_MOFF`   | 일시적으로 손바꿈을 비활성화합니다.                            |
| `SH_TG`     | 각 입력마다 손바꿈 활성화 여부를 전환합니다.                      |
| `SH_TT`     | 한 번 누르면 손바꿈 활성화 상태를 전환하고, 누르고 있으면 임시적으로 작동합니다. |
| `SH_OS`     | 원샷 손바꿈 - 누르고 있는 동안은 토글이거나 이후 키 입력이 있을 때까지 활성화  |

## 유니코드 지원 :id=unicode-support

참조: [유니코드 지원](feature_unicode.md)

| Key                    | Aliases   | Description                                                     |
| ---------------------- | --------- | --------------------------------------------------------------- |
| `UC(c)`                |           | 유니코드 코드 포인트 `c`를 입력, `0X7FFF`까지 가능                              |
| `X(i)`                 |           | 유니코드 코드 포인트에서 `i` 번째 값을 입력(인덱스)                                 |
| `XP(i, j)`             |           | 유니코드 코드 포인트에서 `i` 번째 값을 입력하되, 시프트나 캡스락이 걸려있으면 `j` 번째 값을 입력(인덱스) |
| `UNICODE_MODE_FORWARD` | `UC_MOD`  | 선택된 입력 모드를 순회                                                   |
| `UNICODE_MODE_REVERSE` | `UC_RMOD` | 선택된 입력 모드를 역방향으로 순회                                             |
| `UNICODE_MODE_MAC`     | `UC_M_MA` | macOS 입력 방식으로 전환                                                |
| `UNICODE_MODE_LNX`     | `UC_M_LN` | Linux 입력 방식으로 전환                                                |
| `UNICODE_MODE_WIN`     | `UC_M_WI` | Windows 입력 방식으로 전환                                              |
| `UNICODE_MODE_BSD`     | `UC_M_BS` | BSD 입력 방식으로 전환(지원 예정)                                           |
| `UNICODE_MODE_WINC`    | `UC_M_WC` | WinCompose를 이용하여 Windows 입력 방식으로 전환                             |
