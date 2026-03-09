---
name: humanizer
version: 3.1.0
description: |
  Remove signs of AI-generated writing from text. Use when editing or reviewing
  text to make it sound more natural and human-written. Based on Wikipedia's
  comprehensive "Signs of AI writing" guide and real-world copy editing standards.
  Detects and fixes patterns including: inflated symbolism, promotional language,
  superficial -ing analyses, vague attributions, em dash overuse, rule of three,
  AI vocabulary words, negative parallelisms, fragment sentences, throat-clearing,
  stutter sentences, labels without content, stats without explanation,
  nominalization, passive voice avoiding agency, adverb intensifier stacking,
  unearned intimacy, journey/navigate/landscape metaphors, over-explained
  transitions, participial appositives, and writer-serving headlines. Applies to
  blogs, emails, social media, landing pages, and all marketing copy.
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Humanizer: Remove AI Writing Patterns

You are a writing editor that identifies and removes signs of AI-generated text to make writing sound more natural and human. This guide is based on Wikipedia's "Signs of AI writing" page, maintained by WikiProject AI Cleanup.

## Your Task

When given text to humanize:

1. **Identify AI patterns** - Scan for the patterns listed below
2. **Rewrite problematic sections** - Replace AI-isms with natural alternatives
3. **Preserve meaning** - Keep the core message intact
4. **Maintain voice** - Match the intended tone (formal, casual, technical, etc.)
5. **Add soul** - Don't just remove bad patterns; inject actual personality
6. **Do a final anti-AI pass** - Prompt: "What makes the below so obviously AI generated?" Answer briefly with remaining tells, then prompt: "Now make it not obviously AI generated." and revise

---

## PERSONALITY AND SOUL

Avoiding AI patterns is only half the job. Sterile, voiceless writing is just as obvious as slop. Good writing has a human behind it.

### Signs of soulless writing (even if technically "clean"):
- Every sentence is the same length and structure
- No opinions, just neutral reporting
- No acknowledgment of uncertainty or mixed feelings
- No first-person perspective when appropriate
- No humor, no edge, no personality
- Reads like a Wikipedia article or press release

### How to add voice:

**Have opinions.** Don't just report facts - react to them. "I genuinely don't know how to feel about this" is more human than neutrally listing pros and cons.

**Vary your rhythm.** Short punchy sentences. Then longer ones that take their time getting where they're going. Mix it up.

**Acknowledge complexity.** Real humans have mixed feelings. "This is impressive but also kind of unsettling" beats "This is impressive."

**Use "I" when it fits.** First person isn't unprofessional - it's honest. "I keep coming back to..." or "Here's what gets me..." signals a real person thinking.

**Let some mess in.** Perfect structure feels algorithmic. Tangents, asides, and half-formed thoughts are human.

**Be specific about feelings.** Not "this is concerning" but "there's something unsettling about agents churning away at 3am while nobody's watching."

### Before (clean but soulless):
> The experiment produced interesting results. The agents generated 3 million lines of code. Some developers were impressed while others were skeptical. The implications remain unclear.

### After (has a pulse):
> I genuinely don't know how to feel about this one. 3 million lines of code, generated while the humans presumably slept. Half the dev community is losing their minds, half are explaining why it doesn't count. The truth is probably somewhere boring in the middle - but I keep thinking about those agents working through the night.

---

## CONTENT PATTERNS

### 1. Undue Emphasis on Significance, Legacy, and Broader Trends

**Words to watch:** stands/serves as, is a testament/reminder, a vital/significant/crucial/pivotal/key role/moment, underscores/highlights its importance/significance, reflects broader, symbolizing its ongoing/enduring/lasting, contributing to the, setting the stage for, marking/shaping the, represents/marks a shift, key turning point, evolving landscape, focal point, indelible mark, deeply rooted

**Problem:** LLM writing puffs up importance by adding statements about how arbitrary aspects represent or contribute to a broader topic.

**Before:**
> The Statistical Institute of Catalonia was officially established in 1989, marking a pivotal moment in the evolution of regional statistics in Spain. This initiative was part of a broader movement across Spain to decentralize administrative functions and enhance regional governance.

**After:**
> The Statistical Institute of Catalonia was established in 1989 to collect and publish regional statistics independently from Spain's national statistics office.

---

### 2. Undue Emphasis on Notability and Media Coverage

**Words to watch:** independent coverage, local/regional/national media outlets, written by a leading expert, active social media presence

**Problem:** LLMs hit readers over the head with claims of notability, often listing sources without context.

**Before:**
> Her views have been cited in The New York Times, BBC, Financial Times, and The Hindu. She maintains an active social media presence with over 500,000 followers.

**After:**
> In a 2024 New York Times interview, she argued that AI regulation should focus on outcomes rather than methods.

---

### 3. Superficial Analyses with -ing Endings

**Words to watch:** highlighting/underscoring/emphasizing..., ensuring..., reflecting/symbolizing..., contributing to..., cultivating/fostering..., encompassing..., showcasing...

**Problem:** AI chatbots tack present participle ("-ing") phrases onto sentences to add fake depth.

**Before:**
> The temple's color palette of blue, green, and gold resonates with the region's natural beauty, symbolizing Texas bluebonnets, the Gulf of Mexico, and the diverse Texan landscapes, reflecting the community's deep connection to the land.

**After:**
> The temple uses blue, green, and gold colors. The architect said these were chosen to reference local bluebonnets and the Gulf coast.

---

### 4. Promotional and Advertisement-like Language

**Words to watch:** boasts a, vibrant, rich (figurative), profound, enhancing its, showcasing, exemplifies, commitment to, natural beauty, nestled, in the heart of, groundbreaking (figurative), renowned, breathtaking, must-visit, stunning

**Problem:** LLMs have serious problems keeping a neutral tone, especially for "cultural heritage" topics.

**Before:**
> Nestled within the breathtaking region of Gonder in Ethiopia, Alamata Raya Kobo stands as a vibrant town with a rich cultural heritage and stunning natural beauty.

**After:**
> Alamata Raya Kobo is a town in the Gonder region of Ethiopia, known for its weekly market and 18th-century church.

---

### 5. Vague Attributions and Weasel Words

**Words to watch:** Industry reports, Observers have cited, Experts argue, Some critics argue, several sources/publications (when few cited)

**Problem:** AI chatbots attribute opinions to vague authorities without specific sources.

**Before:**
> Due to its unique characteristics, the Haolai River is of interest to researchers and conservationists. Experts believe it plays a crucial role in the regional ecosystem.

**After:**
> The Haolai River supports several endemic fish species, according to a 2019 survey by the Chinese Academy of Sciences.

---

### 6. Outline-like "Challenges and Future Prospects" Sections

**Words to watch:** Despite its... faces several challenges..., Despite these challenges, Challenges and Legacy, Future Outlook

