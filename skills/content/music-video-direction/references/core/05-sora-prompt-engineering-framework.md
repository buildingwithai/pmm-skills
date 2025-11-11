# Sora Prompt Engineering Framework for Music Videos

## Understanding Sora 2 (2025)

**What is Sora?**
- OpenAI's text-to-video AI model
- Generates up to 10-second 720p videos with synchronized audio
- Diffusion model with Transformer architecture
- Realistic physics modeling and camera behavior

**Key Capabilities:**
- Time-stamped action control
- Synchronized dialogue and audio
- Realistic camera movements
- Physics-accurate material behavior
- Remix/re-cut/blend editing tools

**Key Limitations:**
- 10-second maximum clip length (currently)
- Complex human expressions can look uncanny
- Fine text/details may be unreliable
- Continuity between separate generations requires planning

## The Optimal Sora Prompt Structure

Research shows best-performing prompts follow this structure:

### Length: 50-100 Words
- Too short (< 30 words): Vague, unpredictable results
- Optimal (50-100 words): Detailed but focused
- Too long (> 150 words): Model may ignore details

### Format: 2-4 Sentences
Each sentence has a specific purpose:

**Sentence 1: SCENE SETUP**
`A [setting/environment] at [time of day/lighting condition];`

**Sentence 2: SUBJECT & CAMERA**
`[shot type] of [subject] [doing what]; [lens choice], [camera movement];`

**Sentence 3: LIGHTING & COLOR**
`[lighting description]; [color palette/grading];`

**Sentence 4: TIME-STAMPED ACTIONS**
`At [timestamp]: [specific action]; At [timestamp]: [next action]; At [timestamp]: [final action].`

**Optional Sentence 5: AUDIO & EXCLUSIONS**
`[Audio cues with timing]. [Exclusions - what NOT to do].`

## Component Breakdown

### 1. Scene Setup (Setting & Environment)

**Be specific about:**
- Physical location (urban intersection, forest clearing, abandoned warehouse, infinite white void)
- Time of day (dawn, golden hour, midnight, overcast afternoon)
- Weather if relevant (rain, fog, clear sky)
- Atmosphere (crowded, empty, claustrophobic, vast)

**Examples:**
✅ GOOD: "A rain-slicked urban alley in Tokyo at night with neon signs reflecting in puddles"
❌ VAGUE: "A city street"

✅ GOOD: "An infinite white liminal space with no visible walls or horizon"
❌ VAGUE: "A white room"

✅ GOOD: "A sun-drenched California beach at golden hour with gentle waves"
❌ VAGUE: "A beach"

### 2. Subject & Framing

**Shot Types** (be explicit):
- Close-up (CU): Face fills frame
- Medium close-up (MCU): Head and shoulders
- Medium shot (MS): Waist up
- Medium wide shot (MWS): Full body
- Wide shot (WS): Subject in environment
- Extreme wide shot (EWS): Vast environment, subject small
- Over-the-shoulder (OTS): From behind one subject looking at another
- Point of view (POV): Camera is subject's eyes
- Bird's eye view: Directly overhead
- Low angle: Camera below subject looking up
- High angle: Camera above subject looking down
- Dutch angle: Tilted frame

**Subject Description:**
- What they're wearing (be specific about color, style)
- What they're doing (active verbs)
- Expression/emotion if visible
- Position in frame

**Examples:**
✅ "Medium close-up of woman in gray wool coat, face pressed against invisible glass barrier"
✅ "Wide shot of silhouetted figure standing on wooden stool in middle of calm ocean"
✅ "Bird's eye view of person lying in field of red poppies, arms spread"

### 3. Lens & Camera Movement

**Lens Choices:**
- Wide-angle / 24mm: Distorted, expansive, immersive
- 35mm: Cinematic standard, natural perspective
- 50mm: Human eye POV, neutral
- Telephoto / 85mm+: Compressed perspective, shallow DOF
- Fisheye: Extreme distortion, surreal
- Macro: Extreme close-up detail

**Camera Movements:**
- Static / locked-off: No movement, stability
- Slow push in: Dolly slowly toward subject
- Pull back / reveal: Dolly away to reveal more
- Pan left/right: Rotate horizontally
- Tilt up/down: Rotate vertically
- Crane up/down: Vertical rise or descent
- Steadicam: Smooth floating movement
- Handheld: Organic, shaky, documentary feel
- Orbit / arc: Circle around subject
- Whip pan: Fast, blurred horizontal movement

