# Translating the QMK Docs

최상위 폴더(`docs/`)에 있는 모든 파일들은 영어로 되어 있어야 합니다 - 다른 언어들은 ISO 639-1 언어 코드로 만들어진 하위 폴더 안에 있어야 하며, 관련 국가 코드를 `-` 뒤에 붙입니다. [일반적인 코드는 여기서 찾을 수 있습니다.](https://www.andiamo.co.uk/resources/iso-language-codes/). 해당 폴더가 없을 경우, 새롭게 생성할 수 있습니다. 번역된 파일들은 각각 대응되는 영어 버전의 파일명과 같은 이름을 가져야 하며, 이로써 문제가 발생 시 영어버전으로 돌아갈 수 있습니다.

A `_summary.md` file should exist in this folder with a list of links to each file, with a translated name, and link preceded by the language folder:

각 (번역된) 파일로 이어지는 링크 리스트를 포함하는 `_summary.md` 파일이 폴더 안에 있어야 하며, 리스트는 번역된 이름, 언어 폴더, 링크 순으로 구성됩니다(이하 참조).

```markdown
 * [QMK 간단 소개](ko/getting_started_introduction.md)
```

다른 문서로 연결되는 모든 링크는 반드시 언어 폴더를 앞에 붙여야 합니다. 만일 링크가 페이지의 특정 부분으로 연결되는 경우(예를 들어, 특정 머릿말로 연결한다든가), 머릿말의 영어 ID를 사용하여야 합니다(이하 예시 참조).

```markdown
[사용자 환경 구성](ko/newbs-getting-started.md#set-up-your-environment)

## 사용자 환경 구성 :id=set-up-your-environment
```

새 언어로 번역을 마친 경우, 아래 파일들도 변경하여야 합니다.

* [`docs/_langs.md`](https://github.com/qmk/qmk_firmware/blob/master/docs/_langs.md)  
  각 줄은 [GitHub emoji shortcode](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md#country-flag) 에 따른 국기 이모지와 언어를 표시하는 이름을 포함해야 합니다.:
  
  ```markdown
   - [:kr: 한국어](/zh-cn/)
  ```

* [`docs/index.html`](https://github.com/qmk/qmk_firmware/blob/master/docs/index.html)  
  `placeholder` 와 `noData` 객체 둘 다 문자열로 이루어진 언어 폴더 사전dictionary 엔트리를 가지고 있어야 합니다.
  
  ```js
  '/ko/': '결과 없음!',
  ```
  
  `nameLink` 객체에도 또한, "QMK Firmware" 머릿말 링크를 사이드바에 설정하기 위해서, 마찬가지로 추가되어야 합니다.
  
  ```js
  '/ko/': '/#/ko/',
  ```
  
  `fallbackLanguages` 리스트에도 언어 폴더를 추가해야, 404 대신 영어 문서로 재연결할 수 있습니다.
  
  ```js
  fallbackLanguages: [
    // ...
    'ko',
    // ...
  ],
  ```

## 번역 미리보기

문서의 로컬 인스턴스를 수립하려면 [문서 미리보기](contributing.md#previewing-the-documentation) 항목을 참조하십시오. 우상단 "Translations" 에서 새 언어를 선택할 수 있습니다.

번역에 만족하신다면, 새로운 Pull Request를 열어주세요!
