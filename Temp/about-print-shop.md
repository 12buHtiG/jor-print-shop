# About the project we're building 🚀

Hey everyone,

This term we're building something bigger than anything you've worked on before. By the end, you'll have built and deployed a real web application that runs on the actual internet, with real user accounts, an admin panel, AI-generated artwork, and an in-app economy. Friends and family can visit it. You can show it to people. It will work.

Here's what's coming.

## What we're building

It's called **Print Shop**. Think of it as a tiny version of something like Redbubble or Society6, except you're going to build it from scratch.

Users sign up, generate artwork using AI image generation (the same kind of technology that powers tools like ChatGPT's image features), and then publish their designs onto t-shirts, mugs, stickers, and posters. Other users can buy those designs using in-app credits.

A few important things up front:

- **The credits are not real money.** Nobody is paying anything. The credits exist only inside our app, and they let us learn how online economies actually work without anyone needing a credit card.
- **The AI art is real.** When you type a prompt, an actual AI generates an image for you. Within rules we'll set up.
- **The site is real.** By the end of the project, our marketplace will be live on the internet, with a real domain name. Anyone can visit it.

The marketplace isn't fake. It's the same kind of system used by real platforms, just smaller. The skills you'll pick up are the actual skills used by professional developers building real products.

## What you'll learn

A lot. Here's the short version:

**Authentication.** How websites know who you are when you sign in, and how they decide what you're allowed to do once you're in. You'll build this from scratch.

**Role-based access control (RBAC).** Some users are regular members. Some are moderators (they review and approve content). One is the admin (they run the whole platform). You'll build the system that decides who can do what.

**Database design.** How to structure data so it's fast to read, safe to write, and never loses information. We're using a database called Convex, which is modern and fast.

**Append-only ledgers.** Sounds boring. It isn't. Every credit movement in the marketplace is recorded forever. Even when corrections happen, we never edit the past. This is how real banks track money. You'll build a tiny version of it.

**Why software has to be careful with money and history.** Some bugs are funny. Bugs in financial code are the opposite of funny. You'll learn the patterns that real systems use to avoid them.

**Content moderation.** When a user publishes a design, a moderator reviews it before it appears on the public site. You'll build the queue, the approval flow, and the rules.

**Admin panels.** The admin can manage users, manage tiers (we have something called Earning Tiers, more on that below), see the marketplace's full financial picture, and control everything from one place. You'll build it.

**Real production tools.** You'll use git for version control, the command line, deployment to a real domain, environment variables for secrets, and a database with a live cloud dashboard. Same workflow as a professional developer.

**TypeScript, Astro, Tailwind, and Convex.** The actual stack. You'll be writing real, modern code.

## The pages you'll build

About 35 different pages, divided into four areas based on who can see them.

### Public pages (anyone can see)

- The home page (featured designs)
- A browse page (the full marketplace, with filters)
- Design detail pages (one per design, with mockups on different products)
- Designer profile pages (one per creator)
- Category and collection pages
- Sign-in and sign-up
- About, terms, privacy

### Member pages (you have to be signed in)

- Your dashboard (welcome screen with your stats)
- The Generate page (where you create new artwork using AI)
- Your private gallery (designs you've made but not published yet)
- Your published designs (with their status)
- Design editor (edit a design's title, category, and which products it's printed on)
- Your sales (per-design earnings)
- Your orders (things you've bought)
- Your credits page (balance and full transaction history)
- Profile and settings

### Moderator pages (only mods see these)

- Review queue (pending designs waiting for approval)
- Flagged content (things users have reported)
- Collections manager
- Featured manager (pick which designs appear on the home page)

### Admin pages (only the admin sees these)

- Admin home (key metrics)
- The Treasury (three views showing the platform's full financial picture)
- Users (manage everyone, change roles, change tiers, ban if needed)
- User detail (full audit view of any single user)
- Tiers, Presets, Blocklist, Categories, Product Types (settings)
- Generation log and Transaction log
- API top-ups, grant credits, platform settings

## Some of the cool features you'll build

- **AI image generation** with prompt safety filters (the admin controls what kinds of prompts are allowed) and style presets that wrap your prompt with quality instructions.
- **A credit system** with a "grant pool" that the admin manages, automatic signup bonuses for new users, refunds when something fails, and a complete history of every credit movement ever.
- **Earning Tiers**: Sprout, Maker, Crafter, Patron, House. The admin assigns members to a tier, which determines what percentage of each sale they keep. You can change tiers later, and old sales keep their original rate (this is the snapshot rule, and it's surprisingly important).
- **A moderation system** with status badges (pending, approved, rejected), rejection reasons, and a full audit trail of every decision.
- **A flag system** where any user can report a design or user, and moderators can review and act.
- **Curated collections** that moderators can build to showcase themes ("pixel art picks," "summer vibes," etc.).
- **A real Treasury panel** for the admin showing how much money has been spent on the AI API, how many credits are circulating, and whether the platform is making a profit per generation.
- **Reactive queries** that update the page in real time without a refresh. When the admin grants you credits, your balance updates instantly.

## How it works (the short version)

1. You sign up. The system creates an account for you with the default Member role and the default Maker tier. You get a small starter credit grant.
2. You go to the Generate page, type a prompt, pick a style, and click Generate. Credits are deducted. The AI returns an image. It lands in your private gallery.
3. You publish a design from your gallery. It enters the moderation queue.
4. A moderator reviews it. They approve or reject (with a reason). Approved designs appear on the public marketplace.
5. Other users browse, find your design, click Buy, and pick a product (sticker, mug, t-shirt, poster). Credits move from buyer to designer (your tier determines how much you keep) and the platform gets a small cut.
6. You see the sale in your Sales page. Your buyer sees it in their Orders page. The admin sees the whole thing in the Treasury.

Repeat. Build a portfolio. Make money (in credits). Have fun.

## FAQ

**How long is this project?**
Around 14 milestones, spread across several months of classes. Each milestone is a real chunk of work that leaves the project in a better, working state.

**Will I work alone or with others?**
We code together as a class. Everyone moves through the same milestone at the same time. If you fall behind, we pause and bring you back up. You won't be left behind, and you won't have to wait alone if you finish first (we'll find you something to extend).

**Do I need to be good at design or art?**
No. The AI does the art. You're building the platform around it. If you do enjoy design, you'll get to put that into your work, especially when we're styling the public pages.

**Can I work on this from home?**
Yes, but you don't have to. The class moves together. Working at home is encouraged but optional. If you do, please don't get help from anyone else (parents, friends, AI assistants). Struggling productively is part of how this works.

**What if I get stuck?**
Bring it to class. The class culture is "stuck on something? Say so." Everyone gets stuck. The skill is asking for help instead of staying stuck.

**Is the AI safe?**
Yes. The platform has multiple layers of safety:

- A blocklist of words that get rejected before they reach the AI
- Style presets that wrap every prompt with safety constraints
- A rate limit so no one can generate too many images too fast
- A moderation queue so designs are reviewed before they're public
- Generated images are stored on our system, not on the AI provider's

**Do we need to spend money to use the AI?**
The teacher pays for the AI API, with a hard spending cap to make sure no one accidentally runs up bills. You don't pay anything.

**Will my project be public?**
Yes, eventually. By the end, the site will be deployed to a real domain. Anyone with the link can visit. You'll be able to share it with friends and family.

**Can I keep building on this after the class ends?**
Absolutely. The code is yours. You can keep adding features, change the design, deploy your own version, or use it as a starting point for something new.

**What if I don't get something the first time?**
Nobody gets everything the first time. Coding is iterative. You'll see most of these patterns multiple times across the project, and they'll click the third or fourth time, not the first.

## What I expect from you

- Show up. Sessions build on each other.
- Type along. You learn by typing, not by watching.
- Ask questions. The dumb question someone else was too embarrassed to ask is usually the most useful one in the room.
- Help others. Teaching what you just learned is one of the best ways to make it stick.
- Have fun. This is a real project but it's also play. Don't be too serious.

That's the project. By the end, you'll have built something you can be genuinely proud of. Let's go. 🛠️
