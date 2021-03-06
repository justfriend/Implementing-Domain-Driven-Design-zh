# 第 1 章 DDD 入门

> Chapter 1. Getting Started with DDD

Design is not just what it looks like and feels like. Design is how it works.

> 设计不只是感观，设计就是产品的工作方式。

—Steve Jobs

We strive to produce quality in the software we develop. We achieve some quality by using tests to help us avoid delivering software with a fatal number of bugs. Yet, even if we could produce completely bug-free software, that in itself does not necessarily mean that a quality software model is designed. The software model—the way the software expresses the solution to the business goal being sought—could still suffer greatly. Delivering software with few defects is obviously good. Still, we can reach higher for a well-designed software model that explicitly reflects the intended business objective, and our work may even reach the level of great.

> 我们都致力于开发高质量的软件。通过测试，我们可以消除软件系统中大量的 bug。然而，即便我们的软件中没有 bug，也不能表示我们设计的软件模型本身就是好的。软件中存在少量的瑕疵是无可厚非的，而同时，我们是可以设计出能够准确表达业务意图的软件模型的。

The software development approach called Domain-Driven Design, or DDD, exists to help us more readily succeed at achieving high-quality software model designs. When implemented correctly, DDD helps us reach the point where our design is exactly how the software works. This book is about helping you correctly implement DDD.

> 领域驱动设计（DDD）作为一种软件开发方法，它可以帮助我们设计高质量的软件模型。在正确实现的情况下，我们通过 DDD 完成的设计恰恰就是软件的工作方式。本书便是帮助你如何正确实现 DDD 的。

You may be completely new to DDD, you may have tried it and struggled, or you may have already succeeded with it before. Regardless, you no doubt are reading this book because you want to improve your ability to implement DDD, and you can. The chapter road map helps you target your specific needs.

> 你可能是个 DDD 新手；也可能做过一些 DDD 尝试而目前正苦苦地挣扎着；还有可能你已经成功地运用了 DDD。不管如何，你都希望通过本书来提高自己的 DDD 技能，我相信你是可以的。以下是本章的学习路线图：

::: tip
Road Map to This Chapter

> 本章学习路线图

- Discover what DDD can do for your projects and your teams as you grapple with complexity.
- Find out how to score your project to see if it deserves the DDD investment.
- Consider the common alternatives to DDD and why they often lead to problems.
- Grasp the foundations of DDD as you learn how to take the first steps on your project.
- Learn how to sell DDD to your management, domain experts, and technical team members.
- Face the challenges of using DDD armed with knowledge of how to succeed.
- Look in on a team that is learning how to implement DDD.

---

> - 了解 DDD 可以为你的项目和团队带来哪些好处
> - 如何确定你的项目是否适合采用 DDD
> - 了解 DDD 的常见替代方案和它们将导致问题的原因
> - 学习 DDD 的基础
> - 学习如何向你的管理层、领域专家和技术成员推销 DDD
> - 了解使用 DDD 时所面临的挑战
> - 看看一个正在学习采用 DDD 的团队是如何工作的

:::

What should you expect from DDD? Not a heavy, dense, ceremonial process that blocks your way to progress. Rather, expect to use the agile development techniques you probably already have come to trust. Beyond agile, anticipate the acquisition of methods that help you gain deep insight into your business domain, with the prospect of producing testable, malleable, organized, carefully crafted, high-quality software models.

> 那么，你应该期待从 DDD 中得到什么呢？首先，DDD 不应该是一个仪式性的过程，更不应该成为你项目进度的阻碍。此时你可以采用敏捷开发方法，或者寻找另外的方法来帮你更深层次地了解自己的业务领域。我们的目标应该是创造一个可测试的、可伸缩的、组织良好的软件模型。

DDD gives you both the strategic and tactical modeling tools necessary to design high-quality software that meets core business objectives.

> DDD 同时提供了战略上的和战术（Tactical）上的建模工具来帮助我们设计高质量的软件模型。

## 1.1 CAN I DDD? 我能 DDD 吗？

You can implement DDD if you have

> 你是可以实施 DDD 的，如果你：

- A passion for creating excellent software every day, and the tenacity to achieve that goal
- The eagerness to learn and improve, and the fortitude to admit you need to
- The aptitude to understand software patterns and how to properly apply them
- The skill and patience to explore design alternatives using proven agile methods
- The courage to challenge the status quo
- The desire and ability to pay attention to details, to experiment and discover
- A drive to seek ways to code smarter and better

---

> - 有开发卓越软件的激情和毅力
> - 渴望学习和进步
> - 有能力理解软件模式，并懂得如何应用这些模式
> - 有发掘不同设计方法的能力和耐性
> - 勇于改变现状
> - 看重细节，希望亲自试验
> - 希望编写更好的代码

I’m not going to tell you that there isn’t a learning curve. To put it bluntly, the learning curve can be steep. Yet, this book has been put together to help flatten the curve as much as possible. My goal is to help you and your team implement DDD with the greatest potential for success.

> DDD 不是没有学习曲线，而且学习曲线有可能很陡。不用着急，本书将尽可能地为你降低学习曲线，我的目的就是挖掘你成功的潜能，帮助你和你的团队实现 DDD。

DDD isn’t first and foremost about technology. In its most central principles, DDD is about discussion, listening, understanding, discovery, and business value, all in an effort to centralize knowledge. If you are capable of understanding the business in which your company works, you can at a minimum participate in the software model discovery process to produce a Ubiquitous Language. Sure, you’re going to have to learn more about the business, lots more. Still, you are on your way to succeeding with DDD already because you can comprehend the concepts of your business, you revel in developing great software, and that gives you the proper footing to take DDD all the way.

> DDD 首先并不是关于技术的，而是关于讨论、聆听、理解、发现和业务价值的，而这些都是为了将知识集中起来。如果你了解公司的业务，那么你至少可以为 DDD 的通用语言（Ubiquitous Language）做出贡献。当然，你可能需要学习更多的业务知识。由于你对业务概念的理解，你已经开始走在 DDD 的康庄大道上了。

Won’t having years, even a decade or two, of software development experience help? It might. Nevertheless, software development experience doesn’t give you the ability to listen and learn from domain experts, the people who know the most about some high-priority area of the business. You are at a greater advantage if you can engage with those who seldom, if ever, express themselves using technical lingo. You’re going to have to listen and listen carefully. You’re going to have to respect their viewpoint and trust that they know a lot more than you do.

> 多年的软件开发经验能够帮助我更好地实现 DDD 吗？可能会。然而，你的开发经验并没有教给你向领域专家聆听和学习的能力。在实施 DDD 的过程中，你最好将那些不怎么使用技术语言的人加进自己的团队，此时你得仔细地聆听他们，还应该尊重他们的观点，并且相信他们比你了解得更多。

::: tip
There Are Big Advantages to Engaging with Domain Experts

> 将领域专家引入到团队是大有好处的。

You are at a greater advantage if you can engage with those who seldom, if ever, express themselves using technical lingo. Just as you are going to learn from them, there is a high probability that they are also going to learn from you.

> 在实施 DDD 的过程中，你最好将那些不怎么使用技术语言的人加进自己的团队。就像你会向他们学习一样，他们也会向你学习。

:::

What you may like best about DDD is that the domain experts are also going to have to listen to you. You are on the team just as they are. As strange as it may seem, the domain experts don’t know everything about their business, and they are also going to learn more about it. Just as you are going to learn from them, there is a high probability that they are also going to learn from you. Your questions about what they know will most likely also uncover what they don’t know. You’ll be directly involved in helping everyone on the team discover a deeper understanding of the business, even shaping the business.

> 可能你最希望看到的便是：领域专家同样得听你的。大家都是同一个团队的成员。领域专家不见得就知道所有的业务，他们也得学习。就像你会向他们学习一样，他们也会向你学习。你向领域专家提出的问题有可能暴露出他们不知道的地方。你将直接帮组团队更好地理解业务，甚至确定业务。

It’s great when a team learns and grows together. If you give it a chance, DDD makes that possible.

> 这样一来，团队中的所有成员都在学习和成长——是 DDD 使之成为了可能。

::: tip
But We Don’t Have Domain Experts

> 但是，我们还没有领域专家

A domain expert is not one by job title. These are the people who know the line of business you are working in really well. They probably have a lot of background in the business domain, and they might be product designers or even your salespeople.

> 领域专家并不是一个职位，他可以是精通业务的任何人。他们可能了解更多的关于业务领域的背景知识，他们可能是软件产品的设计者，甚至有可能是销售员。

Look past the job title. The people you are looking for know more about what you are working on than anyone else, and for sure way more than you know. Find them. Listen. Learn. Design in code.

> 如果你发现有人比你更加了解业务知识，找到他们，聆听他们，并向他们学习。

:::

So far we’re off to a pretty reassuring start. Still, I am also not going to tell you that technical ability isn’t important, that somehow you can get by without it. You will have to grasp some advanced software domain modeling concepts. Even so, it doesn’t necessarily mean you are going to be in over your head. If you have abilities somewhere between grasping Head First Design Patterns [Freeman et al.] and grokking the original Design Patterns [Gamma et al.] text, or even more advanced patterns, you stand a really good chance of succeeding with DDD. You can bank on this: I’m going to do everything I can to make that happen by lowering the bar, no matter what your level of experience.

> 现在，我们已经开了一个好头。我并不是说技术不重要，而是说在本书中你得掌握领域建模中更高层次的概念。如果你的能力能够位于理解《Head First 设计模式》[Freeman et al]和《设计模式》[Gamma et al]之间，或者你还学了一些更高级的模式，那么你已经具备很好的 DDD 基础了。在本书中，我将尽量顾及到各个层次的学习者。

::: tip
What’s a Domain Model?

> 什么是领域模型？

It’s a software model of the very specific business domain you are working in. Often it’s implemented as an object model, where those objects have both data and behavior with literal and accurate business meaning.

> 领域模型是关于某个特定业务领域的软件模型。通常，领域模型通过对象模型来实现，这些对象同时包含了数据和行为，并且表达了准确的业务含义。

Creating a unique, carefully crafted domain model at the heart of a core, strategic application or subsystem is essential to practicing DDD. With DDD your domain models will tend to be smallish, very focused. Using DDD, you never try to model the whole business enterprise with a single, large domain model. Phew, that’s good!

:::

Consider the following perspectives of the people who can benefit from DDD. I know you fit in here somewhere:

> 不同角色的人都可以从 DDD 中获益，看看自己属于以下角色的哪一种：

- Newbie, junior developer: “I’m young, with fresh ideas, I’ve got pent-up energy to code, and I’m going to have an impact. What’s got me miffed is one of the projects I sprint on. I didn’t expect that my first gig off campus would mean shoveling data back and forth using lots of almost identical yet redundant ‘objects.’ Why is this architecture so complex if that’s all that’s happening? What’s up with that? The code breaks a lot when I try to change it. Does anyone actually understand what it’s supposed to do? Now there are some complex new features I have to add. I regularly slap an adapter around legacy classes to shield me from the goo. No joy. I’m sure there’s something I can do besides code and debug all day and night just to finish iterations. Whatever that is, I’m going to track it down and own it. I heard some of the others talking about DDD. It sounds like Gang of Four, but tuned for the domain model. Nice.”

> - 新手，初级开发者：“我还年轻，有很多点子，对写代码充满了热情。但是我所在的那个项目简直让人崩溃，我才不想一毕业就被那些重复性的工作纠来缠去。这个项目的架构为什么如此复杂？这到底是怎么呢？我修改了一点代码，却破坏了更多的代码。有人知道这本来应该是什么样子吗？现在，我还得添加一些复杂的新特性。我在遗留代码之上添加了一个适配器来屏蔽那些难看的遗留代码，但是没有用。我相信除了整天写代码和调试外，还有更好的办法。于是有人向我介绍 DDD，听说 DDD 是领域模型中的‘四人帮（Gang of Four）’，不错不错。”

Gotcha covered.

- Midlevel developer: “Over the past few months I’ve been included on the new system. It’s my turn to make a difference. I get it, but what I’m missing are profound insights when I’m meeting with the senior developers. Sometimes things seem whacked, but I’m not sure why. I’m going to help change the way things are done around here. I know that throwing technology at a problem only takes you so far, and that’s basically not far enough. What I need is a sound software development technique that’s going to help me become a wise and experienced software practitioner. One of the senior architects, the new guy, made a pitch for something called DDD. I’m listening.”

> - 中级开发者：“在过去的几个月中，我加入了一个新的项目，这次轮到我来做出改变了。那时，当我和高级开发人员在一起工作时，我发现我缺少对事物的洞察力。有时团队非常涣散，但是我又不知道其中的原因，我决定改变团队成员们的做事方式。我需要一种能够助我成功的软件开发技术。一个高级架构师向我推荐 DDD，我打算了解了解。

You’re sounding senior already. Read on. Your forward-thinking attitude will be rewarded.

> 听起来你已经是个高级开发者了，继续往下读。你超前思考的态度自然会得到回报的。

- Senior developer, architect: “I’ve used DDD on a few projects, but not since landing this new position. I like the power of the tactical patterns, but there’s a lot more I could apply, with strategic design being one. What I found most insightful when reading [Evans] was the Ubiquitous Language. That’s powerful stuff. I’ve had discussions with a number of my teammates and management, trying to influence DDD’s adoption here. One of the new kids and a few of the midlevel and senior members are jazzed about the prospects. Management isn’t so excited. I recently joined this company, and although I was brought in to lead, it seems that the organization is less interested in disruptive advancements than I thought. Whatever. I’m not giving up. With other developers psyched about it, I know we can make it happen. The payoffs are going to be much greater than anticipated. We’ll draw the pure business people—the domain experts—closer to our technical teams, and we’ll actually invest in our solutions, not just grunt them out iteration after iteration.”

> - 高级开发者，架构师：“我曾在多个项目中都使用过 DDD，不过目前所在项目还未使用。我喜欢 DDD 战术模式的威力，但是我还打算应用更多的 DDD 模式，比如战略设计等。在阅读[Evans]时，我发现通用语言的功能非常强大。我已经与团队成员和管理层讨论过采用 DDD 的事情了，但其中有些中高级开发者对 DDD 在项目中的前景并不看好，而管理层也不是那么热衷于 DDD。我是最近才加入公司的，虽然我是团队带头人，但是整个团队似乎并不愿意被一些新奇玩意儿打断了开发进度。不管如何，我是不会放弃的。虽然其他开发者对 DDD 没有信心，但是我是能做到的。我决定将领域专家引入到团队中来，使他们跟技术人员一起工作。”

Now that’s what a leader does. This book has lots of guidance that shows how to succeed with strategic design.

> 这就是一个领导应该做的。本书包含了很多关于战略设计的例子。

- Domain expert: “I’ve been involved in specifying the IT solutions to our business challenges for a long time now. Maybe it’s too much to expect, but I wish the developers understood better what we do here. They’re always talking down to us like we’re stupid. What they don’t understand is, if it wasn’t for us there wouldn’t be jobs here for them to mess around with computers. The developers always have some strange way of talking about what our software does. If we talk about A, they say it’s really called B. It’s like we have to have some sort of dictionary and road map on hand every time we try to communicate what we need. If we don’t let them have their way by calling B what we know is A, they don’t cooperate. We waste so much time in this mode. Why can’t the software just work the way the real experts think about the business?”

> - 领域专家：“我已经在 IT 部门帮他们解决业务问题好长一段时间了，我希望开发者们能够更好地理解他们所做的事情。他们总是认为我们业务人员是愚蠢的。但是他们不知道的是，如果不是我们，他们早就丢了工作。开发者总会以一些奇怪的方式来讨论我们的软件，如果我说这是 A，他们却说这是 B，好像我们需要有本词典才能交流一样。如果我们试图纠正他们的错误叫法，他们就不愿意合作了。我们在这上面浪费了太多的时间。软件为什么不能像真正的业务专家所想象的那样工作呢？”你说对了。软件开发的最大问题之一便是业务人员和技术人员需要某种翻译才能交流。本章将对此做出讨论。你将看到，DDD 将业务人员和技术人员放在同一个层面上。惊讶吧，你已经使一些开发者向你靠近了，多帮帮他们。