**Depth of Field:**
- Shallow depth of field: Subject sharp, background blurred (cinematic)
- Deep focus: Everything sharp (documentary, Wes Anderson style)

**Examples:**
✅ "35mm lens, shallow depth of field, slow dolly push in"
✅ "24mm wide lens creating mild distortion, camera slowly orbiting subject"
✅ "Telephoto lens with compressed perspective, static locked-off frame"
✅ "Handheld camera with organic movement, 50mm lens"

### 4. Lighting

**Direction:**
- Key light from [direction]: Main light source
- Backlight / rim light: From behind, creates outline
- Overhead: From above
- Side light: Creates dramatic shadows
- Motivated by [source]: Sun, window, streetlight, etc.

**Quality:**
- Soft / diffused: Gentle shadows, flattering
- Hard / harsh: Sharp shadows, dramatic
- Natural: Sunlight
- Practical: Visible source in frame (lamp, neon sign)
- Volumetric: Visible light rays through fog/dust

**Descriptors:**
- Golden hour backlighting
- Harsh overhead fluorescents
- Soft window light
- Dramatic rim lighting
- Moody low-key lighting
- Bright high-key lighting

**Examples:**
✅ "Soft golden hour backlighting creating rim light around subject"
✅ "Harsh overhead fluorescent lighting with deep shadows"
✅ "Single dramatic spotlight from above, all else in darkness"
✅ "Natural diffused overcast lighting, even and flat"

### 5. Color Palette & Grading

**Approaches:**
- Specific color names: Teal, amber, crimson, sage green
- Color theory: Warm vs cool, saturated vs desaturated
- Popular grades: Teal and orange, desaturated cool, vintage warm
- Mood descriptors: Moody, bright, pastel, high-contrast

**Formats:**
- "[Primary color] and [secondary color] color palette"
- "[Adjective] [color] color grade"
- "Saturated/desaturated [colors]"

**Examples:**
✅ "Desaturated blue-gray color palette with warm orange key light creating contrast"
✅ "High-contrast teal and orange cinematic color grade"
✅ "Pastel pink and lavender dream-like color palette"
✅ "Monochromatic deep red color scheme"
✅ "Natural colors with slight warmth, film grain texture"

### 6. Time-Stamped Action Progression (CRITICAL)

This is what makes Sora prompts work for music videos. You must specify WHAT HAPPENS WHEN.

**Format:**
`At 0:00: [initial state/action]; At 0:0X: [development]; At 0:0X: [progression]; At 0:0X: [conclusion].`

**Timing Strategy for 10 Seconds:**

**4-Beat Structure (Most Common):**
- At 0:00 (start): Initial state
- At 0:03 (early): First development
- At 0:06 (middle): Peak action or shift
- At 0:09 (end): Conclusion or setup for next clip

**3-Beat Structure (Simpler):**
- At 0:00: Beginning
- At 0:04-05: Middle turn
- At 0:08-09: Ending

**How Much Can Happen?**
- One major action arc per 10 seconds
- 2-3 micro-actions maximum
- Keep it simple: Complexity = unpredictability

**Examples:**

✅ **Simple progression:**
```
At 0:00: figure stands still, hands at sides; At 0:04: slowly raises arms to shoulder height; At 0:08: arms fully extended, head tilts back.
```

✅ **Environmental change:**
```
At 0:00: room is empty and white; At 0:03: flowers begin sprouting from floor; At 0:06: flowers have grown waist-high; At 0:09: entire room filled with blooming flowers.
```

✅ **Emotional progression:**
```
At 0:00: subject sits motionless staring forward; At 0:03: eyes begin to well with tears; At 0:06: single tear rolls down cheek; At 0:09: breaks into full crying, hands cover face.
```

✅ **Camera + action combined:**
```
At 0:00: wide shot, figure tiny in vast space; At 0:03: camera begins slow push in; At 0:06: now medium shot, figure's expression visible; At 0:09: close-up of eyes, single tear forming.
```

❌ **Too much happening:**
```
At 0:00: person runs down street; At 0:02: jumps over car; At 0:04: rolls through window; At 0:05: fights three people; At 0:07: steals keys; At 0:09: drives away in different car.
```
This is unrealistic for one 10-second clip.

