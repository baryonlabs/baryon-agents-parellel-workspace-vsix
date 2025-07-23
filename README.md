# Baryon Agents Parallel Environment | Spec-driven AI Agents Parallel Isolated Workspace
🚀 Integrated Environment for Agents Parallel Programming - Provides simultaneous workspace for Claude, Cursor, Gemini, Kino agents with Git worktree isolation, TMUX session management, and flexible Spec-driven workflow conversion.


## 🎯 Overview

**🚀 Integrated Environment for Agents Parallel Programming** - Complete development ecosystem for simultaneous AI agent collaboration

### 🎪 Core Concepts
- **🤖 Agents Parallel Programming**: Multiple AI agents working simultaneously and independently
- **🔄 Spec-Driven Workflow Conversion**: Flexible conversion from master specification to agent-specific formats (Claude MD, Cursor MDC, Gemini MD, Kino AWS)
- **🌿 Git Worktree Isolation**: Independent branches and workspaces for each agent
- **🖥️ TMUX Session Management**: Stable terminal environment and session persistence
- **📊 Real-time Monitoring**: Real-time tracking of agent activities and status

### 🏆 Key Features
- **🚀 Parallel Development Environment**: Multiple AI agents working simultaneously and independently
- **🔧 Git Worktree-based Isolation**: Each AI agent works in independent Git branches
- **🖥️ TMUX Session Integration**: Stable terminal environment and session persistence
- **🔄 Flexible Spec Conversion**: Seamless conversion from master spec to agent-specific formats with real-time synchronization
- **📈 Real-time Dashboard**: Integrated VSCode Activity Bar for managing all agents

## 🚀 Features

### ✨ 주요 기능 (v1.3.0)
- 🎯 **마스터 스펙 관리**: Requirements, Design, Tasks 중앙 집중 관리
- 🔄 **유연한 스펙 변환**: 마스터 스펙에서 에이전트별 형식으로 자유로운 전환 (Claude MD ↔ Cursor MDC ↔ Gemini MD ↔ Kino AWS)
- 🌿 **Git Worktree 격리**: 각 에이전트별 독립 브랜치 및 워크스페이스 생성
- 🖥️ **TMUX 세션 관리**: 안정적인 터미널 환경 및 세션 지속성 보장
- 📊 **VSCode 통합**: Activity Bar 통합 직관적 UI로 모든 에이전트 관리
- 📈 **실시간 모니터링**: 각 에이전트 상태 및 활동 내역 실시간 추적
- 🎬 **TMUX 터미널 세션**: 안정적인 에이전트 터미널 환경 제공
- 📅 **Activity Timeline**: 시각적 타임라인으로 에이전트 활동 추적
- 💾 **Activity Export**: 감사 추적을 위한 활동 로그 내보내기
- 🚀 **병렬 개발 환경**: 여러 에이전트 동시 작업으로 개발 속도 향상

### 🤖 지원 AI 에이전트
- **Claude**: `.claude/rules.md`
- **Cursor**: `.cursor/rules.mdc`
- **Gemini**: `.gemini/instructions.md`
- **Kino (AWS)**: `.kino/spec.aws`
- **확장 가능**: 새로운 에이전트 쉽게 추가

## 📦 Installation

### 1. VSCode Marketplace에서 설치
```bash
# VSCode에서 Extensions 검색
A3 Agent Spec Spec Extension
```
VScode marketplace: https://marketplace.visualstudio.com/items?itemName=a3agent-spec-baryonai.a3agent-spec-baryonai

### 2. 수동 설치
```bash
# GitHub에서 다운로드     //현재 작동 안 됨. It’s not working now. Please wait for an update.
git clone https://github.com/your-repo/ai-multi-agent-spec-extension 
cd ai-multi-agent-spec-extension
npm install
npm run package
```

### 3. 필수 요구사항
- **VSCode**: 1.80 이상
- **Git**: 2.20 이상 (worktree 지원)
- **Node.js**: 16 이상
- **TMUX**: ```brew install tmux``` 권장

## 🔧 Setup