You’ve got that right. One of the biggest problems is the false need for translation between business people and techies. This chapter is for you. As you’re going to see, DDD puts you and developers on level ground.

And, surprise! You’ve got some developers already leaning your way. Help them here.

- Manager: “We are shipping software. It’s not always with the greatest result, and changes seem to take longer than they should. The developers keep talking about some domain something-or-another. I’m not sure we need to get high centered on yet another technique or methodology, like it’s some kind of silver bullet. I’ve heard all that a thousand times before. We try, the fad dies, and we are right back to the same-old same-old. I keep saying that we need to stay the course and stop dreaming, but the team keeps hounding me. They’ve worked hard, so I owe them a listen. They are smart people and they all deserve a chance to improve things before they get torqued and move on. I could allow them some time to learn and adjust if I can get backing from upper management. I think I could get that approval if I can convince my boss of the team’s claims of achieving critical software investment and a centralization of business knowledge. Truth is, it will make my job easier if I can do something to inspire trust and cooperation between my teams and business experts. Anyway, that’s what I am hearing I can do.”

> - 项目经理：“我们要交付软件，但结果并不总是让人舒心，有时开发时间拖得太长了。开发者在谈论到领域时总是各执一词，莫衷一是。我不确定我们是否需要另一种银弹般的技术或者方法。之前我们不是没有尝试过，但是每次都失败了，结果还是得回到原来的位置。我总是说，我们应该放弃幻想，准备战斗，但是团队成员并不这么认为。他们工作非常努力，我总觉得欠他们些什么，于是听听他们的意见吧。他们都是聪明之人，并且都希望做出些改变。对于我来说，如果我上面的管理层同意，我是完全允许开发者们花时间学习的。团队成员们希望有个集中化的业务知识体系，我想我可以以此说服我的老板。这样一来，我自己的工作也将变得简单，我还可以促进团队和业务专家之间的合作与互信。”

Good manager!

> 多好的项目经理啊！

Whoever you are, here’s an important heads-up. To succeed with DDD you are going to have to learn something, and actually a lot of somethings. That shouldn’t be a big deal, though. You are smart and you have to learn all the time. Yet we all face this challenge:

> 不管你是谁，有一点是重要的：要在 DDD 之路上取得成功，你肯定得学习，并且大量地学习。学习不是什么问题，你是聪明的，并且一直都在学习。然而，我们都面临这样一种困境：

Personally I’m always ready to learn, although I do not always like being taught.

> 就个人来讲，我时刻都在准备着学习，但是我并不喜欢被人教。

——Sir Winston Churchill

That’s where this book comes in. I’ve tried to make the teaching as pleasant as possible while delivering the vital understanding you need to implement DDD with success.

> 在本书中，我会尽量将知识传递变成一件愉悦之事，并且保证你在 DDD 上有所收获。

Your question, though, is: “Why should I do DDD?” That’s fair.

> 你可能又有问题了：“为什么我们需要 DDD 呢？”

## 1.2 WHY YOU SHOULD DO DDD 为什么我们需要 DDD

Actually, I’ve already given you some pretty good reasons why DDD makes so much practical sense. At the risk of breaking the DRY principle (“Don’t repeat yourself”), I reiterate them here and also add to the earlier reasons. Does anyone hear an echo?

> 事实上，在前面我已经提到了一些应该采用 DDD 的原因。冒着有悖 DRY 原则（Don’t repeat yourself，不要做重复的事情）的风险，我重新说说我们需要采用 DDD 的原因。

- Put domain experts and developers on a level playing field, which produces software that makes perfect sense to the business, not just the coders. This doesn’t mean merely tolerating the opposite group. It means becoming one cohesive, tight-knit team.
- That “makes sense to the business” thing means investing in the business by making software that is as close as possible to what the business leaders and experts would create if they were the coders.
- You can actually teach the business more about itself. No domain expert, no C-level manager, no one, ever knows every single thing about the business. It’s a constant discovery process that becomes more insightful over time. With DDD, everybody learns because everybody contributes to discovery discussions.
- Centralizing knowledge is key, because with that the business is capable of ensuring that understanding the software is not locked in “tribal knowledge,” available only to a select few, who are usually only the developers.
- There are zero translations between the domain experts, the software developers, and the software. That doesn’t mean maybe some few translations. It means zero translations because your team develops a common, shared language that everyone on the team speaks.
- The design is the code, and the code is the design. The design is how it works. Knowing the best code design comes through quick experimental models using an agile discovery process.
- DDD provides sound software development techniques that address both strategic and tactical design. Strategic design helps us understand what are the most important software investments to make, what existing software assets to leverage in order to get there fastest and safest, and who must be involved. Tactical design helps us craft the single elegant model of a solution using time-tested, proven software building blocks.

---

> - 使领域专家和开发者在一起工作，这样开发出来的软件能够准确地传达业务规则。当然，对于领域专家和开发者来说，这并不表示单单地包容对方，而是将他们组成一个密切协作的团队。
> - “准确传达业务规则”的意思是说，此时的软件就像如果领域专家是编码人员时所开发出来的一样。
> - 可以帮助业务人员自我提高。没有任何一个领域专家或者管理者敢说他对业务已经了如指掌了，业务知识也需要一个长期的学习过程。在 DDD 中，每个人都在学习，同时每个人又是知识的贡献者。
> - 关键在于对知识的集中，因为这样可以确保软件知识并不只是掌握在少数人手中。
> - 在领域专家、开发者和软件本身之间不存在“翻译”，意思是当大家都使用相同的语言进行交流时，每人都能听懂他人所说。
> - 设计就是代码，代码就是设计。设计是关于软件如何工作的，最好的编码设计来自于多次试验，这得益于敏捷的发现过程。
> - DDD 同时提供了战略设计和战术设计两种方式。战略设计帮助我们理解哪些投入是最重要的；哪些既有软件资产是可以重新拿来使用的；哪些人应该被加到团队中？战术设计则帮助我们创建 DDD 模型中各个部件。

Like any good, high-yielding investment, DDD has some up-front cost of time and effort for the team. Considering the typical challenges encountered by every software development effort will reinforce the need to invest in a sound software development approach.

> 就像其他高回报率的投入一样，DDD 需要我们在时间和精力上都有所投入。但是，考虑到我们在开发软件的过程中经常遇到的各种问题和挑战，这样的投入是值得的。

### 1.2.1 Delivering Business Value Can Be Elusive 难以捉摸的业务价值

Developing software that delivers true business value is not the same thing as developing ordinary business software. Software that delivers true business value aligns with the business strategic initiatives and bears solutions with clearly identifiable competitive advantage—software that is not about technology, but about the business.

> 开发能够传递真正业务价值的软件和开发普通的软件是不同的。具有真正业务价值的软件能够很好地符合业务战略，并且可以将竞争优势融合到解决方案中。此时的软件并不是关于技术的，而是关于业务的。

Business knowledge is never centralized. Development teams have to balance and prioritize among the needs and requests of multiple stakeholders and engage with many people having diverse skill sets, all with the goal of uncovering software functional and nonfunctional requirements. After gathering all that information, how can teams be certain that any given requirement delivers true business value? In fact, what are the business values being sought, and how do you uncover them, prioritize them, and realize them?

> 业务知识从来就没有被集中过。开发团队必须在多方之间权衡各种需求，并确定其中的优先级。同时，团队成员的技能也是良莠不齐的。在获得所有的信息之后，团队所面临的问题在于：如何确定某种需求确实能够传递真正的业务价值？还有，我们如何去发现并暴露出这些业务价值，如何安排它们之间的优先级，并且如何实现它们？

One of the worst disconnects of a business software development effort is seen in the gap between domain experts and software developers. Generally speaking, true domain experts are focused on delivering business value. On the other hand, software developers are typically drawn to technology and technical solutions to business problems. It’s not that software developers have wrong motivations; it’s just what tends to grab their attention. Even when software developers engage with domain experts, the collaboration is largely at a surface level, and the software that gets developed often results in a translation/mapping between how the business thinks and operates and how the software developer interprets that. The resulting software generally does not reflect a recognizable realization of the mental model of the domain experts, or perhaps it does so only partially. Over time this disconnect becomes costly. The translation of domain knowledge into software is lost as developers transition to other projects or leave the company.

> 在开发过程中，最大的鸿沟之一便存在于领域专家和开发者之间。通常来说，领域专家将关注点放在交付业务价值上，而开发者则将注意力放在技术实现上。当然，并不是说开发者的动机是错误的，而是说开发者的眼光被自然而然地吸引到了实现层面上。即便让领域专家和开发者一同工作，他们之间的协作也只是表面的，这时在所开发的软件中便产生了一种映射：将业务人员所想的映射到开发者所理解的。这样一来，软件便不能完全反映出领域专家的思维模型。随着时间的推移，这种鸿沟将增加软件的开发成本。而随着开发者转到其他项目或者离职，本应该驻留在软件中的领域知识也就丢失了。

A different, yet related problem is when one or more domain experts do not agree with each other. This tends to happen because each expert has more or less experience in the specific domain being modeled, or they are simply experts in related but different areas. It’s also common for multiple “domain experts” to have no expertise in a given domain, where they are more of a business analyst, yet they are expected to bring insightful direction to discussions. When this situation goes unchecked, it results in blurred rather than crisp mental models, which lead to conflicting software models.

> 另一个问题发生在当多个领域专家之间存在分歧的时候。这是很有可能发生的，因为每个专家只是熟悉某个或者某些特定的领域。另外，在某个领域里找不到真正的专家也是可能的，此时，有人可能对该领域有所了解，但是他更像一个业务分析员。这些问题将导致相互矛盾的软件模型。

Worse still is when the technical approach to software development actually wrongly changes the way the business functions. While a different scenario, it is well known that enterprise resource planning (ERP) software will often change the overall business operations of an organization to fit the way the ERP functions. The total cost of owning the ERP cannot be fully calculated in terms of license and maintenance fees. The reorganization and disruption to the business can be far more costly than either of those two tangible factors. A similar dynamic is at play as your software development teams interpret what the business needs into what the newly developed software actually does. This can be both costly and disruptive to the business, its customers, and its partners. Furthermore, this technical interpretation is both unnecessary and avoidable with the use of proven software development techniques. The solution is a key investment.

> 更糟的是，软件的技术实现可能错误地改变软件的业务规则。比如，ERP 软件通常需要修改业务操作以满足某个特定用户的需求，因此 ERP 的成本不能单以使用许可和维护费用来计算，对业务规则的修改所产生的成本远远大于前两者。另外一个相似的例子是当开发团队将业务需求翻译成软件功能的时候。这对于业务、用户和合作方来说都是一笔很大的成本。还有，技术上的翻译和解释是没有必要的，并且在使用适当开发方式的情况下是可以避免的。解决方案才是主要的投入。

### 1.2.2 How DDD Helps DDD 如何帮助我们

DDD is an approach to developing software that focuses on these three primary aspects:

> DDD 作为一种软件开发方法，它主要关注以下三个方面：

1. DDD brings domain experts and software developers together in order to develop software that reflects the mental model of the business experts. This does not mean that effort is spent on modeling the “real world.” Rather, DDD delivers a model that is the most useful to the business. Sometimes useful and realistic models happen to intersect, but to the degree that they diverge, DDD chooses useful.

> 1. DDD 将领域专家和开发人员聚集到一起，这样所开发的软件能够反映出领域专家的思维模型。这并不意味这我们将精力都花在了对“真实世界”的建模上，而是交付最具业务价值的软件。有时在实用和理想之间存在冲突，根据它们的互异程度，在 DDD 中我们将选择实用性。

With this aspect the efforts of domain experts and software developers are devoted to jointly developing a Ubiquitous Language of the areas of the business that they are focused on modeling. The Ubiquitous Language is developed with full team agreement, is spoken, and is directly captured in the model of the software. It is worth reiterating that the team is composed of both domain experts and software developers. It’s never “us and them.” It’s always us. This is a key business value that allows business know-how to outlive the relatively short initial development efforts that deliver the first few versions of the software, and the teams that produce it. It’s the point where the cost of developing software is a justifiable business investment, not just a cost center.

> 领域专家将和开发人员一起创建一套适用于领域建模的通用语言。通用语言必须在全队范围之内达成一致；所有成员都使用通用语言进行交流，通用语言也是对软件模型的直接反映。请注意，虽然团队中同时包含领域专家和开发人员，但并不是“我们”和“他们”的关系，团队中只有“我们”的概念。

This entire effort unifies domain experts who initially disagree with each other, or who simply lack core knowledge of the domain. Further, it strengthens the close-knit team by spreading deep domain insight among all team members, including software developers. Consider this the hands-on training that every company should invest in its knowledge workers.

> 通用语言也有助于促使原本存在分歧的领域专家们达成一致意见。此外，通过将领域知识传达给所有的团队成员，包括开发人员，整个团队也将更具凝聚力。我们甚至可以认为，这是每个公司都应该有的对于知识型工作者的起码训练。

2. DDD addresses the strategic initiatives of the business. While this strategic design approach naturally includes technical analysis, it is more concerned with the strategic direction of the business. It helps define the best inter-team organizational relationships and provides early-warning systems for recognizing when a given relationship could cause software and even project failure. The technical aspects of strategic design have the goal of cleanly bounding systems and business concerns, which protects each business-level service. This provides meaningful motivations for how an overall service-oriented architecture or business-driven architecture is achieved.

> 2. DDD 关注业务战略。虽然说战略（Strategic）设计自然地包含了战术设计，但是战略设计关注更多的则是业务的战略方向。它帮助我们定义不同团队之间的组织关系，并在这些关系有可能导致项目失败的时候提供早期预警。DDD 的战略设计用于清楚地界分不同的系统和业务关注点，这样可以保护每个业务层面的服务。更进一步，这将指引我们如何实现面向服务架构（serviceoriented architecture）或者业务驱动（business-driven architecture）架构。

3. DDD meets the real technical demands of the software by using tactical design modeling tools to analyze and develop the executable software deliverables. These tactical design tools allow developers to produce software that is a correct codification of the domain experts’ mental model, is highly testable, is less error prone (a provable statement), performs to service-level agreements (SLAs), is scalable, and allows for distributed computing. DDD best practices generally address a dozen or more higher-level architectural and lower-level software design concerns, with a focus on recognizing true business rules and data invariants, and protecting the rules from error situations.

> 3. 通过使用战术设计建模工具，DDD 满足了软件真正的技术需求。这些战术设计工具使开发人员能够按照领域专家的思维模型开发软件。同时，所开发出来的软件是可测试的，能够尽量避免错误，能执行服务层面协议（Service-LevelAgreement，SLA），具有很好的伸缩性，并且允许分布式计算。DDD 的最佳实践同时包含了高层的架构性实践和底层设计实践，关注业务规则和数据不变性，并且可以对业务规则起到保护作用。

Using this approach to software development, you and your team can succeed in delivering true business value.

> 通过这种方式开发软件，你和你的团队将能成功地交付真正的业务价值。

### 1.2.3 Grappling with the Complexity of Your Domain 处理领域复杂性

We primarily want to use DDD in the areas that are most important to the business. You don’t invest in what can be easily replaced. You invest in the nontrivial, the more complex stuff, the most valuable and important stuff that promises to return the greatest dividends. That’s why we call such a model a Core Domain (2). It is these, and in second priority the significant Supporting Subdomains (2), that deserve and get the biggest investment. Rightly, then, we need to grasp what complex means.

> 在使用 DDD 时，我们首先希望将它应用在最重要的业务场景下。对于那些可以轻易替换的软件来说，你是不会有所投入的。相反，值得你投入的是那些重要的、复杂的东西，因为这些东西将为你带来可观的回报。正因如此，我们将这样的模型命名为核心域（Core Domain，2），而那些相对次要的称为支撑子域（SupportingSubdomain，2）。那么现在，我们需要搞明白的是，“复杂”到底是什么意思？

