## Mike Matthews

I build AI phone and messaging systems for small businesses. Before that I spent five years customer facing inside a regulated financial firm, around twenty live cases a day where the answer had to be right the first time.

### What I do

Take a problem described by someone non technical, work out what it actually is, turn it into a system that runs, then own it when it breaks.

I build AI first. I write the specs, direct the tooling, and verify the rules and the output against requirements before anything ships. I am not a career engineer and I do not claim to be one. What I am is fast from problem to running product, and careful about the part that has to be right.

### Currently

**Matthews Automation LLC**, founder. AI phone agents for home service companies in metro Atlanta. Discovery, configuration, live demos on the customer's own scenarios, go live, then tuning from recorded calls. Production ownership covers call routing failures, number reputation and carrier spam labeling, and reconciling provider logs against what actually happened on a call.

The agent's escalation rules came out of working through 273 recorded call transcripts to define exactly what it handles itself and what goes to a person.

### Shipped

**Body Compass**, meal tracker and food journal. Live on the App Store and Google Play.

**matthewsautomation.net**, marketing site built in Astro and Tailwind.

### Work you can read

**[n8n-lead-response](https://github.com/mikematthewsai/n8n-lead-response)**, eleven n8n workflows, 108 nodes, pulled out of a live production install with the credentials stripped. A missed call turns into a text to the customer, a text to the owner and a call that connects the two, then a follow up cadence that stops the moment a person replies. Quote chasing, invoice reminders and a 7am brief sit on top of it.

It ships with the test log rather than a claim: 11 of 13 checks on the core eight passed on the live system with timestamps, and the two that are not fully verified say which inch is unproven and why. Two real bugs turned up while running it, both written up with symptom, cause, fix and re-test. Every push runs a validator that checks the workflows parse, that the node counts in the README match the files, that every data table filter uses a match type n8n accepts, and that no credentials or real numbers are in the repo.

### Stack

TypeScript, Next.js, React Native and Expo, Supabase and Postgres, Vercel, Twilio, n8n

### Background

Five years in fraud and wire risk at a large brokerage: wire fraud, account takeover, elder financial exploitation, check fraud and crypto related schemes. Currently in a wealth management service seat at the same firm.

FINRA Series 7 and Series 63. BS Criminal Justice, Liberty University.

Open to remote.

[matthewsautomation.net](https://matthewsautomation.net) | [LinkedIn](https://www.linkedin.com/in/michael-matthews-a98485326)
