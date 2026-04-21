---
icon: fas fa-compass
order: 2
mermaid: true
---

<div class="guide-cards">
  <a href="/associate-start/" class="guide-card">
    <i class="fas fa-user-shield"></i>
    <span>심사역으로 시작하기</span>
  </a>
  <a href="/manager-start/" class="guide-card">
    <i class="fas fa-user"></i>
    <span>관리역으로 시작하기</span>
  </a>
  <a href="/features/" class="guide-card">
    <i class="fas fa-book"></i>
    <span>각 기능별 매뉴얼</span>
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
</style>

---

VCworks.kr은 똑똑[^dkdk] 주식회사에서 만든 대한민국 Venture Capital ERP Solution입니다.   

## VC업무의 일반 흐름

VCworks는 **설정 → 결성 → 투심**을 거쳐 투자한 자산을 **가치평가·거래원장·의결**로 운영하고, **영업보고·회수**로 마무리하는 구조입니다. 각 단계를 클릭하면 해당 영역의 대표 화면으로 이동할 수 있습니다.

```mermaid
flowchart TD
    A["설정<br/>구성원·회사·코드"] --> B["결성<br/>조합 생성·출자/배분"]
    B --> C["투심<br/>검토·표결·운용지시"]
    C --> D["가치평가<br/>투자유형별·재원별"]
    C --> E["거래원장<br/>거래 등록·전표"]
    C --> F["의결<br/>응답·정보 반영"]
    D --> G["영업보고<br/>요청·검수·보고서"]
    G --> H["회수<br/>회수위원회·회수 관리"]
    E --> H
    F -. 정보 반영 .-> E

    click A "/manager-start/"
    click B "/manager-start/"
    click C "/associate-start/"
    click D "/posts/pm0300/"
    click E "/posts/pm0001/"
    click F "/posts/sa0002/"
    click G "/posts/br0007/"
    click H "/posts/ex0007/"
```

> 역할별로 화면 단위의 세부 흐름이 필요하면 **[심사역으로 시작하기](/associate-start/)** 또는 **[관리역으로 시작하기](/manager-start/)** 페이지를 참고해주세요. 각 기능의 단독 매뉴얼은 **[각 기능별 매뉴얼](/features/)**에서 찾을 수 있습니다.

버그 및 문의 사항은 다음 이메일로 보내주세요: **[we@dkdk.kr](mailto:we@dkdk.kr)**


---

[^dkdk]:똑똑(dkdk.kr)은 대한민국 벤처투자전문회사인 DSC인베스트먼트가 VC업계의 업무 방식을 혁신하고자 만든 IT자회사입니다. 