::: tip
Use DDD to Simplify, Not to Complicate

> DDD 的作用是简化，而不是复杂化

Use DDD to model a complex domain in the simplest possible way. Never use DDD to make your solution more complex.

> 在使用 DDD 时，我们应该采用最简单的方式对复杂领域进行建模，而不是使问题变得更加复杂。

:::

What qualifies as complex will differ from business to business. Different companies have different challenges, different levels of maturity, and different software development capabilities. So rather than determining what is complex, it may be easier to determine what is nontrivial. Thus, your team and management will have to determine if a system you are planning to work on deserves the cost of making a DDD investment.

> 不同的业务领域对于复杂的定义是不一样的。另外，不同的公司所面临的挑战不一样；成熟度不一样；软件开发能力也不一样。因此，与其去定义什么是复杂的，还不如定义什么是重要的。这时，你的团队和管理层应该做出决定：你们开发的软件系统是否值得做出 DDD 投入。

DDD Scorecard: Use Table 1.1 to determine whether your project qualifies for an investment in DDD. If a row on the scorecard describes your project, place the corresponding number of points in the right-hand column. Tally all the points for your project. If it’s 7 or higher, seriously consider using DDD.

> DDD 计分卡：使用表 1.1 来决定你的项目是否值得做出 DDD 投入。如果你的项目情况在某行的描述范围之内，那么请在右边的列中记上相应的分数，最后将这些分数相加得到总分。如果得分为 7 分或者以上，那么，你应该考虑使用 DDD 了。

Table 1.1. The DDD Scorecard

![](./figures/ch1/t1-1.jpg)

![](./figures/ch1/t1-1b.jpg)

This scoring exercise may have led your team to these conclusions:

> 通过对以上 DDD 计分卡打分，我们可以得出以下结论：

It’s too bad that we can’t shift gears quickly and easily when we discover we are on the wrong side of complexity, no matter if the wrong side is more or less complex than we thought.

> 当我们在复杂性问题上犯错时，我们很难轻易地扭转颓势。

Sure, but that just means that we need to become much better at determining simplicity versus complexity early on in our project planning. That would save us a lot of time, expense, and trouble.

> 这意味着我们应该在项目计划早期便对简单性和复杂性做出判断，这将为我们节约很多时间和开销，并免除很多麻烦。

Once we make a major architectural decision and get several use cases deep in development, we are usually stuck with it. We had better choose wisely.

> 一旦我们做出了重要的架构决策，并且已经在该架构下进行了深入地开发，通常我们也被绑定在这个架构下了，所以在决定时一定要慎重。

If any of these observations resonates with your team, you are making good use of critical thought.

> 如果你对以上几点产生了共鸣，表明你已经在认真地思考问题了。

### 1.2.4 Anemia and Memory Loss

Anemia can be a serious health ailment with dangerous side effects. When the name Anemic Domain Model [Fowler, Anemic] was first coined, it wasn’t meant to be a complimentary term, as if to say that a domain model that is weak, without the power of inherent behavioral qualities, could possibly be a good thing. Strangely enough, Anemic Domain Models have popped up left and right in our industry. The trouble is that most developers seem to think this is quite normal and would not even acknowledge that a serious condition exists when employed in their systems. It’s a real problem.

> 贫血症严重危害着人类健康，并且伴随有危险的副作用。当贫血领域对象（Anemic Domain Object）[Fowler，Anemic]被首次提出来时，它并不是一个博得赞美的词汇，它描述的是一个缺少内在行为的领域对象。奇怪的是，人们对于贫血领域对象的态度褒贬不一。问题在于，多数开发者认为这样的领域对象是正常的，他们并没有意识到这是一个严重的问题。

Are you wondering if your model is feeling tired, listless, forgetful, clumsy, needing a good shot in the arm? If you’re suddenly experiencing technical hypochondria, here’s a good way to perform a self-examination. You’ll either put yourself at ease or confirm your worst fears. Use the steps in Table 1.2 to perform your checkup.

> 你是否想知道你所建模型的健康状况呢？如果你突然患上了技术上的“忧郁症”，这里你可以做个自我检查。你可能心情愉悦，也可能无比恐惧。通过表 1.2 中的步骤开始检查吧。

Table 1.2. Determine Your Domain Model Health History

![](./figures/ch1/t1-2.jpg)

How did you do?

If you answered “No” to both questions, your domain is doing well.

> 如果你对以上两个问题的回答都是“No”，表明你的领域对象是健康的。

If you answered “Yes” to both questions, your “domain model” is very, very ill. It’s anemic. The good news is that you can get help for it by reading on.

> 如果都是“Yes”，表明你的领域对象已经病得不轻了，这便是贫血对象。好消息是，你是可以获得帮助的，继续往下读吧。

If you answered “Yes” to one question and “No” to the other question, you are either in denial or suffering from delusions or another neurological issue that could be caused by anemia. What should you do if you have conflicting answers? Go straight back to the first question and run the self-examination once again. Take your time, but remember that your answer to both questions must be an emphatic “Yes!”

> 如果你对其中一个回答“Yes”，而另一个回答“No”，你可能是在自欺或者患上了由贫血症导致的神经系统紊乱，此时你应该怎么办呢？回到第一个问题重新来一遍，不要着急，要确保对两个问题都回答“Yes”。

As [Fowler, Anemic] says, an Anemic Domain Model is a bad thing because you pay most of the high cost of developing a domain model, but you get little or none of the benefit. For example, because of the object-relational impedance mismatch, developers of such a “domain model” spend a lot of time and effort mapping objects to and from the persistence store. That’s a high price to pay while getting little or no benefit in return. I’ll add that what you have is not a domain model at all, but just a data model projected from a relational model (or other database) into objects. It’s an impostor that may actually be closer to the definition of Active Record [Fowler, P of EAA]. You can probably simplify your architecture by not being pretentious and just admit that you are really using a form of Transaction Script [Fowler, P of EAA].

> 正如[Fowler，Anemic]所说，贫血领域对象是不好的，因为你花了很大的成本来开发领域对象，但是从中却获益甚少。比如，由于存在对象-关系阻抗失配（Object-Relational Impedance），开发者需要将很多时间花在对象和数据存储之间的映射上。这样的代价太大，而收益太小。我得说，你所说的领域对象根本就不是领域对象，而只是将关系型数据库中的模型映射到了对象上而已。这样的领域对象更像是活动记录（Active Record）[Fowler，P of EAA]，此时你可以对架构做个简化，然后使用事务脚本（Transaction Script）[Fowler，P of EAA]进行开发。

Reasons Why Anemia Happens 为什么会有贫血领域对象

So if an Anemic Domain Model is the sickly outcome of a poorly executed design effort, why do so many use it while thinking that their model is experiencing fine health? Certainly it does reflect a procedural programming mentality, but I don’t think that’s the primary reason. A good portion of our industry is made up of sample code followers, which isn’t bad as long as the samples are quality ones. Often, however, sample code is purposely focused on demonstrating some concept or application programming interface (API) feature in the simplest possible way, without concern for good design principles. Yet oversimplified sample code, which usually demonstrates with a lot of getters and setters, is copied every day without a second thought about design.

> 如果说贫血领域对象是由设计不当造成的，为什么还有如此多的人认为他们的领域对象是健康的呢？其中一个原因是：贫血领域对象反映了一种自然的过程式的编程风格，但我并不认为这是首要原因。软件业中有很多开发者都是学着示例代码做开发的，这并不是什么坏事，只要示例代码本身是好的。然而，通常情况是，示例代码只是用尽可能简单的方式来展示某个特定的概念或者 API 特性，而并不强调要遵循多好的设计原则。一些极度简化的示例代码总是包含了大量的 getter 和 setter，于是这些 getter 和 setter 随着示例代码每天被程序员们原封不动地来回复制。

There is another, older influence. The ancient history of Microsoft’s Visual Basic had much to do with where we are today. I’m not saying that Visual Basic was a bad language and integrated development environment (IDE), because it’s always been a highly productive environment and in some ways influenced the industry for the good. Of course, some may have avoided its direct influence altogether, but Visual Basic indirectly caught up with just about every software developer eventually. Just note the timeline shown in Table 1.3.

> 还有历史的影响。Microsoft 的 Visual Basic 对我们现在的软件开发产生了很大的影响。我并不是说 Visual Basic 是门不好的语言和集成开发环境（IDE），因为它的确是种高效的开发方式，并且在某些方面对软件开发产生过正面的影响。当然，有些人可能会拒绝 Visual Basic 的直接影响，但是最终它却间接地影响着每一个程序员。请注意表 1.3 中的时间线。

Table 1.3. The Timeline from Behavior Rich to Infamous Anemia

![](./figures/ch1/t1-3.jpg)

What I am talking about is the influence of properties and property sheets, both backed by property getters and setters that were made so popular by the original Visual Basic forms designer. All you had to do was place a few custom control instances on a form, fill out their property sheets, and voilà! You had a fully functioning Windows application. It took just a few minutes to do that compared to the few days required to program a similar application directly against the Windows API using C.

> 这里，我想谈及的是对象属性和属性列表带来的影响。对象属性和属性列表都得益于 getter 和 setter 的支持，而 Visual Basic 的窗体设计器将 getter 和 setter 变得过于流行了。你需要做的只是将自定义控件拖到窗体上，然后编辑控件的属性列表，大功告成，一个功能完备的窗体程序开发完毕。如果直接采用 C 语言的 Windows API 来开发相同的窗体，可能需要几天时间，而采用 Visual Basic 只是几分钟的事情。

So what does all that have to do with Anemic Domain Models? The Java Bean standard was originally specified to assist in the creation of visual programming tools for Java. Its motivation was to bring the Microsoft ActiveX capabilities to the Java platform. It offered the hope of creating a market full of third-party custom controls of various kinds, just like Visual Basic’s. Soon almost every framework and library jumped on the JavaBean bandwagon. This included much of the Java SDK/JDK as well as libraries such as the popular Hibernate. Specific to our DDD concerns, Hibernate was introduced to persist domain models. The trend continued as the .NET platform reached us.

> 那这和贫血领域对象有什么关系呢？JavaBean 标准最早是用来辅助 Java 的可视化设计工具的，旨在将 Microsoft 的 Active X 开发方式带到 Java 平台。Java 此举希望开创一个第三方自定义控件市场，就像 Visual Basic 一样。此后不久，几乎所有的框架和类库都涌入到了 JavaBean 潮流中，其中包括 Java 本身的 SDK/JDK 和第三方类库，比如 Hibernate。在.NET 平台推出之后，这样的趋势还在继续。

Interestingly, any domain model that was persisted using Hibernate in the early days had to expose public getters and setters for every persistent simple attribute and complex association in every domain object. This meant that even if you wanted to design your POJO (Plain Old Java Object) with a behavior-rich interface, you had to expose your internals publicly so that Hibernate could persist and reconstitute your domain objects. Sure, you could do things to hide the public JavaBean interface, but by and large most developers didn’t bother or even understand why they should have.

> 有趣的是，在早期的 Hibernate 版本中，所有需要持久化的领域对象都必须暴露公有的 getter 和 setter，不管是对于简单类型的属性，还是对复杂类型皆如此。这意味着，即便你希望将自己的 POJO（Plain Old Java Object）设计成富含行为的对象，你都必须将对象的内部暴露给 Hibernate 以保存或重建对象。诚然，你可以隐藏公有的 JavaBean 接口，但是多数开发者都懒得这样做，或者甚至都不知道为什么应该这么做。

::: tip
Should I Be Concerned about Using Object-Relational Mappers with DDD?

> 我应该考虑在 DDD 中使用对象-关系映射（Object-Relational Mapping，ORM）吗？

The preceding critique of Hibernate is from a historical perspective. For quite a while now Hibernate has supported the use of hidden getters and setters, and even direct field access. I demonstrate in later chapters how to avoid anemia in your models when using Hibernate and other persistence mechanisms. So, don’t sweat it.

> 前面主要是从历史的角度对 Hibernate 进行了批评。现在，Hibernate 已经不需要对象暴露 getter 和 setter 了，它甚至可以对对象属性进行直接操作。我将在后面的章节中讲到在使用 Hibernate 或其他持久化机制时如何避免贫血对象。

:::

Most, if not all, of the Web frameworks also function solely on the JavaBean standard. If you want your Java objects to be able to populate your Web pages, the Java objects had better support the JavaBean specification. If you want your HTML forms to populate a Java object when submitted to the server side, your Java form object had better support the JavaBean specification.

> 此外，多数的 Web 框架依然只支持 JavaBean 规范。如果你想将一个 Java 对象显示在网页上，该 Java 对象最好是支持 JavaBean 规范的。如果你想将 HTML 表单中的数据传到一个 Java 对象中，该 Java 对象也最好是支持 JavaBean 规范的。

Just about every framework on the market today requires, and therefore promotes, the use of public properties on simple objects. Most developers can’t help but be influenced by all the anemic classes all over their enterprises. Admit it. You’ve been bitten by it, haven’t you? As a result, we have a situation that might be best labeled anemia everywhere.

> 市场上的几乎每种框架都要求对象暴露公有属性。这样一来，多数开发者只能被动地接受那些贫血对象。于是我们便到了“到处都是贫血对象”的地步。

Look at What Anemia Does to Your Model 看看贫血对象都对你的模型做了些什么

All right, so let’s say we can agree that this is both true and vexing to us. What does anemia everywhere have to do with memory loss? When you are reading through the client code of an Anemic Domain Model (for example, the impostor Application Service (4, 14), à la Transaction Script), what do we usually see? Here’s a rudimentary example:

> 好吧，我们同意这已经是烦人的即成事实。但是这些无处不在的贫血对象和失忆症又有什么关系呢？当你在阅读一个贫血领域对象的示例代码时，比如应用服务（4，14）中的事务脚本，你通常会看到类似如下的代码片段：

```java
@Transactional
public void saveCustomer(
    String customerId,
    String customerFirstName, String customerLastName,
    String streetAddress1, String streetAddress2,
    String city, String stateOrProvince,
    String postalCode, String country,
    String homePhone, String mobilePhone,
    String primaryEmailAddress, String secondaryEmailAddress) {
    Customer customer = customerDao.readCustomer(customerId);
    if (customer == null) {
        customer = new Customer();
        customer.setCustomerId(customerId);
    }
    customer.setCustomerFirstName(customerFirstName);
    customer.setCustomerLastName(customerLastName);
    customer.setStreetAddress1(streetAddress1);
    customer.setStreetAddress2(streetAddress2);
    customer.setCity(city);
    customer.setStateOrProvince(stateOrProvince);
    customer.setPostalCode(postalCode);
    customer.setCountry(country);
    customer.setHomePhone(homePhone);
    customer.setMobilePhone(mobilePhone);
    customer.setPrimaryEmailAddress(primaryEmailAddress);
    customer.setSecondaryEmailAddress (secondaryEmailAddress);
    customerDao.saveCustomer(customer);
}
```

::: tip
Example Purposely Kept Simple

> 刻意保持例子的简单

Admittedly, this example is not from a very interesting domain, but it does help us examine a less-than-ideal design and determine how we can refactor it to a much better one. Let’s be clear that this exercise is not leading us to a cooler way to save data. It’s about crafting a software model that adds value to your business, even though this example may not seem valuable.

> 必须得承认，以上代码并不表示一个有趣的领域，但是却帮助我们看到了一个欠妥的设计，我们可以将其重构成更好的模型。这里我们关注的并不是如何保存 Customer 数据，而是如何向模型中添加业务价值，即便就这个例子本身来说意义并不大。

:::

What did this code just do? Actually it’s pretty versatile code. It saves a Customer no matter whether it is new or preexisting. It saves a Customer no matter whether the last name changed or the person moved to a new home. It saves a Customer no matter whether the person got a new home phone number or discontinued home phone service, or whether he or she got a mobile phone for the first time, or both. It even saves a Customer who switched from using Juno to using Gmail instead, or who changed jobs and now has a new work e-mail address. Wow, this is an awesome method!

