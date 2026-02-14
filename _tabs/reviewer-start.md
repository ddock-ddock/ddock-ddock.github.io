---
icon: fas fa-user-shield
order: 3
indent: true
mermaid: true
---

심사역(Reviewer)은 VCworks에서 투자의 전 과정 — 딜소싱, 투자심의, 포트폴리오 관리, 영업보고, 회수 — 을 담당하는 핵심 사용자입니다.
아래 가이드를 통해 주요 업무를 빠르게 시작해보세요.

## 빠른 시작 가이드

<div class="guide-cards">
  <a href="/posts/vs_guide/" class="guide-card">
    <i class="fas fa-gavel"></i>
    <span>투자심의<br/><small>전체 프로세스</small></span>
  </a>
  <a href="/posts/pm0300/" class="guide-card">
    <i class="fas fa-chart-line"></i>
    <span>가치평가</span>
  </a>
  <a href="/posts/br0009/" class="guide-card">
    <i class="fas fa-file-signature"></i>
    <span>심사역 의견<br/><small>작성</small></span>
  </a>
  <a href="/posts/ex0001/" class="guide-card">
    <i class="fas fa-sign-out-alt"></i>
    <span>회수(EXIT)</span>
  </a>
  <a href="/posts/sa0002/" class="guide-card">
    <i class="fas fa-vote-yea"></i>
    <span>의결 응답</span>
  </a>
</div>

