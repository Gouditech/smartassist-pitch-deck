# Lady Melody — Full Launch Plan

## Phase 1: Visibility (Weeks 1-2)

### 1.1 Google Maps Optimization
- [ ] Create/claim Google Business Profile (if doesn't exist)
- [ ] Fill in: hours, services, photos, description
- [ ] Add 5-10 before/after photos (laser results)
- [ ] Request existing clients for reviews (5⭐ target)
- [ ] Schema markup for "Beauty Salon" in website HTML

### 1.2 Instagram Strategy
**Content Pillars:**
- Before/afters (laser + wax results)
- Educational tips ("5 myths about laser" etc.)
- Client testimonials (video clips)
- Seasonal promotions
- Behind-the-scenes (salon, Melody)

**Execution:**
- [ ] Create 8-10 post templates (I design, Melody approves)
- [ ] Design 2 Reels (before/after carousel, myth-buster)
- [ ] Setup Stories schedule (3x/week)
- [ ] Hashtag strategy (#epilationlaser #étagnières #beauté)
- [ ] Pin booking link in bio

### 1.3 Local Listings
- [ ] Anibis listing: "Lady Melody — Épilation Laser à Étagnières"
- [ ] Tutti.ch entry
- [ ] Facebook Business page optimization
- [ ] Update ALL listings with WhatsApp contact link

### 1.4 Website Integration
- [ ] Add WhatsApp floating button to ladymelody.agenda.ch
- [ ] Copy: "Questions? Chat with Melody 24/7"
- [ ] Track: Count of clicks → WhatsApp (baseline metric)

**Expected outcome (Week 2):**
- 10-15 WhatsApp inquiries from organic traffic
- Agent ready to handle load

---

## Phase 2: AI Agents (Weeks 2-3, Parallel to Phase 1)

### 2.1 Beauty Advisor Agent — Architecture

**Agent Name:** "Melody AI"
**Platform:** Telegram/WhatsApp Bot
**Entry:** Link in bio, floating button on site, Google Maps message

**Agent Brain — Knowledge Base:**

#### Topic 1: "What is Laser Epilations?"
```
User asks: "C'est quoi épilation laser?"
Agent responds:
"La dépilation au laser utilise une lumière intense pour détruire le cheveu à sa racine.

✨ Comment ça marche:
- On cible les cheveux pigmentés
- La lumière détruit le bulbe
- Résultat: peau lisse longtemps

⏱️ Durabilité:
- Résultats visibles: après 3-4 séances
- Durée: 6-12 mois (parfois + long)
- Certains cheveux peuvent repousser finement

🎯 C'est efficace sur:
- Cheveux foncés (blonds moins efficace)
- Peau claire à médium

❓ Des questions? Je peux t'expliquer plus ou te proposer un RDV 👇"
```

#### Topic 2: "Laser vs Waxing"
```
| Laser | Waxing |
|-------|--------|
| Durable (6-12 mois) | Court terme (3-4 semaines) |
| 0 douleur → légère brûlure | Douleur lors du tirage |
| Cher (moins souvent) | Moins cher (plus souvent) |
| Cheveux fins à long terme | Cheveux repoussent normaux |
```

#### Topic 3: "Who is it for?"
```
Parfait pour toi si:
✅ Tu n'aimes pas te raser souvent
✅ Tu veux de la durabilité
✅ T'as des cheveux foncés/visibles

Moins adapté si:
❌ Tu as très peu de poils
❌ Peau ultra bronzée en ce moment
❌ Enceinte (ask doctor first)
```

#### Topic 4: "Pricing"
```
Épilation laser — Jambes: CHF 85 (1h session)
Autres zones: [dynamic based on Melody's pricing]

Forfait 6 séances: -20% (CHF 408)
```

#### Topic 5: "Aftercare"
```
Après ton RDV:
🧴 Hydrate bien (crème neutre 2-3 jours)
☀️ Évite le soleil 48h (SPF 50+)
🚫 Pas de sport intense 24h
🧖 Pas de sauna/piscine 48h
📅 Prochaine séance: 4-6 semaines

Questions? Chat with Melody
```

### 2.2 Booking Agent — Flow

```
User: "Je veux prendre un RDV"

Agent: "Super! 👍

Quel service t'intéresse?
1️⃣ Épilation laser
2️⃣ Épilation cire
3️⃣ Maquillage beauté"

User: "1 (Laser)"

Agent: "Excellente choice! 💪

Quelle zone?
- Jambes
- Aisselles
- Maillot
- Visage
- Autre (précise)"

User: "Jambes"

Agent: "[Checks Agenda.ch API]

Les créneaux dispo cette semaine:
📅 Samedi 15 mars — 10h00
📅 Samedi 15 mars — 14h30
📅 Mercredi 19 mars — 18h00

Ça te convient?"

User: "Samedi 10h"

Agent: "Parfait! Confirmé 👏

📍 Lady Melody, Rte Lausanne 14, Étagnières
📅 Samedi 15 mars 10h00
💅 Épilation laser jambes (1h)
💰 CHF 85

Pour ta première visite, apporte:
- Pièce d'identité
- Hydrate bien la peau la veille

Des questions? Réécris ici ou appelle: [Melody's phone]"

[Auto-syncs to Agenda.ch]
[Melody receives notification: "Nouveau RDV: [Client], Laser jambes, Sam 15h 10h"]
[Client gets SMS/email confirmation]
[Agent sends reminder 24h before]
```

### 2.3 Post-Appointment Flow
```
[Client's RDV finished]

Agent (24h after): "Ça t'a plu? 😊

⭐⭐⭐⭐⭐ Laisse un avis sur Google?
[Link to Google review]

Besoin de réserver la prochaine séance?
👇"
```

### 2.4 Technical Setup

**Tech Stack:**
- Platform: Telegram or WhatsApp Business API
- Integration: Agenda.ch API (read calendar, auto-book)
- AI Model: Claude/ChatGPT + context memory (Melody's specific pricing/services)
- Database: Simple JSON file with:
  - Services & pricing
  - Melody's schedule (synced from Agenda.ch)
  - Client history (optional, privacy-conscious)

**Deployment:**
- Agent runs on Goudi's Mac (Docker container)
- QR code / link shared with Melody
- She can customize agent responses via simple admin panel

---

## Phase 3: Retention & Analytics (Week 4+)

### 3.1 Loyalty & Reminders
- [ ] SMS reminder 2 days before appointment
- [ ] Email reminder 1 week after appointment ("Come back for next session in 4-6 weeks")
- [ ] Loyalty program: "Every 6 sessions = free upgrade"

### 3.2 Review Collection
- Agent asks post-visit: "Rate your experience 1-5"
- If 5⭐: "Would you share on Google?"
- If <5: "How can we improve?" → Flag for Melody

### 3.3 Analytics Dashboard (Simple)
```
This Month:
- Inquiries via agent: X
- Bookings via agent: Y
- Conversion rate: Y/X %
- Average booking time: Z min
- Customer rating: 4.8/5

Compared to last month:
- Traffic ↑ 40%
- Bookings ↑ 25%
```

---

## Deliverables Summary

### For Goudi to Present to Melody:
1. **Pitch deck** (PDF: 5 slides)
   - Before/After vision
   - Agent demo (screenshots)
   - Pricing: 700 CHF/month, 3-month minimum
   - Expected ROI (conservative: +5-10 new clients/month)

2. **Agent demo video** (2-3 min screen recording)
   - Beauty Advisor answering questions
   - Booking flow from start to finish

3. **Contract** (simple 1-page)
   - Scope: Phase 1 + 2 + 3
   - Duration: 3 months
   - Cancellation: 30-day notice
   - Success metrics (baselines)

### For Melody to Execute:
1. **Social media content pack** (8 posts + 2 Reels templates)
2. **Admin guide** (how to update agent responses, prices, schedule)
3. **WhatsApp link** (to share in bio, listings, website)

---

## Timeline

| Week | Goudi | Sam | Melody |
|------|-------|-----|--------|
| 1 | Contact Melody, pitch | Build Beauty Advisor agent | Reviews Phase 1 plan |
| 1-2 | Monitor | Finish agent, create pitch deck | Execute Google/Instagram/Listings |
| 2 | Approve agent, confirm | Deploy agent, setup integrations | Test agent, approve copy |
| 3-4+ | Monitor results, adjust | Monitor metrics, optimize | Use agent daily |

---

## Success Metrics (3 months)

- **Visibility:** +50% more traffic to ladymelody.agenda.ch
- **Engagement:** 20+ WhatsApp inquiries/month
- **Conversion:** 50%+ of inquiries → bookings
- **Revenue:** +5-8 new client bookings/month (400-680 CHF additional revenue)
- **Satisfaction:** 4.8+ average review rating

---

_Status: READY FOR LAUNCH — Awaiting Goudi approval to contact Melody._
