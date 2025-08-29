<<<<<<< HEAD
# Bapsim
소규모 단위 프로젝트


# 🍽️ 밥심(Bapsim)

**1인 가구와 혼밥족을 위한, 외롭지 않은 식사 플랫폼**

---

## 🎯 기획 배경

- 1인 가구의 지속적인 증가와 함께 ‘혼밥’이 일상이 되었지만, 여전히 외롭고 어색함을 느끼는 사람들이 많습니다.
- 혼밥족을 위한 정보, 장소, 사람을 연결해주는 전용 플랫폼이 부재합니다.

---

## 💡 주요 서비스

| 기능 영역 | 설명 |
|-----------|------|
| 🗺️ 혼밥지도 | 현재 위치 기반으로 혼밥하기 좋은 장소 추천 (혼밥 가능 여부) | => AI를 사용하여 추천도 고려
| 🤝 혼밥메이트 | 관심사/위치 기반으로 혼밥 같이 할 사람 매칭 |
| 📚 혼밥 콘텐츠 | 자취생 요리법, 혼밥 팁, 후기 등 정보 큐레이션 |
| 📷 인증/리뷰 | 식사 사진 인증, 혼밥 후기 공유 |
| 🔔 푸시 알림 | 근처 추천 식당, 혼밥 요청 알림 등 제공 |

---

## 👥 타겟 사용자

- 20~40대 1인 가구
- 혼밥에 익숙하지 않거나 외로움을 느끼는 사용자
- 자취생, 유학생, 출장/여행 중 혼자 식사하는 사람

---

## 🚀 차별성 / 장점

- 위치기반 + 혼밥 특화 정보 제공
- 혼밥에 대한 감정적 공감 제공
- 커뮤니티/메이트 기능으로 정서적 연결 제공
- 타겟이 명확하고 지속적인 수요 존재

---

## 🛠️ 기술 스택

### 사용한 외부 라이브러리 정리

### 프론트엔드
- `React Native` + `TypeScript`
  - 크로스플랫폼 대응 (iOS/Android)
  - 기존 React/Next.js 경험 살려 개발 가능
  -  UI/UX도 유연하고 푸시, 위치 등 기능 확장 쉬움 (외부라이브러리 npm)
     
### 백엔드 & Infrastructure
   - `Firebase`
     - Platform: Google의 BaaS(Backend as a Service) 플랫폼을 메인 백엔드로 사용.
     - Core Roles:
       - Authentication: 이메일/비밀번호 가입, 소셜 로그인(Google, Apple 등)을 포함한 모든
         사용자 인증을 처리.
       - Database: Firestore(NoSQL DB)를 사용하여 앱의 모든 데이터(사용자 정보, 게시물,
         '밥심' 데이터 등)를 저장하고 관리.
       - File Storage: Cloud Storage를 사용하여 사용자 프로필 이미지 등 미디어 파일 저장.
       - Push Notifications: Firebase Cloud Messaging(FCM)을 통해 사용자에게 푸시 알림 전송.
       - Serverless Logic: Cloud Functions를 사용하여 특정 이벤트(예: 새 사용자 가입, 신고
         접수)에 반응하는 간단한 서버 사이드 로직 처리.
       - Real-time Sync: Firestore의 실시간 동기화 기능을 활용하여 '혼밥메이트' 매칭, 채팅 등
         실시간 기능 구현.

### 배포/인프라 <-이거는 생각좀 해봐야함
- `AWS` (EC2, RDS, S3) 또는 `Firebase Hosting`

---

## 🧪 우선순위 기능

1. 로그인/회원가입 (소셜 로그인 포함)
2. 위치 기반 혼밥 장소 추천
3. 콘텐츠 피드 (혼밥 팁, 후기 등)
4. 사진 인증 및 간단 후기 작성
5. 혼밥 메이트 요청 및 매칭 기능(미루니)

---

## 💰 수익 모델

- 지역 식당 광고/제휴
- 프리미엄 매칭 서비스
- 혼밥 챌린지 → 굿즈/쿠폰 리워드
- 제휴 브랜드 마케팅 (편의점, 배달앱 등)

---

## 📌 향후 계획 (RoadMap)

### 1. 🔍 사전 조사 및 기획 단계 (1~2주차)

- [x] 기획서 정리 및 깃허브 업로드
- [x] 팀원역할 배분
- [x] 기능 우선순위 정의
- [x] 깃허브 저장소 생성 및 초기 세팅
  
### 2. ✏️ UI/UX 설계 단계 (1~2주차)

- [ ] 사용자 플로우 정의 (회원가입 → 혼밥 장소 탐색 → 메이트 매칭 등)  
- [ ] 와이어프레임 제작 (Figma 사용)  
- [ ] UI 디자인 가이드 정리 (색상, 폰트, 아이콘 등)  
- [ ] 반응형 고려한 모바일 중심 설계 (중요)

