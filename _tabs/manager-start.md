---
icon: fas fa-user
order: 4
indent: true
mermaid: true
---

관리역(Manager)은 VCworks에서 조합 결성, 회계/재무, LP보고, 영업보고 관리 등 운영 전반을 담당하는 사용자입니다.
아래 가이드를 통해 주요 업무를 빠르게 시작해보세요.

## 빠른 시작 가이드

<div class="guide-cards">
  <a href="/posts/hr0001/" class="guide-card">
    <i class="fas fa-user-plus"></i>
    <span>구성원 등록</span>
  </a>
  <a href="/posts/fd0001/" class="guide-card">
    <i class="fas fa-folder-plus"></i>
    <span>신규조합 추가</span>
  </a>
  <a href="/posts/se0003/" class="guide-card">
    <i class="fas fa-user-cog"></i>
    <span>역할/권한 관리</span>
  </a>
  <a href="/posts/br0004/" class="guide-card">
    <i class="fas fa-clipboard-list"></i>
    <span>영업보고 요청</span>
  </a>
  <a href="/posts/lc0101/" class="guide-card">
    <i class="fas fa-file-export"></i>
    <span>LP 정기 보고</span>
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
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  background: var(--card-hovor-bg, #e2e2e2);
  text-decoration: none;
}
.content a.guide-card:hover {
  color: var(--text-color, #333) !important;
  border-bottom: none !important;
}
.content a.guide-card:hover i {
  color: var(--link-color, #0066cc) !important;
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

## 관리역 업무 흐름

- 다음의 항목을 클릭하여 관련 가이드로 바로 이동할 수 있습니다.
- 관리역 업무는 규모가 커서 **7개 섹션별 다이어그램**으로 나누어 제공합니다. 섹션 순서는 실제 업무 순서를 따릅니다.
- 전체 흐름을 한눈에 보시려면 [사용 가이드](/core/) 페이지의 overview를 참고해주세요.

### 1. 설정

> 업무 시작 단계 — 구성원 등록, 역할/권한, 회사 정보, 사용자 코드 등 회사 전반의 기초 정보를 설정합니다.

```mermaid
flowchart TD
    hr0001["구성원 등록"] --> hr0002["구성원 정보 수정"]
    hr0002 --> hr0007["조직도 관리"]
    hr0007 --> se0005["사용자 관리"]
    se0005 --> se0003["역할/권한 관리"]
    se0051["회사 정보"]
    my0001["마이페이지"]
    vs_settings["투자 심의 설정"]
    se0201["사용자 코드 관리"]
    se0202["사용자 정의 항목 관리"]
    cm0009["사용자 작업 이력 조회"]
    ed0100["빈품의서"]

    click hr0001 "{% post_url 2024-07-02-hr0001 %}"
    click hr0002 "{% post_url 2024-07-02-hr0002 %}"
    click hr0007 "{% post_url 2024-07-02-hr0007 %}"
    click se0005 "{% post_url 2024-07-02-se0005 %}"
    click se0003 "{% post_url 2024-07-03-se0003 %}"
    click se0051 "{% post_url 2026-04-21-se0051 %}"
    click my0001 "{% post_url 2026-04-21-my0001 %}"
    click vs_settings "{% post_url 2026-04-21-vs-settings %}"
    click se0201 "{% post_url 2026-04-21-se0201 %}"
    click se0202 "{% post_url 2026-04-21-se0202 %}"
    click cm0009 "{% post_url 2025-09-08-cm0009 %}"
    click ed0100 "{% post_url 2024-08-28-ed0100 %}"
```

### 2. 결성

> 다음 단계: 조합 기본 정보 등록 → 출자·배분 → 결성 완료. 모든 결성 필수 항목이 완료되어야 `결성완료` 상태가 됩니다.

```mermaid
flowchart TD
    fd0001["조합생성(개요등록)"] --> fd0010["투자의무달성현황 등록"]
    fd0001 --> fd0011["조합원명부 등록"]
    fd0001 --> fd0009a["금융정보 등록(계좌등록)"]
    fm0010["재원별 회계원장 등록"] --> fd0009a
    fd0009a --> fd0000(("결성완료"))
    fd0010 --> fd0000
    fd0013["필수 필요서류 등록"] --> fd0000
    fd0012["보수정보 등록"] --> fd0000
    fd0011 --> fd0006["출자/배분 등록"]
    fd0006 --> oi0002["출자 운용지시서 등록(전자결재)"]
    oi0002 --> fd0000
    fd0000 --> pr0011["조합원 명부·출자 증서 출력"]

    click fd0001 "{% post_url 2024-07-04-fd0001 %}"
    click fd0010 "{% post_url 2024-07-04-fd0010 %}"
    click fd0011 "{% post_url 2024-07-04-fd0011 %}"
    click fm0010 "{% post_url 2024-07-04-fm0010 %}"
    click fd0009a "{% post_url 2024-07-05-fd0009a %}"
    click fd0013 "{% post_url 2024-07-05-fd0013 %}"
    click fd0012 "{% post_url 2024-07-06-fd0012 %}"
    click fd0006 "{% post_url 2024-07-07-fd0006 %}"
    click oi0002 "{% post_url 2024-07-07-oi0002 %}"
    click pr0011 "{% post_url 2025-04-22-pr0011 %}"
```

### 3. 조합 운영/관리

> 결성 이후 지속적으로 수행하는 **독립 운영 메뉴**들입니다. 서로 순서 관계가 없어 필요한 시점에 개별 사용하시면 됩니다.

<div class="guide-cards">
  <a href="/posts/fd0029/" class="guide-card">
    <i class="fas fa-users"></i>
    <span>조합원 총회</span>
  </a>
  <a href="/posts/fd0060/" class="guide-card">
    <i class="fas fa-exchange-alt"></i>
    <span>지분양도양수 등록</span>
  </a>
  <a href="/posts/fd0004/" class="guide-card">
    <i class="fas fa-chart-pie"></i>
    <span>투자 현황<br/><small>수익률 관리와 연계</small></span>
  </a>
  <a href="/posts/fd0100/" class="guide-card">
    <i class="fas fa-percentage"></i>
    <span>수익률 관리</span>
  </a>
  <a href="/posts/fd0200/" class="guide-card">
    <i class="fas fa-file-invoice-dollar"></i>
    <span>조합원 소득공제</span>
  </a>
</div>

### 4. 거래원장

> 투자 심의를 거친 투자 건 및 기타 변동 사항을 거래원장에 등록하고 전표로 연결합니다. 일반거래/전환거래/인수합병 거래 3종이 모두 전표입력으로 수렴합니다.

```mermaid
flowchart TD
    pm0001["거래원장관리"] --> pm0004["일반거래 등록"]
    pm0001 --> pm0006["전환거래 등록"]
    pm0001 --> pm0008["인수합병 거래 등록"]
    pm0004 --> fm0002_b["전표입력"]
    pm0006 --> fm0002_b
    pm0008 --> fm0002_b

    click pm0001 "{% post_url 2024-07-15-pm0001 %}"
    click pm0004 "{% post_url 2024-07-16-pm0004 %}"
    click pm0006 "{% post_url 2025-09-05-pm0006 %}"
    click pm0008 "{% post_url 2025-09-05-pm0008 %}"
    click fm0002_b "{% post_url 2024-07-17-fm0002 %}"
```

### 5. 영업보고 관리

> STworks 가입 → 템플릿 준비 → 요청 → 검수(AI 검수 포함) → 보고서 생성 단계로 진행됩니다.

```mermaid
flowchart TD
    stworks_invite["STworks 가입 요청"] --> br0001["템플릿 관리"]
    br0001 --> br0004["영업보고 요청"]
    br0012["포트폴리오 연락망"] --> br0004
    br0004 --> br0007["영업보고 검수"]
    br0007 --> br0008["영업보고 AI 검수"]
    br0008 --> br0011["영업보고서 생성"]

    click stworks_invite "{% post_url 2026-04-21-stworks-invite %}"
    click br0001 "{% post_url 2024-08-23-br0001 %}"
    click br0012 "{% post_url 2024-08-22-br0012 %}"
    click br0004 "{% post_url 2024-08-24-br0004 %}"
    click br0007 "{% post_url 2024-08-25-br0007 %}"
    click br0008 "{% post_url 2024-08-25-br0008 %}"
    click br0011 "{% post_url 2024-08-27-br0011 %}"
```

### 6. 회계/재무 흐름

```mermaid
flowchart TD
 subgraph fa1["기초 설정"]
        fm0009["회계기준 및 회계원장"]
        fm0010_b["재원별 회계원장"]
        fm0005["계정과목"]
        fm0011["재무제표 양식"]
        fm0300["자동 전표 설정"]
  end
 subgraph fa2["기장"]
        fm0002["전표 입력"]
  end
 subgraph fa3["조회"]
        fm0003["분개장 조회"]
        fm0021["전표 조회"]
        fm0015["계정별 원장"]
        fm0016["합계 잔액 시산표"]
        fm0018["재무상태표"]
        fm0017["손익계산서"]
  end
 subgraph fa4["마감"]
        fm0012["표준 계정 연결 관리"]
        fm0019["마감/이월"]
  end
 subgraph fa5["자금 관리"]
        fm0008["금융 정보 관리"]
        fm0020["계좌잔액 조회"]
        fm0100["법인 카드 관리"]
        my0200["내 법인 카드 사용 내역"]
  end
    fm0009 --> fm0010_b
    fm0010_b --> fm0005
    fm0005 --> fm0011
    fm0011 --> fm0300
    fm0300 --> fm0002
    fm0002 --> fm0003 & fm0021 & fm0015 & fm0016 & fm0018 & fm0017
    fm0018 --> fm0012
    fm0017 --> fm0012
    fm0012 --> fm0019
    fm0008 --> fm0020
    fm0100 --> my0200
    fm0100 -. 전표 생성 .-> fm0002

    click fm0009 "{% post_url 2024-07-24-fm0009 %}"
    click fm0010_b "{% post_url 2024-07-04-fm0010 %}"
    click fm0005 "{% post_url 2024-07-26-fm0005 %}"
    click fm0011 "{% post_url 2024-07-28-fm0011 %}"
    click fm0300 "{% post_url 2024-07-31-fm0300 %}"
    click fm0002 "{% post_url 2024-07-17-fm0002 %}"
    click fm0003 "{% post_url 2024-08-01-fm0003 %}"
    click fm0021 "{% post_url 2024-08-02-fm0021 %}"
    click fm0015 "{% post_url 2024-08-03-fm0015 %}"
    click fm0016 "{% post_url 2024-08-04-fm0016 %}"
    click fm0018 "{% post_url 2024-08-05-fm0018 %}"
    click fm0017 "{% post_url 2024-08-06-fm0017 %}"
    click fm0012 "{% post_url 2024-07-30-fm0012 %}"
    click fm0019 "{% post_url 2024-07-29-fm0019 %}"
    click fm0008 "{% post_url 2024-08-07-fm0008 %}"
    click fm0020 "{% post_url 2024-08-08-fm0020 %}"
    click fm0100 "{% post_url 2024-08-29-fm0100 %}"
    click my0200 "{% post_url 2024-08-30-my0200 %}"

```

### 7. LP보고

> VICS(벤처투자종합정보시스템) 전자 보고를 위한 메뉴 모음입니다. **초기 설정 → 정기 보고** 흐름은 순서가 있고, **수시 보고**는 이벤트 발생 시 개별 사용하는 병렬 메뉴입니다.

#### 7-1. 초기 설정

> VICSR에서 부여한 ID·코드를 VCworks와 연결하는 단계. 가장 먼저 완료해야 합니다.

```mermaid
flowchart LR
    lp0001["재원별 보고 LP 설정"] --> lp0520["운용기관 인력정보"]
    lp0001 --> lp0510["투자기업 신청정보"]

    click lp0001 "{% post_url 2024-11-29-lp0001 %}"
    click lp0520 "{% post_url 2024-11-29-lp0520 %}"
    click lp0510 "{% post_url 2024-11-29-lp0510 %}"
```

#### 7-2. 정기 보고 (월보고)

> 매월 익월 1~7일에 제출하는 월보고. 아래 항목들을 취합해 `정기 보고(lc0101)`에서 확정·전송합니다.

```mermaid
flowchart LR
    lp0531["운용기관 정보 보고"] --> lc0101["정기 보고"]
    lp0270["상장 주식 거래"] --> lc0101
    lp0310["투자 기업 부가 정보"] --> lc0101
    lp0600["담당심사역 이력"] --> lc0101

    click lc0101 "{% post_url 2024-11-29-lc0101 %}"
    click lp0531 "{% post_url 2024-11-29-lp0531 %}"
    click lp0270 "{% post_url 2024-11-29-lp0270 %}"
    click lp0310 "{% post_url 2024-11-29-lp0310 %}"
    click lp0600 "{% post_url 2024-11-29-lp0600 %}"
```

#### 7-3. 수시 보고

> 투자 집행·조합원 총회 등 **사건 발생 시점에 제출**하는 메뉴들입니다. 각 보고는 독립적이므로 필요한 항목만 사용하시면 됩니다.

<div class="guide-cards">
  <a href="/posts/lp0630/" class="guide-card">
    <i class="fas fa-gavel"></i>
    <span>투자심사 보고</span>
  </a>
  <a href="/posts/lp0635/" class="guide-card">
    <i class="fas fa-file-contract"></i>
    <span>투자 계약서 보고</span>
  </a>
  <a href="/posts/lp0550/" class="guide-card">
    <i class="fas fa-users"></i>
    <span>조합원 총회</span>
  </a>
  <a href="/posts/lp0610/" class="guide-card">
    <i class="fas fa-calendar-check"></i>
    <span>출자금 납입 요청 계획</span>
  </a>
  <a href="/posts/lp0590/" class="guide-card">
    <i class="fas fa-bolt"></i>
    <span>수시 보고<br/><small>일반</small></span>
  </a>
  <a href="/posts/lp0570/" class="guide-card">
    <i class="fas fa-won-sign"></i>
    <span>관리보수/성과보수</span>
  </a>
  <a href="/posts/lp0620/" class="guide-card">
    <i class="fas fa-file-alt"></i>
    <span>반기 보고</span>
  </a>
  <a href="/posts/lp0681/" class="guide-card">
    <i class="fas fa-rocket"></i>
    <span>액셀러레이터 보고</span>
  </a>
</div>

#### 7-4. 전송 이력

> 정기/수시 보고의 전송 이력을 일괄 조회할 수 있습니다.

<div class="guide-cards">
  <a href="/posts/lc0100/" class="guide-card">
    <i class="fas fa-history"></i>
    <span>보고 전송 내역 조회</span>
  </a>
</div>

※ VICS 보고 전체 개요(개념·설치 안내·VICSR 메뉴 매핑표)는 **[VICS 보고 전송 가이드](/posts/vics-guide/)**를 참고해주세요.

---

## 업무 영역별 상세 가이드

<div class="card categories">
  <div id="h_m0" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m0" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">설정</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m0" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/hr0001/" class="mx-2">구성원 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/hr0002/" class="mx-2">구성원 정보 수정</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/hr0007/" class="mx-2">조직도 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/se0005/" class="mx-2">사용자 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/se0003/" class="mx-2">역할/권한 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/se0201/" class="mx-2">사용자 코드 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/se0202/" class="mx-2">사용자 정의 항목 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/vs-settings/" class="mx-2">투자 심의 설정</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/se0051/" class="mx-2">회사 정보</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/my0001/" class="mx-2">마이페이지</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/cm0009/" class="mx-2">사용자 작업 이력 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/ed0100/" class="mx-2">전자결재 - 빈품의서</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_m1" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m1" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">조합 결성/관리</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m1" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0001/" class="mx-2">신규조합 추가</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0010/" class="mx-2">투자 의무 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0011/" class="mx-2">조합원 명부 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0013/" class="mx-2">조합 결성 필요 서류</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0012/" class="mx-2">보수 관리 정보 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0009a/" class="mx-2">금융정보 등록 (계좌등록)</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0010/" class="mx-2">재원별 회계원장 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0006/" class="mx-2">출자/배분 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/oi0002/" class="mx-2">출자 운용지시서 상신 (전자결재)</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pr0011/" class="mx-2">조합원 명부/출자 증서/출자 확인서 출력</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0029/" class="mx-2">조합원 총회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0060/" class="mx-2">지분양도양수 등록</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0004/" class="mx-2">투자 현황</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0100/" class="mx-2">수익률 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fd0200/" class="mx-2">조합원 소득공제</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_m2" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m2" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">거래원장 관리</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m2" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0001/" class="mx-2">거래 원장 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0004/" class="mx-2">일반거래 등록/조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0006/" class="mx-2">전환거래 등록/조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/pm0008/" class="mx-2">인수합병 거래 등록/조회</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_m3" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m3" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">회계/재무</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m3" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0009/" class="mx-2">회계기준 및 회계원장</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0010/" class="mx-2">재원별 회계원장</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0005/" class="mx-2">계정과목</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0011/" class="mx-2">재무제표 양식</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0300/" class="mx-2">자동 전표 설정</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0002/" class="mx-2">전표 입력</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0003/" class="mx-2">분개장 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0021/" class="mx-2">전표 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0015/" class="mx-2">계정별 원장</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0016/" class="mx-2">합계 잔액 시산표</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0018/" class="mx-2">재무상태표</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0017/" class="mx-2">손익계산서</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0012/" class="mx-2">표준 계정 연결 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0019/" class="mx-2">마감/이월</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0008/" class="mx-2">금융 정보 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0020/" class="mx-2">계좌잔액 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/fm0100/" class="mx-2">법인 카드 관리</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/my0200/" class="mx-2">내 법인 카드 사용 내역</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_m4" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m4" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">영업보고 관리</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m4" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0001/" class="mx-2">영업보고 템플릿</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0012/" class="mx-2">포트폴리오 연락망</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/br0004/" class="mx-2">영업보고 요청</a>
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
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/stworks-invite/" class="mx-2">STworks 가입 요청 (포트폴리오 전환)</a>
      </li>
    </ul>
  </div>
</div>

<div class="card categories">
  <div id="h_m5" class="card-header d-flex justify-content-between hide-border-bottom"
       data-bs-toggle="collapse" data-bs-target="#l_m5" role="button" aria-expanded="false" style="cursor: pointer">
    <span class="ms-2">
      <i class="far fa-folder-open fa-fw"></i>
      <span class="mx-2">LP보고</span>
    </span>
    <span class="category-trigger hide-border-bottom">
      <i class="fas fa-fw fa-angle-down"></i>
    </span>
  </div>
  <div id="l_m5" class="collapse" aria-expanded="false">
    <ul class="list-group">
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lc0101/" class="mx-2">정기 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0531/" class="mx-2">운용기관 정보 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0270/" class="mx-2">상장 주식 거래</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0310/" class="mx-2">투자 기업 부가 정보</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0520/" class="mx-2">운용기관 인력정보</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0510/" class="mx-2">투자기업 신청정보</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0630/" class="mx-2">투자심사 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0600/" class="mx-2">담당심사역 이력</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0590/" class="mx-2">수시 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0550/" class="mx-2">조합원 총회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0610/" class="mx-2">출자금 납입 요청 계획</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0635/" class="mx-2">투자 계약서 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0681/" class="mx-2">액셀러레이터 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0570/" class="mx-2">관리보수/성과보수</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0620/" class="mx-2">반기 보고</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lc0100/" class="mx-2">보고 전송 내역 조회</a>
      </li>
      <li class="list-group-item">
        <i class="far fa-file-alt fa-fw"></i>
        <a href="/posts/lp0001/" class="mx-2">재원별 보고 LP 설정</a>
      </li>
    </ul>
  </div>
</div>

---

> 관리역 권한이 부여되지 않은 경우, 일부 메뉴가 보이지 않을 수 있습니다.
> 역할/권한 설정은 [역할/권한 관리 가이드](/posts/se0003/)를 참고하세요.
{: .prompt-tip }

> 회계 기준 및 계정과목 설정은 조합 결성 전에 미리 완료하는 것을 권장합니다.
> [회계기준 및 회계원장](/posts/fm0009/) 가이드를 참고하세요.
{: .prompt-info }

버그 및 문의 사항은 다음 이메일로 보내주세요: **[we@dkdk.kr](mailto:we@dkdk.kr)**