> 以上代码完成了什么功能呢？事实上，以上代码的功能是相当强大的。不管一个 Customer 是新建的还是先前存在的；不管是 Customer 的名字变了还是他搬进了新家；不管是他的家用电话号码变了还是他有了新的移动电话；也不管他是改用 Gmail 还是有了新的 E-mail 地址，这段代码都会保存这个 Customer。哇，好厉害的方法啊！

Or is it? Actually, we have no idea under what business situations this saveCustomer() method is used—not exactly, anyway. Why was this method created in the first place? Does anyone remember its original intent, and all the motivations for changing it to support a wide variety of business goals? Those memories were quite likely lost only a few weeks or months after the method was created and then modified. And it gets even worse. You don’t believe me? Look at the next version of this same method:

> 情况真是这样的吗？其实，我们并不知道 saveCustomer（）方法的业务场景。为什么一开始会创建这个方法？有人知道它的本来意图吗，还是它原本就是用来满足不同业务需求的？几周或几个月之后，我们便将这些忘得一干二净了。你不相信？那请看看该方法的下一个版本：

```java
@Transactional
public void saveCustomer(
    String customerId,
    String customerFirstName, String customerLastName,
    String streetAddress1, String streetAddress2,
    String city, String stateOrProvince,
    String postalCode, String country,
    String homePhone, String mobilePhone,
    String primaryEmailAddress, String secondaryEmailAddress) {
    Customer customer = customerDao.readCustomer(customerId);
    if (customer == null) {
        customer = new Customer();
        customer.setCustomerId(customerId);
    }
    if (customerFirstName != null) {
        customer.setCustomerFirstName(customerFirstName);
    }
    if (customerLastName != null) {
        customer.setCustomerLastName(customerLastName);
    }
    if (streetAddress1 != null) {
        customer.setStreetAddress1(streetAddress1);
    }
    if (streetAddress2 != null) {
        customer.setStreetAddress2(streetAddress2);
    }
    if (city != null) {
        customer.setCity(city);
    }
    if (stateOrProvince != null) {
        customer.setStateOrProvince(stateOrProvince);
    }
    if (postalCode != null) {
        customer.setPostalCode(postalCode);
    }
    if (country != null) {
        customer.setCountry(country);
    }
    if (homePhone != null) {
        customer.setHomePhone(homePhone);
    }
    if (mobilePhone != null) {
        customer.setMobilePhone(mobilePhone);
    }
    if (primaryEmailAddress != null) {
        customer.setPrimaryEmailAddress(primaryEmailAddress);
    }
    if (secondaryEmailAddress != null) {
        customer.setSecondaryEmailAddress (secondaryEmailAddress);
    }
    customerDao.saveCustomer(customer);
}
```

I have to note here that this example isn’t as bad as it gets. Many times the data-mapping code becomes quite complex, and a lot of business logic gets tucked away in it. I’m sparing you the worst in this example, but you’ve probably seen it for yourself.

> 我得说，以上方法还算不上糟糕到了极点。很多时候数据-映射（datamapping）代码将变得非常复杂，此时大量的业务逻辑便不能反映在代码里了。

Now each of the parameters other than the customerId is optional. We can now use this method to save a Customer under at least a dozen business situations, and more! But is that really a good thing? How could we actually test this method to ensure that it doesn’t save a Customer under the wrong situations?

> 现在，除了 customerId 之外，所有的参数都是可选的，我们至少可以在某些业务场景下使用该方法。但是，我们就能说这是好的代码吗？我们如何测试这段代码以保证在错误的业务场景下该段代码不应该保存一个 Customer 呢？

Without going into extensive detail, this method could function incorrectly in more ways than it could correctly. Perhaps there are database constraints that prevent a completely invalid state from being persisted, but now you have to look at the database to be sure. Almost certainly it will take you some time to mentally map between Java attributes and column names. Once you’ve figured out that part, you find that the database constraints are missing or incomplete.

> 都不用讨论过多的细节我们便知道，在很多情况下该方法是不能正常工作的。可能数据库约束会防止对非法状态的保存，但你是不是又得去查看数据库啦？你会在 Java 对象属性和数据库表的列名之间辗转反侧，然后可能发现你缺少数据库约束或者约束并不完全。

You could look at the possibly many clients (not counting those added after the user interface was completed to manage automatic remote clients) and compare source revisions to gain some insight into why it is implemented the way it is right now. As you search for answers, you learn that nobody can explain why this one method works the way it does, or how many correct uses there are. It could take several hours or days to understand it on your own.

> 你可能会查看很多客户代码，然后比较代码历史，找出 saveCustomer（）的来龙去脉。你会发现，没有人能够解释这个方法为什么会成为现在这个样子，也没有人知道究竟有多少客户代码在正确地使用 saveCustomer（）方法。要自己去搞明白这里面的缘由，你得花上几个小时甚至几天的时间。

Cowboy Logic 牛仔的逻辑

AJ: “That fella’s so confused, he doesn’t know if he’s sackin’ potatoes or rollerskatin’ in a buffalo herd.”

> AJ：“这哥们儿疑惑了，他不知道是应该吃土豆呢，还是吃牛肉？”

![](./figures/ch1/cowboy_logic_aj_talks.jpg)

Domain experts can’t help here because they would have to be programmers to understand the code. Even if a domain expert or two knew enough about programming or could at least read the code, they would probably be at least equally at a loss as a developer regarding all that code is meant to support. With all these concerns in mind, do we dare change this code in any way, and if so, how?

> 这个时候，领域专家是帮不上忙的，因为他们看不懂代码。即便领域专家能够看懂代码，他可能也会被这段代码搞得一头雾水。我们难道就不能用另外一种方式来改善这段代码吗？如果可以，怎么修改？

There are at least three big problems here:

> 上面的 saveCustomer（）至少存在三大问题：

1. There is little intention revealed by the saveCustomer() interface.
2. The implementation of saveCustomer() itself adds hidden complexity.
3. The Customer “domain object” isn’t really an object at all. It’s really just a dumb data holder.

---

> 1. saveCustomer（）业务意图不明确。
> 2. 方法的实现本身增加了潜在的复杂性。
> 3. Customer 领域对象根本就不是对象，而只一个数据持有器（data holder）。

Let’s call this unenviable situation anemia-induced memory loss. It happens all the time on projects that produce this kind of implicit, completely subjective code “design.”

> 我们将这种情况称为“由贫血症导致的失忆症。”在实际项目中，这种症状发生得太多了。

::: tip
Hold On a Minute!

> 等等！

At this point some of you may be thinking, “Our designs never really leave the whiteboard. We just draw some structure, and once agreement on that is reached, we are set free to implement. Scary.”

> 这时你可能在想，“我们的设计都是在白板上进行的啊。我们会绘制设计框图，只有大家都达成一致时，我们才开始编码实现。”

If so, try not to distinguish design from implementation. Remember that when practicing DDD, the design is the code and the code is the design. In other words, whiteboard diagrams aren’t the design, just a way to discuss the challenges of the model.

> 如果情况是这样，那么请不要将设计和实现分开。记住，在实施 DDD 时，设计就是代码，代码就是设计。换句话说，白板图并不是设计，而只是我们讨论模型的一种方式。

Stay tuned, as you’ll learn how to take ideas off the whiteboard and make them work for you.

:::

By now you should be worried about this kind of code and how you can create a better design. The good news is that you can succeed in producing an explicit, carefully crafted design in your code.

> 现在你可能有些担心，“我要如何才能做到更好的设计呢？”用不着担心，你会成功的，继续读下去。

## 1.3 HOW TO DO DDD 如何 DDD

Let’s back away from heavy implementation discussions for a moment to consider one of the most empowering features of DDD, the Ubiquitous Language. It’s one of the two primary pillars of DDD’s strengths, the second being the Bounded Context (2), and one cannot properly stand without the other.

> 让我们暂时撇开关于实现细节的讨论，现在来看看 DDD 最具威力的特性之一：通用语言。通用语言和限界上下文（Bounded Context，2）同时构成了 DDD 的两大支柱，并且它们是相辅相成的。

::: tip
Terms in a Context

> 上下文术语

For now think of a Bounded Context as a conceptual boundary around a whole application or finite system. The reason for this boundary is to highlight that every use of a given domain term, phrase, or sentence—the Ubiquitous Language—inside the boundary has a specific contextual meaning. Any use of the term outside that boundary could, and probably does, mean something different. Chapter 2 explains Bounded Context in depth.

> 就现在来说，可以将限界上下文看成是整个应用程序之内的一个概念性边界。这个边界之内的每种领域术语、词组或句子——也即通用语言，都有确定的上下文含义。在边界之外，这些术语可能表示不同的意思。我们将在第 2 章中对限界上下文做深入探讨。

:::

### 1.3.1 Ubiquitous Language 通用语言

The Ubiquitous Language is a shared team language. It’s shared by domain experts and developers alike. In fact, it’s shared by everyone on the project team. No matter your role on the team, since you are on the team you use the Ubiquitous Language of the project.

通用语言是团队共享的语言。领域专家和开发者使用相同的通用语言进行交流。事实上，团队中每个人都使用相同的通用语言。不管你在团队中的角色如何，只要你是团队的一员，你都将使用通用语言。

::: tip

- So, You Think You Know What a Ubiquitous Language Is
- Obviously it’s the language of the business.
- Well, no.
- Surely it must be adopting industry standard terminology.
- No, not really.
- Clearly it’s the lingo used by the domain experts.
- Sorry, but no.
- The Ubiquitous Language is a shared language developed by the team—a team composed of both domain experts and software developers.
- That’s it. Now you’ve got it!

---

> - 那么，你认为你已经知道了什么是通用语言了？
> - 很明显，通用语言是一种业务语言。
> - 抱歉，不是。
> - 通用语言必须采用工业标准术语。
> - 不完全是。
> - 通用语言是领域专家专用的。
> - 对不起，不是。
> - 通用语言是团队自己创建的公用语言，团队中同时包含领域专家和软件开发人员。
> - 对了。

Naturally, the domain experts have a heavy influence on the Language because they know that part of the business best and may be influenced by industry standards. However, the Language is more centered on how the business itself thinks and operates. Also, many times two or more domain experts disagree on concepts and terms, and they are actually wrong about some because they haven’t thought of every case before. So, as the experts and developers work together to craft a model of the domain, they use discussion with both consensus and compromise to achieve the very best Language for the project. The team never compromises on the quality of the Language, just on the best concepts, terms, and meanings. Initial consensus is not the end, however. The Language grows and changes over time as tiny and large breakthroughs are achieved, much like any other living language.

> 自然地，领域专家对通用语言有很大的影响，因为他们最了解业务，并且深受工业标准的影响。但是，通用语言更多地是关于业务本身如何思考和运作的。此外，很多时候，不同领域专家会在概念和术语上产生分歧，他们甚至也会犯错，因为他们也无法了解每种业务用例。因此，当领域专家和开发者一起创建领域模型的时候，他们有时会达成一致，有时会做一些妥协，但最终目的都是为了创造最适合项目的通用语言。团队成员们妥协的绝对不应是通用语言的质量，而是概念、术语和含义。然而，最初的一致并不表示始终一致，就像其他语言一样，通用语言也会随着时间推移而不断演化改变。

:::

This is no gimmick to get developers to be on the same page as domain experts. It’s not just a bunch of business jargon being forced on developers. It’s a real language that is created by the whole team—domain experts, developers, business analysts, everyone involved in producing the system. The Language may start out with terms that are the natural lingo of the domain experts, but it isn’t limited to that because the Language must grow over time. Suffice it to say that when multiple domain experts are involved in creating the Language, they often disagree ever so slightly on the terms and meanings of what they thought were already ubiquitous.

> 要使开发者和领域专家一样了解业务没有什么窍门。通用语言也不是强加在开发者身上的晦涩业务术语。通用语言是由整个团队共同创建的一门语言，其中包括领域专家、开发者、业务分析员等。在开始的时候，通用语言可能只包含由领域专家使用的术语，但是随着时间推移，通用语言将不断壮大成长。

In Table 1.4, we not only model the administration of flu vaccines in code, but the team must also speak the Language openly. When the team discusses this aspect of the model, they literally speak phrases such as “Nurses administer flu vaccines to patients in standard doses.”

> 在表 1.4 中，对于“注射流感疫苗”这个业务用例，我们不仅要完成建模，还应该让团队使用相同的通用语言。当团队讨论到业务模型时，他们会说：“护士给病人注射标准剂量的流感疫苗。”

Table 1.4. Analyzing the Best Model for the Business

![](./figures/ch1/t1-4.jpg)

There will be some haggling and wrangling over the Language that exists in the minds of experts and what evolves from there. It’s all part of the natural progression of developing the best Language that will matter a lot for a long time. This happens through open discussion, looking at existing documents, business tribal knowledge that finally surfaces, as well as referencing standards, dictionaries, and thesauruses. There’s also a point reached where we come to terms with the fact that some words and phrases just don’t aptly fit the business context as well as we once thought, and we realize that others fit it much better.

> 由于通用语言最初只来自于领域专家，分歧是难免的。然而，这正是创建最佳通用语言的自然过程。在这个过程中，团队成员通过讨论、参考资料、引用标准、查阅词典等对通用语言进行改进。有时我们发现，有些我们曾经认为能很好表达业务的词汇不再适用了，而另外的一些词汇具有更好的效果。

So how do you capture this all-important Ubiquitous Language? Here are some ways that work as experimentation leads to advancement:

> 那么，你该如何掌握通用语言呢？这里有一些试验性的方法：

- Draw pictures of the physical and conceptual domain and label them with names and actions. These drawings are mostly informal but may contain some aspects of formal software modeling. Even if your team does some formal modeling with Unified Modeling Language (UML), you want to avoid any kind of ceremony that will bog down discussions and stifle the creativity of the ultimate Language being sought.
- Create a glossary of terms with simple definitions. List alternative terms, including the ones that show promise and the ones that didn’t work, and why. As you include definitions, you cannot help but develop reusable phrases for the Language because you are forced to write in the Language of the domain.
- If you don’t like the idea of a glossary, still capture some kind of documentation that includes the informal drawings of important software concepts. Again, the goal here is to force additional Language terms and phrases to surface.
- Since only one or a few team members may capture the glossary or other written documents, circle back with the rest of the team to review the resulting phrases. You won’t always, if ever, agree on all the captured linguistics, so be agile and ready to edit heavily.

---

> - 同时绘制物理模型图和概念模型图，并标以名字和行为。虽然这些图并不是正式的设计图，但它们却包含了软件建模的某些方面。即使你的团队在使用统一建模语言（Unified Modeling Language，UML ）来完成正式建模，也不要得意忘形，因为这样可能反而不利于团队的讨论，最终将阻碍通用语言的产生。
> - 创建一个包含简单定义的术语表。将你能想到的术语都罗列出来，包括好的和不好的，并注明好与不好的原因。在你给术语下定义时，你在不经意间就会创造出一些可重用的词汇，因为此时你使用的是领域中的通用语言。
> - 如果你不喜欢术语表，可以采用其他类型的文档，但记得将那些“不正式”的模型图也包含进去。同样，这里最终的目的也是发现通用语言中的术语和词组。
> - 由于团队中有些人工作在术语表上，还有些人工作在文档上，此时你需要找到团队的其他人员来检查你的成果。分歧肯定是有的，你应该对此有所准备。

Those are some ideal first steps to coining a Ubiquitous Language that fits your specific domain. However, this is absolutely not the model that you are developing. It’s only the genesis of the Ubiquitous Language that will very soon be expressed in your system’s source code. We are talking Java, or C#, or Scala, or some other programming language of choice. These drawings and documents also don’t address that the Ubiquitous Language will continue to expand and morph over time. The artifacts that originally led us down an inspiring path to developing a useful Ubiquitous Language that was just right for our specialized domain will very likely be rendered obsolete over time. That’s why in the end it is team speech and the model in the code that are the most enduring and the only guaranteed current denotations of the Ubiquitous Language.

