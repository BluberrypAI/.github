## TEAM 블루베리 파이 (BluberrypAI)

<img width="1200" height="560" alt="SCRAP" src="https://github.com/user-attachments/assets/f4bfdad9-2afd-4ac1-b474-a69405f9c725" />

### 서비스: SCRAP

> 버려지는 자원을 연결하고 안내한다

중소 제조 사업장의 폐기물을 **분류부터 처리업체 인계까지** 이어 주는 자원순환 네비게이터입니다.
법령 지식이 없는 담당자도 AI 에이전트 **베리**의 문진을 따라가면 폐기물 분류번호를 확정하고, 처리 경로와 업체 후보를 확인한 뒤 위탁 직전 단계까지 갈 수 있습니다.

| 단계 | 하는 일 |
| --- | --- |
| 진단 | 자유 서술과 문진으로 「폐기물관리법 시행규칙」 별표 4 분류번호 확정 |
| 경로 | 분류번호 기준 처리 공정·업체 후보 탐색, 비용·탄소 비교 |
| 기록 | 배출·운반·입고·처리 증빙 기록, 로트별 보고서 |

**원칙: LLM은 제안하고, 규칙 엔진이 판정하고, 서버가 검증합니다.** 분류번호와 허용 처리 유형 판정에는 LLM을 쓰지 않아 같은 입력에는 항상 같은 결과가 나옵니다.

### 레포 구성

| 레포 | 역할 |
| --- | --- |
| [scrap-web](https://github.com/BluberrypAI/scrap-web) | 사용자 화면, 지도·3D 시각화 |
| [scrap-server](https://github.com/BluberrypAI/scrap-server) | API 게이트웨이, 인증·회원, 기업·사업장 정보, DB |
| [scrap-diagnosis](https://github.com/BluberrypAI/scrap-diagnosis) | 폐기물 분류 판정 엔진과 문진 에이전트 |
| [scrap-route](https://github.com/BluberrypAI/scrap-route) | 처리 경로 추천: 지식그래프, RAG, 비용·탄소 계산 |
| [scrap-infra](https://github.com/BluberrypAI/scrap-infra) | 전체 통합 실행, Azure 리소스 정의 |
| [.github](https://github.com/BluberrypAI/.github) | 팀 공통 규칙, 이슈·PR 템플릿 |

```
scrap-web ──▶ scrap-server ──▶ scrap-diagnosis   (분류 판정)
                   │       └──▶ scrap-route       (처리 경로)
                   └──▶ PostgreSQL
```

화면은 server만 호출하고, 레포 사이의 약속은 API 형식뿐입니다. 브랜치는 작업 브랜치 → `develop` → `main`(배포) 순서이며, 자세한 규칙은 [CONTRIBUTING.md](https://github.com/BluberrypAI/.github/blob/main/CONTRIBUTING.md)에 있습니다.

### 팀원
<table>
  <tr>
    <td align="center" width="160">
      <a href="https://github.com/Ai-pre">
        <img src="https://github.com/Ai-pre.png" width="100" alt="Ai-pre" /><br />
        <b>윤재상</b>
      </a><br />
      Team Leader, KG, AI
    </td>
    <td align="center" width="160">
      <a href="https://github.com/kallin1">
        <img src="https://github.com/kallin1.png" width="100" alt="kallin1" /><br />
        <b>김다인</b>
      </a><br />
      Web Full Stack
    </td>
    <td align="center" width="160">
      <a href="https://github.com/talaria-02">
        <img src="https://github.com/talaria-02.png" width="100" alt="talaria-02" /><br />
        <b>이규석</b>
      </a><br />
      AI
    </td>
    <td align="center" width="160">
      <a href="https://github.com/leena-0">
        <img src="https://github.com/leena-0.png" width="100" alt="leena-0" /><br />
        <b>이나영</b>
      </a><br />
      RAG
    </td>
  </tr>
</table>
