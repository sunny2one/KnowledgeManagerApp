# 지식인 듀얼 매니저

두 개의 WebView를 좌우로 배치한 Android 앱입니다.

- 왼쪽: 네이버 지식인 질문 페이지
- 오른쪽: 사용자가 직접 입력한 나만의 GPT 주소
- 접이식 설정 패널
- 여러 검색 키워드
- 최신순 + 정확도순 TOP3
- 48시간 이내, 답변 5개 이하 필터
- 1초마다 키워드 하나씩 순환 검색
- Telegram Bot API 알림
- 질문 다시 가져오기
- GPT로 보내기
- 답변 다시 가져오기
- 네이버에 붙여넣기
- 마지막 URL, 화면 비율, 설정값 저장

## GitHub에서 APK 만들기

1. 새 GitHub 저장소를 만듭니다.
2. 이 폴더의 파일을 전부 업로드합니다.
3. `Actions` 탭에서 `Build APK`를 실행합니다.
4. 완료 후 `Artifacts`의 `KnowledgeInDual-debug-apk`를 받습니다.

## 주의

네이버와 ChatGPT의 HTML 구조가 변경되면 JavaScript 선택자를 수정해야 할 수 있습니다.
1초 검색은 네이버 측에서 과도한 요청으로 판단될 수 있으므로 앱에는 오류 시 자동 대기 로직이 포함되어 있습니다.


> GitHub Actions는 Gradle 8.9를 직접 설치하므로 wrapper JAR가 없어도 빌드됩니다.
