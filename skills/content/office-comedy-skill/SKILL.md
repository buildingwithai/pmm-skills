# Office-Style SaaS Comedy Clip Generator

## Purpose

Generate 10-30 second comedy clips in The Office mockumentary style, focused on SaaS startup life, QuickPing platform scenarios, and the absurdities of modern tech culture.

This skill provides a reusable framework for creating short-form comedy videos optimized for Sora 2 generation, with specific characters, scenarios, and visual storytelling structures.

## How to Use This Skill

**In conversation:**
- "Using the Office-style SaaS comedy skill, create a 30-second clip about a failed product demo"
- "Generate a 10-second talking head of Jovanny not taking feedback well"
- "Create a clip showing the engineer rivalry between Wei and Raj"

**What you'll get:**
- Complete scene breakdown with timestamp-specific Sora 2 prompts
- Character-consistent dialogue and behavior
- Mockumentary-style camera directions
- Visual comedy setups that work without dialogue

## Core Framework: The Office Formula for Short Form

### The Mockumentary Foundation

Every clip operates within the conceit that a documentary crew is filming this startup. This enables:

1. **Talking Head Segments** - Characters address camera directly in interview style
2. **Camera Awareness** - Characters glance at camera when something absurd happens (Jim-style)
3. **Verite Realism** - Handheld camera, quick reaction zooms, "imperfect" framing
4. **No Laugh Track** - Humor operates at a "3" instead of sitcom "8" - subtle, uncomfortable, real

### The Cringe Comedy Engine

The heart of Office humor for our SaaS world:

- **Social norm violations** - Characters break workplace/professional norms
- **Lack of self-awareness** - They don't realize they're being inappropriate
- **Unresolved awkwardness** - No neat resolution, discomfort just sits there
- **Prolonged discomfort** - Hold on awkward moments longer than comfortable
- **Mundane setting heightens absurdity** - The ordinary startup environment makes weird behavior weirder

### Character-Driven Comedy

Every joke comes from **who the character is**, not setup-punchline. See `characters.md` for full profiles.

The humor emerges from:
- Putting characters in situations that expose their blind spots
- Specific character pairings that create natural conflict
- Characters staying true to their essence even in absurd situations

## 10-Second Comedy Structures

Since you're working with ultra-short form, here are formulas optimized for 10-second chunks:

### 1. The Visual Reveal (5-10 seconds)
Setup in environment → Reveal the absurd thing → Cut to reaction

**Example:**
- 0-3s: Close-up of someone's screen
- 3-6s: Zoom out to reveal 47 browser tabs all titled "Dashboard_Final_v2_FINAL"
- 6-10s: Cut to their face, completely unbothered, clicking to add another tab

### 2. The Awkward Statement (10 seconds)
Character makes cringe statement → Camera holds on uncomfortable silence/reactions

**Example:**
- 0-4s: Jovanny in all-hands: "We're not just a team, we're a family"
- 4-10s: Cut to series of uncomfortable faces, people looking away, Wei looking at camera

### 3. The Failed Attempt (10 seconds)
Character tries something → Immediate catastrophic failure → Their reaction

**Example:**
- 0-3s: Engineer hovering mouse over "Deploy to Production" button
- 3-4s: Clicks it confidently
- 4-6s: Immediate cascade of error messages
- 6-10s: Slow zoom on their frozen face

### 4. The Oblivious Pride (10 seconds)
Character proud of something obviously terrible

**Example:**
- 0-6s: Chad presenting graph with obviously manipulated metrics, beaming
- 6-8s: Cut to Wei's deadpan face
- 8-10s: Wei slow turn to camera with "are you seeing this" expression

### 5. The Contrast Cut (10 seconds)
Show two things that contradict each other in rapid succession

**Example:**
- 0-5s: Jovanny talking head: "We have infinite runway, we're extremely well capitalized"
- 5-10s: Hard cut to QuickPing Slack #finance channel showing bank balance: $1,247.32

## 30-Second Structure (Three-Beat Story)

When you have 30 seconds, use the three-beat structure:

**Beat 1 (0-10s): Setup**
Establish the situation or character doing something. Your premise.

**Beat 2 (10-20s): Complication**
Things get worse or more absurd. The turn.