> 以上是建立通用语言的一些理想化步骤，这样建立起来模型肯定不能直接用来指导开发，而只是建立通用语言的起步而已。此后，改进之后的通用语言将反映到系统的源代码中，比如 Java、C#或者 Scala 等。以上的模型图和文档并未表明通用语言会随着时间而扩大。在通用语言开发早期，这些材料可能会对我们产生鼓舞，但是时间一久，它们也将变得过时。这也是为什么只有团队的交流和代码才能持续到最后的原因，也只有这两者才能实时地反映通用语言。

Since team speech and the code will be the lasting expression of the Ubiquitous Language, be prepared to abandon the drawings, glossary, and other documentation that will be difficult to keep up-to-date with the spoken Ubiquitous Language and source code as they are rapidly enhanced. This is not a requirement of using DDD, but it is pragmatic because it becomes impractical to keep all the documentation in sync with the system.

> 由于团队交流和代码才是对通用语言的持续表达，你应该试着抛弃那些模型图、术语表和文档。虽然这并不是 DDD 所要求的，但是这样做的确很实用，因为我们很难将项目文档和软件系统保持同步。

With this knowledge we can redesign the saveCustomer() example. What if we chose to make Customer reflect each of the possible business goals that it must support?

> 有了以上认识，我们便可以重新设计 saveCustomer（）方法了。我们将修改 Customer，使其能够反映出它应该支持的业务操作：

```java
public interface Customer {
    public void changePersonalName(
        String firstName, String lastName);
    public void postalAddress(PostalAddress postalAddress);
    public void relocateTo(PostalAddress changedPostalAddress);
    public void changeHomeTelephone(Telephone telephone);
    public void disconnectHomeTelephone();
    public void changeMobileTelephone(Telephone telephone);
    public void disconnectMobileTelephone();
    public void primaryEmailAddress(EmailAddress emailAddress);
    public void secondaryEmailAddress(EmailAddress emailAddress);
}
```

We can argue that this is not the best model for a Customer, but when implementing DDD, questioning the design is expected. As a team we are free to haggle over what is the best model and settle only after we’ve discovered the Ubiquitous Language that is agreed upon. Still, the preceding interface does explicitly reflect the various business goals that a Customer must support, even if the Language could be improved by refinements again and again.

> 当然，以上的 Customer 并不是一个完美的模型，然而在实施 DDD 时，对设计的反思正是我们所期望的。作为一个团队，我们可以自由地讨论什么样的模型才是最好的，在对通用语言达成了一致之后，才开始着手开发。然而，即便我们可以对通用语言进行一遍又一遍地提炼，此时上面的例子已经能够反映出一个 Customer 应该支持的业务操作了。

It’s important to understand too that the Application Service would also be refactored to reflect the explicit intentions of the business goals at hand. Each Application Service method would be modified to deal with a single use case flow or user story:

> 另外，我们还应该知道，对领域模型的修改也将导致对应用层的修改。每一个应用层的方法都对应着一个单一的用例流：

```java
@Transactional
public void changeCustomerPersonalName(
    String customerId,
    String customerFirstName,
    String customerLastName) {
    Customer customer = customerRepository.customerOfId(customerId);
    if (customer == null) {
        throw new IllegalStateException("Customer does not exist.");
    }
    customer.changePersonalName(customerFirstName, customerLastName);
}
```

This is different from the original example because in that code a single method was used to deal with many different use case flows or user stories. In the new example we have limited a single Application Service method to deal with changing the personal name of the Customer, and nothing more. Thus, when using DDD, it is our job to refine Application Services accordingly. This implies that the user interface likewise reflects a narrower user goal, which may have previously been true. Now, however, this specific Application Service method doesn’t require its client to pass ten nulls following the first- and last-name parameters.

这和最开始的 saveCustomer（）例子是不同的，在那个例子中，我们使用了同一个方法来处理多个用例流。在这个新的例子中，我们只用一个应用层方法来修改 Customer 的姓名，除此之外，该方法别无其他业务功能。因此，在使用 DDD 时，我们应该对照着模型的修改相应地修改应用层。同时，这也意味着用户界面所反映的用户操作也变得更加狭窄。但是无论如何，这个特定的应用层方法不再要求我们在用户姓名参数之后跟上 10 个 null 了。

Doesn’t this new design put your mind at ease? You can read the code and easily comprehend it. You can also test it and confirm that it does exactly what it is meant to do, and that it doesn’t do anything that it shouldn’t.

对这个新例子你还算满意吧？通过阅读代码你便能理解它的业务意图。你还可以通过测试来保证它的功能，即只修改 Customer 的姓名。

Thus, the Ubiquitous Language is a team pattern used to capture the concepts and terms of a specific core business domain in the software model itself. The software model incorporates the nouns, adjectives, verbs, and richer expressions formally formulated and spoken by the close-knit team. Both the software and the tests that verify the model’s adherence to the tenets of the domain capture and adhere to this Language, the same one spoken by the team.

因此，我们使用通用语言来捕捉特定核心业务领域中的概念和术语，它是一种团队模式。软件模型包含名词、形容词、动词和一些富有含义的语句等，团队成员便通过这些语言进行交流。软件实现和测试中也使用和团队语言一样的通用语言。

Ubiquitous, but Not Universal 是通用，不是万能

Some further clarification about the reach of a Ubiquitous Language is in order. There are a few basic concepts that we need to keep carefully in mind:

我想，关于通用语言，有必要再做一点澄清。在理解通用语言时，我们必须牢牢记住以下几点：

- Ubiquitous means “pervasive,” or “found everywhere,” as spoken among the team and expressed by the single domain model that the team develops.
- The use of the word ubiquitous is not an attempt to describe some kind of enterprise-wide, company-wide, or worldwide, universal domain language.
- There is one Ubiquitous Language per Bounded Context.
- Bounded Contexts are relatively small, smaller than we might at first imagine. A Bounded Context is large enough only to capture the complete Ubiquitous Language of the isolated business domain, and no larger.
- The Language is ubiquitous only within the team that is working on the project that develops in an isolated Bounded Context.
- On a single project that develops a single Bounded Context, there are always one or more additional isolated Bounded Contexts with which it integrates using Context Maps (3). Each of the multiple Bounded Contexts that integrate has its own Ubiquitous Language, even though some terms of each may overlap.
- If you try to apply a single Ubiquitous Language to an entire enterprise, or worse, universally among many enterprises, you will fail.

---

> - 这里的“通用”意思是“普遍的”，或者“到处都存在的”。通用语言在团队范围内使用，并且只表达一个单一的领域模型。
> - “通用语言”并不表示全企业、全公司或者全球性的万能的领域语言。
> - 限界上下文和通用语言间存在一对一的关系。
> - 限界上下文是一个相对较小的概念，通常比我们起初想象的要小。限界上下文刚好能够容纳下一个独立的业务领域所使用的通用语言。
> - 只有当团队工作在一个独立的限界上下文中时，通用语言才是“通用”的。
> - 虽然我们只工作在一个限界上下文中，但是通常我们还需要和其他限界上下文打交道，这时可以通过上下文映射图（3）对这些限界上下文进行集成。每个限界上下文都有自己的通用语言，而有时语言间的术语可能有重叠的地方。
> - 如果你试图将某个通用语言运用在整个企业范围之内，或者更大的、夸企业的范围内，你将失败。

When you begin a new project in which you are properly using DDD, identify the isolated Bounded Context that is being developed. This places an explicit boundary around your domain model. Discuss, research, conceptualize, develop, and speak the Ubiquitous Language of the isolated domain model within the explicit Bounded Context. Reject all concepts that are not part of the agreed-upon Ubiquitous Language of your isolated Context.

> 当你开始一个项目，而该项目已经在使用 DDD 了，此时你需要将你正在开发的独立限界上下文识别出来，这样便在你的领域模型周围加上了一个显式的边界。此时，你应该在这个限界上下文中使用其专属的通用语言。对于那些不包含在通用语言中的概念，你应该拒绝使用。

## 1.4 THE BUSINESS VALUE OF USING DDD 使用 DDD 的业务价值

If your experience is anything like mine, you know that software developers can no longer pursue technologies and techniques just because they sound cool or intriguing. We must justify everything that we do. I think that has not always been true, but it is a good thing it is true now. I think the best justification for using any technology or technique is to provide value to the business. If we can establish real, tangible business value, why would the business ever refuse to use what we recommend?

> 如果你的经验和我相当，你就应该知道软件开发者不应该只是热衷于技术，而是应该将眼界放得更宽。我认为不管使用什么技术，我们的目的都是提供业务价值。而如果我们采用的技术确实产生了业务价值，人们就没有理由拒绝我们在技术上的建议。

The business case is strengthened especially if we can demonstrate that the business values are higher with our recommended approach than with other options.

> 如果我们提供的技术方案比其他方案更能够产生业务价值，那么我们的业务能力也将增强。

::: tip
Isn’t Business Value Most Important?

> 业务价值最重要吗？

Sure, and perhaps I should have put this subheading “The Business Value of Using DDD” earlier in the book. But it’s done, now. This subheading could actually be “How You Can Sell DDD to Your Boss.” Until you are mostly convinced that there is a real chance that you can actually implement DDD in your company, this book is just hypothetical. And I don’t want you to read this book as just a theoretical exercise. Read it as a concrete reality for your company. Then you can become more excited about how your company can really benefit. So read on.

> 当然啦，我甚至都在想是不是应该将“使用 DDD 的业务价值”这一节再往前放一些。更确切地讲，该章节的题目叫“如何向你的老板推销 DDD”更为合适。我并不希望你将本书看作只是些理论，而是希望本书对你的公司具有实际的指导意义。

:::

Let’s consider the very realistic business value of employing DDD. Be sure to share this openly with your management, domain experts, and technical team members. The value and benefits are summarized here, then I will elaborate. I start off with the less technical benefits.

> 让我们来看看 DDD 所带来的一些非常理想化的业务价值。记得将这些分享给你的管理层、领域专家和技术人员。我们可以将 DDD 的业务价值大致总结为以下几点：

1. The organization gains a useful model of its domain.
2. A refined, precise definition and understanding of the business is developed.
3. Domain experts contribute to software design.
4. A better user experience is gained.
5. Clean boundaries are placed around pure models.
6. Enterprise architecture is better organized.
7. Agile, iterative, continuous modeling is used.
8. New tools, both strategic and tactical, are employed.

---

> 1. 你获得了一个非常有用的领域模型
> 2. 你的业务得到了更准确的定义和理解
> 3. 领域专家可以为软件设计做出贡献
> 4. 更好的用户体验
> 5. 清晰的模型边界
> 6. 更好的企业架构
> 7. 敏捷、迭代式和持续建模
> 8. 使用战略和战术新工具

### 1. The Organization Gains a Useful Model of Its Domain 你获得了一个非常有用的领域模型

The emphasis of DDD is to invest our efforts in what matters most to the business. We don’t over-model. We focus on the Core Domain. Other models exist to support the Core Domain and are important, too. Yet the supporting models may not be given the priority and effort of the Core Domain.

> DDD 强调将精力花在对业务最有价值的东西上。我们并不过度建模，而是关注业务的核心域。有些模型是用来支撑核心域的，它们同样是重要的。但是，这些起支撑作用的模型在优先级上没有核心域高。

When our focus is on what distinguishes our business from all others, our mission is well understood and we have the parameters we need to keep on track. We will deliver exactly what is needed to achieve competitive advantage.

> 当我们将关注点放在自己的业务和别人业务的区别上时，我们便能更好地理解自己的任务所在，同时我们将更具竞争优势。

### 2. A Refined, Precise Definition and Understanding of the Business Is Developed 你的业务得到了更准确的定义和理解

The business may actually come to understand itself and its mission better than before. I have heard others state that the Ubiquitous Language developed for the business’s Core Domain has found its way into marketing materials. Certainly it should be incorporated in vision documents and mission statements.

> 业务人士能够更好地理解业务本身。我甚至听说通用语言曾经出现在某些公司的市场营销材料中。

As the model is refined over time, the business develops a deep understanding that can serve as an analysis tool. Details surface out of the minds of your domain experts as you are challenged by one another and shaped by technical team partners. These details can help your business analyze the value of the current and future direction, both strategic and tactical.

> 随着业务模型的不断改善，人们对业务的理解也将更加深刻。在团队讨论的过程中，一些业务细节被不断地暴露出来，这些细节有助于掌握业务价值。

### 3. Domain Experts Contribute to Software Design 领域专家可以为软件设计做出贡献

There is business value when the organization grows a deeper understanding of the core business. Domain experts don’t always agree on concepts and terminology. Sometimes the differences are fostered by different experiences from outside before joining the organization. Sometimes it happens because of the divergent paths taken by each expert within the same organization. Yet when brought together to a DDD effort, the domain experts gain consensus among themselves. This fortifies the effort and the organization as a whole.

> 当人们对自己的核心业务有了更深的了解时，业务价值自然就出来了。领域专家并不总是同意某些概念和术语。有时，分歧源自于领域专家们在其他公司工作时所积累起来的经验，而有时分歧则源自于公司内部。不管如何，当领域专家们在一起工作时，他们最终将达成一致意见，这对于整个公司来说都是件好事。

Developers now share a common Language as a unified team along with domain experts. They benefit further from the knowledge transfer from the domain experts they work with. As developers inevitably move on, either to a new Core Domain or out of the organization, training and handoffs are easier. The chances of developing “tribal knowledge,” where only a select few understand the model, are reduced. The experts, remaining developers, and new ones continue to share a common knowledge that is available to anyone in the organization who requires it. This advantage exists because there remains an express goal to adhere to the Language of the domain.

> 开发者和领域专家共享同一套交流语言，领域专家将知识传递给开发者。开发者总是会离开的，有可能去接触一个新的核心域，也有可能跳槽到其他公司，这时培训和工作移交也将变得更加简单，而“只有少数人才了解模型”的情况将大大减少。领域专家、剩下的开发者和新进人员可以继续使用通用语言进行交流。

### 4. A Better User Experience Is Gained 更好的用户体验

Often the end user experience can be tuned to better reflect the model of the domain. Domain-Driven is formally “baked in,” influencing human use of the software.

> 用户体验可以更好地反映出领域模型的好坏。

When software leaves too much to the understanding of its users, users must be trained to make a great number of decisions. In essence the users are only transferring the understanding in their minds into data that they enter into forms. The data is then saved to a data store. If users don’t understand exactly what is needed, the results are incorrect. Often this leads to guesswork with related lowered productivity until users can figure out the software.

> 如果软件留下太多的地方让用户自己去理解，用户往往需要经过培训才能做出操作决定。实际上，用户只是将他们所理解的转移到表单（form）中的数据而已。数据将被存储起来，如果用户不知道数据的用途，那么结果也将是错误的。

When the user experience is designed to follow the contours of the underlying expert model, users are led to correct conclusions. The software actually trains the users, which reduces the training overhead to the business. Quicker to productivity with less training—that’s business value.

> 当用户体验是按照领域专家心中的模型来设计时，就不会出现以上的问题了。这时软件本身便能对用户起到培训作用，而不需要业务人员来提供培训。效率提高了，培训减少了——这就是业务价值。

We next move into more technically driven benefits to the business.

> 接下来我们看看技术为业务创造的价值。

### 5. Clean Boundaries Are Placed around Pure Models 清晰的模型边界

The technical team is discouraged from doing what might appeal more to their programming and algorithmic interests by aligning expectations with business advantage. Purity in direction allows for focus on the potency of the solution, with efforts directed to where they matter the most. Achieving this is very closely connected to understanding the Bounded Context of the project.

> 我们并不鼓励技术团队将精力单纯地放在编码和算法上，而是期望他们能够面向业务。明确的目标产生高效的解决方案，而要达到这样的目的往往需要更好地理解项目的限界上下文。

### 6. Enterprise Architecture Is Better Organized 更好的企业架构

When Bounded Contexts are well understood and carefully partitioned, all teams in the enterprise develop an acute understanding of where and why integrations are necessary. The boundaries are explicit, and the relationships between them are as well. The teams that have models that intersect by usage dependency employ Context Maps to establish formal relationships and ways to integrate. This can actually lead to a very thorough understanding of the entire enterprise architecture.