### 7. Audio Synchronization

Sora 2 can synchronize audio to visuals when prompted.

**Dialogue Format:**
```
[Number] lines of dialogue, [language], lip-synced. First line at [timestamp]: [who says what]. Second line at [timestamp]: [who responds].
```

**Example:**
```
Two lines of dialogue in English, lip-synced. First line at 0:02 seconds: woman asks "Where did you go?". Second line at 0:06: man responds "I never left," while looking away.
```

**Music Cues Format:**
```
At [timestamp]: [musical element] [action]. At [timestamp]: [next cue].
```

**Example:**
```
At 0:00: sustained synthesizer note begins (C3, bright pad sound). At 0:03: bass pulse enters (80 BPM), synced to hair movement. At 0:06: vocal sample enters ('oh' vowel, pitched to F4). At 0:09: all elements crescendo as camera completes rotation.
```

**Sound Effects:**
```
[Description of sound] at [timestamp], synchronized with [visual action].
```

**Example:**
```
Gentle breathing audio at 0:01. Desperate vocalization crescendos from 0:03 to 0:08. Sharp glass crack sound at 0:06 synced with visual impact.
```

### 8. Exclusions (What NOT to Do)

Tell Sora what to avoid:

**Common Exclusions:**
- "No lens flare"
- "Maintain natural skin tones"
- "No overexposed highlights"
- "Avoid motion blur"
- "No text or writing"
- "No distorted faces"
- "Consistent lighting (no flickering)"

**Examples:**
✅ "No lens flare, maintain natural skin tones, avoid overexposure"
✅ "No motion blur, ensure sharp focus on subject throughout"
✅ "No text visible, no brand logos, clean background"

## Complete Prompt Templates

### Template 1: Performance/Artist Focus

```
A [setting] at [time]; [shot type] of [artist description] [performing action]; [lens], [camera movement]; [lighting description]; [color palette]; At 0:00: [initial pose/action]; At 0:03: [development]; At 0:06: [peak moment]; At 0:09: [conclusion]. [Audio cues]. [Exclusions].
```

**Filled Example:**
```
A stark black void with single circular spotlight on concrete floor; medium shot of silhouetted figure in long coat holding vintage microphone on stand; 50mm lens, slow 360-degree orbit around subject; dramatic single spotlight from above creating hard shadows; high-contrast black and white; At 0:00: figure stands still, head down; At 0:03: slowly raises head toward camera; At 0:06: begins singing motion, spotlight brightens; At 0:09: head tilts back, arms spread wide. Vocal begins at 0:06, builds to 0:09. No lens flare, maintain silhouette, avoid face detail.
```

### Template 2: Narrative Moment

```
A [specific location] [time/weather]; [shot type] of [character(s)] [doing what]; [lens], [camera movement]; [lighting]; [color palette]; At 0:00: [scene start]; At 0:03: [action/interaction]; At 0:06: [turning point]; At 0:09: [emotional beat]. [Audio if needed]. [Exclusions].
```

**Filled Example:**
```
A 1940s train platform with steam and vintage luggage; medium two-shot of couple embracing, woman in period dress, man in military uniform; 35mm lens, static camera emphasizing stillness of moment; soft diffused morning light through station skylights; warm sepia-toned color grade with slight vignette; At 0:00: couple holds embrace tightly; At 0:03: woman pulls back to look at man's face; At 0:06: they kiss; At 0:09: man steps back toward train, hands still clasped. Distant train whistle at 0:08. No modern elements, maintain period accuracy, natural skin tones.
```

### Template 3: Conceptual/Surreal

```
A [impossible/surreal environment]; [shot type] of [subject/object]; [lens creating specific effect], [unusual camera movement]; [dramatic lighting]; [stylized color palette]; At 0:00: [surreal starting state]; At 0:03: [impossible physics begin]; At 0:06: [surrealism peaks]; At 0:09: [surprising conclusion]. [Soundscape]. [Exclusions].
```

