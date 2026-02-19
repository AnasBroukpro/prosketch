# ProSketch - Future Development Roadmap

## Current Status (v0.1.0)
- ✅ Drawing canvas with Excalidraw
- ✅ Export (PNG, SVG, JSON)
- ✅ Local storage (browser only)
- ✅ Dark/Light theme toggle
- ✅ Welcome screen with custom branding

---

## Phase 1: Authentication & Access Control
**Goal: Team-only access with secure login**

| Feature | Technology | Priority |
|---------|------------|----------|
| User authentication | Clerk or Supabase Auth | High |
| Team management | Custom database tables | High |
| Role-based access (admin/member) | Backend logic | Medium |
| SSO integration (Google, GitHub) | OAuth providers | Medium |

---

## Phase 2: Cloud Storage & Scenes
**Goal: Save and organize drawings in the cloud**

| Feature | Technology | Priority |
|---------|------------|----------|
| Cloud storage for scenes | Supabase Database | High |
| Unlimited scenes | Database + CDN | High |
| Folders organization | Database structure | High |
| Auto-save | Real-time sync | High |
| Version history | Database snapshots | Medium |

---

## Phase 3: Sharing & Collaboration
**Goal: Share drawings with view/edit permissions**

| Feature | Technology | Priority |
|---------|------------|----------|
| Share links (view only) | Unique URLs + permissions | High |
| Share links (edit access) | Permission system | High |
| Read-only embeds | iframe + API | Medium |
| Public/Private scenes | Access control | Medium |

---

## Phase 4: Real-time Collaboration
**Goal: Multiple users editing simultaneously**

| Feature | Technology | Priority |
|---------|------------|----------|
| Real-time cursor presence | WebSockets (Liveblocks) | High |
| Multi-user editing | CRDT or operational transform | High |
| Live presence indicators | WebSocket events | Medium |
| Conflict resolution | Backend logic | High |

---

## Phase 5: Comments & Communication
**Goal: Discuss and annotate drawings**

| Feature | Technology | Priority |
|---------|------------|----------|
| Comments on drawings | Database + real-time | High |
| @mentions | User lookup + notifications | Medium |
| Thread replies | Database structure | Medium |
| Comment resolution | Status tracking | Low |

---

## Phase 6: Voice & Video
**Goal: Live communication while collaborating**

| Feature | Technology | Priority |
|---------|------------|----------|
| Voice hangouts | WebRTC (LiveKit/Daily) | Medium |
| Screen sharing | WebRTC | Medium |
| Video calls | WebRTC | Low |
| Recording (optional) | Cloud recording API | Low |

---

## Phase 7: Presentations
**Goal: Present drawings as slides**

| Feature | Technology | Priority |
|---------|------------|----------|
| Frame-based slides | Custom React components | Medium |
| Presentation mode | Full-screen API | Medium |
| Slide navigation | Keyboard controls | Medium |
| Export as PDF | jsPDF or similar | Low |

---

## Phase 8: AI Features
**Goal: AI-powered drawing assistance**

| Feature | Technology | Priority |
|---------|------------|----------|
| AI shape generation | OpenAI GPT-4 Vision | Medium |
| Text-to-diagram | LLM + Excalidraw format | Medium |
| Auto-layout | Algorithm or AI | Low |
| Smart suggestions | ML model | Low |

---

## Phase 9: Team Management
**Goal: Enterprise team features**

| Feature | Technology | Priority |
|---------|------------|----------|
| Team workspaces | Database multi-tenancy | High |
| Member invitations | Email service | High |
| Usage analytics | Dashboard + charts | Low |
| Billing integration | Stripe | Low |

---

## Recommended Tech Stack

### Backend
- **Database:** Supabase (PostgreSQL) - Free tier available
- **Auth:** Clerk (easiest) or Supabase Auth
- **Real-time:** Liveblocks or Pusher
- **Storage:** Supabase Storage or AWS S3

### Frontend
- **Framework:** React + TypeScript (current)
- **UI:** Tailwind CSS + shadcn/ui
- **Drawing:** Excalidraw (current)

### AI/ML
- **Text-to-diagram:** OpenAI GPT-4 API
- **Image generation:** DALL-E or Stable Diffusion

### Communication
- **Voice/Video:** LiveKit or Daily.co
- **Notifications:** Resend or SendGrid

---

## Estimated Timeline

| Phase | Duration | Dependencies |
|-------|----------|--------------|
| Phase 1 | 1-2 weeks | Auth service account |
| Phase 2 | 2-3 weeks | Database setup |
| Phase 3 | 1-2 weeks | Phase 1 & 2 complete |
| Phase 4 | 2-3 weeks | WebSocket service |
| Phase 5 | 1-2 weeks | Phase 4 complete |
| Phase 6 | 2-3 weeks | WebRTC service |
| Phase 7 | 1-2 weeks | None |
| Phase 8 | 2-3 weeks | OpenAI API key |
| Phase 9 | 2-3 weeks | Stripe account |

---

## Cost Estimates (Monthly)

### Free Tier Options
- Supabase: Free (500MB database, 1GB storage)
- Clerk: Free (5,000 MAU)
- Liveblocks: Free (1M reads/month)
- Vercel: Free (hobby projects)

### Paid Tier (Production)
- Supabase Pro: $25/month
- Clerk Pro: $25/month
- Liveblocks: $49/month
- OpenAI API: Pay per usage
- LiveKit: $50/month

**Total estimated:** $100-150/month for production

---

## Next Steps

1. Create accounts for:
   - [ ] Supabase (supabase.com)
   - [ ] Clerk (clerk.com) or use Supabase Auth
   - [ ] Liveblocks (liveblocks.io) for collaboration

2. Set up development environment:
   - [ ] Configure environment variables
   - [ ] Set up database schema
   - [ ] Implement authentication

3. Begin Phase 1 development

---

*Last updated: February 2026*