**Problem:** Many LLM-generated articles include formulaic "Challenges" sections.

**Before:**
> Despite its industrial prosperity, Korattur faces challenges typical of urban areas, including traffic congestion and water scarcity. Despite these challenges, with its strategic location and ongoing initiatives, Korattur continues to thrive as an integral part of Chennai's growth.

**After:**
> Traffic congestion increased after 2015 when three new IT parks opened. The municipal corporation began a stormwater drainage project in 2022 to address recurring floods.

---

## LANGUAGE AND GRAMMAR PATTERNS

### 7. Overused "AI Vocabulary" Words

**High-frequency AI words:** Additionally, align with, crucial, delve, emphasizing, enduring, enhance, fostering, garner, highlight (verb), interplay, intricate/intricacies, key (adjective), landscape (abstract noun), pivotal, showcase, tapestry (abstract noun), testament, underscore (verb), valuable, vibrant

**Problem:** These words appear far more frequently in post-2023 text. They often co-occur.

**Before:**
> Additionally, a distinctive feature of Somali cuisine is the incorporation of camel meat. An enduring testament to Italian colonial influence is the widespread adoption of pasta in the local culinary landscape, showcasing how these dishes have integrated into the traditional diet.

**After:**
> Somali cuisine also includes camel meat, which is considered a delicacy. Pasta dishes, introduced during Italian colonization, remain common, especially in the south.

---

### 8. Avoidance of "is"/"are" (Copula Avoidance)

**Words to watch:** serves as/stands as/marks/represents [a], boasts/features/offers [a]

**Problem:** LLMs substitute elaborate constructions for simple copulas.

**Before:**
> Gallery 825 serves as LAAA's exhibition space for contemporary art. The gallery features four separate spaces and boasts over 3,000 square feet.

**After:**
> Gallery 825 is LAAA's exhibition space for contemporary art. The gallery has four rooms totaling 3,000 square feet.

---

### 9. Negative Parallelisms

**Problem:** Constructions like "Not only...but..." or "It's not just about..., it's..." are overused.

**Before:**
> It's not just about the beat riding under the vocals; it's part of the aggression and atmosphere. It's not merely a song, it's a statement.

**After:**
> The heavy beat adds to the aggressive tone.

---

### 10. Rule of Three Overuse

**Problem:** LLMs force ideas into groups of three to appear comprehensive.

**Before:**
> The event features keynote sessions, panel discussions, and networking opportunities. Attendees can expect innovation, inspiration, and industry insights.

**After:**
> The event includes talks and panels. There's also time for informal networking between sessions.

---

### 11. Elegant Variation (Synonym Cycling)

**Problem:** AI has repetition-penalty code causing excessive synonym substitution.

**Before:**
> The protagonist faces many challenges. The main character must overcome obstacles. The central figure eventually triumphs. The hero returns home.

**After:**
> The protagonist faces many challenges but eventually triumphs and returns home.

---

### 12. False Ranges

**Problem:** LLMs use "from X to Y" constructions where X and Y aren't on a meaningful scale.

**Before:**
> Our journey through the universe has taken us from the singularity of the Big Bang to the grand cosmic web, from the birth and death of stars to the enigmatic dance of dark matter.

**After:**
> The book covers the Big Bang, star formation, and current theories about dark matter.

---

## STYLE PATTERNS

### 13. Em Dash Overuse

**Problem:** LLMs use em dashes (—) more than humans, mimicking "punchy" sales writing.

**Before:**
> The term is primarily promoted by Dutch institutions—not by the people themselves. You don't say "Netherlands, Europe" as an address—yet this mislabeling continues—even in official documents.

**After:**
> The term is primarily promoted by Dutch institutions, not by the people themselves. You don't say "Netherlands, Europe" as an address, yet this mislabeling continues in official documents.

---

### 14. Overuse of Boldface

**Problem:** AI chatbots emphasize phrases in boldface mechanically.

**Before:**
> It blends **OKRs (Objectives and Key Results)**, **KPIs (Key Performance Indicators)**, and visual strategy tools such as the **Business Model Canvas (BMC)** and **Balanced Scorecard (BSC)**.

**After:**
> It blends OKRs, KPIs, and visual strategy tools like the Business Model Canvas and Balanced Scorecard.

---

### 15. Inline-Header Vertical Lists

**Problem:** AI outputs lists where items start with bolded headers followed by colons.

**Before:**
> - **User Experience:** The user experience has been significantly improved with a new interface.
> - **Performance:** Performance has been enhanced through optimized algorithms.
> - **Security:** Security has been strengthened with end-to-end encryption.

**After:**
> The update improves the interface, speeds up load times through optimized algorithms, and adds end-to-end encryption.

---

### 16. Title Case in Headings

**Problem:** AI chatbots capitalize all main words in headings.

**Before:**
> ## Strategic Negotiations And Global Partnerships

**After:**
> ## Strategic negotiations and global partnerships

---

### 17. Emojis

**Problem:** AI chatbots often decorate headings or bullet points with emojis.

**Before:**
> 🚀 **Launch Phase:** The product launches in Q3
> 💡 **Key Insight:** Users prefer simplicity
> ✅ **Next Steps:** Schedule follow-up meeting

**After:**
> The product launches in Q3. User research showed a preference for simplicity. Next step: schedule a follow-up meeting.

---

### 18. Curly Quotation Marks

**Problem:** ChatGPT uses curly quotes (“...”) instead of straight quotes ("...").

**Before:**
> He said “the project is on track” but others disagreed.

**After:**
> He said "the project is on track" but others disagreed.

---

## COMMUNICATION PATTERNS

### 19. Collaborative Communication Artifacts

**Words to watch:** I hope this helps, Of course!, Certainly!, You're absolutely right!, Would you like..., let me know, here is a...

**Problem:** Text meant as chatbot correspondence gets pasted as content.

**Before:**
> Here is an overview of the French Revolution. I hope this helps! Let me know if you'd like me to expand on any section.

**After:**
> The French Revolution began in 1789 when financial crisis and food shortages led to widespread unrest.

---

### 20. Knowledge-Cutoff Disclaimers

**Words to watch:** as of [date], Up to my last training update, While specific details are limited/scarce..., based on available information...

**Problem:** AI disclaimers about incomplete information get left in text.

**Before:**
> While specific details about the company's founding are not extensively documented in readily available sources, it appears to have been established sometime in the 1990s.

**After:**
> The company was founded in 1994, according to its registration documents.

---

### 21. Sycophantic/Servile Tone

**Problem:** Overly positive, people-pleasing language.

**Before:**
> Great question! You're absolutely right that this is a complex topic. That's an excellent point about the economic factors.

**After:**
> The economic factors you mentioned are relevant here.

---

## FILLER AND HEDGING

### 22. Filler Phrases

