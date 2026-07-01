---
title: 광고 및 분석 공지
description: Ads and analytics notice for Today's Tide.
---

# 광고 및 분석 공지

최종 업데이트: 2026년 7월 1일

이 문서는 `오늘의 간만조` / `Today's Tide` 앱의 광고 및 분석 처리 상태를
설명합니다.

## 현재 광고 송출 상태

현재 Android와 iOS 앱은 Google Mobile Ads SDK 기반 홈 화면 배너 광고를 표시할 수
있는 광고 활성 릴리스로 운영됩니다. Android와 iOS 모두 실제 AdMob 앱 ID와 광고
단위 ID를 사용하며, 앱의 홈 화면 하단 광고 영역에서 광고 요청이 발생할 수
있습니다.

Google Play의 현재 비공개 테스트 배포 범위는 대한민국으로 제한되어 있습니다.
Android에서 EEA, UK, Switzerland 등 별도 광고 동의 요구 지역을 열거나 해당
지역으로 광고 송출을 확장하는 경우 Google EU user consent policy에 맞춰 Android
UMP 또는 Google 인증 CMP 흐름을 추가하고, 본 공지, 개인정보처리방침, Google Play
Data safety 답변을 함께 갱신합니다.

iOS 앱은 Google User Messaging Platform을 포함하며, 광고 동의 또는 개인정보 선택
화면이 필요한 지역에서는 SDK가 제공하는 흐름에 따라 표시될 수 있습니다. App Store
사용 가능 국가 또는 지역을 제한하는 경우 App Store Connect의 가격 및 사용 가능
여부 설정을 별도로 관리합니다.

## Google Mobile Ads

광고가 표시되는 릴리스에서는 Google Mobile Ads SDK 및 광고 파트너가 광고 제공,
측정, 부정 이용 방지, 광고 품질 관리를 위해 정보를 처리할 수 있습니다. 처리될 수
있는 정보에는 앱 상호작용, 진단 정보, 기기 또는 앱 식별자, IP 주소 등 일반적인
기술 정보가 포함될 수 있습니다.

Android 릴리스는 Google Mobile Ads SDK, AdMob application metadata, Android
Advertising ID 권한을 포함합니다. iOS 릴리스는 Google Mobile Ads SDK, Google User
Messaging Platform, `GADApplicationIdentifier`, Google Mobile Ads
`SKAdNetworkItems`를 포함합니다.

iOS 앱은 현재 `AdSupport`, `AppTrackingTransparency`,
`advertisingIdentifier`, `NSUserTrackingUsageDescription` 직접 사용 없이 관리합니다.
향후 IDFA 또는 App Tracking Transparency 흐름을 사용하는 광고 구성이 적용되는
경우 Apple의 App Tracking Transparency 흐름과 App Store privacy labels에 맞춰
별도로 갱신합니다.

## Firebase Analytics

앱은 Firebase Analytics를 사용하여 앱 사용 흐름과 위젯 동작 안정성을 파악할 수
있습니다. 예를 들어 앱 실행, 해변 선택, 위젯 추가/삭제, 위젯 탭, 데이터 갱신
성공/실패 같은 이벤트가 기록될 수 있습니다.

분석 이벤트에는 사용자가 이메일로 작성한 문의 내용, 이름, 전화번호, 결제정보,
건강정보 같은 민감한 개인정보를 포함하지 않습니다.

Firebase Analytics 및 Google Analytics 처리 범위는 Google Play Data safety,
App Store privacy labels, 공개 개인정보처리방침과 일치하도록 관리합니다.

## app-ads.txt

AdMob `app-ads.txt`는 GitHub Pages 개발자 웹사이트에 게시된 상태로 관리합니다.
AdMob은 스토어에 등록된 개발자 웹사이트의 host를 기준으로
`https://<host>/app-ads.txt` 위치를 크롤링하므로, 스토어 개발자 웹사이트 URL과
AdMob의 app-ads.txt 확인 상태를 함께 관리합니다.

## 관련 문서

- 개인정보처리방침:
  https://surftheoryofficial-announcement.github.io/today-tide-policy/privacy-policy
- 지원:
  https://surftheoryofficial-announcement.github.io/today-tide-policy/support

## 참고한 플랫폼 기준

- Google Play Data safety:
  https://support.google.com/googleplay/android-developer/answer/10787469
- Google Mobile Ads SDK Android data disclosure:
  https://developers.google.com/admob/android/privacy/play-data-disclosure
- Google Mobile Ads SDK iOS data disclosure:
  https://developers.google.com/admob/ios/privacy/data-disclosure
- Google AdMob app-ads.txt:
  https://support.google.com/admob/answer/9363762
- Apple App Privacy Details:
  https://developer.apple.com/app-store/app-privacy-details/
- Apple User Privacy and Data Use:
  https://developer.apple.com/app-store/user-privacy-and-data-use/
