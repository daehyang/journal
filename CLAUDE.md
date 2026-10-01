# journal — 회지 「대전향토연구」

대전향토문화연구회 연간 회지의 공개 저장소. 호별 디렉터리(`volNN/`)에 목차·서지 정보를 두고,
PDF는 GitHub Release(배포)와 Zenodo(보존·DOI)로 낸다.

남은 일은 `internal` 저장소의 **Issues**에 있다. 연구회 GitHub 운영 문서도 그 저장소의
`docs/` 에 있다 — `operations.md`(임원용 절차) · `maintenance.md`(기술) ·
`decisions.md`(결정 기록).

## 브랜치와 푸시

이 저장소는 **브랜치를 만들고 PR 로** 올린다. **세 저장소 중 여기만 그렇게 한다**
(`internal/docs/decisions.md` 0012). `internal` 과 홈페이지는 `main` 에 직접 민다.

발간 기록·DOI·ISSN·저자별 라이선스 동의가 걸려 있어, 들어가기 전에 한 번 멈추는 값이
있다고 보았다. 한 번 발행한 DOI 와 한 번 밝힌 라이선스는 되돌리기 어렵다.

## 반드시 지킬 것

- **PDF를 저장소에 커밋하지 않는다.** 이력이 비대해진다. PDF는 Release 첨부와 Zenodo에만 둔다.
- **Zenodo의 GitHub 자동 연동을 켜지 않는다.** 그 연동은 태그 시점의 소스 zip만 보존하고
  Release에 첨부한 PDF는 가져가지 않으므로, DOI가 PDF를 가리키지 못한다
  ([zenodo#1235](https://github.com/zenodo/zenodo/issues/1235),
  [zenodo#1728](https://github.com/zenodo/zenodo/issues/1728)).
  그래서 회지는 Zenodo에 **직접 업로드**한다. Zenodo 프로필 → GitHub 화면에서 이 저장소
  스위치는 **OFF**여야 한다. 켜져 있으면 Release마다 PDF 없는 잘못된 DOI가 하나 더 발급된다.
- **호마다 별개의 Zenodo 업로드**로 올린다. Zenodo의 `New version`은 같은 저작물의 개정판용이므로
  서로 다른 호에는 쓰지 않는다.

## 부록

호마다 부록으로 그 해 새로 확정된 향토문화 항목 목록을 싣는다. 원고는 손으로 쓰지
않고 `internal` 저장소에서 대장으로부터 생성한다(`export_public.py --appendix YYYY`).
**부록은 따로 DOI를 받지 않는다** — 그 부록이 실린 호의 DOI를 쓴다. 누적 전체 목록은
몇 해마다 별도 단행본으로 내고 그때 자체 DOI를 받는다.

## 새 호를 낼 때

절차는 `README.md`의 "새 호를 공개하는 절차"가 정본이다. 요약하면
`volNN/contents.md` 작성 → Zenodo 업로드로 DOI 발급 → GitHub Release(태그 `vol.NN`, PDF 첨부,
설명란에 DOI 링크) → DOI를 `contents.md`와 홈페이지 `journal.md` 표에 기입.

## 파일

- `README.md` — 새 호를 공개하는 절차의 정본. 단 **Zenodo 업로드 화면 절차는 여기 두지
  않는다** — 그 정본은 `internal/docs/operations.md` 6장이고 여기에는 요약과 링크만 둔다
  (단행본도 같은 절차를 쓰므로 한 곳에 모았다. `internal/docs/decisions.md` 0010).
- `.zenodo.json` — Zenodo 업로드 화면에 옮겨 적는 표준 메타데이터. `publication_type`은 `book`
  (회지 한 호 전체이므로 journal article이 아니다). `related_identifiers`의 Q140909556은
  **회지**의 위키데이터 항목이다 (연구회는 Q141162117 — 혼동하지 말 것).
- `CITATION.cff` — GitHub의 "Cite this repository"에 쓰인다.
- `volNN/contents.md` — 호별 서지·목차·저자별 라이선스 동의 여부. 현재 vol01·vol02는
  발행일·ISSN·목차가 `(기입)` 상태로 남아 있다.

## 라이선스

수록 논문은 저자 동의에 따라 CC BY-SA 4.0 공개가 원칙. 다른 조건을 택한 글은
해당 호 `contents.md`의 라이선스 열에 명시한다.