**Filled Example:**
```
An infinite ocean at dusk with perfectly still water reflecting purple sky; wide shot of person sitting upright on wooden bar stool in middle of ocean, water level at their ankles, old-fashioned microphone on stand beside them, cord disappearing into the water; 24mm wide lens creating slight distortion, slow aerial crane shot rising from water level to 20 feet above; soft twilight glow from horizon, volumetric light through misty air; desaturated purple and teal color palette; At 0:00: person sits motionless, staring at horizon; At 0:03: they reach for microphone; At 0:06: begin singing motion, ripples emanate from stool in perfect circles; At 0:09: camera at peak height, person tiny in vast ocean, sky begins to darken. Ambient ocean sounds with ethereal reverb, vocal echo begins at 0:06. No waves, maintain perfect stillness except intentional ripples, ensure stool appears grounded despite impossible scenario.
```

### Template 4: Environmental/Atmospheric

```
A [environment with rich detail] at [specific time]; [establishing shot type]; [lens choice], [revealing camera move]; [natural/motivated lighting]; [realistic or stylized color]; At 0:00: [environment revealed]; At 0:03: [environmental element introduced]; At 0:06: [atmosphere builds]; At 0:09: [payoff or subject revealed]. [Environmental audio]. [Exclusions].
```

**Filled Example:**
```
An abandoned brutalist apartment complex overgrown with vines and moss, broken windows, at overcast dawn; extreme wide shot tilting up from ground level to reveal massive structure; 35mm lens, slow crane up movement; soft diffused overcast natural lighting, patches of warm light from rising sun breaking through clouds; desaturated greens and grays with warm accent light; At 0:00: ground-level view of cracked concrete and wild grass; At 0:03: tilt begins revealing vine-covered walls; At 0:06: halfway up building, birds burst from broken window; At 0:09: full structure revealed against moody sky. Wind rustling leaves at 0:00, bird sounds at 0:06 synced to visual. No people, no modern elements, emphasize decay and nature reclaiming structure.
```

## Advanced Techniques

### Technique 1: Continuity Planning Between Clips

Since Sora generates one clip at a time, plan for cuts:

**Method: End-State to Start-State Matching**

Clip 1 ends: `At 0:09: figure reaches doorway, hand on handle`
Clip 2 starts: `At 0:00: close-up of hand turning door handle`

**Method: Match Cut Preparation**

Clip 1 ends: `At 0:09: extreme close-up of eye, pupil dilating`
Clip 2 starts: `At 0:00: match cut from eye to tunnel opening, camera pulling back`

**Method: Consistent Environment Cues**

All clips in sequence share:
- Same color palette description
- Same lighting cues
- Same weather/time of day

### Technique 2: Escalation Across Clips

Music videos build energy. Reflect this in prompts:

**Verse 1 Clip (Lower Energy):**
```
...static camera; slow, minimal movement; At 0:00-0:09: subtle developments...
```

**Chorus 1 Clip (Higher Energy):**
```
...camera orbiting; faster action; At 0:00-0:09: dynamic movements peaking at 0:06...
```

**Final Chorus Clip (Maximum Energy):**
```
...whip pan camera; rapid action; multiple elements moving; At 0:00-0:09: crescendo of all visual elements...
```

### Technique 3: Motif Repetition with Variation

Establish a visual motif, then vary it:

**Chorus 1:**
```
...single red balloon floating upward in white room...
```

**Chorus 2:**
```
...three red balloons floating upward, room now with shadows...
```

**Final Chorus:**
```
...dozens of red balloons filling entire frame, room transformed...
```

### Technique 4: Physics Specification

For realism, specify material behavior:

✅ "Silk fabric billowing in gentle 5 mph breeze, realistic fluid physics"
✅ "Water splash with realistic droplet physics and gravity"
✅ "Hair movement natural for 10 mph wind, individual strands visible"

### Technique 5: Negative Space and Minimalism

Sometimes less is more:

```
A completely white infinite void with no visible floor or walls; single subject in center, extreme wide shot making them appear tiny and isolated; subject is only element in frame...
```

Minimalism = more AI generation reliability.

## Common Mistakes to Avoid

❌ **Too vague:** "A person in a place doing something cool"
✅ **Specific:** "A woman in red dress on marble staircase, looking over shoulder at camera"

❌ **No timing:** "Person walks and then runs"
✅ **Time-stamped:** "At 0:00: person walks slowly; At 0:05: breaks into run"

❌ **Conflicting directions:** "Bright sunny day, dark moody lighting"
✅ **Coherent:** "Overcast day with soft diffused lighting creating moody atmosphere"