### 1. 프로젝트 초기화
```bash
# 프로젝트 폴더에서
Ctrl+Shift+P → "A3 Agent Spec: Initialize Project"
```

### 2. 마스터 스펙 생성
```markdown
# .ai-specs/master-spec.md

# Project: My Amazing App

## Requirements
### REQ-001: 사용자 인증
- **우선순위**: High
- **설명**: JWT 기반 로그인/로그아웃
- **수용 기준**: 
  - [ ] 이메일/패스워드 로그인
  - [ ] 토큰 자동 갱신
  - [ ] 보안 검증

## Design
### Authentication Architecture
- **기술 스택**: Node.js + Express + JWT
- **데이터베이스**: MongoDB
- **암호화**: bcrypt

## Tasks
### TASK-001: JWT 인증 API 구현
- **담당**: Backend Developer
- **상태**: Todo
- **관련 요구사항**: REQ-001
- **하위 작업**:
  - [ ] 로그인 엔드포인트
  - [ ] 토큰 검증 미들웨어
  - [ ] 패스워드 해싱
```

### 3. 에이전트 워크스페이스 생성
```bash
# 자동으로 생성됨
project/
├── .ai-specs/
│   └── master-spec.md
└── ~/.vscode-a3agent-crew/
    └── worktrees/
        ├── claude-21-session-1852b743bcf3bbb0/    # feat-21-session-1852b743bcf3bbb0 브랜치
        ├── cursor-22-session-2963c854dcf4ccb1/    # feat-22-session-2963c854dcf4ccb1 브랜치
        ├── gemini-23-session-3074d965edf5ddc2/    # feat-23-session-3074d965edf5ddc2 브랜치
        └── kino-24-session-4185ea76fee6eed3/      # feat-24-session-4185ea76fee6eed3 브랜치
```

## 🎮 Usage

### 1. 사이드바 패널 열기
- `Ctrl+Shift+P` → `A3 Agent Spec: Show Panel`
- 또는 Activity Bar에서 🤖 아이콘 클릭

### 2. 마스터 스펙 편집
```typescript
// 실시간 변환 및 동기화
마스터 스펙 수정 → 자동으로 모든 에이전트 워크스페이스 업데이트
```

### 3. 에이전트 인스턴스 관리
```bash
# 새 인스턴스 생성
"Create New Instance" → 에이전트 선택 → 작업 할당

# 인스턴스 시작/정지
Instance Panel → Start/Pause/Stop 버튼

# 상태 모니터링
Real-time status updates in VSCode
```

### 4. 브랜치별 작업
```bash
# 각 에이전트가 독립된 브랜치에서 작업
git worktree list
# ~/.vscode-a3agent-crew/worktrees/claude-21-session-1852b743bcf3bbb0    [feat-21-session-1852b743bcf3bbb0]
# ~/.vscode-a3agent-crew/worktrees/cursor-22-session-2963c854dcf4ccb1    [feat-22-session-2963c854dcf4ccb1]
# ~/.vscode-a3agent-crew/worktrees/gemini-23-session-3074d965edf5ddc2   [feat-23-session-3074d965edf5ddc2]
# ~/.vscode-a3agent-crew/worktrees/kino-24-session-4185ea76fee6eed3     [feat-24-session-4185ea76fee6eed3]
```

## 🔄 Workflow

### 🚀 일반적인 개발 플로우

#### 1. 📋 스펙 정의
```markdown
1. 마스터 스펙 작성 (.ai-specs/master-spec.md)
2. 자동 변환 확인 (모든 워크스페이스)
3. 에이전트별 스펙 검토
```

#### 2. 🌿 Git Worktree & TMUX 세션 생성
```bash
# 각 에이전트별 독립 워크스페이스 생성
1. Git worktree 생성 (feat/agent-claude-session/1)
2. TMUX 세션 시작 (ai-agent-claude)
3. 독립 브랜치에서 작업 환경 준비
```

#### 3. 🤖 멀티 에이전트 병렬 작업
```typescript
1. Claude: 전체 아키텍처 설계 (feat/agent-claude-session/1)
2. Cursor: 실시간 코딩 지원 (feat/agent-cursor-session/1)
3. Gemini: 문서 작성 및 테스트 (feat/agent-gemini-session/1)
4. Kino: AWS 인프라 설정 (feat/agent-kino-session/1)
```

