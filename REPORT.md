# 개인 이력서 - REPORT

| 항목 | 내용 |
|---|---|
| 활동명 | Pio |
| 배포 URL | https://piop2.smu.ai.kr/ |
| 작성일 | 2026-10-19 |

## 1. 인수 검수표

검수 기준일: 2026-10-19  
검수 방법: 저장소 원문 및 소스 정적 확인, 배포 URL 직접 확인, W3C 검사기 확인, 링크 HTTP 응답 확인

| ID | 확인 방법 | 결과 | 근거 |
|---|---|---|---|
| F-01 | 배포 URL의 header에서 활동명·소속·한 줄 소개를 확인하고, 소개가 한 문장 50자 이내인지와 1280px 화면에서 첫 화면에 표시되는 구성을 확인했다. | Pass | [배포 URL](https://piop2.smu.ai.kr/), [index.html](index.html), [소개 원문](docs/profile/f-01.md) |
| F-02 | header의 GitHub 프로필 링크가 본인 프로필로 연결되는지 확인하고, 페이지 소스 전체에서 이메일·전화번호 등 다른 연락처가 없는지 확인했다. | Pass | [GitHub 프로필](https://github.com/piop2), [index.html](index.html), [연락 채널 원문](docs/profile/f-02.md) |
| F-03 | 실적 표의 행 수, 시기·분류·내용·역할 열, 허용된 분류, 중·고등학교 실적 포함 여부와 시기 역순 정렬을 확인했다. | Pass | [index.html](index.html), [실적 원문](docs/profile/f-03.md) |
| F-04 | 2026-2학기 수강 과목 6개와 각 이수 구분을 확인하고, 「웹프로그래밍 및 AI에이전트 활용」 링크가 주차별 링크 영역의 앵커로 이동하는지 확인했다. | Pass | [index.html](index.html), [수강 과목 원문](docs/profile/f-04.md) |
| F-05 | 01~15주차가 모두 표시되는지, 실습 주차 02·03·05·06·07의 실제 링크와 예정·OT·휴강 주차의 링크 부재, 진행·예정 주차의 색상 구분을 확인했다. | Pass | [index.html](index.html), [styles.css](styles.css), [주차 상태 원문](docs/profile/f-05.md), [실습 폴더](practice/) |
| F-06 | footer의 `최종 수정일: YYYY-MM-DD` 표시와 배포 저장소의 마지막 커밋 날짜가 모두 `2026-10-19`인지 확인했다. | Pass | [index.html](index.html), `git log -1`, [최종 수정일 원문](docs/profile/f-06.md) |
| Q-HTML | W3C Nu HTML Checker로 배포 URL을 검사하고 검사 결과의 오류 메시지 수를 확인했다. | Pass (오류 0건) | [HTML 검사 결과](https://validator.w3.org/nu/?doc=https%3A%2F%2Fpiop2.smu.ai.kr%2F&out=json) |
| Q-CSS | W3C CSS Validator로 배포 stylesheet를 검사하고, 소스에서 인라인 `style`·표현용 태그·`script` 사용 여부를 확인했다. | Pass (오류 0건, 경고 2건) | [CSS 검사 결과](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fpiop2.smu.ai.kr%2Fstyles.css&output=json), [styles.css](styles.css), [index.html](index.html) |
| Q-DEPLOY | 배포 URL, GitHub 프로필, stylesheet, 실습 주차 02·03·05·06·07 링크에 HTTP 요청을 보내 응답 상태를 확인하고 페이지의 이미지 표시 여부를 확인했다. | Pass (확인한 링크 HTTP 200) | [배포 URL](https://piop2.smu.ai.kr/), [GitHub 프로필](https://github.com/piop2), [실습 폴더](practice/) |

## 2. 완성도 분석

**완성도 = 충족(Pass)한 요구사항 수 ÷ 평가 대상 요구사항 수(9) = 9 / 9 = 100%**

### 요구사항과 결과가 다른 부분

이번 재검수에서는 F-01~F-06, Q-HTML, Q-CSS, Q-DEPLOY의 수용 기준을 모두 충족했다.

이전 보고서에는 과거 W3C 검사 결과를 근거로 `Q-HTML`을 `Fail`로 기록했지만, 2026-10-19에 배포 URL을 다시 검사한 결과 W3C Nu HTML Checker의 오류는 0건이었다. 이전 결과를 현재 배포본에 대해 재검증하지 않고 실패 상태로 유지한 것이 보고서의 오류였다. 현재 소스의 역할 칩 `div`에는 문제로 지적되었던 `aria-label`이 없으며, 배포 HTML도 오류 없이 검사된다.

### 다음에 다르게 할 점

소스 수정 직후 저장소 파일만 확인하지 않고 배포 URL의 HTML·CSS를 다시 요청해 최신 배포본이 반영되었는지 확인하겠다. 또한 이전 검사 결과를 그대로 재사용하지 않고, 보고서 작성 직전에 W3C 검사 결과와 모든 링크의 HTTP 응답을 다시 확인해 보고서의 결과와 근거가 같은 시점의 상태를 가리키도록 하겠다.

## 3. 추가 요구사항 제안 (선택 - 가산점)

추가 요구사항은 제안하지 않았다.
