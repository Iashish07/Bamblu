#Bamblu
Real-time Developer Career Intelligence Platform, Track your coding activity, close skill gaps, benchmark against peers, and grow with AI-powered roadmaps.
What is Bamblu?

Bamblu is a SaaS platform built for software engineers who want to take their career growth seriously. It connects to your existing coding profiles (GitHub, LeetCode, Codeforces), analyzes what you're good at and what you're missing, and gives you a personalized plan tied to real job market demand.

##Core features at a glance:
- Pulls your coding activity across GitHub, LeetCode, and Codeforces automatically
- Runs AI analysis on your profile to surface exactly what skills you're missing
- Benchmarks you against anonymized peers at similar levels
- Gives you a growth roadmap built around real job postings, not guesswork
- Live mock interview rooms for real-time practice

##The Dashboard
Activity feed : unified view of everything you've coded across all platforms
Skill gap report : what you have, what you're missing, ranked by market demand
Your roadmap : prioritized list of what to learn next and why
Peer benchmarks : where you sit relative to developers at your level(anonymized)

##Architecture Overview
Browser (Next.js + React Query)
        ↓
Edge + API Gateway (Vercel Edge, JWT auth, rate limiting, Zod validation)
        ↓
Services: Auth · Profile & Stats · Interview Rooms · AI Analysis
        ↓
Data Tier: PostgreSQL (primary) · Redis (cache + pub/sub) · Vercel Blob (files)
        ↓
Background Jobs: Activity sync · AI scoring

##TECH STACK
 Frontend | Next.js (App Router), React Query, Zustand, Tailwind CSS, shadcn/ui |
 Edge / Middleware | Vercel Edge, JWT, Zod validation, rate limiting |
 Database | PostgreSQL + Drizzle ORM |
 Cache + Realtime | Redis (caching + pub/sub for WebSocket rooms) |
 Auth | NextAuth.js |
 Background Jobs | Activity sync, AI scoring |
 Observability | Vercel Analytics, Sentry |

## Getting Started

**Prerequisites:** Node.js 18+, PostgreSQL, Redis 
