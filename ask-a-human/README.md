# Ask a human expert

A page where people and AI agents can bring me in on a problem they're stuck on, with my first reply within 15 minutes while I'm online.

**Live:** [cristiandesivo.com/ask/](https://cristiandesivo.com/ask/)

## The problem

AI models do well on known problems, not new ones: on MIPLIB-NL, the best model tested wrote a correct optimization model 82% of the time on textbook problems and 39% on real industrial ones ([paper](https://arxiv.org/abs/2602.10450)). When an agent, or the person running it, gets stuck on something new, there's no quick way to bring in a human: hiring means profiles, calls and contracts, and an agent can't do any of that on its own.

## What I built

A service I built and run end to end on my site:

- You (or your agent) send a summary of the problem, up to 300 words, and an email for the reply.
- 20 USD for the first reply, paid with PayPal checkout on the page. Currently free to try.
- I read it on my phone and reply myself: within 15 minutes while I'm online, or by 09:30 UTC if it arrives while I'm offline.
- If the problem needs more work, my first reply says so, with a tentative budget. Taking it is optional.
- For agents, the same terms are machine-readable: [/ask.md](https://cristiandesivo.com/ask.md) (Markdown), [/status.json](https://cristiandesivo.com/status.json) (JSON, with live online status) and [/llms.txt](https://cristiandesivo.com/llms.txt). Agents can also send the form directly as JSON.

## How it works

Page and terms → summary form → PayPal checkout → confirmation email + request relayed to my phone (Telegram) → my reply in Telegram → emailed back to the client.

- The online status comes from my published hours (every day, 09:00 to 24:00 UTC), so what the page and `/status.json` say is always true.
- The form checks the email and the 300-word limit before payment.
- The client gets a confirmation email right away, so a mistyped address shows up as a missing email.
- I reply to the request in Telegram, and my reply is emailed to the address in the form.

## Results

Launched in October 2026. No client numbers to report yet.

## Built with

Python · Django · PayPal Checkout · email · Telegram Bot API · Markdown, JSON and llms.txt for agents

## Links

- Live page: [cristiandesivo.com/ask/](https://cristiandesivo.com/ask/)
- For agents: [/ask.md](https://cristiandesivo.com/ask.md) · [/status.json](https://cristiandesivo.com/status.json) · [/llms.txt](https://cristiandesivo.com/llms.txt)

Want something like this? [cristiandesivo.com/hire_me/](https://cristiandesivo.com/hire_me/) · [Freelancer.com](https://www.freelancer.com/affiliates/email/18225913/)
