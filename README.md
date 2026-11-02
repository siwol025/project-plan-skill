# project-plan

프로젝트/서비스 기획서를 항목 하나씩 사용자와 대화하며 작성하는 [Claude Code](https://claude.com/claude-code) 스킬.

## 기획서 목차

1. 개요
2. 왜 이 프로젝트/서비스가 필요한가?
3. 이 프로젝트와 유사한 구현 사례
4. 사용 사례 식별 및 프로젝트 필요성 평가
5. 요구사항 수집 및 분석
6. 기술스택 결정 및 트레이드오프 비교
7. 아키텍처 및 기능별 파이프라인
8. 기능목록

## 동작 방식

- 항목마다 필요한 정보를 다 얻을 때까지 질문한다.
- 초안을 보여주고, 사용자가 확정하면 `기획서_<프로젝트명>.md`의 해당 섹션만 갱신한다.
- 필요하면 항목별 하위 항목을 만든다.
- 중간에 멈춰도 같은 파일에서 이어서 작성할 수 있다.

## 설치

모든 프로젝트에서 쓰려면 사용자 스킬 폴더에 복사한다.

macOS / Linux:

```bash
git clone https://github.com/siwol025/project-plan-skill.git
mkdir -p ~/.claude/skills
cp -r project-plan-skill/project-plan ~/.claude/skills/
```

Windows (PowerShell):

```powershell
git clone https://github.com/siwol025/project-plan-skill.git
New-Item -ItemType Directory -Force "$HOME\.claude\skills"
Copy-Item -Recurse project-plan-skill\project-plan "$HOME\.claude\skills\"
```

특정 프로젝트에서만 쓰려면 `project-plan` 폴더를 그 프로젝트의 `.claude/skills/` 아래에 복사한다.

## 사용

Claude Code에서 `/project-plan`을 입력하거나 "기획서 작성해줘"라고 요청한다.
