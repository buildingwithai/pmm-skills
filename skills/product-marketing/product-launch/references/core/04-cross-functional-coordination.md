# Cross-Functional Launch Coordination

**Purpose:** Coordinate product, marketing, sales, customer success, and engineering teams for successful launch execution.

**When to use:** Early in launch planning (Week 2 of 90-day roadmap) to establish roles, responsibilities, and communication cadences.

**Output:** RACI matrix, communication plan, and coordination playbooks for solopreneurs and enterprise teams.

---

## Overview

Product launches fail when teams aren't aligned. This guide provides frameworks for coordination whether you're a solopreneur doing everything yourself or an enterprise with dozens of stakeholders.

**Key principle:** Clear ownership prevents dropped balls. Ambiguity kills launches.

---

## The RACI Framework

### RACI Defined

**R - Responsible:** Does the work
**A - Accountable:** Owns the outcome (only ONE per task)
**C - Consulted:** Provides input (two-way communication)
**I - Informed:** Kept in the loop (one-way communication)

**Rule:** Each task needs exactly ONE "A" (accountable). Multiple Rs are fine.

---

## Enterprise RACI Matrix for Product Launches

### Core Launch Activities

| Activity | PMM | Product | Marketing | Sales | CS | Eng | Exec |
|----------|-----|---------|-----------|-------|----|----|------|
| **Positioning** | A/R | C | C | C | I | I | C |
| **Messaging** | A/R | C | C | C | I | I | I |
| **GTM Strategy** | A/R | C | C | C | I | I | C |
| **Product Roadmap** | C | A/R | I | I | I | R | C |
| **Beta Program** | R | A | I | I | R | R | I |
| **Sales Enablement** | A/R | C | I | R | C | I | I |
| **Website/Landing Page** | C | C | A/R | I | I | I | I |
| **Content Creation** | R | C | A/R | I | I | I | I |
| **Launch Event** | R | C | A/R | I | I | I | C |
| **Metrics Dashboard** | R | C | A | I | R | I | C |
| **Customer Communication** | R | C | R | I | A | I | I |
| **Launch Day Execution** | A | R | R | R | R | I | I |

**A = Accountable (owner), R = Responsible (does work), C = Consulted, I = Informed**

---

## Solopreneur Playbook

### When You're Doing Everything

**Reality check:** As a solopreneur, you are R, A, C, and I for everything. The key is sequencing and leveraging AI/tools.

**Phase 1: Foundation (Weeks 1-2)**
- [ ] **Positioning:** Use `positioning` skill + ChatGPT to draft (2 days)
- [ ] **Messaging:** Use `messaging` skill + AI for multiple variations (2 days)
- [ ] **Landing page:** Use Carrd/Webflow templates (1-2 days)
- [ ] **Analytics setup:** Plausible or Simple Analytics (1 hour)

**Phase 2: Content (Weeks 3-4)**
- [ ] **Video demo:** Loom or ScreenStudio (2-3 hours)
- [ ] **Blog post:** ChatGPT draft + your editing (3-4 hours)
- [ ] **Social content:** Buffer to schedule posts (1 hour)
- [ ] **Product Hunt page:** Use template (2 hours)

**Phase 3: Beta (Weeks 5-6)**
- [ ] **Recruit 5-10 beta users:** From Twitter, LinkedIn, IndieHackers (ongoing)
- [ ] **Collect feedback:** TypeForm survey + direct DMs (daily check-ins)
- [ ] **Iterate:** Ship improvements rapidly (daily)

**Phase 4: Launch (Week 7)**
- [ ] **Product Hunt:** Hour-by-hour engagement (see `advanced/product-hunt-mastery.md`)
- [ ] **Community posts:** Reddit, IndieHackers (authentic, helpful)
- [ ] **Email waitlist:** ConvertKit or Mailchimp (pre-written sequence)
- [ ] **Monitor:** Plausible dashboard + Twitter notifications

**Tools for solopreneurs:**
- **Design:** Canva, Figma (community), Midjourney
- **Video:** Loom, ScreenStudio, Descript
- **Writing:** ChatGPT, Claude, Jasper
- **Email:** ConvertKit, Mailchimp
- **Analytics:** Plausible, Simple Analytics
- **Community:** Discord, Slack
- **Project mgmt:** Notion, Coda

**Time allocation:**
- 60%: Product development and core features
- 20%: Content and community building
- 10%: Tools and infrastructure
- 10%: Launch day execution

---

## Enterprise Coordination Playbook

### Team Structure for Tier 1 Launch

**Core Launch Team (meets weekly):**
- Product Marketing Manager (Lead/DRI)
- Product Manager
- Demand Gen Manager
- Sales Enablement Manager
- Content Manager
- Customer Success Manager

