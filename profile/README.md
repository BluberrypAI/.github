## 블루베리 파이 (Team BluberrypAI)

<img width="1200" height="560" alt="SCRAP" src="https://github.com/user-attachments/assets/f4bfdad9-2afd-4ac1-b474-a69405f9c725" />

### SCRAP의 솔루션
https://app.scrap-ai.org/

<img width="2560" height="1381" alt="스크린샷(719)" src="https://github.com/user-attachments/assets/60630af5-d184-4f70-80c2-40798d043146" />

법 조문을 근거로 폐기물 분류부터 업체 연결까지의 길을 안내하고, 그 과정을 기록합니다.

중소 제조 사업장의 폐기물을 **분류부터 처리업체 인계까지** 이어 주는 자원순환 네비게이터입니다.
법령 지식이 없는 담당자도 AI 에이전트 **베리**의 문진을 따라가면 폐기물 분류번호를 확정하고, 업체후보 검토를 통해 인계까지 도달할 수 있습니다.

### LLM 활용

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