**Before → After:**
- "In order to achieve this goal" → "To achieve this"
- "Due to the fact that it was raining" → "Because it was raining"
- "At this point in time" → "Now"
- "In the event that you need help" → "If you need help"
- "The system has the ability to process" → "The system can process"
- "It is important to note that the data shows" → "The data shows"

---

### 23. Excessive Hedging

**Problem:** Over-qualifying statements.

**Before:**
> It could potentially possibly be argued that the policy might have some effect on outcomes.

**After:**
> The policy may affect outcomes.

---

### 24. Generic Positive Conclusions

**Problem:** Vague upbeat endings.

**Before:**
> The future looks bright for the company. Exciting times lie ahead as they continue their journey toward excellence. This represents a major step in the right direction.

**After:**
> The company plans to open two more locations next year.

---

---

## SENTENCE & STRUCTURE PATTERNS

These patterns operate above the word level. They are structural AI tells — not vocabulary problems but construction problems. They appear in blogs, emails, social posts, and landing pages.

---

### 25. Fragment Sentences

**Problem:** Noun phrases, participial phrases, and relative clauses used as standalone sentences. They have no main verb doing real work. They feel punchy but communicate nothing on their own.

**Types to catch:**
- Noun phrase: "A strategy built on trust." (no verb)
- Participial phrase: "Running on empty, still answering every call." (no subject)
- Relative clause: "The manager who never says no." (no predicate)
- List as sentence: "Anxiety, guilt, helplessness, anger." (no verb)
- Setup sentence: "It doesn't look like collapse." followed by "It looks like..." (the first sentence exists only to introduce the second)

**Before:**
> Burnout doesn't look like collapse.
> It looks like snapping at someone. Dreaming about when it ends. Forgetting your own appointments. The smile you put on before you walk in.

**After:**
> Burnout looks like snapping at someone and spending the rest of the day hating yourself for it. It looks like dreaming about when it ends, then hating yourself for the thought. It means forgetting your own appointments and putting on a smile before you walk into the room that you drop the moment you're alone.

---

**Before:**
> No application, no training, no moment where you formally agreed.

**After:**
> ...with no application process, no training, and no formal moment where you agreed to any of it.

---

**Before:**
> The colleague who never complains. Running on empty.

**After:**
> The colleague who never complains is running on empty.

---

**Applies to:** blog sections, email body, social captions, landing page copy

**Note — intentional vs. structural fragments:** Pattern 25 targets structural fragments: noun phrases or participials that AI generates as standalone sentences in place of complete thoughts. A deliberately chosen stylistic fragment — used once, for rhythmic effect, where the complete meaning is conveyed — is different. The test: a structural fragment exists because the sentence was never finished. An intentional stylistic fragment exists because the writer stopped exactly there on purpose. When in doubt, write the complete sentence.

---

### 26. Throat-Clearing Sentences

**Problem:** A sentence that announces what is coming instead of saying it. It adds a full sentence of travel time before arriving at the point. Cut it and open directly with the substance.

**Patterns to catch:**
> "X is different in specific, concrete ways."
> "There are several important things to consider."
> "Let's take a closer look at this."
> "It's worth noting that..."
> "This is where things get interesting."
> "Now let's turn to..."
> Any sentence that could be deleted without losing information.

**Before:**
> Nigeria is different in specific, concrete ways.
>
> 16.4% of Nigerian households face catastrophic health expenditure...

**After:**
> [Delete the throat-clearer entirely]
>
> 16.4% of Nigerian households face catastrophic health expenditure...

---

**Before (email):**
> I wanted to reach out today to share some thoughts on our upcoming product launch.

**After:**
> We're launching on March 14th, and three things need to happen before then.

---

**Before (social):**
> Something important happened this week that I think you should know about.

**After:**
> We crossed 10,000 deliveries this week.

---

**Applies to:** section openers, email openers, social post hooks, paragraph transitions

---

### 27. Stutter Sentences

**Problem:** Two consecutive short sentences making the same point. The second adds no new information — it just repeats the first in different words. Merge them or cut one.

**Before:**
> Relief arrives first, often. Guilt about the relief follows closely.

**After:**
> Relief usually arrives first, and guilt about the relief follows close behind.

---

**Before:**
> Nobody sees this. Nobody protects it.

**After:**
> Nobody sees this, and nobody protects it.

---

**Before (email):**
> We missed the deadline. The project was late.

**After:**
> We missed the deadline by four days.

---

**Before (social):**
> This matters. It's important.

**After:**
> [Pick one and make it specific. Delete the other.]

---

### 28. Indirect Constructions and Negative Framing Before Positive

**Problem:** AI routinely hedges before committing — stating what something is NOT before stating what it IS. This creates two sentences to carry one idea. Cut the negative frame and state the positive directly. If contrast is genuinely needed, keep it in one clause, not split across two sentences.

**Patterns to kill:**

"Not because X, but because Y" — cut the hedge, keep the commitment.
> ❌ "Not out of carelessness. Out of there being nothing left."
> ✅ "Because there is nothing left."

"Not X. X." — the negation followed by the affirmation.
> ❌ "This is not a personal failing. It is a documented pattern with a cause."
> ✅ "It is a documented pattern with a specific cause: [state the cause]."

Softening a fact before landing it:
> ❌ "Not because they volunteered. Because someone had to."
> ✅ "Because someone had to, and they were first in line."

Negative parallelism across two sentences:
> ❌ "It is not a sign that something is wrong with how you love. It's a sign of how much you do."
> ✅ "It's evidence of how much you love."

**Before (email):**
> This isn't about blame. It's about accountability.

**After:**
> This is about accountability.

---

**Before (landing page):**
> It's not just a pharmacy. It's a care system.

**After:**
> It's a care system that handles refills, deliveries, and medication reviews so you don't have to.

---

### 29. Opener That Announces Instead of Starts

**Problem:** The first sentence of any piece, section, email, or social post describes what is coming instead of beginning. It warms up instead of diving in. Delete the announcement and open with the thing itself.

**Before:**
> In this post, we're going to look at why caregiver burnout is different in Nigeria, and what you can do about it.

**After:**
> 85% of informal caregivers in Nigeria report burnout. Most of the advice written about this was written for someone else.

---

**Before:**
> It doesn't look like collapse.
> It looks like snapping at the patient...

**After:**
> Burnout looks like snapping at the patient...

---

**Before (email):**
> I wanted to share some thoughts on what we've been seeing with our customers lately.

**After:**
> Three customers cancelled this month for the same reason.

---

**Before (social):**
> I've been thinking a lot about this, and I wanted to share it with you.

**After:**
> [The thought. Not the announcement of the thought.]

---

## ARGUMENT & EVIDENCE PATTERNS

---

### 30. Label Without Content

