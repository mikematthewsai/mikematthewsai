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

**[n8n-lead-response](https://github.com/mikematthewsai/n8n-lead-response)**, fifteen n8n workflows pulled out of a live production install with the credentials stripped. A missed call turns into a text to the customer, a text to the owner and a call that connects the two, then a follow up cadence that stops the moment a person replies. Quote chasing, invoice reminders, appointment reminders that work out quiet hours before they wait, and a 7am brief sit on top of it, with hosted forms so a follow up can be started from a phone.

It ships with the test log rather than a claim. Every check says what passed on the live system, with timestamps, and what is still not verified and why. The bugs that turned up while running it are written up with symptom, cause, fix and re-test. Every push runs a validator that checks the workflows parse, that the node counts in the README match the files, and that no credentials or real numbers are in the repo.

![The inbound SMS router, one of the fifteen workflows](https://raw.githubusercontent.com/mikematthewsai/n8n-lead-response/main/docs/images/inbound-sms-router.png)

**[Six standalone SMS templates](https://github.com/mikematthewsai/n8n-lead-response/tree/main/templates)**, each importable on its own with nothing but a Twilio account, and none of them keep their own database:

- **Quote chaser.** Up to three nudges on an unanswered quote. Before each one it asks Twilio whether the customer has texted in, and stops if they have.
- **7am owner brief.** One text each morning built from the Twilio message log: texts in, texts out, anything undelivered, and who is still waiting on a reply.
- **Appointment reminders with quiet hours.** A confirmation and two reminders, with every send time planned the moment the booking arrives so a reminder never lands after the appointment.
- **STOP, START and HELP alerts.** Tells the owner the moment a customer opts out, and can pass it to a CRM.
- **Google review request.** One text with the review link after each job, never twice in 90 days and never in quiet hours. Every customer gets the same link, so there is no review gating.
- **[Website and line watchdog](https://github.com/mikematthewsai/n8n-website-line-watchdog-sms).** Every 5 minutes it checks that the website loads, the Twilio balance is above a floor, the number still routes calls and texts where it did, and carriers are not blocking its texts. One text when something breaks, one when it recovers, and a short morning check-in so silence means something.

Each one was tested against a real Twilio number, and the README lists every run next to what was not covered. The first is in review for n8n's public template library.

**[clinic-billing-architecture](https://github.com/mikematthewsai/clinic-billing-architecture)**, how I chose the architecture for a membership billing and reminder system at a small clinic. The client is not named and none of their data is in it. It is the decision itself: what the constraint actually was, the three designs considered, the PHI boundary drawn as diagrams, why the card processor never receives anything that identifies a person, and a vendor table with the date each fact was checked. It includes the assumption I got wrong in August and corrected when I re-checked it.

**Build logs** on [matthewsautomation.net/blog](https://matthewsautomation.net/blog): what broke, why, and how it was fixed, written as it happened. Most recent: [a watchdog for the things that quietly stop your leads](https://matthewsautomation.net/blog/build-log-website-and-line-watchdog) and [four SMS workflows that do not need a database](https://matthewsautomation.net/blog/build-log-four-sms-templates-no-database).

### Stack

TypeScript, Next.js, React Native and Expo, Supabase and Postgres, Vercel, Twilio, n8n

### Background

Five years in fraud and wire risk at a large brokerage: wire fraud, account takeover, elder financial exploitation, check fraud and crypto related schemes. Currently in a wealth management service seat at the same firm.

FINRA Series 7 and Series 63. BS Criminal Justice, Liberty University.

Open to remote.

[matthewsautomation.net](https://matthewsautomation.net) | [LinkedIn](https://www.linkedin.com/in/michael-matthews-a98485326)