> 一旦限界上下文得到了较好的理解和仔细的划分，那么团队的所有成员应该知道限界上下文间的集成是必要的。上下文之间的边界和关系是明晰的。当不同上下文的模型间存在依赖关系时，我们将使用上下文映射图来集成不同的限界上下文，而这又有助于我们全面地了解整个企业的架构。

### 7. Agile, Iterative, Continuous Modeling Is Used 敏捷、迭代式和持续建模

The word design can evoke negative thoughts in the minds of business management. However, DDD is not a heavyweight, high-ceremony design and development process. DDD is not about drawing diagrams. It is about carefully refining the mental model of domain experts into a useful model for the business. It is not about creating a real-world model, as in trying to mimic reality.

> “设计”这个词可能并不能取悦业务管理层。然而，DDD 并不是一个重量级的设计方法和开发过程。DDD 并不是画模型图，而是将领域专家的思维模型转化成有用的业务模型。DDD 不是创建一个真实世界的模型，而是模仿现实。

The team’s efforts follow an agile approach, which is iterative and incremental. Any agile process that the team feels comfortable with can be used successfully in a DDD project. The model that is produced is the working software. It is refined continuously until it is no longer needed by the business.

> 团队的工作遵循敏捷方法——迭代式的，增量式的。任何一种敏捷方法，只要团队认为合适，都可以用于 DDD 项目。通过 DDD 创建出来的模型便是可工作的软件。团队会对模型做持续的改进，直到业务层没有新的需求为止。

### 8. New Tools, Both Strategic and Tactical, Are Employed 使用战略和战术新工具

A Bounded Context gives the team a modeling boundary in which to create a solution to a specific business problem domain. Inside a single Bounded Context is a Ubiquitous Language formulated by the team. It is spoken among the team and in the software model. Disparate teams, sometimes each responsible for a given Bounded Context, use Context Maps to strategically segregate Bounded Contexts and understand their integrations. Within a single modeling boundary the team may employ any number of useful tactical modeling tools: Aggregates (10), Entities (5), Value Objects (6), Services (7), Domain Events (8), and others.

> 限界上下文为团队创建了一个建模边界，成员在边界内部为特定的业务领域创建解决方案。在单个限界上下文中团队成员共享一套通用语言。不同的团队有时各自负责一个限界上下文，此时可以使用上下文映射图在战略层面上对限界上下文进行界分和集成。在某个建模边界内部，团队将使用战术建模工具：聚合（Aggregate，10）、实体（Entity，5）、值对象（Value Object，6）、领域服务（DomainService，7）和领域事件（Domain Event，8）等。

## 1.5 THE CHALLENGES OF APPLYING DDD 实施 DDD 所面临的挑战

As you implement DDD, you will encounter challenges. So has everyone else who has succeeded at it. What are the common challenges and how do we justify using DDD as we face them? I will discuss the more common ones:

在实施 DDD 的过程中，挑战是不可避免的。那么，有人成功过吗？DDD 都有哪些常见的挑战，我们又如何处理它们？我将讨论以下三点最常见的挑战：

- Allowing for the time and effort required to create a Ubiquitous Language
- Involving domain experts at the outset and continuously with the project
- Changing the way developers think about solutions in their domain

---

> - 为创建通用语言腾出时间和精力
> - 持续地将领域专家引入项目
> - 改变开发者对领域的思考方式

One of the greatest challenges in using DDD can be the time and effort required to think about the business domain, research concepts and terminology, and converse with domain experts in order to discover, capture, and enhance the Ubiquitous Language rather than coding in techno-babble. If you want to apply DDD completely, with the greatest value to the business, it’s going to require more thought and effort, and it’s going to take more time. That’s the way it is, period.

> 使用 DDD 最大的挑战之一便是：我们需要花费大量的时间和精力来思考业务领域，研究概念和术语，并且和领域专家交流，以发现、捕捉和改进通用语言。如果你想完全采用 DDD 来最大化业务价值，你需要做出很多努力，并且花费很多时间。事实就是这样的。

It can also be a challenge to solicit the necessary involvement from domain experts. No matter how difficult it is, make sure you do. If you don’t get commitment from at least one real expert, you are not going to uncover deep knowledge of the domain. When you do get the domain experts’ involvement, the onus falls back on the developers. Developers must converse with and listen carefully to the true experts, molding their spoken language into software that reflects their mental model of the domain.

> 要将领域专家引入你的项目恐怕也不是一件易事。但是不管有多么困难，这是你必须做的。如果你连一个领域专家都找不到，那么你根本无法对一个领域有深入的理解。当你找到领域专家的时候，此时开发者应该表现出主动。开发者应该找领域专家交谈并仔细聆听，然后将你们的谈话转化成软件代码。

If the domain you are working in is truly distinguishing to your business, domain experts have the edge-knowledge locked up in their heads, and you need to draw it out. I’ve been on projects where the real domain experts are hardly around. Sometimes they travel a lot and it can be weeks between one-hour meetings with them. In a small business it can be the CEO or one of the vice presidents, and they have lots of other things to do that may seem more important.

> 如果你所工作的领域和业务相去甚远，领域专家所了解的也只是一些边边角角，那么此时你应该将这种问题暴露出来。在我曾经工作的一个项目里，真正的领域专家很难找到，有时他们还会到处出差，我得等上好几周才能和他们开上一次会。在一些小型的公司里，领域专家通常是 CEO 或者副总裁，他们的事情太多了，这时你也别指望他们能做好你的领域专家。

Cowboy Logic 牛仔的逻辑

AJ: “If you can’t rope the big steer, you’re gonna go hungry.”

> AJ：“如果你逮不到那头公牛，你就得挨饿咯！”

![](./figures/ch1/cowboy_logic_aj_talks.jpg)

Getting domain expert involvement may require creativity . . .

> 引入领域专家需要创造性……

::: tip
How to Involve Domain Experts in Your Project

> 如何在项目中引入领域专家

![](./figures/ch1/domain_expert.jpg)

Coffee. Use that Ubiquitous Language:

> 咖啡。使用这种通用语言：

“Hi, Sally, I got you a tall half-skinny half-one-percent extra-hot split-quad-shot latte with whip. Do you have a few minutes to talk about . . . ?”

> “Hi，Sally，我给你泡了一杯泡沫牛奶咖啡，你有时间聊聊……？”

Learn to use the Ubiquitous Language of C-Level management: “. . . profits . . . revenues . . . competitive edge . . . market domination.” Seriously.

> 学习 C 级经理使用的通用语言：“……利润……收入……竞争优势……市场优势。”

Hockey tickets.

:::

Most developers have had to change the way they think in order to properly apply DDD. We developers are technical thinkers. Technical solutions come easy for us. It’s not that thinking technically is bad. It’s just that there are times when thinking less technically is better. If it’s been our habit to practice software development only in technical ways for years, perhaps now would be a good time to consider a new way of thinking. Developing the Ubiquitous Language of your domain is the best place to start.

> 多数开发者在采用 DDD 时都需要转变自己思考问题的方式。作为开发者，我们都是技术思想者，技术实现对于我们来说并不是什么难事。我并不是说技术地思考不好，只是说有时少从技术层面去思考会更好。这么多年来，我们都习惯了单从技术层面完成软件开发，那么现在，是时候考虑一种新的思考方式了。为你的业务领域开发一门通用语言便是一个好的出发点。

Cowboy Logic 牛仔的逻辑

LB: “That fella’s boots are too small. If he don’t find himself another pair, his toes are gonna hurt.”

> LB：“那家伙的靴子太小了，如果他不换双新的，他的脚指头可能要受罪了。”

AJ: “Yep. If you don’t listen, you’re gonna have to feel.”

> AJ：“对，如果他不听的话，就有他好受的了。”

![](./figures/ch1/cowboy_logic_conversation.jpg)

There’s another level of thought that is required with DDD that goes beyond concept naming. When we model a domain through software, we are required to give careful thought to which model objects do what. It’s about designing the behaviors of objects. Yes, we want the behaviors to be named properly to convey the essence of the Ubiquitous Language. But what an object does by means of a specific behavior must be considered. This is a level of effort that goes beyond creating attributes on a class and exposing getters and setters publicly to clients of the model.

> 在 DDD 中，我们会谈及到对概念的命名。对于概念命名而言，我们有更高层面的要求。当我们对一个领域进行建模时，我们需要仔细地考虑什么样的对象做什么样的事情，这是关于对象行为设计的。我们希望对对象行为的命名能够传达准确的业务含义，也即反映通用语言。要达到这样的目的，肯定不是先在类上定义属性，然后向客户端代码暴露 getter 和 setter 那么简单。

Let’s now look at a more interesting domain, one that is more challenging than the rudimentary one previously considered. I purposely repeat my previous guidance here to reinforce the ideas.

> 现在让我们来看看一个更有趣的领域，这个领域比之前那个 Customer 例子更具挑战性。这里，我刻意重复一下先前所讲的。

Again, what happens if we simply provide data accessors to our model? To reemphasize, if we only expose the data accessors for our model objects, the results will look much like a data model. Consider the following two examples and decide for yourself which of the two requires more thorough design thought, and which produces the greater benefit to its clients. The requirement is in a Scrum model, where we need to commit a backlog item to a sprint. You probably do this all the time, so it’s most likely a familiar domain.

> 如果我们只是对领域模型提供 getter 和 setter 会怎么样？答案是，结果我们只是在创建纯数据模型。看看下面的两个例子，自己思考一下，哪一个在设计上是欠妥的，哪一个对客户代码更有益。在这两个例子中是一个 Scrum 模型，我们需要将一个待定项（Backlog Item）提交到冲刺（Sprint）中去。这样的事情你可能一直在做，因此对这个领域你应该是很熟悉的。

The first example, as is commonly done today, uses attribute accessors:

> 第一个例子，通常的做法，使用属性访问的方式：

```java
public class BacklogItem extends Entity {
    private SprintId sprintId;
    private BacklogItemStatusType status;
    ...
    public void setSprintId(SprintId sprintId) {
        this.sprintId = sprintId;
    }

    public void setStatus(BacklogItemStatusType status) {
        this.status = status;
    }
    ...
}
```

As for the client of this model:

> 客户代码如下：

```java
// client commits the backlog item to a sprint
// by setting its sprintId and status

backlogItem.setSprintId(sprintId);
backlogItem.setStatus(BacklogItemStatusType.COMMITTED);
```

The second example uses a domain object behavior that expresses the Ubiquitous Language of the domain:

> 第二个例子使用了领域对象的行为，这种行为表达出了领域中的通用语言：

```java
public class BacklogItem extends Entity {
    private SprintId sprintId;
    private BacklogItemStatusType status;
    ...
    public void commitTo(Sprint aSprint) {
        if (!this.isScheduledForRelease()) {
            throw new IllegalStateException(
                "Must be scheduled for release to commit to sprint.");
        }
        if (this.isCommittedToSprint()) {
            if (!aSprint.sprintId().equals(this.sprintId())) {
                this.uncommitFromSprint();
            }
        }
        this.elevateStatusWith(BacklogItemStatus.COMMITTED);
        this.setSprintId(aSprint.sprintId());
        DomainEventPublisher
            .instance()
            .publish(new BacklogItemCommitted(
                    this.tenant(),
                    this.backlogItemId(),
                    this.sprintId()));
    }
    ...
}
```

The client of this explicit model seems to operate on safer ground:

> 此时的客户代码如下：

```java
// client commits the backlog item to a sprint
// by using a domain-specific behavior

backlogItem.commitTo(sprint);
```

The first example uses a very data-centric approach. The onus is entirely on the client to know how to correctly commit the backlog item to a sprint. The model, which is not really a domain model, doesn’t help at all. What if the client mistakenly changes only the sprintId but not the status, or the opposite? Or what if in the future another attribute must be set? The client code must be analyzed for correct mapping of data values to the proper attributes on the BacklogItem.

> 第一个例子采用的是以数据为中心的方式，此时客户代码必须知道如何正确地将一个待定项提交到冲刺中。这样的模型是不能称为领域模型的。如果客户代码错误地修改了 sprintId，而没有修改 status 会发生什么呢？或者，如果在将来有另外一个属性需要设值时又该怎么办？我们需要认真分析客户代码来完成从客户数据到 BacklogItem 属性的映射。

This approach also exposes the shape of the BacklogItem object and clearly focuses attention on its data attributes and not on its behaviors. Even if you argue that setSprintId() and setStatus() are behaviors, the case in point is that these “behaviors” have no real business domain value. These “behaviors” do not explicitly indicate the intentions of the scenarios that the domain software is supposed to model, that of committing a backlog item to a sprint. They do cause cognitive overload when the client developer tries to mentally select from among the BacklogItem attributes needed to commit a backlog item to a sprint. There could be many because it’s a data-centric model.

> 这种方式同时也暴露了 BacklogItem 的数据结构，并且将关注点集中在数据属性上，而不是对象行为。你可能会反驳道：“setSprintId（）和 setStatus（）就是行为啊。”问题在于，这里的“行为”没有真正的业务价值，它并没有表明领域模型中的概念——此处即“将待定项提交到冲刺中”。开发者在开发客户代码时，他并不清楚到底需要为 BacklogItem 的哪些属性设值，而这样的属性有可能存在很多，因为这是一个以数据为中心的模型。

Now consider the second example. Instead of exposing the data attributes to clients, it exposes a behavior that explicitly and clearly indicates that a client may commit a backlog item to a sprint. Experts in this particular domain discuss the following requirement of the model:

> 现在，我们来看看第二个例子。有别于第一个例子，它将行为暴露给客户，行为方法的名字清楚地表明了业务含义。这个领域的专家在建模时讨论了以下需求：

Allow each backlog item to be committed to a sprint. It may be committed only if it is already scheduled for release. If it is already committed to a different sprint, it must be uncommitted first. When the commit completes, notify interested parties.

> 允许将每一个待定项提交到冲刺中。只有在一个待定项位于发布计划（Release）中时才能进行提交。如果一个待定项已经提交到了另外一个冲刺中，那么需要先将其回收 。提交完成时，通知相关客户方。

Thus, the method in the second example captures the Ubiquitous Language of the model in context, that is, the Bounded Context in which the BacklogItem type is isolated. And as we analyze this scenario, we discover that the first solution is incomplete and contains bugs.

With the second implementation clients don’t need to know what is required to perform the commit, whether simple or complex. The implementation of this method has as much or as little logic as necessary. We easily added a guard to protect against committing a backlog item that is not yet scheduled for release. True, you can also place guards inside the setters of the first implementation, but the setter now becomes responsible for understanding the full context of the object’s state rather than just the requirements for sprintId and status.

> 在第二个例子中，客户代码并不需要知道提交 BacklogItem 的实现细节。实现代码所表达的逻辑恰好能够描述业务行为。我们很容易地添加了几行代码，以确保在发布计划之外的待定项是不能被提交的。诚然，在第一个例子中，你可以修改 setter 以达到同样的目的，但此时该 setter 的职责便不单一了，它需要了解 BacklogItem 对象的内部状态，而不再只是对 sprintId 和 status 属性赋值。

There’s another subtle difference here, too. Note that if the backlog item is already committed to another sprint, it will first be uncommitted from the current sprint. This is an important detail, because when a backlog item is uncommitted from a sprint, a Domain Event is to be published to clients:

> 这里还有一个微小的区别。如果一个待定项已经被提交到了另外的冲刺中，那么我们应该先从那个冲刺中回收该待定项。这一点也是重要的，因为当一个待定项从冲刺中回收时，将有领域事件发出以通知客户方：

Allow each backlog item to be uncommitted from a sprint. When the backlog item is uncommitted, notify interested parties.

> 允许从冲刺中回收任何一个待定项，回收时通知相关客户方。

The publication of the uncommitted notification is obtained for free just by using the domain behavior uncommitFrom(). Method commitTo() doesn’t even need to know that it notifies. All it needs to know is that it must uncommit from any current sprint before committing to a new sprint. Additionally, the commitTo() domain behavior also notifies interested parties with an Event as its final step. Without placing this rich behavior in BacklogItem we would have to publish Events from the client. That would certainly leak domain logic from the model. Bad.