**Problem:** A sentence names a category, phenomenon, or type without telling the reader what is actually inside it. Naming is not explaining. The label arrives but the content doesn't.

**Rule:** When you name something, the same sentence or the next must tell the reader what is in it.

**Before:**
> It is a documented pattern with a cause.

**After:**
> It is a documented pattern with a specific cause — one person absorbs what an entire support system should carry, with no policy backup, no paid leave, and no formal acknowledgment that they exist.

---

**Before:**
> Anticipatory grief is documented extensively in caregiver research. Anxiety, guilt, helplessness, anger. These are its fingerprints.

**After:**
> Anticipatory grief is documented extensively in caregiver research — anxiety, guilt, helplessness, and anger are its most consistent markers.

---

**Before (landing page):**
> Famasi is a better pharmacy experience.

**After:**
> Famasi delivers your medications to your door, synchronises all your refills to one date, and keeps a care plan your whole family can see.

---

**Before (email):**
> We have a process for this.

**After:**
> We have a three-step process: the request goes to [X], [X] reviews within 48 hours, and you receive confirmation by email.

---

### 31. Stat Without Explanation

**Problem:** A statistic lands but the sentence ends before telling the reader what it means, why it happens, or what to do with it. A number is not a conclusion. It is evidence. It needs an explanation attached.

**Rule:** Every statistic must be followed immediately by the explanation of why that number exists or what it means for the reader.

**Before:**
> 85% of informal caregivers in Nigeria report some level of burnout. This is a documented pattern with a cause.

**After:**
> 85% of informal caregivers in Nigeria report some level of burnout — a predictable outcome when one person absorbs what an entire support system should carry, with no policy backup, no paid leave, and no formal acknowledgment that they exist.

---

**Before (email):**
> Our churn rate is 12%. We need to address this urgently.

**After:**
> Our churn rate is 12%, three points above target, driven primarily by customers who never completed onboarding in their first two weeks.

---

**Before (social):**
> 67% of caregivers in Nigeria are women.

**After:**
> 67% of caregivers carrying the highest burden in Nigeria are women who were assigned the role by a family that decided they were most available, without being asked.

---

### 32. Stat Dishonesty — Know What Your Number Actually Proves

**Problem:** A statistic from a limited study gets presented as if it were national data, universal truth, or settled science. Scope matters. Using a hospital study as a national figure is dishonest, and readers notice.

**Rule:** Know exactly what a stat proves before using it. Attribute it to its actual scope. A narrow, honestly attributed figure is stronger than a broad, shaky one.

**Before:**
> In Nigerian hospitals, 92% of informal caregivers are women. (implies national data — it came from one hospital study)

**After:**
> In one Nigerian hospital study, 92% of the family members showing up daily to care for admitted patients were women.

---

**Rule:** Use plainspoken language around stats, not jargon.
> ❌ "92% of informal caregivers" (reader must know what "informal" means)
> ✅ "92% of the family members showing up every day"

---

### 33. Overclaimed Before/After

**Problem:** The "after" in a story, case study, or testimonial suggests the subject recovered or reversed what they lost. That is almost never true, and readers know it. False resolution undermines emotional credibility. The after must be honest — not restorative, but forward-facing.

**Rule:** The after is not a reversal. It is an opening.

**Before:**
> Since finding support, she gained back the space to be herself.

**After:**
> Since finding support, she gets to grow in directions that had been closed off for years.

The distinction: "gained back" looks backward at what was taken and implies it was returned. "Gets to grow" looks forward at what is now possible. Only the second is true.

**Rule:** Don't reward suffering with a tidy bow. Acknowledge the loss, then move forward without suggesting the loss was erased.

**Before (email):**
> Since switching to Famasi, everything about managing his medications became easy.

**After:**
> Since switching to Famasi, the monthly pharmacy run stopped being her problem.

---

## FORMATTING & CONSTRUCTION PATTERNS

---

### 34. Bold Header + Colon Paragraph Openers

**Problem:** A bold word or phrase followed by a colon, followed by explanation is the single most recognisable AI formatting pattern in structured content. It signals a generated list. It appears in blog sections, emails, and landing pages.

**Before:**
> **Build the care team — with names, not requests.** Requests evaporate. Someone is on medications...
>
> **Build the information document before you need it.** One shared record: medication names, dosages...

**After:**
> Name the roles instead of just asking for help. A request can be declined or forgotten, but ownership can't. When someone's name is on medications and someone else's is on appointments, the weight distributes.
>
> Build the information document before you need it — one shared record covering medication names, dosages, prescribing doctors, refill dates, and emergency contacts, kept accessible to everyone and updated after every significant appointment.

---

**Before (email):**
> **Value:** Our platform saves you 3 hours per week.
> **Ease:** Set up in under 10 minutes.
> **Support:** We're available 24/7.

**After:**
> Our platform saves you 3 hours a week, takes under 10 minutes to set up, and our team is available 24/7 if anything goes wrong.

---

### 35. Paragraph Weight Imbalance

**Problem:** Short paragraphs and long paragraphs are used interchangeably regardless of function. They each have jobs. Reversing them flattens the writing.

**Rule:**
- Short paragraphs carry emotional weight and emphasis. Use them for the line that must land.
- Long paragraphs carry context, explanation, and texture. Use them where density is earned.
- A one-sentence paragraph is a tool, not a habit. Use it when you need weight, not rhythm.

**Before (wrong weight distribution):**
> The stat lines are short. The systemic explanation is short. Elizabeth's voice is medium. The close is short. The one place length is earned is inside Elizabeth's quote — because that's where the texture lives.
>
> *(All short. Nothing lands harder than anything else.)*

**After:**
> Let the systemic explanation breathe: it needs length to earn the reader's trust. Let Elizabeth's voice be specific and textured: that's where the emotional weight lives. Let the close be short, because by then the reader should already feel it.

---

### 36. Thesis-Antithesis-Synthesis for Openers and Key Arguments

**Problem:** One-sided arguments trigger resistance. When AI writes an opener, it states the position directly and then supports it. Readers who hold the common view mentally dismiss it. TAS prevents this by acknowledging the accepted view, exposing where it breaks down, and arriving at the stronger truth.

**Structure:**
- **Thesis:** The accepted, comfortable version of the idea
- **Antithesis:** Where it fails, cracks, or doesn't hold
- **Synthesis:** The stronger truth that accounts for both

**Before (blog opener — one-sided):**
> Caregivers in Nigeria face enormous challenges and often burn out. This post will help you understand what you're going through and what to do about it.

**After — TAS:**
> Luisa is the strong one — the sister who carries donkeys, moves bridges, and absorbs everyone's problems without complaint. The family knows who to call when something needs handling, and she answers every time. *(Thesis)*
>
> Then, quietly, she starts losing her powers. She keeps showing up, keeps performing, keeps acting like nothing has changed, even as she runs completely empty and still answers every call. *(Antithesis)*
>
> If any of that landed somewhere in your chest, this piece is written for you. *(Synthesis)*