**Beat 3 (20-30s): Payoff**
Punchline or reaction that sells it. Often a talking head reflecting on what happened.

**Example: "The Pivot Announcement"**

- **0-10s:** Jovanny in all-hands Zoom, everyone visible: "I've been thinking a lot, and we need to pivot. We're now a Web3 company."
- **10-20s:** Cut to rapid sequence of faces dropping, someone's hand going to their forehead, laptop being slowly closed. Cut to QuickPing Slack DMs lighting up.
- **20-30s:** Talking head of Wei: "This is the third pivot this month. Last week we were doing AI agents for dogs."

## Mockumentary Techniques for Sora 2

### Camera Work Vocabulary

Describe cameras like this in your Sora prompts:

- **"Handheld mockumentary style"** - Slight shake, follows action
- **"Quick zoom to catch reaction"** - The signature Office move
- **"Dirty frame"** - Shoot through/past objects (plant leaves, monitor, doorframe)
- **"Talking head setup"** - Character centered, slightly off-center, plain background, direct eye contact with camera
- **"Verite style coverage"** - Camera discovering the action, not perfectly framed
- **"Whip pan to reaction"** - Fast camera movement to catch someone's face

### The Reaction Economy

In 10 seconds, you don't have time for dialogue exchanges. Use REACTIONS:

1. Person A does/says absurd thing (4 seconds)
2. Cut to Person B's reaction face (3 seconds)
3. Cut back to Person A being oblivious (3 seconds)

**Key reaction types:**
- **The Jim look** - Direct camera look with raised eyebrows (Wei specializes in this)
- **The uncomfortable shift** - Looking away, tight smile, physical discomfort
- **The frozen face** - Complete stillness as they process something terrible
- **The slow head turn** - Gradual turn to camera in disbelief

### Visual Comedy Over Dialogue

Since Sora 2 will add dialogue unless you prevent it, lean heavily on:

- **Facial expressions** - Describe exactly: "eyebrows raised," "tight-lipped smile," "eyes widening"
- **Physical actions** - "Rubbing temples," "slowly closing laptop," "leaning back in chair"
- **Text on screens** - Slack messages, error messages, dashboards, code - show don't tell
- **Environmental details** - "Motivational poster behind them says 'FAIL FAST,'" "Coffee mug says 'World's Best CEO'"

## Sora 2 Prompting: The Technical Format

### Critical Rules for Sora 2

Based on current Sora 2 behavior:

1. **Explicit timestamps required** - Break every clip into time segments
2. **Dialogue must be specified or blocked** - If you don't want dialogue, say "NO DIALOGUE" or "SILENT EXCEPT [specific sound]"
3. **Camera angles per segment** - Each time segment needs camera position stated
4. **Precise character positioning** - Where are they, what are they doing, what's their expression

### Prompt Template Structure

```
[CLIP DURATION: 10 seconds]

SEGMENT 1 (0-3 seconds):
- Camera: [angle, movement, style]
- Scene: [location, what's in frame]
- Character(s): [who, position, action, expression]
- Audio: [dialogue with "quotes" OR "NO DIALOGUE" OR specific sounds]

SEGMENT 2 (3-7 seconds):
- Camera: [angle, movement, style]
- Scene: [location, what's in frame]
- Character(s): [who, position, action, expression]
- Audio: [dialogue with "quotes" OR "NO DIALOGUE" OR specific sounds]

SEGMENT 3 (7-10 seconds):
- Camera: [angle, movement, style]
- Scene: [location, what's in frame]
- Character(s): [who, position, action, expression]
- Audio: [dialogue with "quotes" OR "NO DIALOGUE" OR specific sounds]

VISUAL STYLE: Mockumentary, handheld, The Office-style, natural lighting, slightly desaturated colors

CHARACTER DETAILS: [Physical descriptions for any characters in scene - reference characters.md]
```

### Example Sora 2 Prompt

