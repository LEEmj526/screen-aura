# Privacy / 개인정보

Screen Aura has no analytics, advertising, screen capture, global input monitoring or user account. It does not request Screen Recording, Accessibility, camera or microphone permissions.

Settings are stored in `~/Library/Application Support/ScreenAura/`. Exported JSON contains selected display identifiers, settings and user-entered bundle IDs for app exclusions and Pro profiles. It never includes the license key. The frontmost app bundle ID is read in memory to apply those rules; document titles, screen pixels, inputs and app-use history are not collected. Charging state comes from macOS power-source notifications.

An optional 14-day trial and Pro license record are stored in the local macOS Keychain (`local.codex.ScreenAura.commerce`, account `entitlement-v1`). License activation sends the entered key and Screen Aura Pro product ID to `https://api.gumroad.com/v2/licenses/verify` using HTTPS. Activation requires a network connection. An activated license is rechecked at launch after 24 hours; a connection failure keeps the cached activation, while a refund, chargeback or revoked key returns the app to Free. The app does not store buyer email or payment data. Payment and receipt delivery happen on Gumroad under its privacy policy.

Removing the app does not automatically remove preferences or the Keychain record. You can forget the license from Pro settings; this preserves the used trial record. Delete the named Keychain item yourself if you want to remove the remaining trial data.

한국어: 설정은 Mac의 Application Support 폴더에, 체험·구매 키는 로컬 Keychain에 저장합니다. 앱은 분석·광고·화면 캡처·전역 키 입력 감시를 하지 않습니다. 앱 제외/Pro 프로필을 적용할 때 활성 앱의 bundle ID만 메모리에서 읽습니다. 키 활성화 및 주기적인 재확인 때 Gumroad HTTPS API에 제품 ID와 키를 전송합니다. 구매자 이메일·결제 정보는 앱에 저장하지 않습니다. 네트워크 오류 시 기존 활성화를 유지하며 환불·키 무효화가 확인되면 Free로 돌아갑니다. 설정 JSON에는 구매 키가 포함되지 않습니다.
