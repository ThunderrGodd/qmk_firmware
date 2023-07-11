# 핸드와이어링 가이드

## 부품 목록

필요한 것들: (*x*는 당신이 계획중인 키보드의 키의 갯수입니다)

* QMK를 지원하는 마이크로컨트롤러 보드 (Teensy, 프로마이크로 , QMK Proton C 등.)
* 스위치 *x*개 (체리 MX, Matias, 게이트론, 등)
* 쓰루홀 다이오드 *x*개
* 키보드 보강판과 보강판용 스테빌라이저
* 전기선
* 인두기
* 로진 코어 땜납
* 충분한 환기/팬
* 와이어 커터/니퍼

유용할수 있는 선택사항Optional but useful:

* 피복 스트리퍼/날카로운 칼Wire strippers/a sharp knife
* 핀셋 &/ 작은 노즈 플라이어Tweezers and/or small needle nose pliers
* 솔더링 스테이션/보조 집게Soldering station/Helping hands

## 빌드 시작하기

PCB 매트릭스를 핸드와이어 하는 데에는 많은 방법이 있습니다. 이 가이드에서는 기초적인 부분과 몇몇 추천하는 방법을 기술할 것입니다.

우리는 핸드와이어링을 진행할 것이므로, 당신이 이미 보강판을 가지고 있다고 가정하겠습니다. 만약 당신이 당신만의 커스텀 레이아웃을 계획중이라면, [ai03 보강판 생성기](https://kbplate.ai03.me/) 와 [Swillkb 보강판&케이스 빌더](http://builder.swillkb.com/) 같은 툴이 도움이 될 것입니다.

보강판에 스위치와 스테빌라이저를 제자리에 꽂는 것으로 시작하십시오. 보강판의 두께와 재질에 따라 글루건으로 칠해야 할 수 있습니다.

## 매트릭스 계획하기

만약 당신이 핸드와이어 예제를 따르는 중이라면 (예를 들어 [핸드와이어 펌웨어 폴더](https://github.com/qmk/qmk_firmware/tree/master/keyboards/handwired)의 키보드들같은), 이 단계를 생략할 수 있습니다. 단, 묘사된 대로 매트릭스를 연결했는지 확인하십시오.

당신이 이루려고 하는 것은 각 스위치의 한쪽 다리를 양옆에 있는, 짝이 맞는 스위치에 연결하는 것이며(rows), 또한 다른쪽 다리를 위아래의 스위치에 연결하는 것이고 (columns), 다이오드를 한쪽 다리(매우 흔하게 rows 쪽의)에 연결하는 것입니다. 그리고 다이오드는 거기서 먼 쪽을 향하게 될 것입니다 (Column to Row) 그리고 검은 선으로 보이듯이, 스위치에 연결된 다이오드끼리 연결해야 합니다 (전류는 다이오드를 통해 한 방향으로만 진행할 것입니다).

이것은 (플랭크같은) 오쏘리니어 키보드를 계획하는 꽤 쉬운 방법입니다.

![ㅍ플랭크 매트릭스 예시시](https://i.imgur.com/FRShcLD.png)
Image from [RoastPotatoes' "How to hand wire a Planck"](https://blog.roastpotatoes.co/guide/2015/11/04/how-to-handwire-a-planck/)

But the larger and more complicated your keyboard, the more complex the matrix.  [Keyboard Firmware Builder](https://kbfirmware.com/) can help you plan your matrix layout (shown here with a basic fullsize ISO keyboard imported from [Keyboard Layout Editor](https://www.keyboard-layout-editor.com).

![Example ISO matrix](https://i.imgur.com/UlJ4ZDP.png)

Bear in mind that the number of rows plus the number of columns can not exceed the number of I/O pins on your controller.  So the fullsize matrix shown above would be possible on a Proton C or Teensy++, but not on a regular Teensy or Pro Micro.

### Common Microcontroller Boards

| Board         | Controller    | # I/O  | Pinout |
| :------------ |:-------------:| ------:| ------ |
| Pro Micro*    | ATmega32u4    |     20 | [link](https://learn.sparkfun.com/tutorials/pro-micro--fio-v3-hookup-guide/hardware-overview-pro-micro#Teensy++_2.0)       |
| Teensy 2.0    | ATmega32u4    |     25 | [link](https://www.pjrc.com/teensy/pinout.html)       |
| [QMK Proton C](https://qmk.fm/proton-c/)      | STM32F303xC   |     36 | [link 1](https://i.imgur.com/RhtrAlc.png), [2](https://deskthority.net/wiki/QMK_Proton_C)       |
| Teensy++ 2.0  | AT90USB1286   |     46 | [link](https://www.pjrc.com/teensy/pinout.html#Teensy_2.0)       |

*Elite C is essentially the same as a Pro Micro with a USB-C instead of Micro-USB

There are also a number of boards designed specifically for handwiring that mount directly to a small number of switches and offer pinouts for the rest.  Though these are generally more expensive and may be more difficult to get hold of.

<img src="https://i.imgur.com/QiA3ta6.jpg" alt="Postage board mini mounted in place" width="500"/>

| Board         | Controller    | # I/O  |
| :------------ |:-------------:| ------:|
| [Swiss helper](https://www.reddit.com/r/MechanicalKeyboards/comments/8jg5d6/hand_wiring_this_might_help/) |  ATmega32u4 | 20 |
| [Postage board](https://github.com/LifeIsOnTheWire/Postage-Board/)| ATmega32u4| 25 |
| [Postage board mini](https://geekhack.org/index.php?topic=101460.0)| ATmega32u4| 25 |

## Wiring the matrix

There is no one right way to do this.  What you want to achieve is good connection at all of the joints planned and no unintentional shorts.

Established materials and techniques include:

| Technique     | Examples | Pros | Cons | Image
| :-----------| :------- | :------ | :--- | :---
| Lengths of wire with stripped segments | [Sasha Solomon's Dactyl](https://medium.com/@sachee/building-my-first-keyboard-and-you-can-too-512c0f8a4c5f) and [Cribbit's modern hand wire](https://geekhack.org/index.php?topic=87689.0) | Neat and tidy | Some effort in stripping the wire | ![Stripped wire](https://i.imgur.com/0GNIYY0.jpg)
| Short lengths of wire | [u/xicolinguada's ortho build](https://www.reddit.com/r/MechanicalKeyboards/comments/c39k4f/my_first_hand_wired_keyboard_its_not_perfect_but/) | Easier to strip the wire | More difficult to place | ![individual wire lengths](https://i.imgur.com/mBe5vkL.jpg)
| Magnet/Enamelled wire | [fknraiden's custom board](https://geekhack.org/index.php?topic=74223.0) | Can be directly soldered onto (insulation burns off with heat) | Appearance? | ![Magnet wire](https://i.imgur.com/b4b7KDb.jpg)
| Bending the legs of the diodes for the rows | [Matt3o's Brownfox](https://deskthority.net/viewtopic.php?f=7&t=6050) | Fewer solder joints required | Uninsulated | ![Bent diode legs](https://i.imgur.com/aTnG8TV.jpg)
| Using rigid wiring (e.g. brass tube) | [u/d_stilgar's invisible hardline](https://www.reddit.com/r/MechanicalKeyboards/comments/8aw5j2/invisible_hardline_keyboard_progress_update_april/) and [u/jonasfasler's first attempt](https://www.reddit.com/r/MechanicalKeyboards/comments/de1jyv/my_first_attempt_at_handwiring_a_keyboard/) | Very pretty | More difficult. No physical insulation | ![Hardline hand wire](https://i.imgur.com/CnASmPo.jpg)
| Bare wire with insulation added after (e.g. kapton tape) | [Matt3o's 65% on his website](https://matt3o.com/hand-wiring-a-custom-keyboard/) | Easier (no wire stripping required) | Not as attractive | ![Bare wire](https://i.imgur.com/AvXZShD.jpg)
| Copper tape | [ManuForm Dactyl](https://github.com/tshort/dactyl-keyboard) | Very easy | Only really works when your plate/case aligns with the bottom of your switches | ![Copper tape](https://i.imgur.com/RFyNMlL.jpg)


Note that these methods can be combined.  Prepare your lengths of wire before moving on to soldering.


### A note on split keyboards

If you are planning a split keyboard (e.g. Dactyl) each half will require a controller and a means of communicating between them (like a TRRS or hardwired cable).  Further information can be found in the [QMK split keyboard documentation.](feature_split_keyboard.md)


### Soldering

There are a lot of soldering guides and tips available elsewhere but here are some of the most useful and relevant for hand wiring:

To ensure a strong solder joint you want a good amount of contact between the solder and the two pieces of metal you are connecting. A good way of doing this (though not required) is looping around pins or twisting wires together before applying solder.

<img src="https://i.imgur.com/eHJjmnU.jpg" alt="Looped around rod" width="200"/> <img src="https://i.imgur.com/8nbxmmr.jpg?1" alt="Looped diode leg" width="200"/>

If your diodes are on a packaging strip and need a bend in them (either the start of a loop or for connecting to its neighbour) this can easily done by bending it over something straight like the edge of a box, table, or ruler.  This also helps keep track of the direction of the diode as all the bends will be on the same side.

<img src="https://i.imgur.com/oITudbX.jpg" alt="Bent diode legs" width="200"/>

If your iron has temperature control, set it to 315ºC (600ºF).

Once heated, tin your soldering iron - this means melting a small amount of solder on the end of the iron and then quickly wiping it off on a wet sponge or wire cleaning pad, leaving a shiny silvery coating on the end which helps keep oxidisation at bay and helps solder to flow.

When you come to apply the solder, hold the soldering iron against the two surfaces for a second to heat it, then apply a small amount of solder to join the two pieces together.  Heating the surfaces ensures that the solder adheres to it and that it does not cool too quickly.

Don't hold the iron on the solder/joint longer than necessary. Heat will be conducted through the surfaces and can damage components (melt switch housings etc.).  Also, solder contains flux, which aids in ["wetting"](https://en.m.wikipedia.org/wiki/Wetting).  The longer heat is applied to the solder the more flux will evaporate meaning you may end up with a bad solder joint with peaks which, apart from looking bad, may also increase the risk of electrical shorts.

#### Soldering the Diodes

Starting at the top-left switch, place the diode (with tweezers if you have them) on the switch so that the diode itself is vertically aligned, and the black line is facing toward you. Make sure the diodes are soldered in parallel (diode outputs shouldn't connect to diode inputs). The input lead of the diode should be touching the left contact on the switch, and the bent, output end should be facing to the right and resting on the switch there, like this:

![soldering-diodes-01.png](https://raw.githubusercontent.com/noroadsleft/qmk_images/master/docs/hand_wire/soldering-diodes-01.png)

Letting the diode rest, grab your solder, and touch both it and the soldering iron to the left contact at the same time - the rosin in the solder should make it easy for the solder to flow over both the diode and the keyswitch contact. The diode may move a little, and if it does, carefully position it back it place by grabbing the bent end of the diode - the other end will become hot very quickly. If you find that it's moving too much, using needle-nose pliers of some sort may help to keep the diode still when soldering.

The smoke that the rosin releases is harmful, so be careful not to breath it or get it in your eyes/face.

After soldering things in place, it may be helpful to blow on the joint to push the smoke away from your face, and cool the solder quicker. You should see the solder develop a matte (not shiny) surface as it solidifies. Keep in mind that it will still be very hot afterwards, and will take a couple minutes to be cool to touch. Blowing on it will accelerate this process.

When the first diode is complete, the next one will need to be soldered to both the keyswitch, and the previous diode at the new elbow. That will look something like this:

![soldering-diodes-02.png](https://raw.githubusercontent.com/noroadsleft/qmk_images/master/docs/hand_wire/soldering-diodes-02.png)

After completing a row, use the wire cutters to trim the excess wire from the tops of the diodes, and from the right side on the final switch. This process will need to completed for each row you have.

When all of the diodes are completely soldered, it's a good idea to quickly inspect each one to ensure that your solder joints are solid and sturdy - repairing things after this is possible, but more difficult.

#### Soldering the Columns

You'll have some options in the next process - it's a good idea to insulate the column wires (since the diodes aren't), but if you're careful enough, you can use exposed wires for the columns - it's not recommended, though. If you're using single-cored wire, stripping the plastic off of the whole wire and feeding it back on is probably the best option, but can be difficult depending on the size and materials. You'll want to leave parts of the wire exposed where you're going to be solder it onto the keyswitch.

If you're using stranded wire, it's probably easiest to just use a lot of small wires to connect each keyswitch along the column. It's possible to use one and melt through the insulation, but this isn't recommended, will produce even more harmful fumes, and can ruin your soldering iron.

Before beginning to solder, it helps to have your wire pre-bent (if using single-cored), or at least have an idea of how you're going to route the column (especially if you're making a staggered board). Where you go in particular doesn't matter too much, as we'll be basing our keymap definitions on how it was wired - just make sure every key in a particular row is in a unique column, and that they're in order from left to right.

If you're not using any insulation, you can try to keep the column wires elevated, and solder them near the tips of the keyswitch contacts - if the wires are sturdy enough, they won't short out to the row wiring an diodes.

## Wiring up the controller

Now that the matrix itself is complete, it's time to connect what you've done to the microcontroller board.

Place the microcontroller where you want it to be located, give thought to mounting and case alignment.  Bear in mind that the location of the USB socket can be different from the controller by using a short male to female cable if required,.

Find the pinout/documentation for your microcontroller board ([links here](#common-microcontroller-boards)) and make a note of all the digital I/O pins on it (note that on some controllers, like the teensy, analogue I/O can double as digital) as these are the pins you want to connect your wires to.

----

### Specific instructions for the Teensy 2.0

There are some pins on the Teensy that are special, like D6 (the LED on the chip), or some of the UART, SPI, I2C, or PWM channels, but only avoid those if you're planning something in addition to a keyboard. If you're unsure about wanting to add something later, you should have enough pins in total to avoid a couple.

The pins you'll absolutely have to avoid, as with any controller, are: GND, VCC, AREF, and RST - all the others are usable and accessible in the firmware.

----


Cut wires to the length of the distance from the a point on each column/row to the controller.  You can solder anywhere along the row, as long as it's after the diode - soldering before the diode (on the keyswitch side) will cause that row not to work.

Ribbon cable can be used to keep this extra tidy.  You may also want to consider routing the wires beneath the exisiting columns/rows.

<img src="https://i.imgur.com/z2QlKfB.jpg" alt="Ribbon Cable" width="350"/>

As you solder the wires to the controller make a note of which row/column is going to which pin on the controller as we'll use this data to setup the matrix when we create the firmware.

As you move along, be sure that the controller is staying in place - recutting and soldering the wires is a pain!


## Getting Some Basic Firmware Set Up

From here, you should have a working keyboard once you program a firmware.

Simple firmware can be created easily using the [Keyboard Firmware Builder](https://kbfirmware.com/) website.  Recreate your layout using [Keyboard Layout Editor](https://www.keyboard-layout-editor.com), import it and recreate the matrix (if not already done as part of [planning the matrix](#planning-the-matrix).

Go through the rest of the tabs, assigning keys until you get to the last one where you can compile and download your firmware.  The .hex file can be flashed straight onto your keyboard, and the .zip of source files can be modified for advanced functionality and compiled locally using the method described in [Building Your First Firmware](newbs_building_firmware?id=build-your-firmware).

The source given by Keyboard Firmware Builder is QMK, but is based on a version of QMK from early 2017. To compile the code from your .zip file in a modern version of QMK Firmware, you'll need to open the .zip and follow these instructions:

1. Extract the `kb` folder to `qmk_firmware/keyboards/handwired/`.
2. Open the extracted `kb` folder, then proceed to the `keymaps/default/` folder, and open `keymap.c`.
3. Locate and delete the `action_get_macro` code block:
   ```
    const macro_t *action_get_macro(keyrecord_t *record, uint8_t id, uint8_t opt) {
        ...
        return MACRO_NONE;
    }
   ```
4. Save and close `keymap.c`.

## Flashing the Firmware

Install [QMK Toolbox](https://github.com/qmk/qmk_toolbox).

![QMK Toolbox](https://raw.githubusercontent.com/noroadsleft/qmk_images/master/docs/hand_wire/qmk_toolbox.png "QMK Toolbox 0.0.16 on Windows 8.1")

Under "Local File" navigate to your newly created .hex file.  Under "Microcontroller", select the corresponding one for your controller board (common ones available [here](#common-microcontroller-boards)).

Plug in your keyboard and press the reset button (or short the Reset and Ground pins if there is no button) and click the "Flash" button in QMK toolbox.


## Testing Your Firmware

Use a website such as [QMK Configurator's Keyboard Tester](https://config.qmk.fm/#/test), [Keyboard Tester](https://www.keyboardtester.com/tester.html), or [Keyboard Checker](https://keyboardchecker.com/) or just open a text editor and try typing - you should get the characters that you put into your keymap. Test each key, and make a note of the ones that aren't working. Here's a quick trouble-shooting guide for non-working keys:

1. Flip the keyboard back over and short the keyswitch's contacts with a piece wire - this will eliminate the possibility of the keyswitch being bad and needing to be replaced.
2. Check the solder points on the keyswitch - these need to be plump and whole. If you touch it with a moderate amount of force and it comes apart, it's not strong enough.
3. Check the solder joints on the diode - if the diode is loose, part of your row may register, while the other may not.
4. Check the solder joints on the columns - if your column wiring is loose, part or all of the column may not work.
5. Check the solder joints on both sides of the wires going to/from the Teensy - the wires need to be fully soldered and connect to both sides.
6. Check the `<project_name>.h` file for errors and incorrectly placed `KC_NO`s - if you're unsure where they should be, instead duplicate a k*xy* variable.
7. Check to make sure you actually compiled the firmware and flashed the Teensy correctly. Unless you got error messages in the terminal, or a pop-up during flashing, you probably did everything correctly.
8. Use a multimeter to check that the switch is actually closing when actuated (completing the circuit when pressed down).

If you've done all of these things, keep in mind that sometimes you might have had multiple things affecting the keyswitch, so it doesn't hurt to test the keyswitch by shorting it out at the end.

## Finishing up

Once you have confirmed that the keyboard is working, if you have used a seperate (non handwire specific) controller you will want to secure it in place.  This can be done in many different ways e.g. hot glue, double sided sticky tape, 3D printed caddy, electrical tape.

If you found this fullfilling you could experiment by adding additional features such as [in switch LEDs](https://geekhack.org/index.php?topic=94258.0), [in switch RGB](https://www.reddit.com/r/MechanicalKeyboards/comments/5s1l5u/photoskeyboard_science_i_made_a_handwired_rgb/), [RGB underglow](https://medium.com/@DavidNZ/hand-wired-custom-keyboard-cdd14429c7b3#.7a1ovebsk) or even an [OLED display!](https://www.reddit.com/r/olkb/comments/5zy7og/adding_ssd1306_oled_display_to_your_build/) 

There are a lot of possibilities inside the firmware - explore [docs.qmk.fm](https://docs.qmk.fm) for a full feature list, and dive into the different keyboards to see how people use all of them. You can always stop by [the OLKB subreddit](https://reddit.com/r/olkb) or [QMK Discord](https://discord.gg/Uq7gcHh) for help!

## Links to Other Guides

- [matt3o's step by step guide (BrownFox build)](https://deskthority.net/viewtopic.php?f=7&t=6050) also his [website](https://matt3o.com/hand-wiring-a-custom-keyboard/) and [video guide](https://www.youtube.com/watch?v=LVzpsjFWPP4)
- [Cribbit's "Modern hand wiring guide - stronger, cleaner, easier"](https://geekhack.org/index.php?topic=87689.0) 
- [Sasha Solomon's "Building my first Keyboard"](https://medium.com/@sachee/building-my-first-keyboard-and-you-can-too-512c0f8a4c5f)
- [RoastPotatoes' "How to hand wire a Planck"](https://blog.roastpotatoes.co/guide/2015/11/04/how-to-handwire-a-planck/)
- [Masterzen's "Handwired keyboard build log"](https://www.masterzen.fr/2018/12/16/handwired-keyboard-build-log-part-1/)


# Legacy Content

This page used to include more content. We have moved a section that used to be part of this page its own page. Everything below this point is simply a redirect so that people following old links on the web find what they're looking for.

## Preamble: How a Keyboard Matrix Works (and why we need diodes) :id=preamble-how-a-keyboard-matrix-works-and-why-we-need-diodes

* [How a Keyboard Matrix Works](how_a_matrix_works.md)