> 此时，我们并不需要关心如何发布回收事件，因为 uncommitFrom（）方法会为我们处理这些。而 commitTo（）方法甚至都不知道发布回收事件这码事，它只需要知道，在将待定项提交给一个新的冲刺时，必须先将该待定项从它当前所在的冲刺中回收。另外，commitTo（）的领域行为还包括：在提交待定项完毕后，以事件形式通知相关客户方。如果不是这个富含行为的 BacklogItem，我们得在客户代码中发布领域事件，这显然是一种领域逻辑的泄漏。

Clearly, more thought is needed to create the BacklogItem of the second example than that of the first. Yet the thought needed is not so much greater, and the benefits are so much higher. The more we learn to design in this way, the easier it becomes. In the end, there is certainly more required thought, more effort, more collaboration and orchestration of team efforts, but not so much that DDD becomes heavy. New thought is well worth the effort.

> 很明显，在第二个例子中，我们对 BacklogItem 有了更多的思考，但同时我们也获得更多的回报。沿着这条路往下走，我们将越走越容易。到后来，我们肯定会需要更多的思考、付出和团队协作，但是这并不会使 DDD 变得笨重。

Whiteboard Time 白板时间

- Using the specific domain you currently work in, think of the common terms and actions of the model.
- Write the terms on the board.
- Next, write phrases that should be used by your team when you talk about the project.
- Discuss them with a real domain expert to see how they could be refined (remember to bring the coffee).

---

> - 对于你目前正在工作的业务领域，思考一下模型中的通用术语和业务操作。
> - 将术语写在白板上。
> - 然后，将项目中所用到的短语也写下来。
> - 与真正的领域专家交流一下，看看哪些词汇是可以改善的（记得带上咖啡哦）。

### 1.5.1 Justification for Domain Modeling 为领域建模正名

Tactical modeling is generally more complex than strategic modeling. Thus, if you intend to develop a domain model using the DDD tactical patterns (Aggregates, Services, Value Objects, Events, and so forth), doing so will require more careful thought and greater investment. Since this is so, how does an organization justify tactical domain modeling? What criteria can be used to qualify a given project for the extra investment needed to properly apply DDD from top to bottom?

通常来说，战术建模比战略建模复杂。因此，如果你打算采用 DDD 的战术模式（聚合、领域服务、值对象和领域事件等）来建立领域模型的话，你需要更仔细的思考和更大的投入。那么，我们有什么理由依然要采用战术建模呢？我们又拿什么标准来衡量在 DDD 上的投入是值得的呢？

Picture yourself leading an expedition through unfamiliar territory. You would want to understand the surrounding landmasses and borders. Your team would study maps, maybe even draw their own, and determine their strategic approach. You would consider aspects of the terrain and how it could be used to your advantage. No matter how much planning is done, some facets of such an endeavor are going to be really difficult.

你可能已经在盘算，这将把你带到一个陌生的领地，你发现你得好好研究一下周边的情况。你的团队可能会学着既有的线路图，甚至开辟一条新路来决定自己的战略设计方案。你可能会仔细捉摸这片新的领地，然后试图使其为你所用。然而，不管你事先做了多少准备，这都将是一条荆棘丛生之路。

If your strategy indicated that you’d have to scale a vertical rock face, you’d need some fitting tactical tools and maneuvers for that ascent. Standing at the bottom and looking up, you might see some indication of specific challenges and perilous areas. Yet, you wouldn’t see every detail until you were on the rock face. You might need to drive pitons into slick rock, but you could use various-size cams to wedge into natural cracks. To latch on to these climbing protections, you’d bring along your carabiners. You would try to take as straight a path as possible but would have to make specific determinations point by point. Sometimes you might even have to backtrack and reroute depending on what the rock dictated. Many people think of climbing as a dangerous thrill sport, but those who actually climb will tell you it’s safer than driving a car or flying an airplane. Clearly, for that to be true, climbers need to understand the tools and techniques and how to judge the rock.

如果你发现你需要在战略的岩石上攀爬，那么你得找到一套合适的战术工具来辅助你。站在低处往上看，你有可能看到一些特别的挑战和危险地带。然而，如果不爬到那样的高度，你又是看不清楚的。你可能需要在坚硬的岩石上打孔插钉，但是也可以找到那些自然形成的裂缝。你可能还需要带上锁环以保证安全。你可以沿着一条路线顺直而上，也可以打点布阵、步步为营。有时随着岩石形状的走势，你可能需要往回撤，再重新设计路线。有人认为攀岩是种危险的运动，但是那些尝试过的人会告诉你，攀岩实际上比驾驶汽车和飞机还安全。攀岩者需要知道如何使用工具和运用好技能，并且能够根据岩石状况做出相应的反应。

If developing a given Subdomain (2) requires such a difficult, even precarious, ascent, we’d bring the DDD tactical patterns along for the climb. A business initiative that matches the criteria of the Core Domain should not quickly dismiss the use of the tactical patterns. The Core Domain is an unknown and complex area. The team is best protected against a disastrous mid-asset fall if using the right tactics.

如果说开发一个业务子域（Subdomain，2）就像攀岩一样困难，那么我们需要随身携带 DDD 的战术模式来武装自己。对于满足核心域标准的业务来说，我们不应该将战术模式拒之门外。半途而废的项目时有发生，而正确的战术模式可以帮助我们减少这种情况的发生。

Here’s some practical guidance. I begin with the high-level ones and progress to more details:

这里是一些实际的指导意见，我会先讲高层次的，然后讲更具体的：

- If a Bounded Context is being developed as the Core Domain, it is strategically vital to the success of the business. The core model is not well understood and will require lots of experimentation and refactoring. It likely deserves commitment to longevity with continuous enhancement. It may not always be your Core Domain. Nonetheless, if the Bounded Context is complex, innovative, and needs to endure for a long time as it undergoes change, strongly consider the use of the tactical patterns as an investment in the future of your business. This assumes that your Core Domain deserves the best developer resources with a high skill level.
- A domain that may become a Generic Subdomain (2) or Supporting Subdomain to its consumers may actually be a Core Domain to your business. You don’t always judge a domain from the viewpoint of its ultimate consumers. If you are developing a Bounded Context as your chief business initiative, it is your Core Domain regardless of how it is viewed by customers outside your business. Strongly consider the use of the tactical patterns.
- If you are developing a Supporting Subdomain that, for various reasons, cannot be acquired as a third-party Generic Subdomain, it is possible that the tactical patterns would benefit your efforts. In this case consider the skill level of the team and whether or not the model is new and innovative. It is innovative if it adds specific business value, captures special knowledge, and is not just technically intriguing. If the team is capable of properly applying tactical design, and the Supporting Subdomain is innovative and must endure for years in the future, this is a good opportunity to invest in your software using tactical design. However, this does not make this model the Core Domain since in the eyes of the business it is merely Supporting.

---

> - 如果一个限界上下文被当成核心域来开发，那么从战略上来说，这个限界上下文对业务的成功是极其重要的。核心模型是不易理解的，需要不断地尝试和重构。通过持续改进，我们可以延长它的效用生命，这样的做法显然是值得的。当然，这个限界上下文不见得始终是你的核心域。即便如此，如果它是复杂的，创新性的，并且需要在不断的变化中持续存在很长时间，我们还是建议在该限界上下文中使用战术模式。这里，我们假设你的核心域是值得配置最好的开发者的。
> - 一个领域，对于消费方来说有可能成为通用子域（Generic Subdomain，2）或者支撑子域，但是却有可能成为你自己的核心域。我们并不站在最终消费方的角度来评价一个领域。如果你正在开发的限界上下文是你主要的业务，那么它便是你的核心域，而不管消费方是如何看待的。此时，一定记得使用战术模式。
> - 如果你正开发一个支撑子域，但是由于种种原因，该支撑子域不能从第三方的通用子域直接获得，那么此时战术模式将帮上你大忙。在这种情况下，你需要考虑团队成员的技能水平，还有模型是否具有创新性。如果此时的模型增加了特定的业务价值，而且不只是拥有技术上的绚丽，那么该模型就可以认为是创新性的。如果团队有能力实施战术设计，这个支撑子域又是创新性的，并且将持续存在很长时间，那么此时便是采用战术设计的大好时机。尽管如此，这并不能使该子域称为核心域，因为在业务人士眼中，这样的领域只是支撑性的。

These guidelines may be somewhat confining if your business employs a good number of developers with vast experience in and a very high comfort level with domain modeling. Where experience is very high, and the engineers themselves believe the tactical patterns would be the best choice, it makes sense to trust their opinion. Honest developers, no matter how experienced, will indicate in a specific case that developing a domain model is, or is not, the best choice.

> 对于有丰富 DDD 经验的开发者来说，上面的指导建议可能就不够了。如果你的团队经验丰富，其中的开发者又确信战术建模是种好的选择，那么此时他们的意见可能就更值得相信。诚实的开发者，不管经验丰富与否，都会在特定的情况下明确地指出领域建模是否为最佳的选择。

The type of business domain itself is not automatically the determining factor for choosing a development approach. Your team should consider important questions to help you make the final determination. Consider the following short list of more detailed decision parameters, which is more or less aligned with and expands on the preceding higher-level guidelines:

> 业务领域的类型本身并不自动地决定应该选择哪种开发方式。你的团队应该考虑一些重要的问题，然后做出决定。请考虑以下因素，这些因素和上面提到的高层次指导是有对应关系的。

- Are domain experts available and are you committed to forming a team around them?
- Although the specific business domain is somewhat simple now, will it grow in complexity over time? There is risk in using Transaction Script1 for complex applications. If you use Transaction Script now, will the potential for refactoring to a behavioral domain model later on be practical if/when the Context becomes complex?

---

> - 团队是否有领域专家，如果有，你如何围绕领域专家组织自己的团队？
> - 虽然就目前来说，你的业务领域是简单的，但它将来会变得复杂吗？对于复杂的系统来说，使用事务脚本是存在风险的。当领域变得复杂时，是否有可能将系统重构到富含行为的领域模型？

1. Here I am generalizing terms. In this list I use Transaction Script to represent several non-domain-model approaches.

- Will the use of the DDD tactical patterns make it easier and more practical to integrate with other Bounded Contexts, whether third-party or custom developed?
- Will development really be simpler and require less code if you use Transaction Script? (Experience with both approaches proves that many times Transaction Script requires as much or more code. This is probably because the complexity of the domain and the innovation of the model were not well understood during project planning. Underestimating domain complexity and the innovation involved happens often.)
- Do the critical path and timeline allow for any overhead required for tactical investment?
- Will the tactical investment in a Core Domain protect the system from changing architectural influences? Transaction Script may leave it exposed. (Domain models are often enduring while architectural influences tend to be more disruptive to other layers.)
- Will clients/customers benefit from a cleaner, enduring design and development approach, or could their application be replaced by an off-the-shelf solution tomorrow? In other words, why would we ever develop this as a custom application/service in the first place?
- Will developing an application/service using tactical DDD be more difficult than using other approaches such as Transaction Script? (Skill level and availability of domain experts is vital to answering this question.)
- If the team’s toolkit was complete with DDD enablers, would we conscientiously choose to use another approach instead? (Some enablers make model persistence practical, such as using object-relational mapping, full Aggregate serialization and persistence, an Event Store, or a framework that supports tactical DDD. There may be other enablers, too.)

---

> - DDD 的战术模式是否可以简化与其他限界上下文的集成，不管是第三方的还是定制开发的？
> - 使用事务脚本是否的确可以减少代码量？（经验表明，不管是对于哪种开发方式，事务脚本都不能减少代码量。这可能是由于在项目计划阶段，领域复杂性并没得到正确的认识所致。因此，我们需要在领域复杂性上下足功夫。）
> - 你项目的进度安排是否允许在战术模式上有所投入？
> - 在核心域上的战术投入能否消除架构变化所带来的影响？事务脚本是做不到这一点的（和领域模型层相比，其他层更易受到架构变化的影响）。
> - 客户是否的确能从这种持续设计和开发的方式中获益，或者有现成的产品就能满足他们的需求？换句话说，我们是否应该一开始就考虑定制化开发？
> - 使用 DDD 的战术开发模式会比其他开发方式更加困难吗，比如事务脚本？（这个问题很大程度上取决于团队成员的技能水平和是否有领域专家。）
> - 如果团队已经具备了实施 DDD 的条件，我们还会刻意地选择另一种开发方式吗？有些开发者已经将模型的持久化变得很实用了，比如使用 ORM、全聚合序列化和持久化、事件存储（Event Store）、或者战术 DDD 框架等。但是我们也不能排除还有热衷于其他开发方式的开发者。

This list is not prioritized for your domain, and you can probably assemble additional criteria. You understand the compelling reasons for using the best and most empowering methods possible to your advantage. You also know your business and technology landscape. In the end it is the business customer, not the object practitioners and technologists, who must be pleased. Choose wisely.

> 上面的列表项并没有先后顺序，而你自己也可以制定另外的衡量标准。你应该知道哪些开发方法对你来说是最好的，同时还应该全景式地了解你的业务和技术。有一点需要记住：你最终得取悦你的客户，而不是技术开发者，所以你得慎重地做出选择。

### 1.5.2 DDD Is Not Heavy DDD 并不笨重

In no way do I want to imply that properly practicing DDD leads to a heavyweight process with lots of ceremony and all the crufty documentation artifacts that must be supported. That’s not what DDD is about. It is meant to fit well into any agile project framework, such as Scrum, that the team desires to use. Its design tenets lean toward rather rapid test-first refinements of a real software model. If you were in need of developing a new domain object, such as an Entity or a Value Object, the test-first approach works like this:

> 在我看来，DDD 绝非是充满繁文缛节的笨重开发过程。事实上，DDD 能够很好地与敏捷项目框架结合起来，比如 Scrum。DDD 也倾向于“测试先行，逐步改进”的设计思路。在你开发一个新的领域对象时，比如实体或值对象，你可以采用以下步骤进行：

1. Write a test that demonstrates how the new domain object should be used by a client of the domain model.
2. Create the new domain object with enough code to make the test compile.
3. Refactor both until the test properly represents the way a client would use the domain object, and the domain object has proper behavioral method signatures.
4. Implement each domain object behavior until the test passes, refactoring the domain object until no inappropriate code duplications exist.
5. Demonstrate the code to team members, including domain experts, to ensure that the test is using the domain object according to the current meaning of the Ubiquitous Language.

---

> 1. 编写测试代码以模拟客户代码是如何使用该领域对象的。
> 2. 创建该领域对象以使测试代码能够编译通过。
> 3. 同时对测试和领域对象进行重构，直到测试代码能够正确地模拟客户代码，同时领域对象拥有能够表明业务行为的方法签名。
> 4. 实现领域对象的行为，直到测试通过为止，再对实现代码进行重构。
> 5. 向你的团队成员展示代码，包括领域专家，以保证领域对象能够正确地反映通用语言。

You may conclude that this is not any different from the test-first approach you already practice. Well, it might be a little different, but the point is that it’s basically the same. This test stage is not attempting to prove with absolute certainty that the model is bulletproof. Later we will add tests to do that. First we want to focus on how the model will be used by clients, and these tests drive the model’s design. The good news is that it really is an agile approach. DDD promotes lightweight development, not ceremonious, heavy, up-front design. From that standpoint it really isn’t different from common agile development. So, while the preceding steps may not enlighten you about agile, I think they clarify the position of DDD, that it is meant to be used in an agile way.

> 你可能会想：“这和我之前采用的测试驱动开发没什么区别啊。”对，他们可能有细微的区别，但是基本思路是一样的。测试代码并不能保证我们的领域对象就是无懈可击的。之后，我们还会添加另外的测试代码。首先，我们关注的是客户代码如何使用领域对象，此时的测试代码驱动着模型的设计。这种方式和敏捷开发并没有多大区别。因此，即便你并不认为上面的步骤是敏捷，但它们的确表明，DDD 采用的是一种“敏捷的”方式进行软件开发的。

