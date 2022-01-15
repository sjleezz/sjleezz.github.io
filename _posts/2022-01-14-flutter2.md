---
layout: post
title: flutter 만들기
subtitle: flutter를 이용한 APP만들기 (1) - 설치
categories: flutter
tags: [flutter, Android, IOS]
---

 이전에 프로젝트 진행 과정에서 만든 파이썬 코드를 웹과 안드로이드, ios 모두에서 돌릴 수 있도록 해야 하는 일이 있었는데, beeware, Kivy 등을 이용하여 진행했지만 불편함이 많았다. 그러나 Flutter를 이용하여 하나의 코드로 Web/AOS/IOS 모든 서비스를 제공할 수 있는 크로스 플랫폼의 강력함은 가히 매력적이라고 할 수 있다. 
 
 본 포스트에선 Flutter의 시작과 기초적인 앱을 만드는 과정을 작성하고자 한다. 

**해당 포스트는 [재즐보프채널](https://www.youtube.com/watch?v=Yt-DjG5b4iA&list=PLnIaYcDMsScxP2Nl8pEbmI__wkF0YVu0a&index=1)을 참고하여 작성되었음을 알립니다.**


## 1. Flutter 설치

우선 [안드로이드 스튜디오](https://developer.android.com/studio?hl=ko)를 설치한다.

안드로이드 스튜디오 설치는 위 링크의 잘 정리된 공식 문서를 따라서 만들면 된다.

[Flutter](https://docs.flutter.dev/get-started/install)에서 SDK 파일을 다운로드하고 압축 해제한다.   
(다운로드 경로를 기억해두면 좋다)

Flutter SDK를 설치했다면, 해당 설치 폴더 내의 flutter_console.bat을 실행한다.

실행 후 다음 명령어를 입력한다.

```
flutter doctor
```
본 명령어는 flutter 실행을 위한 필수 프로그램들을 점검하는 코드이다.

해당 코드를 실행하면 체크표시들과 함께 설치된 프로그램들의 목록이 나온다.

Accetp들을 다 y로 하나 하나 넘기고 나면, No issues found! 라고 뜨며 점검이 완료된다.

---

**오류가 발생하는 경우**

```
X cmdline-tools component is missing
...
```
```
X Android license status unknown.
...
```
위와 같이 오류가 나오는 경우, 안드로이드 스튜디오를 들어가서 Tools > SDK Manager > SDK Tools탭에 들어간다.

우하단의 Hide Obsolete Packages의 체크를 해제하면 Android SDK Tools (Obsolete)가 나타나는데, 이것이 체크되어 있지 않았다면 체크 후 설치한다.

만일 Android SDK Command-line Tools (latest)가 설치되어 있지 않다면 이 역시 체크 후 설치한다.

다시 flutter doctor를 실행하면, 첫번째 오류는 해결되고 두번째 에러가 그대로 남아 있을 수 있는데, 오류 description을 살펴보면 
```
Run `flutter doctor --android-licenses` to accept the SDK licenses.
```
라고 나와 있음을 알 수 있다. 이를 따라서 
```
flutter doctor --android-licenses
```
를 실행하고 다시 flutter doctor를 실행하면 해결되었을 것이다.

**만일 해결이 되지 않았다면 안드로이드 스튜디오와 Flutter SDK를 모두 삭제하고 다시 설치해보길 바랍니다.**

---

## 2. Flutter 프로젝트 실행

안드로이드 스튜디오, Flutter가 모두 설치되어있다면 Flutter로 프로젝트를 만들 차례이다.

이전까지는 Java나 kotlin을 이용하여 프로젝트를 만들었지만, 이젠 Flutter를 이용하여 만들어 볼 것이다.

우선 안드로이드 스튜디오 첫 화면의 plugins 에서 flutter를 검색하여 설치해야한다.

설치가 완료되고 다시 스튜디오를 껐다 켜면 New Flutter Project 버튼이 보일 것이다. 이를 클릭한다.

Flutter SDK가 설치된 주소를 지정해주고 Next를 누르고 프로젝트 명과 서비스를 제공할 플랫폼들을 선택하고 Finish를 누르면 실행이 완료된다.








