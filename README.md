# Difficult Client Simulator

Claude plays an angry customer. You respond as the CS rep. 
You get scored and coached after every message.

## What it does

Three difficulty levels, four scenarios. Trainee gets you 
a customer who's upset but willing to be helped — good for 
getting comfortable. Pro is impatient and won't budge 
without specific timelines and real ownership, not "our 
team will look into it." Expert is someone on the edge of 
cancelling, testing you with questions like "why should I 
trust you now," who only calms down after a few genuinely 
strong responses.

The scenarios: a delivery that's three weeks late before a 
big event, a double charge nobody's fixed in two weeks, a 
feature that broke right before someone's client 
presentation, a cancellation that kept getting billed 
anyway. Same setups across all three levels — what changes 
is how the customer opens and how forgiving they are.

After each reply: a score out of 10, why, what worked, what 
didn't, and how an expert would've said the same thing. A 
mood badge tracks the customer from "Furious" toward 
"Resolved" as the conversation goes, plus a running average 
of your scores.

## Tech

Vanilla HTML/CSS/JS, no build step. Every message fires two 
Claude API calls at once — one plays the customer with a 
prompt tuned to the difficulty level, the other grades your 
response and returns structured JSON for the score, 
feedback, and rewrite.

Bring your own API key. Stays in the browser, nothing gets 
sent anywhere else.

## Setup

Open `index.html`, drop in an Anthropic API key, pick a 
difficulty and scenario, start typing.

Practice tool only — don't put a production key in here on 
a shared computer.

## Why I built this

The tickets that actually test you are the ones where the 
person's already furious before you've typed a word, and 
training for that is usually just "read this, watch this." 
I wanted something where you're in the actual exchange and 
find out right away whether what you said helped or made 
it worse — and where the bar gets higher as you get better, 
instead of staying easy forever.

---

Note: this repo also includes `simulator.html`, an earlier 
version without difficulty levels. The live version uses 
`index.html`
