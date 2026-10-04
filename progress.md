# Progress

## 2026-09-23

### Summary

- experiment run 안에서 분석·판정용 `results/`와 재현·검증용 `reproducibility/`를 분리했다.
- 실행 환경과 artifact SHA-256을 담는 `run_manifest.json`을 추가하고 새 layout을 end-to-end test로 검증했다.
- 외부 제출용 `submission.csv`와 관련 설정·최종 fit·test 추론을 formal experiment 단계에서 제거했다.

### Experiments

- 등록된 실험 없음. 이후 생성되는 experiment부터 artifact layout version 2를 사용한다.

### Handoff

- 결과 분석은 `results/`, 재실행과 artifact 무결성 확인은 `reproducibility/`를 기준으로 한다.
- 제출이 필요하면 Reviewer 검증을 마친 후보를 대상으로 별도 output 단계를 설계한다.

## 2026-09-22

### Summary

- 첨부된 EDA 재사용안을 검토해 표형 데이터에 공통 적용 가능한 target 분포, 숫자형 histogram, Pearson 상관 heatmap을 선택 옵션으로 추가했다.
- 시계열 개요는 timestamp와 신호 열에 대한 도메인 판단이 필요하므로 공통 기본 기능에는 포함하지 않았다.
- 회귀 target은 고유값별 빈도 대신 기술통계로 요약하도록 수정하고, 신규 EDA 테스트를 포함한 전체 7개 테스트를 통과했다.

### Experiments

- 등록된 실험 없음. EDA 표현과 코드만 변경했다.

### Handoff

- 실제 데이터가 들어오면 기본 EDA와 `--render-visuals` 결과를 확인하고, 시간·그룹 구조가 있으면 해당 구조 전용 EDA 범위를 결정한다.

## 2026-09-21

### Summary

- 이전 예시 데이터의 산출물과 실험 참조를 제거하고 새 데이터용 템플릿으로 초기화했다.
- 공통 분석 파이프라인과 검증 규칙은 유지했다.
- HTML 결과물을 요청받을 때 사용할 GitHub Pages 게시 위치를 `https://yunseo326.github.io/data_study_bank/`로 지정했다.

### Experiments

- 등록된 실험 없음.

### Handoff

- 새 데이터를 배치하고 `configs/baseline.json`을 확인한 뒤 첫 실험을 시작한다.

## 작성 원칙

중요한 실험, 방향 변경, 결정, 문제와 milestone을 시간순으로 기록한다. 상세 조건과 수치는 각 experiment artifact에 둔다.
