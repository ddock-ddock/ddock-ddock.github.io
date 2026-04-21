---
title: 국내 기업 STworks 가입 요청 (투자심의 > 등기)
author: dkdk.kr
date: 2026-04-21 14:00:00 +0800
categories:
  - 투자 심의
  - STworks 연동
tags:
  - STworks
  - 가입요청
  - 재간
  - 등기
  - 포트폴리오
render_with_liquid: true
---
국내 투자 기업을 포트폴리오로 전환할 때(등기 단계) 상호 데이터 연동이 가능한 STworks 가입을 요청하는 기능입니다.

## 설명

- 투자 심의가 `납입` 상태까지 진행되고, 심의 업체의 `국가` 값이 `대한민국`일 때 이 절차를 수행할 수 있습니다.
- STworks 가입 이후 VCworks와 STworks 간 기업 기본 정보, 주주 구성, 영업보고 등이 자동으로 연동됩니다.
- 국내 기업의 STworks 식별 키는 `법인등록번호`입니다. 잘못된 번호로 초대하면 중복 법인이 생성되므로 주의해주세요.
- 해외 기업의 포트폴리오 전환은 별도 플로우입니다. [해외 기업 투자 심의(vs_foreign)](/posts/vs_foreign/) 가이드를 참고해주세요.

#### 1. 투자심의 상세 페이지 이동

`투자/회수 > 투자 심의`에서 대상 투자심의 카드를 클릭해 상세 페이지로 이동해주세요.

![투자심의 상세 진입](assets/img/stworks_invite_01.png)

#### 2. 주요 연락처 입력

STworks 가입 요청 메일은 상세 페이지에 등록된 연락처로 발송되므로, 사전에 정확한 연락처를 등록해야 합니다.

1. `회사정보` 탭을 클릭해주세요.

![회사정보 탭](assets/img/stworks_invite_02.png)

2. **[수정]** 버튼을 클릭해주세요.

![수정 모드 진입](assets/img/stworks_invite_03.png)

3. `주요 연락처` 섹션을 추가해주세요.

![주요 연락처 추가](assets/img/stworks_invite_04.png)

4. 생성된 행의 각 셀을 클릭해 연락처 정보를 입력해주세요.

![연락처 입력](assets/img/stworks_invite_05.png)

5. **[저장]** 버튼을 클릭해주세요.

![저장](assets/img/stworks_invite_06.png)

#### 3. STworks 가입 요청 전송

1. 투자 심의 단계에서 **[등기 >]** 버튼을 클릭해주세요.

![등기 버튼 클릭](assets/img/stworks_invite_07.png)

2. STworks 가입을 요청할 대상자를 선택해주세요. 복수 선택이 가능합니다.

![대상자 선택](assets/img/stworks_invite_08.png)

3. **[전송하기]** 버튼을 클릭해주세요.

![전송](assets/img/stworks_invite_09.png)

4. 전송이 완료되면 아래와 같이 상태가 표시됩니다.

![전송 완료](assets/img/stworks_invite_10.png)

## 자주 묻는 질문

> 타 운용사를 통해 이미 STworks에 가입한 기업인지 어떻게 확인하나요?
{: .prompt-tip }
- 투자심의 상세(또는 포트폴리오 상세)의 `회사정보` 탭에서 `STworks 가입` 여부를 확인할 수 있습니다.

![STworks 가입 여부 확인](assets/img/stworks_invite_11.png)

> 이미 STworks에 가입된 기업은 어떻게 해야 하나요?
{: .prompt-tip }
- `법인등록번호`를 식별 키로 자동 연동되므로 가입 요청 절차는 생략하셔도 됩니다.
- 이미 가입된 기업은 투자심의 상세에서 연동 정보가 자동으로 표시됩니다.

![이미 가입된 기업 확인](assets/img/stworks_invite_12.png)

> 잘못된 법인등록번호로 초대한 경우 어떻게 하나요?
{: .prompt-tip }
- 잘못된 번호로 가입 요청이 전송되면 중복 법인이 생성될 수 있습니다.
- 발견 즉시 [we@dkdk.kr](mailto:we@dkdk.kr)로 문의해주시면 초기화·재발송을 도와드립니다.

> STworks 가입은 매 투자 건마다 해야 하나요?
{: .prompt-info }
- 아닙니다. 한 번 가입한 기업은 이후 다른 투자사로부터 투자를 받더라도 재가입이 불필요합니다.
- 동일 법인등록번호로 VCworks 사용 운용사 간 투자 데이터가 자동 공유됩니다.

버그 및 문의 사항은 다음 이메일로 보내주세요: **[we@dkdk.kr](mailto:we@dkdk.kr)**
