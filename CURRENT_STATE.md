# Current State

Last Updated: 2026-09-21

## Objective

- 새 데이터 분석을 시작하기 위한 재사용 템플릿 준비.
- Target, Primary Metric, Primary Validation은 새 데이터의 구조를 확인한 뒤 결정한다.

## Current Best

- 없음. 등록된 experiment가 없다.

## Active Work

- 새 데이터와 설정 입력 대기.

## Current Candidates

- 없음.

## Known Issues

- 기본 시간 예산 검사는 단계 사이에서 수행되므로 단일 model fit을 강제로 중단하지 못한다.
- OOF Parquet 저장에는 `pyarrow`가 필요하다.
- 기본 CV는 모든 데이터 구조에 적합하지 않다. 첫 baseline 전에 데이터의 시간·그룹 구조를 확인한다.

## Next Actions

1. `data/`에 새 데이터를 배치한다.
2. `configs/baseline.json`의 경로, target, ID와 시간 예산을 확인한다.
3. 새 데이터에 맞는 Primary Validation과 metric을 정한 뒤 첫 baseline을 실행한다.

## Blockers

- 분석할 데이터가 아직 없다.

## 작성 원칙

현재 상태만 기록한다. 전체 실험 이력, 상세 config와 metric은 각각 `progress.md`와 experiment artifact에 기록한다.
