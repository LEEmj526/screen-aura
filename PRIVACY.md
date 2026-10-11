# Privacy / 개인정보

이 개발 버전의 데이터는 Mac에만 저장합니다. 서버, 회원가입, 원격 분석, 광고, 화면 캡처, 키보드/마우스 전역 감시, 마이크/카메라 사용이 없습니다. Screen Recording, Accessibility TCC, Input Monitoring 권한을 요청하지 않습니다.

활성 앱의 bundle ID는 사용자가 지정한 앱 제외 규칙과 비교하기 위해 메모리에서만 읽습니다. 앱 사용 이력, 창 위치, 문서 제목, 화면 픽셀 또는 입력 내용을 수집하지 않습니다. 사용자 지정 제외 목록과 화면 UUID 선택은 로컬 설정과 사용자가 내보낸 JSON에 포함됩니다.

설정 위치: `~/Library/Application Support/ScreenAura/`. 선택한 테마·색상·화면 선택·시간표·집중 세션·언어·온보딩 상태가 저장됩니다. 손상 파일은 같은 폴더에 사본으로 보존합니다. 가져오기/내보내기는 macOS 파일 선택 창에서 사용자가 지정한 파일에만 접근합니다. 진단 파일은 자동 생성하지 않습니다.

이 버전은 라이선스나 결제 정보를 저장하지 않고 네트워크 요청을 하지 않습니다. 추후 라이선스/업데이트 기능을 연결할 때에는 이 정책을 갱신하고 사용자에게 목적을 설명해야 합니다.

This development build stores preferences locally, reads only the frontmost bundle ID for user-defined exclusions, and has no network client, telemetry, screen recording, input monitoring or account system. Exported JSON includes the exclusions and display identifiers chosen by the user. No commerce secrets are present.