Later you also add tests that verify the correctness of the new domain object from every possible (and practical) angle. At this point you are interested in the correctness of the expression of a domain concept that is embodied in the new domain object. Reading the demonstrative clientlike test code must reveal the proper expressiveness using the Ubiquitous Language. Domain experts who are nontechnical should be able, with the help of a developer, to read the code well enough to get a clear impression that the model has achieved the goal of the team. This implies that test data must be realistic and support and enhance the desired expressiveness. Otherwise, domain experts cannot make a complete judgment about the implementation.

> 在这之后，你会添加更多的测试，从多个角度确保新建领域对象的正确性。此时你关注的是领域对象对于领域概念的表达力，而测试代码本身便是通用语言在程序中的表达。在开发人员的帮助下，领域专家可以通过阅读测试代码来检验领域对象是否满足业务需求。这也意味着测试数据应该是真实的，因为这样可以增加测试代码的业务表达力。否则，领域专家是很难对你的实现做出评判的。

This test-first agile methodology repeats until you have a model that is working according to the tasks outlined for the current iteration. The steps outlined previously are agile and represent what Extreme Programming originally promoted. Using agile does not eliminate any essential DDD patterns and practices. They go together quite well. Of course, you can choose to use full DDD without doing test-first development. You can always develop tests against existing model objects. However, designing from the model client’s perspective adds a very desirable dimension.

> 以上的开发步骤将不断重复，直到领域模型满足本次迭代的计划任务为止。这种方法是敏捷的，同时，它也是极限编程（Extreme Programming）所倡导的。因此，使用敏捷并不会消除 DDD 的模式和实践，而相反，它们可以很好地结合起来。当然，在实施 DDD 时，你也可以不采用测试驱动开发，而是对既有的模型编写测试。但无论如何，从客户的角度来设计领域模型是大有好处的。

## 1.6 FICTION, WITH BUCKETFULS OF REALITY 虚构的案例，真实的实践

As I contemplated how to best present implementation guidance for contemporary use of DDD, I wanted to provide justification for everything I say should be done. That meant supplying not just the how, but the why. It occurred to me that looking at a few projects as case studies would appropriately illustrate why I made a certain suggestion and demonstrate how proper use of DDD will solve the challenges commonly faced.

> 当我在考虑如何以最好的方式向读者展示现代 DDD 的实践指导时，我希望对每个知识点都做周到的解释。这意味着我不但需要解释“怎么做”，还需要解释“为什么这么做”。通过案例研究，我可以阐述为什么我会给出这样那样的建议，以及 DDD 是如何解决我们日常遇到的困难的。

Sometimes it’s easier to look at the problems faced by other project teams and learn from their misuse of DDD than it is to look inward. Certainly, once you recognize the flaws of others’ work, you’ll be able to judge whether or not you are leaning in the same precarious direction, or even standing in the thick of the same morass. Then, knowing where you are headed or where you already are, you can make the precise adjustments to correct problems and avoid the same in the future.

> 有时，我们可以了解一下其他团队所面临的问题和他们在 DDD 上所犯的错误，而这比单纯地讲解 DDD 更加容易。通过学习别人的经验教训，我们可以对自己做出评判，避开潜在的错误，向着正确的方向迈进。

Rather than present a series of actual projects that I have worked on—ones that I could not discuss openly anyway—I decided to use a bit of fiction based on real-world situations that I and others have experienced. That way I could create the perfect state of affairs to demonstrate the reasons a specific implementation approach works best, or at least better, when dealing with challenges in DDD.

> 我并不打算以我曾经工作过的实际项目作为本书案例（当然这也是我不能公开讨论的），而是采用一个虚构的案例，但是里面却包含了真实的经验和实践。在这个虚构案例中，我将展示实现 DDD 的最好方式及其原因。

So it is not just fiction on which I am interested in building case studies. It is a fictitious company with a real-world business charter, fictitious teams within the company with real-world software to build and deploy, and real-world DDD challenges and resulting problems with real-world solutions to them. It’s what I call “fiction with bucketfuls of reality.” I have found it quite effective to write in this style. I hope you benefit from it.

> 在这个虚构的案例中是一个虚构的公司，公司里有一个虚构的开发团队，他们有真实的业务章程，并且有一个真实的软件系统需要开发部署，而他们所面临的 DDD 挑战和问题也是真实存在的。我发现这种案例是很有效的，同时我也希望你能从中获益。

When presenting any set of examples, we must limit the scope to make it practical. Otherwise, the volume will drown efforts to teach and learn. Examples cannot be overly simplistic either, or vital lessons would be lost. To balance this effort, the business situation I have chosen is largely based on greenfield development.

> 在这个团队进行开发的不同阶段，我们将看到他们所面临的种种问题，同时我们还将看到他们是如何解决这些问题并且逐步走向成功的。该团队所开发核心域的复杂性对于讲解 DDD 是足够的。另外，不同限界上下文之间存在依赖关系，这将有助于我们学习限界上下文的集成。然而，其中的三个示例模型并不能覆盖到 DDD 战略设计的各个方面。我并不刻意回避那些看似不相关的地方，而是在有必要给出建议的时候就给出建议。

As we peer into the projects at various points in time, we’ll see different problems and successes that the teams experience. The Core Domain that is the focus of the examples is sufficiently complex to examine DDD from various perspectives. Our Bounded Contexts use one or more others, which enables us to investigate integration with DDD. Still, the three sample models cannot possibly demonstrate every aspect of strategic design, such as occurs in a “brownfield” environment common where many legacy systems exist. I don’t completely dodge those less attractive regions, as if they are irrelevant. Whenever advisable we will diverge from the main samples and study areas where DDD guidance can be used in additional advantageous ways.

Now allow me to introduce you to the company and tell you a little bit about its teams and the projects they are working on.

> 那么现在，请允许我介绍这家虚构的公司，它的团队和软件项目。

::: tip
SaaSOvation, Its Products, and Its Use of DDD

> SaaSOvation，它的产品和对 DDD 的使用

![](./figures/ch1/team_huddle.jpg)

The company is SaaSOvation. As its name implies, SaaSOvation’s charter is to develop a series of software as a service, or SaaS, products. The SaaS products are hosted by SaaSOvation and accessed and used by subscribing organizations. The company’s business plan includes two planned products, one to precede the other.

这个公司叫做 SaaSOvation。正如它的名字所暗示，该公司旨在开发一系列 SaaS（Software as a Service，软件即服务）产品，这些产品作为一种服务被订阅用户使用。公司计划先后开发两套产品。

The flagship product is named CollabOvation. It is a corporate collaboration suite, which sports the features of leading social networks. These include forums, shared calendars, blogs, instant messaging, wiki, message boards, document management, announcements and alerts, activity tracking, and RSS feeds. All of the collaboration tools are focused on the needs of corporate businesses, helping them spike productivity in smaller projects, in larger programs, and across business units. Business collaboration is important for creating and facilitating a synergistic atmosphere in today’s changing and sometimes uncertain, yet fast-paced economy. Anything that can help propel productivity forward, transfer knowledge, promote idea sharing, and associatively manage the creative process so results will not be misplaced will be a boon to the corporate success equation. CollabOvation provides a high-value proposition to customers, and the challenge will also please its developers.

> 旗舰产品名为 CollabOvation，这是一套企业协作（collaboration）软件，并且加入了社交网络的功能。该产品的功能包括论坛（forum）、共享日历（sharedcalendar）、博客（blog）、即时消息（instant message）、wiki、留言板（message board）、文档管理（document management）、通知（announcement）和提醒（alert）、活动跟踪（activity tracking）和 RSS 等。所有的这些协作工具都旨在满足企业业务的需求，帮助他们在项目中提高工作效率。在这个经济步伐不断加快的时代里，业务协作对于企业氛围的营造起着重要的作用。任何有助于提高生产率、鼓励知识分享和增进团队协作的实践都是企业成功的促成因素。

CollabOvation 希望给客户带来有价值的产品；而对于开发者，他们所面对的挑战也是富有意义的。

The second product, named ProjectOvation, is the Core Domain of primary focus. The tool focuses on the management of agile projects, using Scrum as the iterative and incremental project management framework. ProjectOvation follows the traditional Scrum project management model, complete with product, product owner, team, backlog items, planned releases, and sprints. Backlog item estimation is provided through business value calculators that use cost-benefit analysis. If you think of Scrum at its richest, that’s where ProjectOvation is headed. But SaaSOvation plans to get more bang for its buck.

> 第二套产品名为 ProjectOvation，这是该公司的开发团队主要关注的核心域。ProjectOcation 主要用于敏捷项目的管理，使用 Scrum 作为项目管理方式，并且采用增量式的管理框架。该产品采用传统的 Scrum 项目管理模型，其中包括产品（product）、产品负责人（product owner）、团队（team）、待定项（backlog item）、计划发布（planned release）和冲刺（sprint）。对待定项的评估通过对业务价值的分析来确定。

CollabOvation and ProjectOvation would not go down entirely separate paths. SaaSOvation and its board of advisers envisioned innovation around weaving collaboration tools in with agile software development. Thus, CollabOvation features will be offered as an optional add-on to ProjectOvation. Without a doubt, supplying collaboration tools for project planning, feature and story discussions, team and inter-team group discussion, and support will be a popular option. SaaSOvation forecasts that more than 60 percent of ProjectOvation subscribers will add on CollabOvation features. And this kind of add-on sales often ends up leading to new full sales of the add-on product itself. Once a sales channel is established and software development teams see the power of collaboration in their project management suite, their enthusiasm will influence full corporate adoption of the complete collaboration suite. Due to this viral sales approach, SaaSOvation further forecasts that at a minimum 35 percent of all ProjectOvation sales will lead to full corporate adoption of CollabOvation. They consider this a conservative estimate, but one that will make it extremely successful.

> CollabOvation 和 ProjectOvation 并不是两套互不相关的产品。SaasOvation 公司非常看重敏捷软件开发过程中的团队协作。因此，CollabOvation 可以作为 ProjectOvation 的增值服务。毫无疑问，在项目计划和团队讨论中使用协作工具将是一个不错的选择。SaasOvation 公司预测，60%的 ProjectOvation 用户将使用 CollabOvation 所提供的功能，这将在很大程度上增加 CollabOvation 的销量。一旦建立起了销售渠道，而用户团队也意识到了协作工具的好处，他们很有可能购买整套 CollabOvation 产品。基于此，SaasOvation 公司进一步做出预测，至少 35%的 ProjectOvation 用户会全面使用 CollabOvation，这还只是一个很保守的预测。

The CollabOvation product development team is staffed first. There are a few seasoned veterans on the team, but a greater number of midlevel developers. Early meetings pointed to Domain-Driven Design as the favored design and development approach. One of the two senior developers had used a minimal set of DDD patterns on a previous project at his former employer. As he described his experience to the team, it would have been clear to a more experienced DDD practitioner that this was not full use of DDD. What he had done is sometimes referred to as DDD-Lite.

> 首先启动的项目是 CollabOvation。该团队中有为数不多的几个“老兵”，但大量的是些中级开发人员。在项目组的早期会议中，他们决定采用 DDD。其中一个高级开发者在他上家公司中使用过非常有限的 DDD。在他谈到自己 DDD 经验之后，我们可以看出他并没有全面地使用 DDD，他使用的其实是 DDD-Lite。

DDD-Lite is a means of picking and choosing a subset of the DDD tactical patterns, but without giving full attention to discovering, capturing, and enhancing the Ubiquitous Language. As well, this technique generally bypasses the use of Bounded Contexts and Context Mapping. Its focus is much more technical, with a desire to solve technical problems. It can have benefits, but generally not with as high a reward as including strategic modeling along with it. SaaSOvation bought into this. In its case doing so soon led to problems because the team didn’t understand Subdomains and the power and safety of explicit Bounded Contexts.

> DDD-Lite 是 DDD 战术模式的一个子集，它并不强调对通用语言的使用。此外，DDD-Lite 通常也忽略了限界上下文和上下文映射图。更多的，DDD-Lite 是关于技术实现层面的，虽然这也是有好处的，但是好处并没有与 DDD 战略模式一同使用时那么大。SaaSOvation 决定采用 DDD-Lite，然而不久之后他们就遇到问题了，因为他们并不了解子域和限界上下文。

Things could have been worse. SaaSOvation actually avoided some major pitfalls of using DDD-Lite, just because its two core products formed a natural set of Bounded Contexts. This tended to keep the CollabOvation model and the ProjectOvation model formally segregated. But that was just by chance. It didn’t mean the team understood Bounded Context, which is why the problems they did experience happened in the first place. Well, you either learn or you fail.

> 更糟糕的是，SaaSOvation 虽然避开了 DDD-Lite 的陷阱，但这纯属侥幸，因为他们的两套核心产品自然地形成了各自的限界上下文。这也使得 CollabOvation 模型和 ProjectOvation 模型得到了正式地分离，但是这也是偶然的，并不意味着团队就是了解限界上下文的，而这也是为什么该团队在一开始就遇到了问题的原因。不学就得落后啊。

:::

It’s good that we can benefit from examining SaaSOvation’s incomplete use of DDD. The team eventually learned from their mistakes by acquiring a better grasp of strategic design. You will also learn from the adjustments the CollabOvation team made, as the eventual ProjectOvation team benefited from retrospectives of the early conditions of its sister and partner project. See Subdomains (2) and Bounded Contexts (2), as well as Context Maps (3), for the full story.

> 通过调查 SaaSOvation 对 DDD 的不完整使用，我们可以学到很多。该团队从他们所犯的错误中学到了如何使用 DDD 的战略设计。同时，我们还可以从 CollabOvation 团队所做的修改调整中受益匪浅。前人栽树，后人乘凉，之后的 ProjectOvation 团队也从 CollabOvation 的回顾会议中学到不少。完整的故事，请参考子域（2）、限界上下文（2）和上下文映射图（3）。

![](./figures/ch1/own_it.jpg)

## 1.7 WRAP-UP 本章小结

Well, that’s a pretty encouraging start with DDD. I think by now you probably have gotten a good feeling that you and your team can actually succeed with an advanced software development technique. I agree.

> 好吧，现在我们有了一个好的开始。我想到现在你应该知道，你的团队是可以从高级的软件开发实践中获得成功的。

Of course, we aren’t going to oversimplify things. Implementing DDD takes real concerted effort. If it were easy, everybody would be writing great code, and we know that just doesn’t happen. So get ready. It will be worth it, because your design will be exactly how your software works.

> 当然，我们也不是在将问题过于简单化。实现 DDD 需要团队同心协力。如果 DDD 是简单的，那么任何人都可以写出好代码，但事实却并非如此。因此，为学习 DDD 做好准备吧。

Here’s what you’ve learned so far:

> 到现在为止，你学到了：

- You’ve discovered what DDD can do for your projects and your teams to help you grapple with domain complexity.
- You found out how to score your project to see if it deserves the DDD investment.
- You considered the common alternatives to DDD and why using those approaches often leads to problems.
- You’ve grasped the foundations of DDD and are prepared to take the first steps on your project.
- You’ve found out how to sell DDD to your management, domain experts, and technical team members.
- You are now armed with knowledge of how to succeed while facing the challenges of DDD.

---

> - DDD 可以为我们的团队带来什么。
> - 如何确定自己的项目是否适合采用 DDD。
> - 常见的 DDD 替代方案以及它们为什么会导致问题。
> - DDD 的基础，并准备在自己的项目中做个尝试。
> - 如何向管理层、领域专家和技术人员推销 DDD。
> - 如何面对 DDD 所带来的挑战。

Here’s where we’re going next. The next two chapters are on the all-important strategic design, followed by a chapter on software architectures with DDD. This is really important stuff to get a handle on before you move to the subsequent chapters on tactical modeling.

> 在接下来的两章中，我将讲到 DDD 的战略设计，之后的第 4 章是关于 DDD 软件架构的，这些章节对于你学习本书后面的战术建模非常重要。