**Extended Team (informed, consulted as needed):**
- Engineering Lead
- Design Lead
- Data/Analytics
- Legal/Compliance
- Finance (pricing)
- PR/Communications

**Executive Sponsors (monthly updates):**
- CPO or VP Product
- CMO or VP Marketing
- CRO or VP Sales

---

### Communication Cadences

**Daily Standups (Final 2 weeks before launch):**
- **Who:** Core launch team
- **Duration:** 15 minutes
- **Format:** What shipped yesterday, what's shipping today, blockers
- **Tool:** Slack standup bot or quick Zoom

**Weekly Launch Syncs (Weeks 1-12 of 90-day roadmap):**
- **Who:** Core launch team
- **Duration:** 60 minutes
- **Agenda:**
  - Review roadmap progress
  - Review open action items
  - Identify risks and blockers
  - Preview next week's priorities
- **Tool:** Zoom + shared doc for notes

**Biweekly Stakeholder Updates (Weeks 1-12):**
- **Who:** Core team + extended team
- **Duration:** 30 minutes
- **Format:** Async Loom video or written update
- **Content:** Progress, metrics, key decisions, asks

**Monthly Executive Reviews:**
- **Who:** Core team lead + executive sponsors
- **Duration:** 30 minutes
- **Agenda:** High-level progress, resource needs, strategic decisions

---

### Stakeholder Management Tactics

**1. Single Source of Truth**
- Create one launch brief document (Notion, Coda, Confluence)
- All key info in one place: positioning, messaging, timeline, metrics
- Update weekly
- Share link widely

**2. Decision Log**
- Document all major decisions (why, when, who decided)
- Prevents relitigating decisions
- Example: "Decided to use PLG motion based on price point and TTValue analysis - 3/15/24"

**3. RACI Review at Kickoff**
- Week 1: Review RACI matrix with all teams
- Get explicit agreement on roles
- Surface concerns early
- Update RACI as scope changes

**4. Escalation Paths**
- Define what requires escalation (e.g., budget overruns >10%, timeline delays >1 week)
- Clear escalation path: PMM → Marketing Director → CMO
- Don't escalate prematurely, but don't wait too long

---

## Common Coordination Failures

### Failure 1: Product and Marketing Not Aligned

**Symptom:** Marketing creating content for features that aren't ready, or product shipping without marketing awareness.

**Root cause:** Different roadmaps, poor communication

**Fix:**
- Product and PMM meet weekly
- Product roadmap shared 4 weeks in advance
- Marketing lockdown 2 weeks before launch (no more changes)

---

### Failure 2: Sales Unprepared at Launch

**Symptom:** Sales team learning about launch on launch day, can't articulate value.

**Root cause:** Sales enablement too late, no training

**Fix:**
- Sales enablement starts Week 6 (4 weeks before launch)
- Required training session Week 7
- Battlecards ready Week 7
- Demo environment ready Week 7
- See `sales-enablement` skill for details

---

### Failure 3: Customer Success Surprised

**Symptom:** Support tickets flood in, CS team doesn't know how to help.

**Root cause:** CS not looped in, no documentation ready

**Fix:**
- CS involved in beta program (see customer feedback firsthand)
- Help center articles ready Week 8
- CS training session Week 8
- First-week support plan (extra staffing)

---

### Failure 4: Engineering Shipping Bugs on Launch Day

**Symptom:** Critical bugs discovered right before or during launch.

**Root cause:** Inadequate testing, compressed timeline

**Fix:**
- Code freeze 1 week before launch (only critical bugs)
- Beta testing minimum 2 weeks (3-4 weeks for Tier 1)
- Load testing before launch day
- Rollback plan ready

---

## Launch Roles and Responsibilities

### Product Marketing Manager (DRI - Directly Responsible Individual)

**Pre-Launch:**
- Own positioning and messaging
- Create GTM strategy
- Build launch plan and timeline
- Coordinate all teams
- Create enablement materials
- Own launch brief

**Launch Day:**
- War room leader
- Monitor all channels
- Coordinate responses
- Track metrics real-time
- Communicate to stakeholders

**Post-Launch:**
- Week 1 report
- Iteration plan
- Retrospective facilitation

---

### Product Manager

**Pre-Launch:**
- Define feature scope
- Lead beta program
- Make product decisions
- Provide feature explanations for content
- Ensure product ready for launch

**Launch Day:**
- Monitor for bugs
- Rapid response to technical issues
- Coordinate with engineering

**Post-Launch:**
- Collect product feedback
- Prioritize post-launch iterations
- Ship rapid improvements

