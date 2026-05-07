# Skill Test

> 작성일: 2026-05-07

Claude Code 스킬을 만들고 공유하는 방법을 소개하는 예제 저장소입니다.

## 소개

이 저장소는 Claude Code에서 사용할 수 있는 **스킬(Skill)** 을 직접 만들어보고, Git으로 공유하는 전체 흐름을 예제와 함께 정리합니다.

스킬이란 Claude에게 특정 작업을 수행하는 방법을 알려주는 재사용 가능한 명령어 묶음입니다.

## 스킬 구조

스킬은 하나의 폴더와 그 안의 `SKILL.md` 파일로 구성됩니다.

```
my-skill/
└── SKILL.md
```

`SKILL.md` 파일은 다음과 같은 frontmatter를 포함해야 합니다.

```markdown
---
name: my-skill
description: 이 스킬이 언제 사용되어야 하는지에 대한 설명
---

# My Skill

스킬이 수행해야 할 작업을 단계별로 작성합니다.

## 사용 방법
1. ...
2. ...
```

### 필수 필드

| 필드 | 설명 |
|------|------|
| `name` | 스킬 이름 (폴더명과 동일하게 권장) |
| `description` | 스킬이 어떤 상황에서 사용되어야 하는지 명확하게 기술 |

## 스킬 만드는 법

1. 저장소 루트에 스킬 이름의 폴더를 생성합니다.
2. 폴더 안에 `SKILL.md` 파일을 만듭니다.
3. frontmatter와 본문(작업 절차)을 작성합니다.
4. 필요하다면 참고 파일이나 스크립트를 함께 포함시킵니다.

## 스킬 공유하는 법

### 1. Git 저장소에 푸시
```bash
git add .
git commit -m "feat: add my-skill"
git push origin main
```

### 2. 다른 사람이 사용하기

저장소를 클론하여 Claude Code의 스킬 디렉토리에 복사하거나 심볼릭 링크를 걸어두면 사용할 수 있습니다.

```bash
git clone <repository-url>
cp -r <skill-folder> ~/.claude/skills/
```

## 예제 스킬

이 저장소에 포함된 예제 스킬:

- [markdown-toc](markdown-toc/) — 마크다운 파일의 TOC 자동 생성/갱신

## 참고

- Claude Code 공식 문서
- 본 저장소의 예제 스킬 폴더

## 라이선스

자유롭게 사용하고 수정하실 수 있습니다.
