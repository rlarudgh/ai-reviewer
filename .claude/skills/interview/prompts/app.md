# App Track - React Native, Flutter

모바일 앱 엔지니어링 실무 역량을 평가합니다. 크로스 플랫폼과 네이티브 연동, 배포/운영 경험에 집중합니다.

## Topic Guide

### React Native
- 아키텍처: Bridge 모델과 New Architecture (Fabric/TurboModules), JSI의 의미
- 성능 최적화: FlatList 가상화, Reanimated를 활용한 애니메이션, 메모리 관리, Hermes 엔진
- 네이티브 모듈: Native Module 작성, 네이티브 라이브러리 연동, Bridging 헤더
- 상태 관리: 모바일 특화 상태 관리, 오프라인 지원, 백그라운드 동기화
- 네비게이션: React Navigation 심화, Deep Linking, 인증 플로우 설계
- 테스팅: Detox E2E, 컴포넌트 테스트, 네이티브 모킹 전략

### Flutter
- Widget 시스템: Widget vs Element vs RenderObject, 트리 구조 이해
- 상태 관리: Riverpod vs Bloc vs GetX 선택 기준, InheritedWidget의 동작 원리
- 네이티브 연동: Platform Channel, FFI, MethodChannel vs EventChannel
- 성능: Widget rebuild 최적화, const 생성자, Isolate 활용, 프로파일링
- 아키텍처: Clean Architecture 적용, Feature-first vs Layer-first 구조
- 테스팅: Widget Test, Integration Test, Golden Test

### 공통 모바일 주제
- 크로스 플랫폼 vs 네이티브: 선택 기준, 트레이드오프 분석
- 앱스토어 배포: iOS/Android 심사 프로세스, 리젝 사례 대응
- OTA 업데이트: CodePush, Fastlane, 무중단 업데이트 전략
- 푸시 알림: FCM/APNs 연동, 백그라운드 처리, 알림 권한 관리
- 보안: 인증서 관리, 난독화, 민감 데이터 저장(Keychain/Keystore)
- 모니터링: Crashlytics, Sentry, ANR/Crash 대응 프로세스

### 실무 시나리오 예시
- "iOS에서만 특정 화면에서 크래시가 발생합니다. Android에서는 정상 동작합니다. 디버깅 접근법은?"
- "앱 시작 시간이 3초 이상 걸립니다. 어떻게 최적화하시겠어요?"
- "카메라/위치 권한을 요구하는 기능에서 사용자가 권한을 거부한 경우 UX를 어떻게 설계하시겠어요?"
- "실시간 채팅 기능을 추가해야 합니다. WebSocket 연결 관리와 오프라인 대응 전략은?"

### 경력 질문 예시
- "React Native에서 Flutter로(또는 반대로) 마이그레이션한 경험이 있나요?"
- "앱스토어 심에서 거절된 경험이 있나요? 원인과 해결 과정을 설명해주세요."
- "모바일 앱의 프로덕션 장애 대응 프로세스를 경험한 적이 있나요?"
- "디자인팀과 네이티브 컴포넌트 스펙을 맞추는 과정에서 어려웠던 점은?"
