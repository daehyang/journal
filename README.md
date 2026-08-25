# 대전향토연구 (Daejeon Local Studies)

대전향토문화연구회 연간 회지 「대전향토연구」의 공식 공개 저장소입니다.

- 발행: 대전향토문화연구회 (창립 2019-06-17, 위키데이터 [Q141162117](https://www.wikidata.org/wiki/Q141162117))
- 창간: 2022년
- 공개 방식: 호별 디렉터리 + **GitHub Release에 PDF 첨부** + Zenodo 자동 보존(DOI 발급)

## 저장소 구조

```
journal/
├── vol01/   # 창간호 (2022) — 목차, 논문별 정보
├── vol02/   # 제2호 (2023)
└── ...
```

각 호 디렉터리에는 `contents.md`(호 정보·목차·저자·라이선스 동의 여부)를 두고,
최종 PDF는 Release에 첨부합니다. 저장소 본문에는 대용량 PDF를 직접 넣지 않습니다
(이력 비대화 방지).

## 새 호를 공개하는 절차

1. `volNN/` 디렉터리를 만들고 `contents.md` 작성 (아래 vol01/contents.md 참조)
2. 저장소 우측 **Releases → Draft a new release**
3. 태그: `vol.NN` (예: `vol.03`) / 제목: `대전향토연구 제N호 (YYYY)`
4. 발간사 요약을 설명란에 쓰고 **최종 PDF를 첨부**
5. **Publish release** → Zenodo가 자동으로 보존하고 DOI를 발급
6. 발급된 DOI를 `contents.md`와 홈페이지 `journal.md` 표에 기입

## Zenodo 연동 (최초 1회 설정)

1. https://zenodo.org 에 GitHub 계정으로 로그인
2. 우측 상단 → **GitHub** 메뉴 → `daehyang/journal` 저장소 스위치 **ON**
3. 이후 Release를 발행할 때마다 자동 보존 + DOI 발급
4. 이 저장소의 `.zenodo.json`이 보존 시 메타데이터(발행처·라이선스 등)로 사용됨

## 라이선스

수록 논문은 저자 동의에 따라 **CC BY-SA 4.0** 공개를 원칙으로 합니다.
저자가 다른 조건을 택한 글은 해당 호 `contents.md`에 명시합니다.
