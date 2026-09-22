---
layout: home
title: Home
nav_order: 0
permalink: /
---

# Eval-ATS

**AI 기반 채용 프로세스 자동화 및 지원자 통합 관리 플랫폼**
{: .fs-6 .fw-300 }

3축 자동 서류 심사, 칸반 보드, 도구 호출 에이전트 '아르', RAG 검색, AI 면접 실시간 분석, 제출물 무결성 원장까지 — 채용 프로세스를 하나의 플랫폼에서 자동화합니다. 최종 합불은 사람이 확정합니다.
{: .fs-5 .fw-300 }

[목차 보기](/toc/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[GitHub](https://github.com/Seuk-Team/jekyll){: .btn .fs-5 .mb-4 .mb-md-0 }

---

<table class="cv-table">
<tr><td class="cv-label">사업명</td><td><div class="cv-main">AI 기반 채용 프로세스 자동화 및 지원자 통합 관리 플랫폼</div></td></tr>
<tr><td class="cv-label">시스템명</td><td><div class="cv-main">Arda (Eval-ATS)</div></td></tr>
<tr><td class="cv-label">개발 기간</td><td><div class="cv-main">2026년 8월 20일 (목) ~ 2026년 10월 27일 (화)</div><div class="cv-sub">총 69일 · 10주, 애자일 스크럼 (2주 1스프린트 · 총 5스프린트)</div></td></tr>
<tr><td class="cv-label">개발팀 : SEUK</td><td><div class="cv-main">진수택 · 이우정 · 김민아 · 박소연</div><div class="cv-sub">4명</div></td></tr>
<tr><td class="cv-label">문서 작성일</td><td><div class="cv-main">2026년 8월 20일</div></td></tr>
<tr><td class="cv-label">깃허브 주소</td><td><div class="cv-main"><a href="https://github.com/Seuk-Team/Arda">github.com/Seuk-Team/Arda</a></div><div class="cv-sub">문서 저장소 — <a href="https://github.com/Seuk-Team/jekyll">github.com/Seuk-Team/jekyll</a></div></td></tr>
<tr><td class="cv-label">문서 사이트</td><td><div class="cv-main"><a href="https://ats.suvisdev.cloud">ats.suvisdev.cloud</a></div></td></tr>
<tr><td class="cv-label">서비스</td><td><div class="cv-main"><a href="https://seuk.suvisdev.cloud">seuk.suvisdev.cloud</a></div><div class="cv-sub">Vercel 배포 · API api.seuk.suvisdev.cloud (Swagger /docs)</div></td></tr>
</table>

---

## 핵심 기능 6축 (2026-09-22 기준)

| # | 축 | 내용 | 상태 |
|---|-----|------|------|
| 1 | 채용 파이프라인 통합 관리 | 공고 등록과 공개 지원 링크 → 접수(이력서는 브라우저에서 S3 직행 · 해시는 무결성 원장) → **AI 3축 채점으로 서류 단계 자동 판정**(ADR-0034) → 칸반에서 면접 이후 심사·드래그·일괄 변경 → 모든 이동 이력 → 안내 메일(n8n + SMTP · 재발송) → 평가·면접관 배정 → 최종 합불은 사람 | ✅ 완료 |
| 2 | 면접 일정 자동화 · 지원자 포털 | 면접관 가용 시간 → 후보 슬롯 → 지원자 링크 또는 이메일+생년월일 로그인 → 확정·양측 통보 → 캘린더 · 전형 현황·설문·AI 면접 한 화면 · FAQ 챗봇(기본 질문 $0) | ✅ 완료 |
| 3 | AI 에이전트 "아르" | 접수 즉시 요약·평가·추천 3단 체인 · 자연어 한 문장으로 검색·단계 변경·배정·메일·이력서 드롭 접수(도구 12종 · 쓰기는 확인 카드) · RAG 시맨틱 검색 · 빈출 요청 규칙 라우터 · 호출마다 원가 기록 · 무관 질문은 데이터 근거 기준 거절 | ✅ 완료 |
| 4 | AI 면접 · 실시간 분석 | 이력서·자소서 기반 맞춤 질문 · 음성 STT · 답변↔서류 대조 · 담당자 1:1 WebRTC 실시간 화면 · 표정/음성 **참고 지표**(점수 미반영, ADR-0029) · 종료 시 수치 요약 → 종합평가 | ✅ 완료 |
| 5 | 멀티 클라이언트 | React 웹 + Flutter 앱이 같은 FastAPI 사용 (웹 25 · 앱 23 화면) | ✅ 완료 |
| 6 | 운영·모델 전략 | Docker · AWS 자동 CD(2분 폴링) · CI 5잡 · 경보·백업 · 헥사고날 4 컨텍스트 · **Qwen 자체학습 vs Claude 동일 채점기 비교 → 클라우드 + Claude 확정** | ✅ 완료 |

**규모(09/22)**: API 107 · 테이블 28 · pytest 1,165건 · 앱 테스트 30파일 · ADR 36편 · 커밋 1,095 · 필수 기능 27/27 · 자체학습 chat v9 73.9%
{: .fs-3 }
