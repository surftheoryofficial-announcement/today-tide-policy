---
title: 광고 및 분석 공지
description: Ads and analytics notice for Today's Tide.
---

# 광고 및 분석 공지

최종 업데이트: 2026년 6월 30일

이 문서는 `오늘의 간만조` / `Today's Tide` 앱의 광고 및 분석 처리 상태를 설명합니다.

## 현재 첫 제출 후보 상태

현재 첫 제출 후보는 비광고 release입니다. 앱 안에는 향후 광고 활성화를 위한 기능
코드나 화면 영역이 준비되어 있을 수 있지만, 아래 조건을 만족하는 제출 빌드는
`광고 없음` 후보로 관리합니다.

- 현재 제출 후보에서는 사용자에게 광고를 표시하지 않습니다.
- Android release 산출물에는 Google Mobile Ads SDK runtime, Android Advertising ID
  권한, Android Ad Services 권한, AdMob application metadata를 포함하지 않는 방향으로
  검증합니다.
- iOS release 후보는 Google Mobile Ads SDK를 링크하지 않고,
  `GADApplicationIdentifier`, `SKAdNetworkItems`, IDFA, App Tracking Transparency
  직접 사용 없이 제출하는 방향으로 검증합니다.
- Google Play의 광고 포함 여부와 App Store의 Tracking/Data Used to Track You 답변은
  실제 제출 바이너리와 콘솔 SDK 안내를 기준으로 최종 확인합니다.

광고 UI만 숨겼더라도 release 산출물에 광고 SDK나 광고 식별자 관련 권한이 포함되는
경우에는 SDK가 처리할 수 있는 데이터가 Google Play Data safety 또는 App Store App
Privacy 답변에 영향을 줄 수 있습니다. 이 경우 광고가 화면에 보이지 않더라도 최종
바이너리와 스토어 콘솔 안내를 기준으로 보수적으로 다시 고지합니다.

## Firebase Analytics

앱은 Firebase Analytics를 사용하여 앱 사용 흐름과 위젯 동작 안정성을 파악할 수
있습니다. 예를 들어 앱 실행, 해변 선택, 위젯 추가/삭제, 위젯 탭, 데이터 갱신
성공/실패 같은 이벤트가 기록될 수 있습니다.

분석 이벤트에는 사용자가 이메일로 작성한 문의 내용, 이름, 전화번호, 결제정보,
건강정보 같은 민감한 개인정보를 포함하지 않습니다.

Firebase Analytics 및 Google Analytics 처리 범위는 Google Play Data safety,
App Store privacy labels, 공개 개인정보처리방침과 일치하도록 관리합니다.

## 향후 광고 활성 빌드

나중에 광고를 활성화하는 빌드를 제공하는 경우, 실제 광고 SDK 포함 여부와 광고
설정에 맞춰 다음 항목을 다시 갱신합니다.

- 이 광고 및 분석 공지
- 개인정보처리방침
- Google Play Data safety 답변
- App Store App Privacy 답변
- iOS IDFA/App Tracking Transparency 사용 여부
- Android Advertising ID 및 Android Ad Services 권한 포함 여부

광고 활성 빌드에서는 Google Mobile Ads SDK 및 광고 파트너가 광고 제공, 측정,
부정 이용 방지를 위해 정보를 처리할 수 있습니다. iOS에서 IDFA/App Tracking을
사용하는 광고 구성이 적용되는 경우 Apple의 App Tracking Transparency 흐름에 따라
별도로 관리합니다.

## 관련 문서

- 개인정보처리방침:
  https://surftheoryofficial-announcement.github.io/today-tide-policy/privacy-policy
- 지원:
  https://surftheoryofficial-announcement.github.io/today-tide-policy/support

## 참고한 플랫폼 기준

- Google Play Advertising ID:
  https://support.google.com/googleplay/android-developer/answer/6048248
- Google Mobile Ads SDK Android setup:
  https://developers.google.com/admob/android/quick-start
- Apple App Privacy Details:
  https://developer.apple.com/app-store/app-privacy-details/
- Apple User Privacy and Data Use:
  https://developer.apple.com/app-store/user-privacy-and-data-use/