```
[CLIP DURATION: 10 seconds]

SEGMENT 1 (0-4 seconds):
- Camera: Handheld mockumentary style, medium shot, slightly unstable
- Scene: Modern startup office, QuickPing logo visible on wall, afternoon natural light through windows
- Character: Jovanny (32, 6'4", athletic build, wearing startup casual - fitted henley shirt) standing confidently in front of team seated at long table
- Audio: Jovanny says: "Team, I have amazing news. We're pivoting to blockchain."
- NO OTHER DIALOGUE

SEGMENT 2 (4-7 seconds):
- Camera: Quick whip pan right, handheld, landing on medium close-up
- Scene: Same office, focus on seated team members
- Character: Wei (28, Asian, glasses, hoodie, deadpan expression) sitting at table, slowly turns head toward camera
- Audio: NO DIALOGUE, ambient office sounds only

SEGMENT 3 (7-10 seconds):
- Camera: Tight close-up, handheld, slight zoom in
- Scene: Wei's face filling frame
- Character: Wei with classic "Jim face" - raised eyebrows, slight head tilt, direct eye contact with camera, expression says "can you believe this"
- Audio: NO DIALOGUE, ambient sounds continue

VISUAL STYLE: The Office mockumentary style, handheld camera, natural office lighting, slightly desaturated colors, verite documentary feel

CHARACTER DETAILS:
- Jovanny: 6'4", athletic build, 32 years old, wearing fitted henley that shows gym physique, energetic body language
- Wei: 28, Asian American, slim build, glasses, gray hoodie, naturally deadpan facial expressions
```

## The Clip Generation Workflow

### Step 1: Choose Your Scenario
Pick from `scenarios.md` or identify a specific SaaS/QuickPing situation:
- Product/technical scenarios
- Culture/people dynamics
- Business/metrics situations
- QuickPing platform-specific moments

### Step 2: Select Characters
Who's involved? Check `characters.md` for:
- Their core delusion/blind spot
- Their verbal tics
- Their relationship dynamics
- Who they clash with