#### 4. 🔄 코드 통합
```bash
1. 각 Git worktree에서 독립 작업
2. 완료된 작업을 main으로 머지
3. 충돌 없는 깔끔한 통합
4. TMUX 세션 정리 및 정리
```

## 🎨 UI Components

### 1. Activity Bar 통합 패널
```
🤖 A3 Agent Spec
├── 📊 Agent Dashboard
│   ├── 📝 Master Spec Status
│   ├── 🤖 Agent Instances
│   │   ├── Claude (Running) ✅
│   │   ├── Cursor (Idle) ⏸️
│   │   ├── Gemini (Working) 🔄
│   │   └── Kino (Offline) ❌
│   ├── 🔄 Sync Status
│   └── 📖 Usage Guide
└── 📈 System Status
    ├── 📊 Activity Stats
    ├── 📅 Activity Timeline
    │   ├── [10:30] Claude: File modified README.md
    │   ├── [10:25] Gemini: Terminal session started
    │   ├── [10:20] Cursor: Git commit created
    │   └── [10:15] Claude: Agent registered
    ├── 🎛️ Filter Controls
    └── 💾 Export Options
```

### 2. 상태 표시기
```typescript
// 하단 상태바
"🤖 Multi-Agent: 4 instances | ✅ Synced | 📊 75% Complete"
```

### 3. 명령 팔레트
```bash
Ctrl+Shift+P 명령어:
- A3 Agent Spec: Initialize Project
- A3 Agent Spec: Create Agent Instance
- A3 Agent Spec: Sync All Agents
- A3 Agent Spec: Show Dashboard
- A3 Agent Spec: Export Report
- A3 Agent Spec: Open Dashboard in Editor
- A3 Agent Spec: Settings
```

## ⚙️ Configuration

### 1. 에이전트 설정
```json
// .ai-specs/config.json
{
  "agents": {
    "claude": {
      "enabled": true,
      "format": "markdown",
      "path": ".claude/rules.md",
      "branch_prefix": "feature/claude-"
    },
    "cursor": {
      "enabled": true,
      "format": "mdc",
      "path": ".cursor/rules.mdc",
      "branch_prefix": "feature/cursor-"
    },
    "gemini": {
      "enabled": true,
      "format": "markdown",
      "path": ".gemini/instructions.md",
      "branch_prefix": "feature/gemini-"
    },
    "kino": {
      "enabled": false,
      "format": "aws",
      "path": ".kino/spec.aws",
      "branch_prefix": "feature/kino-"
    }
  },
  "sync": {
    "auto_sync": true,
    "watch_files": true,
    "debounce_ms": 1000
  }
}
```

### 2. 워크스페이스 설정
```json
// .ai-specs/config.json
{
  "workspace": {
    "baseDir": "~/.vscode-a3agent-crew/worktrees",
    "logsDir": "~/.vscode-a3agent-crew/logs",
    "tempDir": "~/.vscode-a3agent-crew/temp",
    "cleanupOnExit": true,
    "maxWorktrees": 10
  },
  "sync": {
    "autoSync": true,
    "watchFiles": true,
    "debounceMs": 1000
  }
}
```

## 🔧 Troubleshooting

### 일반적인 문제 해결

#### 1. 동기화 실패
```bash
문제: 에이전트별 파일이 업데이트되지 않음
해결: 
1. Ctrl+Shift+P → "A3 Agent Spec: Force Sync"
2. .ai-specs/config.json 확인
3. 파일 권한 확인
```

#### 2. 워크스페이스 충돌
```bash
문제: Git worktree 생성 실패
해결:
1. git worktree prune
2. 기존 브랜치 정리
3. 프로젝트 재초기화
```

#### 3. 에이전트 인스턴스 오류
```bash
문제: 에이전트가 시작되지 않음
해결:
1. 각 에이전트 설치 상태 확인
2. API 키 설정 확인
3. 로그 파일 확인 (.ai-specs/logs/)
```

