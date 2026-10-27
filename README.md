# 름셰브 (reumshev-agent)

내 PC와 내 보안 연결이 지금 괜찮은지 한 화면에서 정직하게 보여 주는 보안 Agent 앱입니다. 작성: 장아름(reum2kr), SKT ALEPH 과정 학생 프로젝트.

## 먼저 알아 둘 것

- **앱은 `on-client` 폴더 안에 있습니다.** 이 맨 위 폴더에서 실행하면 「-File 매개 변수에 대한 인수 … 없습니다」 오류가 납니다.
- 필요한 것: Windows, PowerShell, Node.js 22~24(수업 기준 24.19.0, 24.22.0에서도 실행 확인). `npm install`은 필요 없습니다.

## 바로 실행 (3단계)

1. `on-client` 폴더에서 PowerShell을 엽니다. 탐색기의 빈 곳에서 마우스 오른쪽 버튼 → 터미널에서 열기를 누르고, 프롬프트 끝이 `\on-client>`인지 봅니다.
2. 아래 **한 줄 전체**를 그대로 붙여 넣고 Enter를 누릅니다. 맨 앞 `powershell`까지 포함합니다. `\`가 `₩`로 보여도 같은 글자입니다.

       powershell -NoProfile -ExecutionPolicy Bypass -File .\tools\start-alekov.ps1

3. 「케셰브가 켜졌습니다」가 나오면 브라우저에서 아래 주소를 엽니다. 「보호 현황」 맨 위의 「름셰브 핵심 3가지」가 첫 화면입니다.

       http://127.0.0.1:5189/

화면 맨 위의 빨간 상자와 `[ENGINE_NOT_CONNECTED]`가 붙은 빨간 칸 여러 개는 **정상**입니다. 회사 시스템(SDP)이 아직 연결되지 않았다는 뜻이며, 앱 고장이 아닙니다.

끌 때는 앱을 켤 때 명령을 입력했던 PowerShell(터미널) 창, 곧 「끄려면 이 창에서 Ctrl+C 를 누르세요.」가 보이는 창을 클릭하고 Ctrl+C를 누릅니다.

## 자세한 안내

- 실행 절차, 정상 신호, 오류별 대처: [`on-client/docs/STUDENT_RUNBOOK.md`](on-client/docs/STUDENT_RUNBOOK.md) 4장, 8장
- 시연 순서, 제공·직접 만든 부분, 한계와 근거(7일차 완성 기록): [`on-client/docs/ALEPH_FINAL_WORK_RECORD.md`](on-client/docs/ALEPH_FINAL_WORK_RECORD.md)
- 재현 기록과 실제로 확인한 범위: [`on-client/docs/RELEASE_RECORD.md`](on-client/docs/RELEASE_RECORD.md)
- 화면의 **[실측]**은 이 PC에서 실제로 읽은 값, **[예시]**는 설명용 값, **확인 불가**는 읽지 못한 값입니다. 지금 시작 틀(0.2.11)에서는 PC 실측이 0개이고 회사 시스템(SDP)도 미연결입니다.
