---
version: alpha
name: Seonghosa
description: 관공서의 신뢰감과 친근한 안내 톤을 함께 담은 셀프등기 가이드 디자인 시스템
colors:
  primary: "#1D4ED8"
  primary-container: "#EFF6FF"
  on-primary: "#FFFFFF"
  ink: "#0F172A"
  secondary: "#64748B"
  neutral: "#F8FAFC"
  surface: "#FFFFFF"
  border: "#E2E8F0"
  amber: "#B45309"
  amber-container: "#FFFBEB"
  amber-border: "#FCD34D"
  success: "#15803D"
  success-container: "#F0FDF4"
  type-sale: "#2563EB"
  type-sale-container: "#EFF6FF"
  type-mortgage: "#16A34A"
  type-mortgage-container: "#F0FDF4"
  type-jeonse: "#7C3AED"
  type-jeonse-container: "#F5F3FF"
  type-gift: "#DB2777"
  type-gift-container: "#FDF2F8"
  type-inheritance: "#475569"
  type-inheritance-container: "#F1F5F9"
typography:
  display:
    fontFamily: Pretendard
    fontSize: 2rem
    fontWeight: 800
    lineHeight: 1.25
    letterSpacing: -0.02em
  h2:
    fontFamily: Pretendard
    fontSize: 1.25rem
    fontWeight: 800
    lineHeight: 1.3
    letterSpacing: -0.01em
  body-lg:
    fontFamily: Pretendard
    fontSize: 1.125rem
    fontWeight: 400
    lineHeight: 1.7
  body-md:
    fontFamily: Pretendard
    fontSize: 0.9375rem
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Pretendard
    fontSize: 0.8125rem
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: Pretendard
    fontSize: 0.75rem
    fontWeight: 700
    letterSpacing: 0.01em
rounded:
  sm: 8px
  md: 14px
  lg: 20px
  pill: 999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
components:
  card-select:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-select-hover:
    backgroundColor: "{colors.primary-container}"
  type-icon-badge:
    rounded: "{rounded.pill}"
    size: 44px
  tag-pill:
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.sm}"
    padding: 14px 24px
---

## Overview

셀프등기 도우미는 "관공서 서류처럼 딱딱하지만, 안내는 다정한" 톤을 지향한다.
파랑을 뼈대 색으로 두되, 등기 유형마다 서로 다른 강조색을 부여해 "지금 내가
어떤 갈래를 보고 있는지"를 색으로도 구분할 수 있게 한다. 선택 화면(등기 유형
카드, 질문 옵션 카드)은 텍스트만 나열하지 않고 아이콘·색 배지·호버 반응으로
"고를 만한 지점"이 분명히 드러나야 한다.

## Colors

- **Primary (#1D4ED8):** 헤더 배지, 기본 버튼, 링크. 신뢰감을 주는 진한 파랑.
- **Secondary (#64748B):** 보조 설명 텍스트, 카운트 라벨.
- **Neutral (#F8FAFC):** 페이지 배경. 흰 카드가 배경 위에 떠 보이게 한다.
- **Amber (#B45309) / Amber Container (#FFFBEB):** 경고·주의 배너 전용. 다른
  용도로 쓰지 않는다.
- **Success (#15803D):** "난이도 낮음" 같은 긍정적 배지에만 쓴다.
- **Type 색상 5종 (sale/mortgage/jeonse/gift/inheritance):** 등기 유형 선택
  카드의 아이콘 배지, 결과 화면 헤더 배지에 유형별로 고정 배정한다. 절대 서로
  바꿔 쓰지 않는다 — 사용자가 색으로 유형을 다시 찾아올 수 있어야 한다.

## Typography

Pretendard 한 폰트로 통일한다 (본문 가독성과 숫자 조판이 좋은 국문 서체).

- **display:** 랜딩 페이지 h1 전용.
- **h2:** 섹션 제목, 카드 안 제목.
- **body-lg:** 랜딩 리드 문단.
- **body-md:** 기본 본문, 카드 설명.
- **body-sm:** 캡션, 서류 note, 배지 아래 부가 설명.
- **label:** 대문자/굵은 라벨 — 배지, 버튼 텍스트.

## Layout

8px 배수 스페이싱(4/8/16/24/40)을 쓴다. 카드 내부 패딩은 `md`(16px), 카드 사이
간격도 `md`, 섹션 간 큰 간격은 `xl`(40px)로 리듬을 준다.

## Shapes

- 카드·패널: `rounded.md`(14px)
- 버튼·입력 필드: `rounded.sm`(8px)
- 배지·태그: `rounded.pill`

## Components

### Card Select (등기 유형 / 질문 옵션 카드)

흰 배경 카드에 얇은 테두리. 좌측에 유형별 강조색 원형 아이콘 배지를 두고,
호버 시 테두리가 강조색으로 바뀌며 살짝 떠오르는 그림자(hover lift)를 준다.
선택형 카드는 절대 밋밋한 텍스트 박스로 두지 않는다 — 아이콘 배지 또는 진행
표시(1/3 등) 중 하나는 항상 동반한다.

### Tag Pill

카드 우상단에 붙는 작은 배지. "가장 많이 찾는 유형"(primary 톤), "난이도
낮음"(success 톤)처럼 판단에 도움이 되는 정보만 담는다. 장식용 배지는 넣지
않는다.

### Button Primary / Secondary

Primary는 파랑 배경 + 흰 텍스트, 페이지당 하나(가장 중요한 다음 행동)에만
쓴다. Secondary(답변 수정, 처음부터 등)는 흰 배경 + 테두리로 시각적 무게를
낮춘다.

## Do's and Don'ts

- **Do:** 등기 유형마다 지정된 강조색을 아이콘 배지·배지 텍스트에 일관되게 쓴다.
- **Do:** 선택 카드에는 아이콘 배지 + 제목 + 한 줄 설명을 항상 함께 둔다.
- **Do:** 경고 배너는 amber, 긍정 정보는 success로만 표현한다.
- **Don't:** 경고가 아닌 곳에 amber를 쓰지 않는다.
- **Don't:** 카드 배경을 흰색이 아닌 다른 색으로 채우지 않는다 (강조는 아이콘
  배지·배지·테두리로만).
- **Don't:** Pretendard 외 다른 폰트를 섞지 않는다.