### 로그 확인
```bash
# 확장 로그
Ctrl+Shift+P → "Developer: Show Extension Host"

# 에이전트별 로그
.ai-specs/logs/
├── claude.log
├── cursor.log
├── gemini.log
└── sync.log
```

## 📊 Advanced Features (v1.3.0)

### 1. 🖥️ TMUX 세션 & Git Worktree 통합 관리
```typescript
// Agent Hook Service로 실시간 추적
- 파일 변경 감지 (VSCode FileSystemWatcher)
- TMUX 터미널 세션 추적 및 관리
- Git worktree 상태 모니터링 (커밋, 상태 변경)
- 에이전트 상태 라이프사이클 (active, idle, working, offline, error)
```

### 2. Activity Timeline 인터페이스
```markdown
📅 실시간 타임라인 뷰
├── 🤖 에이전트별 활동 카드 (색상 코딩)
├── 📊 활동 통계 (총 활동, 파일 변경, 커밋, 세션)
├── 🎛️ 에이전트별 필터링
├── 📤 활동 로그 내보내기 (JSON)
└── 🔄 자동 새로고침 (10초 간격)
```

### 3. 🖥️ TMUX 터미널 통합
```bash
# 각 에이전트마다 독립적인 TMUX 세션
tmux list-sessions
# ai-agent-claude   (attached)
# ai-agent-cursor   (detached)
# ai-agent-gemini   (attached)

# Git worktree와 TMUX 세션 1:1 매핑
agent/claude-1640995200000  →  ai-agent-claude
agent/cursor-1640995300000  →  ai-agent-cursor
agent/gemini-1640995400000  →  ai-agent-gemini

# 자동 브랜치 생성 및 체크아웃
feat/agent-claude-session/1
feat/agent-cursor-session/1
feat/agent-gemini-session/1
```

### 4. 활동 로그 및 감사 추적
```json
// .ai-specs/logs/agent-activities-YYYY-MM-DD.json
{
  "id": "activity-1640995200000-abc123",
  "agentType": "claude",
  "timestamp": "2024-07-17T10:30:00.000Z",
  "activityType": "file_changed",
  "details": "File modified: README.md",
  "location": "/path/to/worktree/README.md",
  "branch": "agent/claude-1640995200000",
  "metadata": {
    "relativePath": "README.md"
  }
}
```

### 5. 템플릿 시스템
```yaml
# 프로젝트 타입별 템플릿
templates/
├── web-app.yaml
├── mobile-app.yaml
├── api-service.yaml
└── custom.yaml
```

### 6. 진행률 추적
```typescript
// 자동 진행률 계산
const progress = {
  requirements: completedReqs / totalReqs,
  design: completedDesigns / totalDesigns,
  tasks: completedTasks / totalTasks
};
```

### 7. 보고서 생성
```markdown
# 자동 생성 보고서
- 에이전트별 작업 통계 및 활동 내역
- 완료율 및 소요 시간 분석
- 파일 변경 패턴 및 Git 활동
- 터미널 세션 사용량 추적
- 협업 효율성 분석
```

## 🤝 Contributing

### 새로운 에이전트 추가
```typescript
// src/agents/newAgent.ts
export class NewAgentTransformer implements AgentTransformer {
  transform(masterSpec: MasterSpec): string {
    // 변환 로직 구현
  }
  
  getConfigPath(): string {
    return '.newagent/config.yaml';
  }
}
```

### 변환 규칙 커스터마이징
```typescript
// 커스텀 변환기 등록
registerTransformer('custom-agent', new CustomTransformer());
```

## 🆘 Support

- **GitHub Issues**: 버그 리포트 및 기능 요청
- **Documentation**: 상세 가이드 및 API 문서
- **Community**: Discord 커뮤니티 참여

---

**"🚀 Unify all AI agents with one specification, enable flexible format conversion, and build a stable development environment with 🌿 Git Worktree and 🖥️ TMUX sessions!"**

🎯 **Get Started**: `Ctrl+Shift+P` → `A3 Agent Spec: Initialize Project`