---

### Marketing/Demand Gen

**Pre-Launch:**
- Create all launch content (blog, video, social)
- Build landing pages
- Set up email campaigns
- Prepare paid ads
- Plan launch event

**Launch Day:**
- Publish all content
- Activate campaigns
- Monitor engagement
- Amplify top performers

**Post-Launch:**
- Optimize campaigns
- A/B test variations
- Scale what works

---

### Sales/Revenue

**Pre-Launch:**
- Participate in enablement training
- Provide feedback on battlecards
- Update CRM for tracking
- Align on sales plays

**Launch Day:**
- Monitor inbound leads
- Rapid follow-up on qualified leads
- Use launch as outbound hook

**Post-Launch:**
- Report win/loss reasons
- Update battlecards with real objections
- Share best practices

---

### Customer Success

**Pre-Launch:**
- Participate in beta
- Create help center content
- Train support team
- Plan for increased volume

**Launch Day:**
- Monitor support tickets
- Respond rapidly
- Escalate critical issues

**Post-Launch:**
- Collect qualitative feedback
- Update documentation
- Create tutorials based on common questions

---

## Decision-Making Framework

### Types of Decisions

**1. One-Way Doors (Hard to reverse)**
- Pricing and packaging
- Market positioning
- Product architecture changes
- Brand decisions

**Required:** Executive approval, cross-functional input
**Timeline:** Allow 2-4 weeks for alignment

---

**2. Two-Way Doors (Easy to reverse)**
- Launch messaging variations
- Channel tactics
- Content topics
- Beta program structure

**Required:** PMM decision with consultation
**Timeline:** Can decide in days

---

### Decision Rights Matrix

| Decision | Who Decides | Who Must Approve | Who Consulted |
|----------|-------------|------------------|---------------|
| **Positioning** | PMM | CMO, VP Product | Sales, CS |
| **Messaging** | PMM | Dir Marketing | Product, Sales |
| **Launch Date** | Product | CPO, CMO | All teams |
| **Pricing** | Product/PMM | CFO, CEO | Sales, Marketing |
| **Feature Scope** | Product | CPO | PMM, Eng |
| **Launch Tier** | PMM | Dir Marketing | Product, Sales |
| **Channel Mix** | Marketing | CMO | PMM, Sales |
| **Sales Plays** | Sales Enablement | CRO | PMM, Product |

---

## War Room Setup (Launch Day)

### Physical or Virtual

**Purpose:** Real-time coordination on launch day

**Who:** Core launch team (PMM, Product, Marketing, Sales lead, CS lead)

**Duration:** 8 hours on launch day (9am-5pm)

**Setup:**
- Central Slack channel (#launch-war-room)
- Zoom room (optional, for critical issues)
- Shared dashboard (metrics visible to all)
- Incident response protocol

**Roles:**
- **Commander:** PMM (makes calls, coordinates)
- **Product monitor:** PM (watches for bugs)
- **Marketing monitor:** Marketing (watches campaigns, social)
- **Customer monitor:** CS (watches tickets, feedback)
- **Scribe:** Takes notes, logs issues

**Activities:**
- Hourly check-ins (what's working, what's not)
- Real-time issue triage
- Celebration of milestones
- Rapid decision-making

See `06-launch-day-playbook.md` for hour-by-hour execution.

---

## Post-Launch Retrospective

### Week After Launch: What Went Well, What Didn't

**Facilitator:** PMM or neutral party

**Attendees:** Core launch team

**Duration:** 90 minutes

**Format:**
1. **Wins (20 min):** What went well? Celebrate successes.
2. **Learnings (30 min):** What didn't go as planned? Why?
3. **Improvements (30 min):** What would we do differently next time?
4. **Action Items (10 min):** What specific changes will we make?

**Document and share:** Update launch playbook template for next time.

---

## Next Steps

**After establishing coordination:**

1. **Create your RACI matrix:** Use template in `assets/templates/raci-matrix.md`
2. **Set up communication cadences:** Schedule recurring meetings
3. **Build launch brief:** Single source of truth for all stakeholders
4. **Review decision rights:** Ensure clarity on who decides what

**For solopreneurs:**
- Accept you're doing everything
- Use AI and tools to multiply productivity
- Focus on highest-leverage activities
- Ship fast, iterate faster

**For enterprise teams:**
- Clarity prevents chaos
- Over-communicate rather than under
- Document decisions to prevent re-litigation
- Celebrate team wins throughout the journey

**Related guides:**
- `06-launch-day-playbook.md` - War room execution
- `sales-enablement` skill - Deep sales coordination
- `rollout-and-launch` skill - Internal rollout tactics
