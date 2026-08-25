# 대전향토연구 (Daejeon Local Studies)

대전향토문화연구회 연간 회지 「대전향토연구」의 공식 공개 저장소입니다.

- 발행: 대전향토문화연구회 (창립 2019-06-17, 위키데이터 [Q141162117](https://www.wikidata.org/wiki/Q141162117))
- 창간: 2022년
- 공개 방식: 호별 디렉터리 + **GitHub Release에 PDF 첨부**(배포) + **Zenodo 직접 업로드**(보존·DOI 발급)

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

2. **Zenodo에 PDF를 올려 DOI를 받습니다.**
   1. https://zenodo.org 로그인 → 우측 상단 **New upload**
   2. 최종 PDF 한 개를 올리고 메타데이터 입력 (기준값은 `.zenodo.json` 참조)
      - Resource type: `Publication` → `Book` (회지 한 호 전체)
      - Title: `대전향토연구 제N호 (YYYY)`
      - Creators: `대전향토문화연구회` (Organization)
      - Publication date: 실제 발행일 / Language: `Korean`
      - License: `CC BY-SA 4.0`
   3. **Publish** → DOI 발급
   - 호마다 **별개의 업로드**로 올립니다. Zenodo의 `New version`은 같은 저작물의 개정판용이므로,
     서로 다른 호에는 쓰지 않습니다 (호별로 독립된 DOI를 갖게 합니다).

3. 저장소 우측 **Releases → Draft a new release**
4. 태그: `vol.NN` (예: `vol.03`) / 제목: `대전향토연구 제N호 (YYYY)`
5. 발간사 요약과 **2단계에서 받은 DOI 링크**를 설명란에 쓰고 **최종 PDF를 첨부**
6. **Publish release**
7. 발급된 DOI를 `volNN/contents.md`와 홈페이지 `journal.md` 표에 기입

## Zenodo 메타데이터 기준

이 저장소의 `.zenodo.json`에 회지의 표준 메타데이터(발행처·라이선스·언어·키워드·관련 식별자)를
적어 두었습니다. Zenodo 업로드 화면에 이 값을 그대로 옮겨 적으면 호마다 기록이 일관됩니다.

> **GitHub–Zenodo 자동 연동은 사용하지 않습니다.**
> Zenodo의 GitHub 연동은 태그 시점의 **소스 zip만** 보존하고 Release에 첨부한 PDF는 가져가지
> 않습니다. 그래서 회지는 위와 같이 Zenodo에 직접 올립니다.
> Zenodo 프로필 → GitHub 화면에서 이 저장소 스위치는 반드시 **OFF**로 두십시오.
> 켜 두면 Release를 발행할 때마다 PDF가 빠진 잘못된 DOI가 하나씩 더 발급됩니다.

## 라이선스

수록 논문은 저자 동의에 따라 **CC BY-SA 4.0** 공개를 원칙으로 합니다.
저자가 다른 조건을 택한 글은 해당 호 `contents.md`에 명시합니다.
