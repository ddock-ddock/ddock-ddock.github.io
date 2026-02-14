---
icon: fas fa-lightbulb
order: 6
---

VCworks.kr 사용 과정에서 꼭 필요한 팁과 자주 묻는 질문을 정리하였습니다.

<div class="guide-cards">
  <a href="#모바일-앱-다운로드" class="guide-card">
    <i class="fas fa-mobile-alt"></i>
    <span>모바일 앱<br/><small>다운로드</small></span>
  </a>
  <a href="#pwa" class="guide-card">
    <i class="fas fa-desktop"></i>
    <span>PWA<br/><small>데스크톱 앱 설치</small></span>
  </a>
  <a href="#다중-정렬-지원" class="guide-card">
    <i class="fas fa-sort-amount-down"></i>
    <span>다중 정렬<br/><small>지원</small></span>
  </a>
  <a href="#편집기-헤더-사용법" class="guide-card">
    <i class="fas fa-heading"></i>
    <span>편집기 헤더<br/><small>사용법</small></span>
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
.app-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin: 1rem 0;
}
.app-buttons .btn {
  flex: 1;
  min-width: 200px;
  text-align: center;
}
</style>

---

## 모바일 앱 다운로드

VCworks는 이동 중 전자결재 및 정보조회 편의성을 위해 Mobile 버전을 제공합니다.

<div class="app-buttons">
  <a href="https://apps.apple.com/kr/app/vcworks/id6738978723" class="btn btn-primary">
    <i class="fab fa-apple"></i> iOS 앱스토어
  </a>
  <a href="https://play.google.com/store/apps/details?id=com.vcworks.mobile&hl=ko" class="btn btn-primary">
    <i class="fab fa-android"></i> 구글 플레이스토어
  </a>
</div>

---

## PWA

VCworks.kr은 PWA(Progressive Web Apps)를 지원하여 마치 프로그램처럼 사용할 수 있는 사용성을 제공합니다.

### 동영상

{% include embed/youtube.html id='X5y2KXVuUpc' %}

1. VCworks.kr에 접속합니다.
2. 주소창에 있는 다음의 아이콘을 클릭합니다.

   ![PWA 설치 아이콘](/assets/img/Pasted%20image%2020241015191906.png)

3. 앱 설치를 누릅니다.
4. 작업표시줄에 고정을 누릅니다.
5. 이제 작업표시줄에서 아이콘을 선택하여 넓은 화면에서 마치 프로그램처럼 VCworks를 사용할 수 있습니다.

   ![VCworks 데스크톱 앱](/assets/img/Pasted%20image%2020241015192135.png)

> 넓은 화면에서 VCworks를 프로그램처럼 사용하려면 PWA 설치를 권장합니다.
{: .prompt-info }

---

## 다중 정렬 지원

VCworks는 그리드 내 다중 정렬을 제공합니다. 다중 정렬은 먼저 정렬을 설정한 것을 1번 우선순위로, 다음에 정렬 설정한 것을 2번 우선순위로 하는 기능입니다.

### 동영상

{% include embed/youtube.html id='p_lLOmKI1Zk' %}

> VCworks에서 정렬은 ▲/▼ 아이콘이 아닌 **컬럼명을 클릭**하여 동작합니다.
{: .prompt-tip }

- 다음의 상태는 아무런 정렬이 적용되지 않은 모습입니다.

  ![정렬 적용 전](/assets/img/Pasted%20image%2020241015192538.png)

- 한 번 클릭하게 되면 오름차순 정렬이 되며 다음과 같이 ▲가 나타납니다.

  ![오름차순 정렬](/assets/img/Pasted%20image%2020241015192637.png)

- 한 번 더 클릭하게 되면 내림차순 정렬이 되며 다음과 같이 ▼가 나타납니다.

  ![내림차순 정렬](/assets/img/Pasted%20image%2020241015192706.png)

- 이때 다른 컬럼을 마찬가지로 클릭하게 되면 첫 번째 선택한 보고일은 내림차순으로 하고, 같은 보고일일 경우 부서명 기준으로 오름차순을 하게 됩니다.

  ![다중 정렬](/assets/img/Pasted%20image%2020241015192728.png)

---

## 편집기 헤더 사용법

VCworks 편집기는 헤더 기능을 제공합니다. `#`을 입력할 때마다 글씨 크기가 줄어듭니다. `#`과 스페이스 바를 입력한 후 글씨를 쓰면 크기가 달라집니다.
`#`은 1개부터 6개까지 지원합니다. 아래 사진을 참고해 주세요.

![편집기 헤더 사용법](https://github.com/user-attachments/assets/1bd5f825-f935-488a-8b94-3eef8d045d31)

---

버그 및 문의 사항은 다음 이메일로 보내주세요: **[we@ddock.kr](mailto:we@ddock.kr)**
