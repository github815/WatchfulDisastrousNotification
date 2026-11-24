# 성경 본문 데이터 출처와 권리

이 폴더의 JSON은 `index.html` 웹앱의 **전체 성경 검색**(구약·신약 66권, 31,101절)에 쓰입니다.

| 폴더 | 역본 | 권리 | 출처 |
| --- | --- | --- | --- |
| `ko/` | 개역한글 (1961) | 공개 도메인 (대한성서공회) | `github.com/crizin/bible-db` → `data/krv/krv_holybible.jsonl` (holybible.or.kr 본문) |
| `en/` | Berean Standard Bible (BSB) | 퍼블릭 도메인 (2023-04-30 공표, CC0) | `github.com/crizin/bible-db` → `data/bsb/bsb.jsonl` (berean.bible 본문) |
| `search/` | 위 두 역본의 키워드 검색용 묶음 | 위와 같음 | 위와 같음 |

- 절 수: 개역한글 31,101절, BSB 31,102절.
- 두 역본의 절 구분이 다른 5곳(사무엘상 23장, 시편 147편, 아가 7장, 고린도후서 13장, 요한삼서)은 각 역본의 절 번호를 그대로 표기합니다.
- 앱의 **오늘의 말씀** 기본 40개 구절은 손으로 넣어 둔 개역개정·NIV 본문이며, 검색 결과에서 그 40개 구절이 나오면 같은 본문을 보여 줍니다(`본문: 개역개정 · NIV` 표기).
- BSB 저작권 안내(권장 사항): "The Holy Bible, Berean Standard Bible, BSB is produced in cooperation with Bible Hub, Discovery Bible, OpenBible.com, and the Berean Bible Translation Committee. This text of God's Word has been dedicated to the public domain."

## 파일 구조

- `index.json` — 66권 목록(한국어·영어 이름, 약어, 장별 절 수)과 역본 정보
- `ko/NN.json`, `en/NN.json` — 권별 본문. `{"id":1,"ko":"창세기","chapters":[["1절","2절",...],...]}`
- `search/ko-ot.json`, `ko-nt.json`, `en-ot.json`, `en-nt.json` — 키워드 검색용 묶음. `{"lang":"ko","books":{"1":[["1절",...]]}}`

생성 스크립트는 위 두 JSONL에서 만들었으며, 본문은 가공 없이 그대로 옮겼습니다.
