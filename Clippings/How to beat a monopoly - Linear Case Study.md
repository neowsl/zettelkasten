---
title: "How to beat a monopoly - Linear Case Study"
source: "https://www.youtube.com/watch?v=pRf8_40EDtM"
author:
  - "[[Tom Delalande]]"
published: 2026-08-24
created: 2026-08-26
description: "A case study analyzing how Linear broke into Jira's Monopoly. Focusing on design, craft, quality and processes.Some of the editing is bad, I'm sorry. It's a skill issueChapters0:00 SaaS is dead1"
tags:
  - "clippings"
---

![](https://www.youtube.com/watch?v=pRf8_40EDtM)

A case study analyzing how Linear broke into Jira's Monopoly. Focusing on design, craft, quality and processes.  
  
Some of the editing is bad, I'm sorry. It's a skill issue  
  
Chapters  
0:00 SaaS is dead  
1:45 Minimum Viable Product  
3:52 Sync Engine  
9:49 Focus & Patience  
10:57 Product Philosophy  
16:09 Hiring  
16:58 Key Takeaways

## Transcript

### SaaS is dead

**0:00** · The year is 2019. This meme is brand new. Paris is on fire, and software as a service is dead. It's not just dead, though. It's been mummified, buried, forgotten, excavated, and put up in a museum. You're not creating anything new anymore. This isn't the same internet where you can just make Flappy Bird and retire off advertisement money alone.

**0:15** · It's competitive, especially if you're making productivity tools, and especially if you're making an issue tracker for software companies.

**0:21** · Atlassian is valued at $25 billion and has essentially established itself as a monopoly by acquiring Trello, the indie competitor to its flagship product. This video is about how Lineia broke into that monopoly. What I learned by studying their company and product and how you can replicate that in your ventures. I've condensed their entire playbook into four easy steps that I will tell you right now. Step one, be finished.

**0:41** · Step two, work at a Fortune 500 company. Step three, quit. And step four, profit. But surely there's more to it than that. Could this be replicated by someone who was Danish? For example, Jira might be the most hated developer software. If animators have Adobe, we have Atlasian.

**0:53** · All it needs to do is track what work is being done, but apparently that's too hard. You want to update the ticket right before stand up? Cool. But no one's going to see any of your changes until three minutes later when the entire board shifts at once and now everything is in a completely different spot. There's so many workflows and customizations and edge cases and slowness that turns something that should be very simple, sharing what work needs to be done with others into something that most developers actively try to avoid. But just like Adobe, Jira is everywhere. You cannot escape it. As soon as you collaborate with another team, there's a nine out of 10 chance that they use Jira. You may as well use Jira so that you can share issues directly.

**1:22** · This is what our three Finnish founders, Carrie Sarinon, Jory Lo, and Thomas Artman working at Fortune 500 companies were facing when they launched Lineia in 2019. And they did so by hitting Jurro right where it hurt. Where there is enough people complaining, there is an opportunity. And Lineia's killer feature was its quality and speed. While Jira sends updates over what feels like Telegram, Linear is fast and multiplayer is seemingly instant.

**1:42** · While Jira is complex and confusing, Linear is focused and opinionated. Linear's first interesting decision was to rethink the minimum viable product. General advice is to condense your product down into its single most valuable feature and ship that as your first version. This helps you stay focused on the problem you're solving.

### Minimum Viable Product

**1:56** · This is good advice, but it's also bad advice. Modern products aren't defined by a single feature. Users expect more those greedy bastards. You need to match expectations and provide a holistic solution to their problem just to be considered. And then you need to stand out with non-functional advantages like speed, price or design. Instead of building an MVP by reducing the scope to a singular feature, the linear team reduced the scope to a singular user persona. Jura has the enterprise lockdown. there's no chance of beating them at their own game. But for a startup with 10 people or less, it's much easier to make a compelling product. And I don't know if you noticed, but that exact description describes Lineia's company.

**2:26** · You either got to be a subject matter expert or build something for yourself, or you will just build something nobody wants.

**2:32** · Again, Linear's approach was to focus their entire MVP on solving the issue tracking problem for the smallest of startups. This still reduces the scope while remaining competitive and targeting users that are more likely to consider other options. They did not even consider and outright turned away mid-sized and enterprise companies early on. Their product was not ready for that scale and they were focused on nurturing it in a healthy way. Each user only has one chance at a first impression of your product and I have to be honest with you, your product has a lot of problems.

**2:55** · Linear avoided onboarding too many customers while the product was still finding its feet. More important to spend time talking to your initial users and build a better product than to burn through even when the product isn't ready yet. You just get the same bug report from all your prospects anyway.

**3:07** · Practically speaking, this meant that they would invite about 10 new users a week. They had a steady stream of new users providing feedback for months and this helped them nail the product market fit early. The linear team was very deliberate about avoiding investments and hiring until they felt that the product was right. The founders had previously experienced hyperrowth at companies like Uber and Airbnb and they certainly wanted to avoid that again at all cost. They did not start trying to capture an entire market as quickly as possible. They started building a product for a very specific user group and slowly as time went on eventually added features and improved infrastructure such that years later they were ready to call those larger companies back. This isn't easy.

**3:37** · It takes a lot of confidence to back yourself and focus on the product first. But it gives you a strong foundation. Despite not seeking funding, Linear was eventually approached by investors directly and managed to secure funding that way. And despite a slow on boarding process, the company was profitable within 2 years. This is Thomas Artman.

### Sync Engine

**3:53** · If you let this guy anywhere near your company, he will build a sync engine. He built his first sync engine for a Finnish game company in 2004. This one makes sense. He then moved to an animation studio in China and built a sync engine. Then he built one for Groupon. And then he left and built one for Uber with a Java and a Swift client that no one ever used. And then he left and joined Linear. Would you like to guess what the first thing he did at Linear was? Would you like to guess what he's still doing now? Instead of working on anything to do with the product, he spent 6 months working on a sync engine.

**4:19** · The sync engine is Linear's secret weapon that everyone knows about because he talks about it all the time. This guy is obsessed. It's what lets them build a reactive product with instantly shared changes, tiny server costs, and massive developer productivity. When you first open Linear, it downloads everything for the current workspace. Every user, every status, every issue, every comment, it all gets downloaded and stored on dis, even in the browser. I bet you can see why they didn't want to start with enterprise customers. Can you imagine downloading 30,000 issues and all their comments for a workspace with 300 members? But the beauty of it is that after the initial download, everything is done locally.

**4:48** · If you want to update an issue title or assign, you just update the state in React. They use a dependency called Mobox that uses the observer pattern to rerender components automatically when you update the state of an object that it depends on. From the engineer's point of view, it's all front end. And the sync engine does two things. First, it intercepts all those state changes and sends them as transactions to the back end. Second, it keeps a web socket open to detect incoming changes from other users and updates the state directly. From the UI's point of view, a local change and a remote change are identical. This means that client side changes are always optimistically rendered and server side changes are synced without any extra work.

**5:19** · Transactions are synced to the back end using GraphQL. The back end can either accept or reject them. If transactions are rejected, then the client will roll back to the previous state. Roll back. This mechanism is also the reason why the legally safe My Little Pony fighting game with characters created by the same person who created the original My Little Pony series has a better online experience than Super Smash Bros. Ultimate.

**5:38** · Nintendo, do better. Delaybased net code is ass. Roll back is the only way I want roll back in every game and platform.

**5:44** · And now I want it in all my SAS products, too. React, GraphQL, and the observer pattern are three words that would usually make me grab the nearest gun and brutally murder the first person I see. But this is actually an amazing way to build an app. Not every application, but it works really well for a product like Linear. My big problem with React is that you end up with the state in two places. Back end has a set of state and you serialize it and send it to the front end. Lots of weird bugs start happening when the client and the server aren't aligned. My solution to this has been to prefer server side rendering and keep everything on the back end. But I am false. The cost of that is that your servers work more and the front end is inherently less reactive and it's got to feel good.

**6:14** · This approach flips that on its head. The client state is the source of truth. Everything is instant and reactive. The back end, just like your dad, feels like it doesn't even exist because while you're using the app, it kind of doesn't. Things just happen. You click on something, it's there. No loading, no spinners, no waiting, no inconsistencies. And when the backend changes do come in, they slide right in just like your mom's new boyfriend. The objects update and rerender using the exact same mechanism that you used to change the state on the climb. Though everything is always in sync, but it's not all come shots in Rainbow. You know how I told you that everything gets downloaded when you first launch the app? I lied. I have the mic. I can do that. No facteing.

**6:43** · That used to be the case, but as they scaled up, it was genuinely too much for bigger companies.

**6:48** · They now download a skeleton of the workspace and populate issues and comments lazily. The initial bootstrap is also another problem. As companies got more issues, it became too slow and kept crashing the server. So they added some bookmark, a MongoDB cache and cues on the back end. It's not exactly the simplest architecture and it wouldn't work well for every product and MongoDB is not webcale. What makes linear unique is that most of the validation can be done on the front end. Issue trackers are almost all userenerated content. But in a context where the user is allowed to edit almost anything in the workspace by default. For the vast majority of cases, the client side validation is more than enough. And this isn't true for every product.

**7:18** · You probably need more validation because of your dad. A major benefit of this is that all your engineers are product engineers by default. The engineers are thinking about the user experience, how the workflow feels, and what problems it's solving. No one is thinking about endpoints or cing or syncing or errors.

**7:31** · It's all handled for you. They perform changes directly on the state and everything is taken care of. Even with something as sophisticated as Tanstack, adding optimistic client side rendering to every endpoint on every page is a large endeavor. Adding real-time updates across the whole app is nightmarish.

**7:44** · Tanstack is great. You're probably right. Don't you think that maybe you've been using bad tools so long that the bare minimum feels fantastic? Every single view in linear just gets that for free and it's fast and easy and it just works. Engineers can even disable the backend syncing and prototype features completely local. If they like the way it feels, they can add some backend validations, flick a switch, and it's ready to ship. A minor benefit is the server cost. This is client side rendering to the Mac. You don't even need to send all updates to the back end. You can take your time, batch them up, and send them whenever the server has time. Server costs aren't the most impactful thing, but it's nice. I would be lying to you if I said it wasn't a lot to maintain.

**8:14** · There are a few engineers, including one of the founders, working full-time on the Sync Engine, and there isn't really a plug-and-play solution I can find that would be nearly as sophisticated as what Linear is using today. This is a pattern that I would love to be explored more, and I generally believe that it will be a staple for development in the future.

**8:28** · The tooling is just lacking today, though. Still, I don't think the lesson here is you should build a sync engine.

**8:33** · I'm not giving you an excuse to waste 6 months of development cost building a custom sync engine for your horse Tinder project. Despite how cool it is and the advantages it has, the sync engine is not a fit for every product. The lesson here is more that you should invest in your infrastructure early, especially infrastructure that either a gives you a competitive advantage or b makes it easier for you to focus on the product in the future. Linear sync engine is the perfect example of this. The sync engine gives it a strict speed advantage over Jira, an advantage that Jira can't copy without investing huge amounts of work into a migration that affects their entire codebase.

**9:00** · This only works because they started with the sync engine first and it also happens to make development faster, allowing all the engineers to go all in on the product. It's funny reading about Linear's processes. You talk to Carrie and Jory and they're like, "Yeah, we ship so fast. users are using features within 3 days of deciding we want to work on something. We don't know what we're doing and we just experiment and see what happens. And then you talk to Tomas and he's like, "Yeah, we meticulously plan out our infrastructure needs a year in advance and go really slowly to make sure everything is stable. It's like the three founders themselves have ideologies pulling in completely different direction.

**9:28** · The fast product cycles, which we will talk about later, only work because the infrastructure is so solid. The whole ecosystem works together to create a great product. This is especially important when it comes to infrastructure that has high migration costs. First thing Thomas worked on was the sync engine and they started off on Kubernetes and Google Cloud immediately.

**9:43** · Thomas was traumatized from the hypergraph of Uber. He was one of the first 15 mobile engineers and when he left there was 300. He did not want to do that again. That takes discipline though especially because overindexing on the wrong thing is why most businesses failed. They could comfortably make the bold decision to invest in the infrastructure because they knew that the market existed for this product. I mean if Atlassian is worth 25 billion, there's definitely a market there. You should still find product market fit and validate your idea. But there's more to it than that now. You can't just pump a small MVP and hope to blow it from there. Anyone can do that. You have to be able to adapt and grow, and you have to do so better than everyone else.

### Focus & Patience

**10:12** · You can't just ride the wave of being an early bloomer in middle school. You have to find a way to be hot in high school. The early days of linear weren't as much hustle and grind as it was focus and patient. But I \[ \_\_ \] hate hustle and grind. They didn't have to force any doors open.

**10:24** · They focused on building a great product and a lot of opportunities came searching for them, which was a good sign that they were heading in the right direction. But there might be a bit of survivorship bias here. The team is very honest that their background at companies like Airbnb, Uber, Groupon and Coinbase is a big part of what gave them those initial opportunities. The initial weight list was mostly people who followed them as ambassadors for those company. And when it comes to startups, investors are investing in the founders, not the product itself. Easier to get money with a nice resume. So basically, you're \[ \_\_ \] Still, I can't help but feel that building a great product speaks for itself. Grind and hustle never lasts forever. Focus and patience is a more sustainable long-term plan.

**10:53** · If you are solving a real painoint, the opportunities will present themselves.

### Product Philosophy

**10:58** · Harry says that the more saturated a market is, the more design matters. When it was 2008, you could just make IBR and become a multi-millionaire. It was the only app of its kind on release. But now, everything has been done, and everything has been done more times than you can count. No one will care about your product unless it stands out. Great design is your differentiator. Linear feels so special because modern software has lost its soul. In a way, everything is too optimized. We've overindexed on datadriven everything and forgotten how to build software that helps humans instead of taking advantage of them. AB testing is harmful to humans. It's not prioritizing their experience. It's maximizing their attention without consent. Like a reality is ambiguous.

**11:28** · It can mean many different things to different people. But for most companies, quality means number go up at the cost of everything else. Everyone is doing whatever it takes to make the number go up instead of leaning on their own experiences and expertise to craft a better human experience. When a measure becomes a target, it ceases to be a good measure. Abraham Lincoln. It's like when you watch a Mr. Beast type video and you can feel your brain being farmed for attention. There's no respect in the transact. They would kill you if it made the number go higher. Linear differentiates itself by forgoing AB test and not relying on metric and instead relying on their own taste and experience to build something for humans.

**11:58** · The goal isn't to optimize any specific part of the system. It's for the system to work cohesively as a whole. They still measure and inform themselves using metric, but that doesn't drive the decision. They are in control. They always build their feature with a user in mind, but not some hypothetical user, Gary from company X, who wants to bulk import issues from a floppy disc. Man, Gary's a \[ \_\_ \] They are thinking about a specific real life person that is currently having a problem. Identifying the root cause and coming up with a solution. This means talking to users. I know, gross. Who wants to talk to humans when you could just watch a dashboard that gives you quantitative data?

**12:26** · But if you want to build products for humans, you might have to deal with humans sometimes. Almost all engineers at Linear are working directly on the user experience, and all of them have Slack channels talking directly to the customers that they are building those experiences for.

**12:37** · Leaning on your own intuition and taste can be scary. There isn't always a right and a wrong. That's a skill to be learned, a skill that most designers have let atrophy in favor of letting the metrics decide for them. But this confidence and trust in themselves spreads throughout the whole company.

**12:49** · They work in small teams, which is not groundbreaking. I struggled to find a company punching above its weight that's not working in groups of three to five. But their teams are also dynamic. A team is brought together for a project and then disbanded. I like that. I get bored. They don't have rigid processes in place. Product managers, which there are only two of, maintain a small backlog of 30 to 50 items and that's it.

**13:05** · Employees have a huge amount of agency on what they work on next. This only works when you have a relatively small team. But Lineia have been very deliberate in not hiring more than they need. They prioritize quality over quantity and prefer to lean towards having fewer people rather than too many. They have great people and put trust above the process. Both at a macro level when prioritizing work and organizing teams and at a micro level when letting designers use taste over metrics to make decisions. The linear team believes that productivity software should be opinionated. The tool is just a means to an end. No one's job should be to manage and maintain the tool itself. This is how they avoid becoming big and bloated like Jira.

**13:33** · More specifically, they have already decided that they will never add any features that fall under the umbrella of customization requested by middle managers in order to make reporting easier at the cost of the individual contributor's workflow. Round of applause. Can we just make this a general rule like worldwide for every product? The individual contributor is Linear's end user. Regardless of who signs for check or approves the tool, the user who actually lives in the tool always takes first priority. When working on features, they try to get a working prototype as soon as possible, preferably within 3 to 5 days, and they ship it straight to production under feature total.

**14:02** · It starts with internal use only, sometimes with the sync engine disabled so they can make breaking changes. Since they spend all day every day using their own product, they can get a firsthand feel for the feature, see what works and see what doesn't, and then they immediately start refining. Just like babies, all ideas start out ugly. That's why it's important to get something out as quickly as possible.

**14:17** · You're never going to think your way through the whole experience. The more iterations you can get in, the better it will be. Once a feature feels good internally, they enable it for a subset of users. If this feature was requested by a specific company, they will enable it for them. But they also have a group of beta users that are open to testing new, less polished features and provide feedback. They have a mature internal feature flag tool that lets them do these more complex rollouts without deployment. Do you remember the bit about setting up good infrastructure?

**14:38** · That's like this whole company's thing at this stage. Engineers talk directly to customers and keep refining until the feature is ready for general availability. I love that this three-stage roll out for releasing mirrors how linear initially released their product by focusing only on startups which is their own use case and releasing to mid-size companies which demand more but will still provide helpful feedback and then releasing to enterprise where the stakes are the highest. There are generally no deadlines but if there is a deadline it's always treated as P 0. Same thing for bugs. Once a feature is released, it will be monitored for bugs. Linear has a zero bug policy. The public SLA is one week but the internal one is 1 day.

**15:05** · If there is a bug, it becomes the highest priority and all other work is paused for whomever is working on it. This comes at a cost. It means they might sacrifice feature work, but this is a deliberate choice like being gay, aligning with the rest of the company to create a great product and take pride in their work. It also makes sense economically long-term. Bas is all about retention. New features is work for hypothetical new users, but fixing bugs is for your existing real paying customers. Putting quality above all else isn't just for the engineering team. It's companywide.

**15:29** · Sales, marketing, customer service, and management are all expected to put quality above everything else, including revenue, and that has to come from the top down. To use Car's own analogy, you cannot complete the main quest and chase side quest simultaneously. Actually, that doesn't really work because I always manage to do the Dark Brotherhood and the main quest on every playthrough.

**15:46** · Like, you can just go back. The game waits for you. Linear's main quest is to build a quality product. The leadership is very clear about that, even at the cost of revenue. And there is no doubt that they are leaving some money on the table. But that is the trade-off they have decided to make. For a lot of CEOs, prioritizing revenue is an outright non-negotiable. It defines their entire role. It defines their entire personality. My god, have you tried talking to some of these guys? But has used that to differentiate itself in a crowded market and to create something that people genuinely love. Hiring is something that always comes up with linear. Somehow or another, it finds its way into almost every interview, podcast, or blog post about this company's processes. At first, I really didn't get it.

### Hiring

**16:17** · They do a full week paid work trial working on the actual product before you get hired, which I guess is kind of cool, but also kind of stupid.

**16:24** · Are you supposed to just use up a week of annual leave at your current workplace every time you go for an interview now? I only have four weeks, brother. What are you doing? But after researching the rest of the company, I understand why people are obsessed with their hiring. Linear's whole approach to developing product only works if you have the right people. Lineers bar when hiring is extremely high. They don't hire many people and only hire people who show craft and care, who think about decisions, have their own opinions and are able to articulate those opinions.

**16:46** · Because of that, they have very little process. The people like me always come first. Kind of like the contrast between their infrastructure and product development. The only way that these processes or lack thereof work is because they have the best talent. There is a higher upfront cost for a better result long term. Jira is still far more popular than linear, but linear is now the heavy favorite amongst startups and developer focused companies. Citation needed, but will not be provided. They broke into the monopoly and carved out a small $1.25 billion valuation for themselves by creating something that all their employees can be proud of.

### Key Takeaways

**17:14** · Linear story is a story of craftsmanship and choosing quality above everything else. It's also a story of focus and patience and investing in strong foundations. The biggest takeaway for me is that you actually have to prioritize quality to create a quality product. And that means depp prioritizing other things. Choosing to fix bugs at the cost of new features, choosing to build great experiences at the cost of higher click-through rate. That's not always easy, but it's what's worked for them long term. More granularly than that, there are some tangible processes that you can apply from a linear approach.

**17:38** · Start by being patient, slowly going through your backlog of prospects, 10 or so at a time, to make sure your product solves a real problem for all of them. Prefer to underhire, but hire quality people that you trust. Focus on product market fit over investor money. Nope.

**17:49** · Your MVP down by targeting a specific user group, preferably one that applies to you so that you can use your own product. Follow similar approach when shipping features, moving quickly and focusing on iteration over perfection.

**17:58** · Start with internal users, then do a rolled release once the feature is ready. Build strong foundations by hiring the right people and by investing in infrastructure early in a way that gives you a competitive advantage so that you can ship faster in the future and reduce the need for processes. And finally, build software for humans.

**18:12** · Prioritize your individual users and think about their experience, not just as a data point on a chart, but as a real person that you are impacting. There are a lot of mediocre products. Linear is an excellent reminder that building great products isn't necessarily complex. The hardest part is just choosing to do so.