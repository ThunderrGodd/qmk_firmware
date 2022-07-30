# 자주 묻는 질문들

## QMK가 무엇입니까?

Quantum Mechanical Keyboard의 약자인 [QMK](https://github.com/qmk)는, 커스텀 키보드용의 툴을 빌드하는 사람들의 그룹입니다. [TMK](https://github.com/tmk/tmk_keyboard)를 대폭으로 수정한 포크인 [QMK firmware](https://github.com/qmk/qmk_firmware)로부터 시작했습니다.

## 어디서부터 시작해야할지 모르겠습니다!

이 경우, [초보자 가이드](newbs.md)부터 시작해야 합니다. 여기에는 훌륭한 정보가 많이 있으며, 그것들은 당신이 시작하기에 필요한 모든 것을 커버할 수 있습니다.

문제가 있는 경우, [QMK Configurator](https://config.qmk.fm)에 접속해보십시오. 당신이 필요한 것의 대부분을 처리 할 수 있을 것입니다.

## 내가 빌드한 펌웨어를 어떻게 플래시할 수 있습니까?

먼저, [컴파일/플래시 FAQ 페이지](faq_build.md에 접속해 보십시오. 거기에는 많은 정보가 있으며, 대부분의 일반적인 이슈의 해결책을 찾으실수 있을 것입니다.

## 여기에서 커버하지 못하는 이슈가 있으면 어떻게 합니까?

좋습니다, 문제 없습니다. 그럴땐 [Github에서 열린 이슈들](https://github.com/qmk/qmk_firmware/issues)을 확인해서, 누군가가 같은 경험을 하지 않았는지 살펴보십시오. (비슷하기만 한 것이 아니고, 정확히 같은 것인지 확인하십시오).

아무것도 찾지 못했다면, [새 이슈](https://github.com/qmk/qmk_firmware/issues/new)를 열어오보십시오!

## 버그를 찾았으면 어떻게 해야 합니?

[이슈](https://github.com/qmk/qmk_firmware/issues/new)를 열어 주십시오. 그리고 어떻게 고치는지도 아신다면, Github에서 고치는 방법과 함께 풀 리퀘스트를 열어 주십시오.

## 하지만 `git`과 `GitHub`가 무섭습니다!

걱정하지 마십시오, 개발이 쉬워지도록 `git'과 Github를 어떻게 사용해야할지 알려드릴 예쁘고 멋진 [가이드라인](newbs_git_best_practices.md)이 있습니다.

또, 추가적인 `git`과 깃허브에 관련된 링크를 [여기](newbs_learn_more_resources.md)에서 보실 수 다습니다.

## 지원을 추가하고싶은 키보드가 있습니

Awesome! Open up a Pull Request for it. We'll review the code, and merge it!

### What if I want to brand it with `QMK`?

That's amazing! We would love to assist you with that!

In fact, we have a [whole page](https://qmk.fm/powered/) dedicated to adding QMK Branding to your page and keyboard. This covers pretty much everything you need (knowledge and images) to officially support QMK.

If you have any questions about this, open an issue or head to [Discord](https://discord.gg/Uq7gcHh).

## What Differences Are There Between QMK and TMK?

TMK was originally designed and implemented by [Jun Wako](https://github.com/tmk). QMK started as [Jack Humbert](https://github.com/jackhumbert)'s fork of TMK for the Planck. After a while Jack's fork had diverged quite a bit from TMK, and in 2015 Jack decided to rename his fork to QMK.

From a technical standpoint QMK builds upon TMK by adding several new features. Most notably QMK has expanded the number of available keycodes and uses these to implement advanced features like `S()`, `LCTL()`, and `MO()`. You can see a complete list of these keycodes in [Keycodes](keycodes.md).

From a project and community management standpoint TMK maintains all the officially supported keyboards by himself, with a bit of community support. Separate community maintained forks exist or can be created for other keyboards. Only a few keymaps are provided by default, so users typically don't share keymaps with each other. QMK encourages sharing of both keyboards and keymaps through a centrally managed repository, accepting all pull requests that follow the quality standards. These are mostly community maintained, but the QMK team also helps when necessary.

Both approaches have their merits and their drawbacks, and code flows freely between TMK and QMK when it makes sense.
