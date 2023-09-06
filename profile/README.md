# Cloud Development Team 에 어서오세요!!

우리는 우리가 구축하는 모든 소프트웨어, 제품의 발전을 위해 노력하는 클라우드 전문가 그룹입니다.

## 레파지토리 명명 규칙

레파지토리의 이름은 아래의 규칙을 따릅니다.

```
<project code>-<purpose>-<specific name> 
```

여기서 `<project code>`의 경우, 프로젝트 이름의 길이가 긴 경우가 존재하여 레파지토리 명명 규칙에 적용시키기 쉽도록 적합하게 줄인 약어 입니다.
코드와 프로젝트 이름의 관계는 아래의 프로젝트 리스트에서 확인하실 수 있습니다.

## 도메인 이름 규칙

아래의 Confluence Page를 참고 부탁드립니다.
https://hanwhavision.atlassian.net/wiki/spaces/KDOG/pages/290848889/DNS+Naming+Convention+for+Hanwha+Vision

## 프로젝트 리스트

프로젝트에 대한 간단한 설명과 레파지토리 이름에 사용할 약어 등을 정리해 두는 테이블입니다.

| Project Name | Abbreviation | Description                     |
|--------------|--------------|---------------------------------|
| hanwhacloud  | hc           | 클라우드 플랫폼 개발 프로젝트 (이전 프로젝트 이름으로 현재는 dmpro입니다. 추후 삭제 예정)                |
| dmpro        | dmpro        | Device Manager Pro 프로젝트  |
| sokcho       | sokcho       | hanwhacloud 개발 이전에 사용할 pilot 용도 |
| cloudrnd     | cloudrnd     | Cloud 개발팀에서 전반적으로 사용될 리소스용      |
|              |              |                                 |

## Commit Convention

본 조직 내의 레파지토리는 모두 conventional commit을 사용하고 있습니다.

아래와 같은 형식으로 commit message를 작성하며 더 자세한 내용은 https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional 에서 확인할 수 있습니다.

```
<type>(<scope>): <short summary> (<jira issue>)
  │       │             │         │
  │       │             │         └─⫸ Jira Issue(티켓) 번호, DEVO-123, CPD-456등의 형식으로 해당 커밋이 어떠한 Issue(티켓)와 연관이 있는지 작성합니다.
  │       │             └─⫸ 명령문, 현재 시제로 작성합니다. 대문자를 사용하지 않으며, 마침표로 끝내지 않습니다.
  │       │
  │       └─⫸ Commit Scope: 영향을 미치는 범위, 모듈, 라이브러리 등
  │
  └─⫸ Commit Type: build | chore | ci | docs | feat | fix | perf | refactor | revert | style | test
<type>과 <summary> 필드는 필수 항목이며, (<scope>)와 (<jira issue>) 필드는 선택사항입니다.
```

`(<jira issue>)` 필드의 경우, 선택사항이지만 아래의 링크에 설명된 Autolink 설정을 해주면 코드의 변경점을 쉽게 트래킹 할 수 있으므로 가능하면 사용하는 것을 권장드립니다.
https://htw-cloud.atlassian.net/wiki/spaces/KDOG/pages/255295491/Repository+Autolink