### 3. ⚙️ 개발 준비 단계 (1주차)

- [ ] 프로젝트 폴더 구조 설계 (Front: React Native + TypeScript / Back: Firebase)  
- [ ] React Native 환경 구성 (Expo or CLI) 및 TypeScript 설정  
- [ ] Firebase 연동 준비 (OAuth, FCM 등)  
- [ ] Git 브랜치 전략 수립 (main, develop, feature/*)  
- [ ] CI/CD 기초 설정 (GitHub Actions + Firebase Hosting or AWS CodeDeploy)

### 4. 🧪 개발 단계 (2주차)

**Front-end**
- [ ] 로그인/회원가입 (Google 소셜 로그인 포함, 가능하면 카톡도)  
- [ ] 위치 기반 혼밥 장소 리스트 페이지  
- [ ] 혼밥 메이트 요청 및 매칭 UI  
- [ ] 후기 / 정보 콘텐츠 피드 구현  

**Back-end**
- [ ] Spring Boot 기반 API 서버 구축  
- [ ] 회원/장소/메이트/후기 관련 DB 설계  
- [ ] JWT 인증 및 보안 처리  
- [ ] Firebase 연동 (푸시 알림, 실시간 채팅 가능성 검토)  

### 5. 🧑‍🔬 테스트 및 피드백 단계 (3주차)
- [ ] 클로즈드 베타 테스터 모집 (주변 지인 or 커뮤니티)  
- [ ] 사용자 행동 분석 (Hotjar 또는 Firebase Analytics)  
- [ ] 피드백 기반 기능 개선 및 UI 수정  
- [ ] 버그 수정 및 안정화 작업


### 6. 📈 확장 및 운영 단계
- [ ] 정기적 콘텐츠 업데이트 (혼밥 팁, 유저 후기)  
- [ ] 기능 추가 계획: 실시간 매칭, AI 기반 추천 등  
- [ ] 커뮤니티 활성화를 위한 게시판/댓글 도입  
- [ ] 수익화 모델 도입 (프리미엄, 제휴광고 등)

---

## ⚠️ 현재 문제점
- [ ] 프로젝트 이름 미정
- [ ] 데이터 확보의 어려움 ('혼밥맵'이 유용하려면 충분한 식당 데이터가 있어야 하고, '혼밥메이트'가 활성화되려면 충분한 사용자가 있어        야 함. 처음에는 두 가지 모두 부족
- [x] * [사용자 안전 문제 (각종 범죄, 노쇼)](#사용자-안전-문제)

## ⚠️ 예상되는 문제점과 대응 방안

1. 📱 React Native와 Firebase의 호환 이슈
- 문제 가능성: Firebase의 일부 기능(특히 푸시 알림, 인증)은 React Native에서 native module 설정이 필요함.
  ㄴ native module 사용 이유
    ㄴ iOS와 Android에서 동일한 기능을 구현
    ㄴ 네이티브 코드로 인한 메모리 감소 ⬇️, 성능 향상 ⬆️
- 대응 방안:
    - Expo 사용 시 expo-firebase-* 패키지로 쉽게 구현 가능하지만, 특정 기능은 eject가 필요함.
      
2. 🔐 Firebase 인증 및 보안 설정 미숙
- 문제 가능성: 인증 흐름이 복잡하거나, Firestore/Realtime DB 권한 설정이 미흡할 경우 보안 취약.
- 대응 방안:
    - Firebase의 보안 규칙(Security Rules)을 철저히 설계.
    - ⭐⭐ 민감 데이터는 Firebase 대신 Spring Boot + DB에서 처리하고 토큰만 연동.
    - ⭐ 인증 관련 흐름 (가입 → 토큰 발급 → 세션 관리) 미리 플로우차트로 정리해 둘 것.

---

## 🅰️ 해결!
### 사용자 안전 문제
      1. 명칭과 시각화 구체화: '밥심' 시스템
        - 아이콘: 텍스트와 함께 직관적인 아이콘을 사용합니다.
             - 찬밥 (신뢰도 최하): 금이 가거나 이가 빠진 밥그릇, 혹은 파란색의 차가운 느낌.
             - 미지근한 밥 (보통): 평범한 흰 밥그릇.
             - 따끈한 밥 (신뢰도 좋음): 김이 모락모락 나는 밥그릇.
             - 윤기나는 밥 (신뢰도 최상): 황금색으로 빛나거나 윤기가 흐르는 밥.
        - 게이지 바: 프로필에 밥 아이콘과 함께 '밥심 게이지'를 두어, 다음 단계까지 얼마나
                남았는지 시각적으로 보여주면 사용자의 참여를 더 효과적으로 유도
         
      2. 시스템 세분화 및 게임 요소 도입
        - 세분화된 평가 태그:
             - 밥심을 올리는 태그 (긍정): 식사 약속 후 상대방에게 칭찬 태그를 남길 수 있습니다.
             - (예: "맛집 네비게이터", "분위기 메이커", "깔끔한 식사매너", "시간 칼같아요")
             - 밥심을 내리는 태그 (부정):
             - (예: "프로 지각러", "대화가 불편했어요", "노쇼!")
        - '밥심' 등급과 칭호 부여:
             - 일정 '밥심' 점수를 달성하면 등급이 오르고 특별한 칭호를 부여합니다.
             - (예: 새싹 밥친구 → 든든한 밥친구 → 밥장군 → 밥통령)
             - 이 칭호는 프로필에 자랑스럽게 표시되어, 사용자에게 성취감을 줍니다.
        - '첫 밥' 보너스:
             - 첫 '혼밥메이트' 약속을 성공적으로 마치면 '밥심'을 추가로 많이 올려주어, 첫 참여의
                   허들을 낮추고 긍정적인 경험을 심어줍니다.
         
      3. 정책 및 예외 처리
        - '밥이 식는' 시스템 (비활성 페널티): 오랫동안 활동하지 않는 사용자의 '밥심'은 서서히
           떨어지게 만듭니다. ("밥이 식어요!") 이는 지속적인 활동을 유도하는 효과가 있습니다.
        - '노쇼'에 대한 강력한 페널티: 약속 불이행으로 신고가 누적되면 '찬밥' 신세가 되는 것을
           넘어, 일정 기간 '혼밥메이트' 기능을 사용할 수 없도록 제한해야 합니다.
        - 어뷰징 방지: 친구끼리 서로 '밥심'을 올려주는 행위를 막기 위해, 동일한 사용자 간의 평가는
           한 달에 한 번만 '밥심'에 영향을 주도록 제한할 수 있습니다.
         
## ✨ 기여 방법
- 저꾸꾸저꾸로 참여


=======
This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

# Getting Started

> **Note**: Make sure you have completed the [Set Up Your Environment](https://reactnative.dev/docs/set-up-your-environment) guide before proceeding.

## Step 1: Start Metro

First, you will need to run **Metro**, the JavaScript build tool for React Native.

To start the Metro dev server, run the following command from the root of your React Native project:

```sh
# Using npm
npm start

# OR using Yarn
yarn start
```

## Step 2: Build and run your app

With Metro running, open a new terminal window/pane from the root of your React Native project, and use one of the following commands to build and run your Android or iOS app:

### Android

```sh
# Using npm
npm run android

# OR using Yarn
yarn android
```

### iOS

For iOS, remember to install CocoaPods dependencies (this only needs to be run on first clone or after updating native deps).

The first time you create a new project, run the Ruby bundler to install CocoaPods itself:

```sh
bundle install
```

Then, and every time you update your native dependencies, run:

```sh
bundle exec pod install
```

For more information, please visit [CocoaPods Getting Started guide](https://guides.cocoapods.org/using/getting-started.html).

```sh
# Using npm
npm run ios

# OR using Yarn
yarn ios
```

If everything is set up correctly, you should see your new app running in the Android Emulator, iOS Simulator, or your connected device.

This is one way to run your app — you can also build it directly from Android Studio or Xcode.

## Step 3: Modify your app

Now that you have successfully run the app, let's make changes!

Open `App.tsx` in your text editor of choice and make some changes. When you save, your app will automatically update and reflect these changes — this is powered by [Fast Refresh](https://reactnative.dev/docs/fast-refresh).

When you want to forcefully reload, for example to reset the state of your app, you can perform a full reload:

- **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Dev Menu**, accessed via <kbd>Ctrl</kbd> + <kbd>M</kbd> (Windows/Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (macOS).
- **iOS**: Press <kbd>R</kbd> in iOS Simulator.

## Congratulations! :tada:

You've successfully run and modified your React Native App. :partying_face:

### Now what?

- If you want to add this new React Native code to an existing application, check out the [Integration guide](https://reactnative.dev/docs/integration-with-existing-apps).
- If you're curious to learn more about React Native, check out the [docs](https://reactnative.dev/docs/getting-started).

# Troubleshooting

If you're having issues getting the above steps to work, see the [Troubleshooting](https://reactnative.dev/docs/troubleshooting) page.

# Learn More

To learn more about React Native, take a look at the following resources:

- [React Native Website](https://reactnative.dev) - learn more about React Native.
- [Getting Started](https://reactnative.dev/docs/environment-setup) - an **overview** of React Native and how setup your environment.
- [Learn the Basics](https://reactnative.dev/docs/getting-started) - a **guided tour** of the React Native **basics**.
- [Blog](https://reactnative.dev/blog) - read the latest official React Native **Blog** posts.
- [`@facebook/react-native`](https://github.com/facebook/react-native) - the Open Source; GitHub **repository** for React Native.
>>>>>>> db2fceb (Initial commit)