❌ **Too many actions:** 10 different things in 10 seconds
✅ **Focused:** 1 clear action arc with 2-3 beats

❌ **Ignoring 10-second limit:** Describing 30 seconds of action
✅ **Realistic pacing:** What can actually happen in 10 seconds

❌ **No camera specified:** Assumes default
✅ **Camera explicit:** "35mm lens, slow dolly push in"

❌ **Generic color:** "Nice colors"
✅ **Specific palette:** "Teal and orange cinematic grade" or "Desaturated cool blue-grays"

## Prompt Length Examples

### TOO SHORT (Unpredictable):
```
Person on stool in ocean singing.
```

### TOO LONG (Model may ignore details):
```
An expansive, seemingly infinite ocean stretching to the horizon in every direction, with perfectly calm, mirror-like water that reflects the sky above, which is painted in hues of deep purple transitioning to soft lavender near the horizon line, at the precise moment of dusk when the sun has just set but ambient light still fills the sky, creating that magical twilight glow that photographers call the blue hour; positioned in the exact center of the frame is a person, appearing to be in their mid-twenties, wearing casual contemporary clothing including a light gray cotton t-shirt and dark blue denim jeans, sitting with perfect upright posture on a vintage wooden bar stool that looks like it belongs in a 1950s American diner, with chrome legs and a round wooden seat showing signs of wear and age, the water level reaching precisely to their ankle height, just covering their feet but not the stool's lowest rung; beside them stands an old-fashioned dynamic microphone on a tall metal stand, the kind you'd see in recordings from the 1940s, with a thick black cable that extends from the microphone down into the water and disappears beneath the surface as if plugged into the ocean floor itself...
```

### OPTIMAL (50-100 words):
```
An infinite ocean at dusk with perfectly still water reflecting purple sky; wide shot of person in gray t-shirt and jeans sitting on wooden bar stool in middle of ocean, water at ankle level, vintage microphone on stand beside them, cord disappearing into water; 24mm wide lens, slow aerial crane rising; soft twilight glow, volumetric mist; desaturated purple and teal palette; At 0:00: person motionless staring at horizon; At 0:03: reaches for microphone; At 0:06: begins singing, ripples emanate; At 0:09: camera at peak, person tiny in vast ocean. No waves, maintain perfect stillness.
```

## Testing and Iteration

**Generate variations:**
1. Create core prompt
2. Generate 3-5 variations with slight changes
3. Review results
4. Identify what worked / didn't work
5. Refine prompt with learnings
6. Regenerate

**Use remix feature:**
- Strength levels: subtle, mild, strong, custom
- Make targeted changes: "enhance shadow depth" or "slow pan by 20%"

## Music Video-Specific Prompt Strategies

### Strategy 1: Beat-Synced Actions

If song has prominent beat at 90 BPM:
- 90 BPM = 1 beat every 0.67 seconds
- In 10 seconds = ~15 beats
- Place visual accents on beat divisions

```
At 0:00: [on beat]; At 0:67: [on beat]; At 1:34: [on beat]... etc.
```

More practical: Hit major beats
```
At 0:00: beat 1; At 2:68: beat 4; At 5:36: beat 8; At 8:04: beat 12
```

### Strategy 2: Lyric Visualization

If generating for specific lyric moment:

Include in prompt: `Scene visualizes lyric "..." through [metaphor/literal approach]`

This helps you maintain conceptual coherence.

### Strategy 3: Establishing vs Developing vs Payoff

**Establishing clip** (intro/first verse):
- Longer, slower reveals
- Set the world/rules
- At 0:00-0:05: slow setup, At 0:05-0:09: first hint of concept

**Developing clip** (verse 2, bridge):
- Build on established visuals
- Add complexity
- At 0:00: reference previous clip, At 0:03-0:09: develop further

**Payoff clip** (final chorus):
- Fastest action
- Biggest visual moment
- At 0:00-0:09: rapid escalation to peak

---

**Next Steps:**
1. Read `06-10-second-scene-structure.md` for breaking down timing
2. Reference `08-cinematography-technical-reference.md` for all camera/lens terminology
3. Use the templates in `/templates/sora-prompt-template.md` for structured prompt creation

**Remember:** The key to great Sora prompts is SPECIFICITY + TIMING + COHERENCE. Every word should serve the vision.
