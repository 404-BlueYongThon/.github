# 404 BlueYongThon

![404 Found Banner](../assets/banner.png)

[![Website](https://img.shields.io/badge/Website-emergency--ai--call.log8.kr-4A90E2)](https://emergency-ai-call.log8.kr)
[![Hackathon](https://img.shields.io/badge/Hackathon-청룡톤_2026-FF6B6B)](https://github.com/404-BlueYongThon)
[![Team](https://img.shields.io/badge/Team-4_Developers-00D9FF)](https://github.com/orgs/404-BlueYongThon/people)

> 404 Not Found → 404 Found

응급 환자를 위한 병원을, AI가 찾아드립니다.

---

## Problem

2026년, 대한민국의 응급실 포화율은 평균 **85%**입니다.  
응급대원은 환자를 싣고 평균 **7개 병원**에 전화합니다.  
매번 같은 증상을 설명하고, 거절당하고, 다시 전화하는 동안...  
**골든타임은 계속 흘러갑니다.**

---

## Solution

### 404 Found: Emergency AI Call System

AI 음성 전화를 통해 여러 병원에 동시 연락하고 실시간으로 수용 가능한 응급실을 매칭하는 시스템입니다.

**Core Features:**

- **AI Voice Call**: GPT-4o 기반 자연스러운 대화
- **Parallel Calling**: 10개 병원에 동시 전화 (Twilio)
- **Real-time Matching**: 거리/중증도 기반 우선순위 (C++)
- **Auto Termination**: 한 병원 승인 시 나머지 자동 끊김
- **Korean Language**: Google Cloud TTS/STT

---

## Repositories

| Repository | Description | Tech Stack |
|------------|-------------|-----------|
| [**BE**](https://github.com/404-BlueYongThon/BE) | Backend API & Voice Processing | NestJS, Python, C++, Docker |
| [**FE**](https://github.com/404-BlueYongThon/FE) | Frontend Web Application | Next.js 14, TypeScript, Tailwind |

---

## Tech Stack

### Backend

| Category | Technology |
|----------|-----------|
| Framework | NestJS 10.x |
| Language | TypeScript 5.0+ |
| AI & Voice | Python FastAPI 3.10+ |
| Algorithm | C++ 17+ |
| Database | PostgreSQL (Prisma) |
| Voice API | Twilio |
| Speech | Google Cloud TTS/STT |
| AI Model | OpenAI GPT-4o |
| Container | Docker Compose |
| Cloud | AWS EC2, RDS, S3 |

### Frontend

| Category | Technology |
|----------|-----------|
| Framework | Next.js 14.x |
| Language | TypeScript 5.0+ |
| Styling | Tailwind CSS 3.x |
| UI Components | Shadcn/ui |
| State Management | Zustand 4.x |
| Server State | TanStack Query 5.x |
| Real-time | Socket.io Client 4.x |
| Maps | Kakao Maps API |
| Deployment | Vercel |

---

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    Frontend (Next.js)                    │
│              emergency-ai-call.log8.kr                   │
└────────────────────┬────────────────────────────────────┘
                     │ HTTPS
┌────────────────────▼────────────────────────────────────┐
│                  Backend (NestJS)                        │
│                   AWS EC2 + Docker                       │
├──────────────┬──────────────┬──────────────────────────┤
│ Voice Module │ Hospital API │ Emergency Manager         │
└──────┬───────┴──────┬───────┴──────────────────────────┘
       │              │
       ▼              ▼
┌─────────────┐  ┌──────────────┐
│   Python    │  │     C++      │
│   FastAPI   │  │   Library    │
├─────────────┤  ├──────────────┤
│ - STT       │  │ - Distance   │
│ - TTS       │  │ - Priority   │
│ - GPT-4o    │  │ - Async      │
└──────┬──────┘  └──────┬───────┘
       │                │
       └────────┬───────┘
                ▼
        ┌──────────────┐
        │    Twilio    │
        │  Voice API   │
        └──────┬───────┘
               │
               ▼
        ┌──────────────┐
        │   Hospitals  │
        └──────────────┘
```

---

## Impact

| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| Hospital Matching Time | 10+ min | < 1 min | **90% ↓** |
| Call Efficiency | Sequential (avg 7 calls) | Parallel (10 calls) | **300% ↑** |
| Paramedic Workload | Patient + Calling | Patient Only | **50% ↓** |
| Golden Time Utilization | 10 min wasted | 9 min saved | **Survival Rate ↑** |

---

## Team

| Name | Role | Contribution |
|------|------|--------------|
| **김덕환** | Full Stack | Next.js, NestJS, 전체 일정 조율, 인프라 |
| **김대준** | Backend & Infra | NestJS, Docker, AWS 배포 |
| **정현승** | Backend | NestJS, API 설계, 페어 프로그래밍 |
| **최대영** | AI & Algorithm | Python AI 음성, C++ 거리 계산 |

**팀의 강점:**

4명 모두 완전히 다른 프레임워크(Next.js, Node.js, NestJS, Spring Boot, Python, C++)를 사용했지만, 하나의 목표를 위해 협력했습니다. 페어 프로그래밍을 통해 기술 융합과 엄청난 성장을 경험했습니다.

---

## Roadmap

### Phase 1: MVP (Hackathon) ✅

- Twilio 음성 통화
- 기본 AI 대화
- Frontend 배포
- Docker 통합

### Phase 2: Hospital Pilot (2-3 months)

- 실제 병원 협업
- 의료법 규제 대응
- HIPAA 보안 강화
- 성능 최적화

### Phase 3: Nationwide Expansion (6 months)

- 전국 병원 DB 구축
- 실시간 응급실 현황 연동
- 모바일 앱 (iOS/Android)
- 119 시스템 통합

### Phase 4: Global (1 year+)

- 다국어 지원 (English, Japanese, Chinese)
- 190개국 Twilio 번호
- WHO 응급 의료 표준 준수

---

## Getting Started

### Backend

```bash
git clone https://github.com/404-BlueYongThon/BE.git
cd BE
npm install
docker-compose up
```

### Frontend

```bash
git clone https://github.com/404-BlueYongThon/FE.git
cd FE
npm install
npm run dev
```

**Detailed documentation**: See individual repository READMEs

---

## Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md).

### Branch Strategy

- `main`: Production-ready code
- `dev`: Development integration
- `feature/<description>`: Feature branches

### Commit Convention

```
feat: Add new feature
fix: Bug fix
docs: Documentation updates
refactor: Code refactoring
test: Test updates
chore: Build/tooling changes
```

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgments

- **중앙대학교 청룡톤 2026**
- **UNIVERSITY MAKEUS CHALLENGE CAU**
- **Google Developer Groups (On Campus · Chung-Ang University)**
- Team member's brave sharing of real emergency experience

---

## Contact

- **Website**: [emergency-ai-call.log8.kr](https://emergency-ai-call.log8.kr)
- **Email**: sachi009955@gmail.com
- **University**: 중앙대학교 (Chung-Ang University)
- **Hackathon**: 청룡톤 2026

---

<div align="center">

**Made with ❤️ by 404 BlueYongThon**

*작고 귀여운 서비스로 소중한 생명을 지킵니다*

</div>