<style>
.guide-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-bottom: 2rem;
}
.guide-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 1.5rem 1rem;
  min-width: 140px;
  flex: 1;
  background: var(--card-bg, #f8f9fa);
  border: 1px solid var(--card-border-color, #dee2e6);
  border-radius: 0.5rem;
  text-decoration: none;
  color: var(--text-color, #333);
  transition: transform 0.2s, box-shadow 0.2s;
}
.guide-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  text-decoration: none;
}
.guide-card i {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--link-color, #0066cc);
}
.guide-card span {
  font-size: 0.9rem;
  font-weight: 500;
  text-align: center;
}
.guide-card small {
  font-weight: 400;
  font-size: 0.75rem;
  color: var(--text-muted-color, #6c757d);
}
</style>

---

## 심사역 업무 흐름

- 다음의 항목을 클릭하여 관련 가이드로 바로 이동할 수 있습니다.

```mermaid
flowchart TD
 subgraph s1["투자심의"]
        wr0003["주간회의(딜소싱)"]
        vs0003["투자정보입력"]
        vs0006["투자심의(표결)"]
        ed0001a["계약품의(전자결재)"]
        oi0003["투자 운용지시(전자결재)"]
        vs0009["투자완료(첨부파일등록)"]
  end
 subgraph s2["포트폴리오 관리"]
        pm0100["포트폴리오 정보"]
        pm0300["가치평가"]
        vs0031["담당 심사역 관리"]
  end
 subgraph s3["영업보고"]
        br0009["심사역 의견 작성"]
        br0007["영업보고 검수"]
        br0011["영업보고서 생성"]
  end
 subgraph s4["회수(EXIT)"]
        ex0001["회수위원회(표결)"]
        oi0001["출고 운용지시(전자결재)"]
        ex0007["회수관리"]
  end
 subgraph s5["의결"]
        sa0002["의결 응답"]
        sa0003["의결 정보 반영"]
  end
 subgraph s6["LP보고"]
        lp0600["담당심사역 이력"]
  end
    wr0003 --> vs0003
    vs0003 --> vs0006
    vs0006 --> ed0001a
    ed0001a --> oi0003
    oi0003 --> vs0009
    vs0009 --> pm0100
    pm0100 --> pm0300
    pm0100 --> br0009
    pm0100 --> ex0001
    vs0009 -. 선택적 .-> sa0002
    br0009 --> br0007
    br0007 --> br0011
    ex0001 --> oi0001
    oi0001 --> ex0007
    sa0002 -. 선택적 .-> sa0003
    vs0031 --> lp0600

    click wr0003 "{% post_url 2024-07-09-wr0003 %}"
    click vs0003 "{% post_url 2024-07-10-vs0003 %}"
    click vs0006 "{% post_url 2024-07-11-vs0006 %}"
    click ed0001a "{% post_url 2024-07-12-ed0001a %}"
    click oi0003 "{% post_url 2024-07-13-oi0003 %}"
    click vs0009 "{% post_url 2024-07-14-vs0009 %}"
    click pm0300 "{% post_url 2024-09-01-pm0300 %}"
    click vs0031 "{% post_url 2025-04-03-vs0031 %}"
    click br0009 "{% post_url 2024-08-26-br0009 %}"
    click br0007 "{% post_url 2024-08-25-br0007 %}"
    click br0011 "{% post_url 2024-08-27-br0011 %}"
    click ex0001 "{% post_url 2024-07-18-ex0001 %}"
    click oi0001 "{% post_url 2024-07-19-oi0001 %}"
    click ex0007 "{% post_url 2024-07-20-ex0007 %}"
    click sa0002 "{% post_url 2024-09-11-sa0002 %}"
    click sa0003 "{% post_url 2024-09-12-sa0003 %}"
    click lp0600 "{% post_url 2024-11-29-lp0600 %}"

```

---

## 업무 영역별 상세 가이드

<div class="card categories">
  <div id="h_r0" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">투자심의 (딜소싱 → 투자완료)</span>
    </span>
    <a href="#l_r0" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r0-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r0" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs_guide/" class="mx-2"><strong>투자심의 이용 가이드 (전체 프로세스)</strong></a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/wr0003/" class="mx-2">주간보고 (딜소싱)</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs0003/" class="mx-2">투자정보 입력</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs0006/" class="mx-2">예비투심/본투심 표결</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/ed0001a/" class="mx-2">계약품의 및 전자결재</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/oi0003/" class="mx-2">투자 운용지시 및 전자결재</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs0009/" class="mx-2">투자완료 첨부파일</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs_foreign/" class="mx-2">해외(외화) 투자 가이드</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_r1" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">포트폴리오 관리</span>
    </span>
    <a href="#l_r1" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r1-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r1" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <span class="mx-2">포트폴리오 정보</span>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0300/" class="mx-2">가치평가</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0301/" class="mx-2">가치평가 등록 (비상장/투자유형별)</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0302/" class="mx-2">가치평가 등록 (재원별)</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0303/" class="mx-2">가치평가 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs0031/" class="mx-2">담당 심사역 관리</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_r2" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">영업보고</span>
    </span>
    <a href="#l_r2" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r2-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r2" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0009/" class="mx-2">심사역 의견 작성</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0007/" class="mx-2">영업보고 검수</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0008/" class="mx-2">영업보고 AI 검수</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0011/" class="mx-2">영업보고서 생성</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_r3" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">회수 (EXIT)</span>
    </span>
    <a href="#l_r3" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r3-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r3" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/ex0001/" class="mx-2">회수위원회 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/ex0007/" class="mx-2">회수관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/oi0001/" class="mx-2">회수 운용지시 (전자결재)</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_r4" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">의결</span>
    </span>
    <a href="#l_r4" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r4-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r4" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/sa0002/" class="mx-2">의결 응답</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/sa0003/" class="mx-2">의결 정보 반영</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_r5" class="card-header d-flex justify-content-between hide-border-bottom">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">LP보고 (심사역 관련)</span>
    </span>
    <a href="#l_r5" data-bs-toggle="collapse" aria-expanded="false"
       aria-label="h_r5-trigger" class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </a>
  </div>
  <div id="l_r5" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0600/" class="mx-2">담당심사역 이력</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0630/" class="mx-2">투자심사 보고</a>
      </li>
    </ul>
  </div>
</div>

---

> 심사역 권한이 부여되지 않은 경우, 일부 메뉴가 보이지 않을 수 있습니다.
> 권한 설정은 관리역에게 문의하세요.
{: .prompt-tip }

> 해외(외화) 투자 건의 경우, 환율 처리 등 추가 고려사항이 있습니다.
> [해외 투자 가이드](/posts/vs_foreign/)를 참고하세요.
{: .prompt-info }

버그 및 문의 사항은 다음 이메일로 보내주세요: **[we@dkdk.kr](mailto:we@dkdk.kr)**