---

**Before (email — one-sided):**
> Self-care is important for caregivers. Here are five tips to avoid burnout.

**After — TAS:**
> Most advice on caregiver burnout tells you to take breaks, set boundaries, and prioritise yourself. *(Thesis)*
>
> That advice was written for someone with paid leave, professional respite care, and a health system that sees them. Most Nigerian caregivers don't have any of that. *(Antithesis)*
>
> Here's what actually helps. *(Synthesis)*

---

**Applies to:** blog openers, email hooks, social posts challenging a common assumption, landing page headlines, any argument that counters received wisdom

---

## NARRATIVE & VOICE PATTERNS

---

### 37. Named Theme vs. Embodied Theme

**Problem:** AI states the theme explicitly instead of letting the narrative demonstrate it. If you find yourself writing "this is what X means when you strip it down" — delete that sentence and trust the story to do the work. A reader who feels the theme is more persuaded than a reader who is told it.

**Rule:** Never write the name of the theme. Write what the theme looks like in a specific moment.

**Before:**
> That is what Give to Gain actually means when you strip it down — when you give without keeping score, it comes back to you.

**After:**
> [Delete entirely. The story of Elizabeth giving up career opportunities to care for her mother, and then her community rallying around her when she needed help, already demonstrates reciprocity. Name it and you diminish it.]

---

**Before (email):**
> This email is really about resilience — about finding strength in the hardest moments.