**Consider character pairings that create natural tension:**
- Jovanny + Wei (oblivious founder + deadpan engineer)
- Wei + Raj (local vs remote engineer rivalry)
- Jovanny + Marcus (trying too hard to be cool + young sales guy who sees through it)
- Chad + anyone (growth hacker intensity vs anyone's sanity)

### Step 3: Decide the Beat
What's the specific funny moment?
- A statement that reveals delusion?
- An action that fails?
- A reveal of something absurd?
- A clash between characters?

### Step 4: Choose Your Structure
For 10 seconds: Pick from the 5 structures above
For 30 seconds: Use the three-beat structure

### Step 5: Break Into Time Segments
Map out exactly what happens when:
- 0-X seconds: This happens
- X-Y seconds: Then this
- Y-Z seconds: Ends with this

Consider:
- Where are the visual beats?
- Where do you need reactions?
- What's shown on screens?
- What physical actions happen?

### Step 6: Write the Sora 2 Prompt
Use the template format:
- Explicit timestamps
- Camera angles per segment
- Character positions and expressions
- Dialogue in quotes OR "NO DIALOGUE"
- Visual style notes
- Character physical descriptions

### Step 7: Review for Character Consistency
Check against `characters.md`:
- Would this character actually say/do this?
- Is their blind spot showing appropriately?
- Are relationships dynamics accurate?
- Does their physicality match (especially Jovanny's height, Wei's deadpan, Raj's accent)?

## SaaS & QuickPing Specific Angles

### The QuickPing Meta Layer

Since QuickPing is a portfolio-building platform with Slack-like channels, you have built-in comedy opportunities:

**Portfolio Anxiety:**
- Over-curated campaigns hiding disasters
- "Results: TBD" on every project
- Extremely detailed explanations of why things failed
- Someone organizing channels obsessively while avoiding actual work

**Platform as Character:**
- Notification chaos
- @channel abuse (someone @channels for lunch order)
- Thread that becomes a novel
- Channel names that are too specific (#brand-refresh-iteration-47)

**The Showcase vs Reality:**
- Campaign channel showing beautiful work
- Cut to talking head: "Yeah, that client fired us"
- Projects marked "Successful" but comments tell different story

### Universal SaaS Archetypes

Tap into situations anyone in SaaS instantly recognizes:

**Product/Tech:**
- Demo breaks during crucial moment
- "It works on my machine"
- Bug renamed as feature
- The pivot announcement
- Name debates that get existential
- Design review becomes philosophical crisis

**Culture/People:**
- Forced fun (mandatory team building)
- All-hands where no cameras are on
- "Quick sync" that's 90 minutes
- Someone unmuted on Zoom saying something they shouldn't
- Startup perks that are depressing (pizza party instead of raises)

**Business:**
- Celebrating users that are clearly bots
- MRR chart that's obviously flatlining
- "We're default alive" delusion
- Competitor launches your exact feature
- Customer churn excuse bingo

**Remote Work Dynamics:**
- Raj on laptop in meeting while everyone else is in room
- Time zone confusion ("It's 2am for Raj but this is important")
- "Can you hear me?" technical difficulties
- Background chaos in remote worker's feed
- Someone clearly in bed on Zoom call

### Character Blind Spots in Action

Use character flaws to drive scenarios:

**Jovanny's ADHD/Prioritization:**
- Starts meeting about Q4 goals, ends talking about office plant arrangement
- Three different "top priority" initiatives announced in one day
- Rabbit hole visible in his screen share (started checking analytics, now on Wikipedia about Byzantine history)

**Jovanny Can't Take Feedback:**
- Someone gently suggests something, Jovanny gets defensive: "Well I think it's great actually"
- Cut to talking head of that person: "He asked for feedback"

**Jovanny Trying to Be Cool with Marcus:**
- "Yo bro, you hitting the gym today? I can bench like 285, used to be 300 but you know..."
- Marcus dead-eyed: "...okay"
- Jovanny talking head: "Marcus and I have great rapport, very mentorship vibe"
- Marcus talking head: "I don't know what he's talking about"

**Zoe the Intern Gets Away with Everything:**
- Accidentally deletes production database
- "Ohmigod I'm so sorry I didn't mean to!" (sweet innocent voice)
- Everyone: "It's okay! These things happen!"
- Cut to talking head of Wei: "If I did that I'd be fired. She deleted the entire customer database."

## Reference Files

- **characters.md** - Complete character profiles, blind spots, relationships, physical descriptions
- **scenarios.md** - Library of SaaS/startup situations organized by category
- **examples.md** - Full example clips with complete Sora 2 prompts

## QuickPing Product Context

When working in a project with QuickPing product information, reference:
- Product features and value propositions
- User personas and use cases
- Platform-specific UI/UX details
- Channel structures and workflows

This grounds scenarios in actual QuickPing functionality and creates opportunities for platform-specific visual comedy (showing actual QuickPing interface, channel setups, portfolio presentations, etc.)

## Tips for Maximum Comedy

1. **Silence is powerful** - Don't fill every second with dialogue. Awkward pauses are gold.

2. **Physical comedy lands fast** - Someone spilling coffee, slow-mo laptop close, dramatic standing up - these read immediately.

3. **Screen content is a character** - What's on someone's monitor/phone is often funnier than what they say.

4. **The Jim camera look is your best friend** - Wei looking at camera sells so many jokes without a word.

5. **Escalation within 10 seconds** - Start normal, end absurd. The arc matters even in short form.

6. **Specificity over generality** - "We need to align on our Q4 OKRs around the strategic initiative" is funnier than "We need a meeting."

7. **Character over joke** - If you have to choose between a funny line and character consistency, choose character. That's what makes The Office work.

8. **The reveal is everything** - Structure clips so there's a moment where you SEE the absurd thing, not just hear about it.

9. **Talking heads are setup machines** - Use them to frame what we're about to see OR reflect on what we just saw.

10. **One joke per clip** - Don't cram. A single perfectly executed awkward moment beats three rushed jokes.

## Common Mistakes to Avoid

❌ **Too much dialogue** - You have 10 seconds, make faces do the work
❌ **Explaining the joke** - Show it, don't say it
❌ **Out of character behavior** - Chad suddenly being chill breaks believability
❌ **Rushed timing** - Let awkwardness breathe
❌ **No visual anchor** - Every clip needs something to LOOK at
❌ **Generic office humor** - Make it specifically SaaS/QuickPing
❌ **Forgetting the mockumentary style** - The documentary conceit is what makes it feel real
❌ **Not specifying "NO DIALOGUE" when needed** - Sora will add talking if you don't block it

---

**Ready to generate?** Pick a scenario from `scenarios.md`, grab characters from `characters.md`, choose your structure from above, and build your Sora prompt using the template. See `examples.md` for full reference implementations.