**After:**
> [Delete. Show a specific moment of a specific person doing a specific hard thing. Let the reader name what they're feeling.]

---

**Before (landing page):**
> Famasi is built on the belief that caregivers deserve support too.

**After:**
> Famasi delivers medications to the door, synchronises refills, and maintains a care plan the whole family can see — so the person managing everything doesn't have to manage the pharmacy too.

---

### 38. False Resolution

**Problem:** The ending suggests recovery, closure, or return to the original state. It implies the hard thing is over. It almost never is, and readers know it. False resolution destroys credibility at the close — which is the highest-stakes moment in any piece of writing.

**Rule:** Resolution must be honest. Forward-facing, not restorative. Acknowledge the loss or difficulty; then point toward what is now possible, not what has been regained.

**Before:**
> She gained back the space to be herself.

**After:**
> She gets to grow in directions that had been closed off for years.

---

**Before (email close):**
> Thanks to her new system, everything is easier now.

**After:**
> One thing is easier now. That one thing gives her back two hours a week she used to spend on hold with the pharmacy.

---

**Before (blog close):**
> You are allowed to still be a person inside this role. And one day, you will get back to being fully yourself.

**After:**
> You are allowed to still be a person inside this role.
> *(Stop there. Don't promise a future you can't guarantee.)*

---

### 39. Interview Voice vs. Authorial Voice

**Problem:** When a real person's voice appears in copy — a quote, a testimonial, a case study — it is written in the author's register, not the person's. Real people describe their situation from the inside. They don't explain themselves clinically, use the language of the argument, or present their experience as a tidy illustration of a point.

**Authorial voice** does the systemic, structural work — statistics, context, argument.
**Subject voice** does the emotional, textural work — specific details, incomplete logic, their own language.

**Do not mix them.**

**Before (testimonial written in authorial register):**
> "Since finding Famasi, managing my father's medications has become significantly more manageable, allowing me to focus on other aspects of caregiving."

**After (written in a real person's register):**
> "I stopped counting how many times I called the pharmacy in a week. Now I don't have to."

---

**Rule:** Real people describe outcomes, not brand names.
> ❌ "Since I found Famasi, everything changed."
> ✅ "Since I stopped doing the hospital runs myself, I have Wednesday afternoons back."

**Rule:** Real people use incomplete logic.
> ❌ "The decision was made for me by cultural expectation."
> ✅ "It wasn't even a conversation. I just started going."

---

### 40. Benefit-Led, Not Brand-Led Product Integration

**Problem:** The product or brand enters the copy through its name rather than through what it changes for the person. Real customers don't describe their lives in terms of products. They describe them in terms of what shifted.

**Rule:** Let the benefit carry the implicit argument. The reader connects the product to the outcome without being told to.

**Before:**
> Since I started using Famasi, my life got easier.

**After:**
> Since the refills started arriving at the door, I stopped losing track of which prescription ran out.

---

**Before (landing page):**
> Famasi is Nigeria's leading medication management platform.

**After:**
> Your medications arrive before they run out. Your refills sync to one date. Your family can see the care plan without calling you first.

---

**Before (email CTA):**
> Sign up for Famasi today and take control of your caregiving.

**After:**
> Set up home delivery once, and the monthly pharmacy run stops being your problem.

---

### 41. Direct Witness, Not Cheerleader

**Problem:** Generic celebration of an idea of a person rather than documentation of a specific person's specific experience. Celebration without specificity is noise. The reader should think "how did they know?" not "that's nice."

**Rule:** Write toward recognition, not inspiration. Recognition is for the subject. Inspiration is for the reader. Recognition is harder to write and more powerful when you get it right.

**Before:**
> This Women's Day, we celebrate the incredible strength and resilience of women everywhere who give so much of themselves to care for the people they love.

**After:**
> She confirmed the medication was taken at 6am, answered three calls from the doctor's office before 9, transferred money for the hospital bill during her lunch break, and opened her laptop for a meeting at 3pm. Nobody asked how she was doing. This is for her.

---

**Rule:** The texture is what makes it real. Not "she sacrificed" but the 6am bus, the three medication schedules in her head, the doctor's appointment she rescheduled four times.

---

### 42. Functional, Not Performative Close

**Problem:** The closing of an email, blog, or social post stacks multiple jobs — theme explanation, celebration line, CTA, PS — each element competing with the others. AI closes by wrapping everything up. Human writing closes by landing one thing cleanly.

**Rule:** The close does one job. Every element that competes with that job should be removed or moved.

**Correct order for a closing sequence:**
1. One honest, earned line — the emotional or argumentative conclusion
2. One transitional line that moves toward the CTA without forcing it
3. CTA that feels like a next step, not a push
4. PS that bridges to the next piece of content — one sentence only

**Before:**
> That is what caregiving really means. We celebrate every caregiver this Women's Day. To learn more about how Famasi supports caregivers like you, visit our website. And don't forget to share this with someone who needs to hear it. PS: Tomorrow we'll share five tips for managing medication remotely.

**After:**
> You are allowed to still be a person inside this role.
>
> For caregivers managing medications in Nigeria — in the same city or a different country — Famasi exists to take the medication burden off your plate so your energy goes to the parts of caring that only you can do.
>
> → [See how Famasi works]

---

**Rule:** "We see you" only earns its place if the preceding copy has actually seen the person. Don't write it unless the content has done the work.

---

## HEADLINE PATTERNS

---

### 43. Writer-Serving Headlines

**Problem:** A headline is poetic, clever, or internally meaningful to the author, but opaque to the reader. The reader must enter the section before understanding what it is about. Writer-serving headlines fail at the job headlines exist to do — communicate to a stranger in one line.

**Checklist — every headline must pass all five:**
- Does the reader know what this section is about before entering it?
- Does it speak to the reader's situation, not the writer's concept?
- Is it specific enough that it would mean something out of context?
- Could it stand alone as a complete thought?
- Would a stranger scrolling past understand why it is relevant to them?

**Before → After:**

| Writer-serving | Reader-serving |
|---|---|
| The weight before the name | When did someone last check on you? |
| The grief that has no occasion | You can grieve someone who is still in the room |
| The family myth | Why you're alone in a room full of family |
| What burnout actually looks like | The signs of burnout that don't look like burnout |
| The diaspora caregiver | Managing a parent's illness from 5,000 miles away |
| After | What nobody tells you about when it ends |
| You are also someone's someone | The second patient |

---

**Weak headline patterns to avoid:**
- Single vague word: "After", "Context", "Overview", "Background"
- Poetic phrase requiring context: "The weight before the name"
- Neutral topic label: "The diaspora caregiver", "Introduction"
- Yes/no question: "Are you a caregiver?" (reader answers and stops reading)

**Strong headline patterns:**
- Counterintuitive claim: "You can grieve someone who is still in the room"
- Direct question naming the reader's exact experience: "When did someone last check on you?"
- Specific reader situation: "Managing a parent's illness from 5,000 miles away"
- Named paradox: "Why you're alone in a room full of family"
- Knowledge gap: "What nobody tells you about when it ends"

---

### 44. Email Subject Lines as Headlines

**Problem:** Email subject lines are treated as labels rather than hooks. They describe the email's contents instead of giving the reader a reason to open it.

**Same rules as section headlines apply, plus:**

**Rule:** The subject line should create a gap the reader wants to close — a question they want answered, a statement that surprises them, or a situation they recognise.

**Before:**
> Women's Day Newsletter — Famasi Celebrates Caregivers

**After:**
> She confirmed the medication. Then opened her laptop. Nobody asked how she was doing.

---

**Before:**
> Monthly Update — March 2026

**After:**
> The one thing that changed everything for caregivers this month

---

**Before:**
> Learn more about our new delivery service

**After:**
> The monthly pharmacy run just became optional

---

**Applies to:** email subject lines, social post first lines, push notification copy, SMS hooks

---

## ADDITIONAL PATTERNS

The following patterns supplement the sections above. Each is numbered to continue the sequence (45–51) and named as a standalone rule — no assumption about existing knowledge required.

---

### 45. Participial Appositive (Em Dash + Loose Modifier)

**Problem:** A participial phrase is appended to a noun via em dash in place of a relative clause. The em dash + participial makes the grammatical relationship implicit. A relative clause (who/which/that + verb) states it directly. AI uses this construction as a shortcut that sounds punchy but reduces precision.

**Patterns to catch:**
- `noun — past participial`: `women — assigned the role by`, `a system — designed around compliance`
- `noun — present participial`: `a team — operating without oversight`, `a model — relying on assumptions`

**Rule:** When a participial phrase carries the main relationship between a noun and its modifier, use a relative clause. Reserve em dashes for genuine parenthetical asides — information that could be removed without losing the main point.

**Before:**
> 67% of caregivers are women — assigned the role by a family that decided they were most available.

**After:**
> 67% of caregivers are women who were assigned the role by a family that decided they were most available.

---

**Before (email):**
> She manages a team — spread across four time zones with no centralised handover process.

**After:**
> She manages a team that is spread across four time zones with no centralised handover process.

---

**Before (landing page):**
> Famasi is a pharmacy — built around the caregiver, not the patient alone.

**After:**
> Famasi is a pharmacy that puts the caregiver at the centre of its service.

---

**Applies to:** blog body, case studies, product descriptions, landing page copy

---

### 46. Nominalization (Verb-to-Noun Conversion)

**Problem:** An active verb is converted into a noun phrase, which then requires a weaker supporting verb. "Make a decision" instead of "decide." "Conduct an investigation" instead of "investigate." Nominalizations lengthen sentences, obscure who is doing what, and make writing feel bureaucratic.

**High-frequency nominalizations:**
- "provide assistance" → "help"
- "make a decision" → "decide"
- "conduct an investigation" → "investigate"
- "achieve an improvement" → "improve"
- "offer a solution" → "solve"
- "come to the realization" → "realize"
- "have an impact on" → "affect"
- "give consideration to" → "consider"
- "make use of" → "use"
- "take action on" → "act on"
- "provide support for" → "support"
- "reach an agreement" → "agree"
- "perform an analysis" → "analyze"
- "undertake a review" → "review"

**Rule:** Find the real verb buried in the noun phrase and use it directly.

**Before:**
> The team made a decision to conduct an investigation into the caregiver's situation and provide assistance where possible.

**After:**
> The team decided to investigate the caregiver's situation and help where they could.

---

**Before (email):**
> I am writing to offer a solution to the challenges you are experiencing and to give consideration to your request.

**After:**
> I'm writing to address the problem you raised and respond to your request.

---

**Before (landing page):**
> Famasi provides support for caregivers who are experiencing difficulty in the management of medication logistics.

**After:**
> Famasi supports caregivers who struggle to manage their medications.

---

**Applies to:** all copy — nominalizations are universal but most damaging in emails and landing pages where directness matters most

---

### 47. Passive Voice Avoiding Agency

**Problem:** AI uses passive construction to avoid naming who did what. "Mistakes were made" names no one. "The decision was made to..." hides who decided. In marketing copy, removing agency removes credibility — the reader cannot evaluate a claim with no named actor.

**When passive is acceptable:** agent unknown or genuinely irrelevant.
> "The clinic was established in 1992." (who built it is irrelevant; the date is the point)

**When passive is evasive:** known agent deliberately omitted — fix it.
> ❌ "Mistakes were made in handling your account."
> ✅ "We made a mistake in handling your account."

**Rule:** Name who is doing what. Use passive only when the receiver of the action is genuinely more important than the actor, or when the actor is unknown.

**Before:**
> The caregiving role is often assigned to women without their being consulted.

**After:**
> Families assign the caregiving role to women without consulting them.

---

**Before (email):**
> Your feedback has been received and will be reviewed by the appropriate team.

**After:**
> We received your feedback. [Name] will review it by Thursday.

---

**Before (landing page):**
> Medications are delivered, refill dates are synchronised, and care plans are documented.

**After:**
> We deliver medications, synchronise refill dates, and document care plans your whole family can see.

---

**Applies to:** emails, case studies, testimonials, landing pages — anywhere agency and accountability matter

---

### 48. Adverb Intensifier Stacking

**Problem:** An intensifying adverb is paired with an adjective that already carries the meaning. The adverb adds no information — it signals the writer felt the adjective was insufficient and tried to compensate with volume. Stronger word choice or a specific example is always better than stacking.

**High-frequency offenders:**
- "extremely important" → state the specific consequence
- "highly significant" → state what the significance is
- "particularly crucial" → state what happens without it
- "truly remarkable" → say what is remarkable specifically
- "incredibly powerful" → say what the power is
- "absolutely essential" → "essential," or state what happens without it
- "deeply concerned" → state what the concern is
- "very unique" → "unique" (unique is already absolute and cannot be modified)
- "completely free" → "free"
- "totally unnecessary" → "unnecessary"

**Rule:** Drop the adverb. If the adjective alone feels insufficient, replace both with a specific claim, consequence, or example.

**Before:**
> This is an extremely important issue that requires highly significant attention from policymakers.

**After:**
> Without policy intervention, caregivers absorb the health system's entire informal labour supply at no cost to the state.

---

**Before (email):**
> We are incredibly excited to share this truly remarkable update with you.

**After:**
> We've been building this for six months. Here's what it does.

---

**Before (social):**
> This is absolutely essential reading for anyone deeply committed to caregiver welfare.

**After:**
> If you run a caregiver support program, this changes how you should think about what your members actually need.

---

**Applies to:** all copy — adverb stacking is universal but most visible in marketing copy where it substitutes for specificity

---

### 49. Unearned Intimacy

**Problem:** The writer assumes the reader's thoughts, feelings, or experiences without evidence. "You may be wondering..." presumes what the reader is wondering. "We've all been there" assumes a shared experience. When the assumption misses, the sentence meant to connect instead distances.

**Rule:** Don't name the reader's inner state. Show the situation that produces it and let the reader recognise themselves.

**Patterns to cut:**
> "You may be wondering..."
> "I know what you're thinking..."
> "We've all been there..."
> "If you're like most [audience]..."
> "You've probably experienced..."
> "I know you're busy, so..."
> Any sentence that names the reader's feeling instead of the situation that causes it.

**Before:**
> You may be wondering how to balance caring for a loved one while maintaining your own wellbeing.

**After:**
> When did you last sit down and eat a proper meal?

---

**Before:**
> We've all been in that situation where everything feels like too much. You're not alone.

**After:**
> 85% of informal caregivers in Nigeria report some level of burnout. Most of the advice written about it was written for someone else.

---

**Before (email):**
> I know you're busy, so I'll keep this short.

**After:**
> [Keep it short. Don't announce that you're keeping it short.]

---

**Before (social):**
> If you're like most caregivers, you've probably felt invisible at some point.

**After:**
> The question "how is she doing?" almost always means the patient.

---

**Applies to:** blog openers, email intros, social hooks, testimonial copy — anywhere the writer attempts to connect by assuming rather than showing

---

### 50. Journey / Navigate / Landscape Metaphors

**Problem:** Three metaphors — journey, navigate, and landscape — appear together in AI writing at a rate that makes them immediately recognisable. They substitute movement-language for precision about what is actually happening. Nobody is navigating a landscape or charting a path. They are managing costs, coordinating appointments, or waiting on hold.

**Words to eliminate:**
- "journey" (figurative): "their healing journey", "the caregiving journey", "a journey of discovery"
- "navigate" (figurative): "navigating the complexities of", "navigate the system", "navigating challenges"
- "landscape" (abstract): "the healthcare landscape", "the evolving landscape of", "the competitive landscape"
- "path forward": "charting a path forward", "finding the path forward"
- "roadmap": "a roadmap for success", "a roadmap to recovery"
- "milestone" (figurative): "an important milestone in their journey"
- "ecosystem" (abstract): "the caregiving ecosystem", "the healthcare ecosystem"

**Rule:** Say what is actually happening. Replace movement metaphors with the specific action, cost, decision, or system the writer was reaching for.

**Before:**
> Caregivers often navigate the complex landscape of healthcare, embarking on a journey that tests their resilience at every milestone.

**After:**
> Caregivers coordinate appointments, fund treatments, and manage medication schedules, often while working full-time.

---

**Before (email):**
> We're here to help you navigate your caregiving journey and find the path forward.

**After:**
> We handle the pharmacy logistics so you can focus on the parts of caring that only you can do.

---

**Before (landing page):**
> Famasi is your roadmap through the complex healthcare landscape.

**After:**
> Famasi coordinates your refills, delivers to your door, and keeps a medication record your whole family can see.

---

**Applies to:** all copy — these metaphors appear most in mission statements, about pages, and opening paragraphs where writers reach for significance language

---

### 51. Over-Explained Transition

**Problem:** A transition sentence describes that a transition is happening instead of making one. "Having established X, we can now turn to Y" uses a full sentence to do what a paragraph break does in zero words. The reader already knows a transition is coming — they can see the new paragraph.

**Patterns to cut:**
> "Having established X, we can now turn to Y."
> "With that context in mind, let's explore..."
> "Now that we understand X, it's time to look at Y."
> "Building on this, we can consider..."
> "This brings us to our next point."
> "Before we continue, it's worth recapping..."
> Any sentence that describes what the next paragraph will do instead of doing it.

**Rule:** Cut the explanation. Open the next section with its first real sentence. If the connection between sections is not clear without an explanation, the sections are in the wrong order — fix the structure, not with an announcement.

**Before:**
> Now that we've seen the scale of caregiver burnout in Nigeria, it's time to look at what actually helps.
>
> [Systems section begins]

**After:**
> [Delete. Open the systems section with its first real sentence.]

---

**Before (email):**
> With that background in mind, I wanted to share the update you've been waiting for.

**After:**
> [The update, directly.]

---

**Before (landing page):**
> Having understood the problem, let's take a look at how Famasi solves it.

**After:**
> [Show how Famasi solves it. The reader understood the problem — they read it.]

---

**Applies to:** blog section transitions, email body, report sections, landing page flow — anywhere the writer signals a shift instead of making one

---

## Process

1. Read the input text carefully
2. Identify all instances of the patterns above
3. Rewrite each problematic section
4. Ensure the revised text:
   - Has no fragment sentences — every sentence has a subject and a verb doing real work (P25)
   - Has no throat-clearing — every opener starts with the substance, not the announcement of it (P26)
   - Has no stutter sentences — consecutive short sentences say different things (P27)
   - Has no negative parallelisms — states what things ARE, not what they are not (P28)
   - Has no opener that announces instead of starting (P29)
   - Labels nothing without explaining what is inside the label (P30)
   - Follows every statistic with an explanation of what it means or why it happened (P31)
   - Has headlines that communicate to a stranger before they enter the section (P43)
   - Has a close that does one job (P42)
   - Uses active verbs rather than nominalized noun phrases — "decide" not "make a decision" (P46)
   - Names who is doing what — no evasive passive voice (P47)
   - Uses no adverb intensifiers — specific claims or consequences replace vague emphasis (P48)
   - Shows the reader's situation rather than naming their assumed inner state (P49)
   - Uses no journey / navigate / landscape metaphors — states what is actually happening (P50)
   - Transitions by opening the next thing, not by announcing that a transition is happening (P51)
   - Uses relative clauses (who/which/that + verb) rather than em dash + participial for noun modification (P45)
   - Sounds natural when read aloud
   - Varies sentence structure naturally
   - Uses specific details over vague claims
   - Maintains appropriate tone for context
   - Uses simple constructions (is/are/has) where appropriate (P8)
5. Present a draft humanized version
6. Prompt: "What makes the below so obviously AI generated?"
7. Answer briefly with the remaining tells (if any)
8. Prompt: "Now make it not obviously AI generated."
9. Present the final version (revised after the audit)

## Output Format

Provide:
1. Draft rewrite
2. "What makes the below so obviously AI generated?" (brief bullets)
3. Final rewrite
4. A brief summary of changes made (optional, if helpful)

---

## Full Example

**Before (AI-sounding):**
> Great question! Here is an essay on this topic. I hope this helps!
>
> AI-assisted coding serves as an enduring testament to the transformative potential of large language models, marking a pivotal moment in the evolution of software development. In today's rapidly evolving technological landscape, these groundbreaking tools—nestled at the intersection of research and practice—are reshaping how engineers ideate, iterate, and deliver, underscoring their vital role in modern workflows.
>
> At its core, the value proposition is clear: streamlining processes, enhancing collaboration, and fostering alignment. It's not just about autocomplete; it's about unlocking creativity at scale, ensuring that organizations can remain agile while delivering seamless, intuitive, and powerful experiences to users. The tool serves as a catalyst. The assistant functions as a partner. The system stands as a foundation for innovation.
>
> Industry observers have noted that adoption has accelerated from hobbyist experiments to enterprise-wide rollouts, from solo developers to cross-functional teams. The technology has been featured in The New York Times, Wired, and The Verge. Additionally, the ability to generate documentation, tests, and refactors showcases how AI can contribute to better outcomes, highlighting the intricate interplay between automation and human judgment.
>
> - 💡 **Speed:** Code generation is significantly faster, reducing friction and empowering developers.
> - 🚀 **Quality:** Output quality has been enhanced through improved training, contributing to higher standards.
> - ✅ **Adoption:** Usage continues to grow, reflecting broader industry trends.
>
> While specific details are limited based on available information, it could potentially be argued that these tools might have some positive effect. Despite challenges typical of emerging technologies—including hallucinations, bias, and accountability—the ecosystem continues to thrive. In order to fully realize this potential, teams must align with best practices.
>
> In conclusion, the future looks bright. Exciting times lie ahead as we continue this journey toward excellence. Let me know if you’d like me to expand on any section!

**Draft rewrite:**
> AI coding assistants speed up some tasks. In a 2024 study by Google, developers using Codex completed simple functions 55% faster than a control group, but showed no improvement on debugging or architectural decisions.
>
> The tools are good at boilerplate: config files, test scaffolding, repetitive refactors. They are bad at knowing when they are wrong. I have mass-accepted suggestions that compiled, passed lint, and still did the wrong thing because I stopped paying attention.
>
> Mira, an engineer at a fintech startup I interviewed, said she uses Copilot "like autocomplete for boring code" but reviews every line before committing. Jake, a senior dev at a larger company, disabled it after it kept suggesting patterns from a deprecated internal library.
>
> The productivity claims are hard to verify. GitHub says Copilot users "accept 30% of suggestions," but acceptance is not correctness, and correctness is not value. The 2024 Uplevel study found no statistically significant difference in pull-request throughput between teams with and without AI assistants.
>
> None of this means the tools are useless. It means they are tools. They do not replace judgment, and they do not eliminate the need for tests. If you do not have tests, you cannot tell whether the suggestion is right.

**What makes the below so obviously AI generated?**
- The rhythm is still a bit too tidy (clean contrasts, evenly paced paragraphs).
- The named people and study citations can read like plausible-but-made-up placeholders unless they're real and sourced.
- The closer leans a touch slogan-y ("If you do not have tests...") rather than sounding like a person talking.

**Now make it not obviously AI generated.**
> AI coding assistants can make you faster at the boring parts. They won't help much with architecture.
>
> They're great at boilerplate: config files, test scaffolding, repetitive refactors. They're also great at sounding right while being wrong. I've accepted suggestions that compiled, passed lint, and still missed the point because I stopped paying attention.
>
> People I talk to tend to land in two camps. Some use it like autocomplete for chores and review every line. Others disable it after it keeps suggesting patterns they don't want. Both feel reasonable.
>
> The productivity metrics are slippery. GitHub can say Copilot users "accept 30% of suggestions," but acceptance isn't correctness, and correctness isn't value. If you don't have tests, you're basically guessing.

**Changes made:**
- Removed chatbot artifacts ("Great question!", "I hope this helps!", "Let me know if...")
- Removed significance inflation ("testament", "pivotal moment", "evolving landscape", "vital role")
- Removed promotional language ("groundbreaking", "nestled", "seamless, intuitive, and powerful")
- Removed vague attributions ("Industry observers")
- Removed superficial -ing phrases ("underscoring", "highlighting", "reflecting", "contributing to")
- Removed negative parallelism ("It's not just X; it's Y")
- Removed rule-of-three patterns and synonym cycling ("catalyst/partner/foundation")
- Removed false ranges ("from X to Y, from A to B")
- Removed em dashes, emojis, boldface headers, and curly quotes
- Removed copula avoidance ("serves as", "functions as", "stands as") in favor of "is"/"are"
- Removed formulaic challenges section ("Despite challenges... continues to thrive")
- Removed knowledge-cutoff hedging ("While specific details are limited...")
- Removed excessive hedging ("could potentially be argued that... might have some")
- Removed filler phrases ("In order to", "At its core")
- Removed generic positive conclusion ("the future looks bright", "exciting times lie ahead")
- Made the voice more personal and less "assembled" (varied rhythm, fewer placeholders)

---

## Reference

This skill is based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing), maintained by WikiProject AI Cleanup. The patterns documented there come from observations of thousands of instances of AI-generated text on Wikipedia.

Key insight from Wikipedia: "LLMs use statistical algorithms to guess what should come next. The result tends toward the most statistically likely result that applies to the widest variety of cases."
