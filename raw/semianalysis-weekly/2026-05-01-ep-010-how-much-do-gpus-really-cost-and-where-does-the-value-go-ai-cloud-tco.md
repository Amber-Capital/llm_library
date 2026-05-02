---
title: "Ep. 010 - How Much Do GPUs Really Cost, and Where Does the Value Go? (AI Cloud TCO)"
source_kind: "youtube_video"
source_url: "https://www.youtube.com/watch?v=cfIm-Ply0O8"
webpage_url: "https://www.youtube.com/watch?v=cfIm-Ply0O8"
published_at: "2026-05-01"
author: "SemiAnalysis Weekly"
transcript_source: "youtube-auto-captions"
collected_at: "2026-05-02T04:38:54.871944+00:00"
tags:
  - "topic/ai-cloud-tco"
  - "topic/value-go"
  - "topic/ai-value-capture"
  - "topic/accurately-calculate-total"
  - "topic/dan-interviews-jordan"
  - "company/nvidia"
  - "company/semianalysis"
  - "company/tsmc"
  - "technology/ai"
  - "technology/gpus"
  - "technology/inference"
  - "market/cloud-computing"
  - "ticker/nvda"
  - "ticker/tsm"
  - "asset-class/equities"
  - "macro/pricing"
  - "signal/pricing-power"
  - "guest/how-much-do"
  - "guest/really-cost"
  - "guest/value-capture"
  - "guest/the-shift-to"
topics:
  - "ai-cloud-tco"
  - "value-go"
  - "ai-value-capture"
  - "accurately-calculate-total"
  - "dan-interviews-jordan"
  - "calculate-total-cost"
  - "recent-articles"
  - "ownership-tco"
  - "model-labs"
  - "flipped"
  - "script"
companies:
  - "NVIDIA"
  - "SemiAnalysis"
  - "TSMC"
technologies:
  - "AI"
  - "GPUs"
  - "Inference"
markets:
  - "Cloud Computing"
tickers:
  - "NVDA"
  - "TSM"
asset_classes:
  - "Equities"
macro_factors:
  - "Pricing"
thesis_signals:
  - "pricing-power"
guests:
  - "How Much Do"
  - "Really Cost"
  - "Value Capture"
  - "The Shift To"
  - "Model Labs"
  - "Hyperpod Checkpointless Training"
  - "Kang Wen Cheung"
  - "Zane Fong"
---

# Ep. 010 - How Much Do GPUs Really Cost, and Where Does the Value Go? (AI Cloud TCO)

In this episode we break down two of our most recent articles: "How Much Do GPUs Really Cost" and 
"AI Value Capture - The Shift To Model Labs". The script is flipped as Dan interviews Jordan, who walks through how to accurately calculate Total Cost of Ownership (TCO). They examine how reliability differences between top-tier and lower-tier providers create significant cost disparities that aren't captured in per-GPU/hr pricing, and how fault-tolerant frameworks such as TorchFT, TorchPass, and AWS SageMaker Hyperpod Checkpointless Training work.

Then, Dan and Jordan are joined by Kang Wen Cheung and Zane Fong to walk through Vera Rubin pricing and TCO, where the V stands for Value and analyze where value is accruing across the stack. The conclusion is that the value is shifting from end users to inference providers, Neoclouds as well as hardware providers. The team unveils how TSMC and Nvidia are venting large amounts of value into every vertical of the ecosystem.

https://newsletter.semianalysis.com/p/how-much-do-gpu-clusters-really-cost
https://newsletter.semianalysis.com/p/ai-value-capture-the-shift-to-model

## Summary
- So, uh 6% on the gold tier, 10% on the hyperscaler, and 20% on the silver tier.
- So, that's the $1.90 that you see on the left.
- I I like the graphic.
- And what do you think of the VR pricing?
- And this shows you the IRR.

## Metadata
- **Author:** SemiAnalysis Weekly
- **Published:** 2026-05-01
- **Source:** https://www.youtube.com/watch?v=cfIm-Ply0O8
- **Webpage:** https://www.youtube.com/watch?v=cfIm-Ply0O8
- **Transcript Source:** youtube-auto-captions
- **Guests:** How Much Do, Really Cost, Value Capture, The Shift To, Model Labs, Hyperpod Checkpointless Training, Kang Wen Cheung, Zane Fong
- **Companies:** NVIDIA, SemiAnalysis, TSMC
- **Technologies:** AI, GPUs, Inference
- **Markets:** Cloud Computing
- **Tickers:** NVDA, TSM
- **Asset Classes:** Equities
- **Macro Factors:** Pricing
- **Thesis Signals:** pricing-power
- **Topics:** ai-cloud-tco, value-go, ai-value-capture, accurately-calculate-total, dan-interviews-jordan, calculate-total-cost, recent-articles, ownership-tco, model-labs, flipped, script

## Transcript

Do you believe in
magic?
Well, I still have cautious um Mike. I
was reminded of this like Vine. Dan, do
you remember Vine before Tik Tok?
>> Yeah, that died like yeah, yeah, I
remember that.
>> Do you remember those ones of the guys
who would have the like room fan going
and they'd sing into the fan and it
sound like auto-tune? Baby girl, what's
your name?
>> [laughter]
>> Said shorty.
Shorty come downtown.
>> [laughter]
>> Kongwen this is before your time, dude.
Yeah, Kongwen doesn't even know what
shorty is. Who the is shorty?
Hey everyone, so welcome to Summit
Analysis Weekly. Jordan and I are are
switching roles. Tables have the turns
of table
this week. Um I'm going to be hosting
Jordan as he talks about a new article
that we've done on rethinking the total
cost of a GPU cluster. So Kongwen and I
spent a lot of our time working on the
total cost of ownership. But often times
this is from a theoretical or a quoted
perspective. So it's a bit like being at
a car dealership and you're saying this
thing does 36 miles per gallon, but you
know what when you take it on the road,
you know, you have your mix of highway
versus city,
the performance going to be different.
So that's what this article is all
about. Jordan's had a lot of experience
actually using GPUs and many clusters.
He's worked with dozens, maybe even a
hundred Neo clouds and so he's drawn on
that experience in terms of saying like,
hey, what is the actual on the road
performance? Jordan, yeah, you want to
kick us off and talk about a few points
in your article? Sure, yeah, thanks Ben.
Um so I think the like high-level is in
the title, which is how much do GPU
clusters really cost? The article really
explores implied costs that are not like
explicitly called out on a you know,
bill of materials or on like a purchase
order, but like maybe let's take a a
step back. When people are renting GPUs,
in many cases the price is not the same
and so you get a cheaper price from many
different providers, but you really want
to look beyond the individual price of
an individual GPU and figure out how
much useful work you can get out of the
cluster. And so what we did in this
article was introduce um a framework for
actually calculating good put. Good put
being measured as how much useful work
you can do on the cluster, how many jobs
you can run or how much inference you
can serve. And yeah, we got on the
screen for the people viewing. Basically
we try to include like line items that
people would explicitly purchase, which
is the GPUs, any sort of orchestration
premiums, the cost of storage, the cost
of networking, the cost of support
nodes. So these are CPUs. The cost of
support itself. Many of the hyperscalers
charge a premium just to give you, you
know, response times within a certain
SLA.
Uh you got to pay more money if you want
quicker responses basically. And then
there's these implied costs, which is
the time spent setting things up or
running POCs, the time spent debugging
on the cluster if there's issues, and
then good put, which is that basically
way to calculate how much downtime
you're going to have on the cluster
while you operate it. As Dan said, it's
like mileage on a car. If if some of
your GPUs are not accessible and they're
not working and there's interruptions or
failures while you're trying to run
jobs,
this doesn't just cost you time on that
one GPU, it actually costs you time on
the entire cluster because nothing can
do useful work if one GPU fails
depending on how you're setting up your
clusters. Anyway, the yeah, the article
explores all of that and well, yeah,
there's there's lots of ways in which we
can go from here to talk about maybe
like what sort of contribution we did on
the research and and what we found,
which is yeah, maybe like the the
high-level findings is that there's a
big discrepancy especially for big jobs
on big clusters between top-tier
providers that have less failures and
like a quicker recovery time from a
failure when compared to lower-tier
providers that just have a bunch of
failures and it takes them a long time
to recover from, which is previously to
this I think a lot of people didn't have
a way to put numbers to that intuition.
They'd know it'd be somewhere 5, 10, 20%
I'd be willing to pay a premium, but
exactly how much should you be willing
to pay? We think we have a way of
answering that based on this calculator,
which for what it's worth is is
available for free for people listening
at clustermax.ai/tco.
You can go and use that calculator for
yourself, input whatever values you want
and see what what it looks like under
different scenarios. Yeah, so Jordan,
how do you measure the good put? I saw
the I saw the good put calculator and
this is your good put expense
calculator, but what is the range of
assumptions that that you should use?
What has been your experience? What are
the failure modes? What are the things
to watch out for? And as you use this
calculator to run through actual
scenarios, you know, how have you set it
up and what kind of base assumptions are
are reasonable for this? Yeah, so I
think at a high-level there's two ways
to recover from failures if you're
running training jobs. I can talk about
inference in a second because there is
reasons to to run fault tolerance and
inference, but just thinking about
training for a second is it's like the
first primary way is checkpoint restart,
which basically means means you're like
auto-saving the job as it runs and then
if a failure occurs, you're going to
have to restart the entire job meaning
the whole cluster grinds to a halt and
then you start the job again from
scratch. This is the standard way to to
do things for like basic PyTorch users.
This is the torch.DCP distributed
checkpoint API and and you just kind of
save your your work. Yeah, and and
that's on screen here for for those
watching, which is like basically
showing that the more failures that you
have or the more interruptions you have
in the cluster because this can be
failures can be hard failures like
there's a uh issue with the power supply
on the server, a GPU fails, a GPU falls
off the bus, a network fails. Things
like that are like hard and immediate,
but there's also many other types of
failures that are like gradual over
time. These are ECC mirror errors on
memory. This is certain types of GPU
failure failures, links flapping on the
network where things are like slowly
degrading and you want to remove that
node from the job or from the cluster
and just keep it running, keep it making
progress. And so the second way of
recovering from failure would be for
to use fault-tolerant training
frameworks. And in the article we walked
through three of them. They're called
torch.FT, torch.PASS and AWS's
checkpointless training framework that's
built into their SageMaker HyperPod
clusters. Anyway, all three of them take
a slightly different approach, but they
kind of approximate what the Frontier
Labs have.
Uh especially torch.PASS, which is to
say a way to keep training running if
there's failures. And in our hands-on
testing that we saw and this visual on
screen is is from the torch.PASS from
the Clockwork team in their torch.PASS
past blog, basically shows a blue line
and a green line tracking up where
they're making good progress at expected
performance and then other checkpoint
restart and torch.FT scenarios where you
can keep training running, but it's
either like running with overhead on the
network or it's uh it's having to
recover from checkpoints at some
interval. And so the these first inputs
to the good put calculator is which
software framework you are using to
accommodate for these failures. If it's
checkpoint restart, it's going to be
lower good put. In other words, more
expense due to every failure or every
upgrade or every other interruption
where there's downtime on the cluster.
If you're using fault tolerance, then
you have to configure things like how
much time it how how long it takes to
fail over as well as how many idle spare
nodes you have and how much memory
overhead or network overhead you're
you're actually accommodating for, which
is part of torch.FT and part of uh
checkpointless training where they both
of them the way in which they keep the
jobs running is they basically pay a
performance penalty either by using
certain network collectives or by using
certain way to do the like in-memory
checkpointing. And so uh So those inputs
are are part of it. And then in addition
to that, there's a way to configure
based on which provider you're assessing
the average number of job failures
you're expecting to see on the cluster.
People tend to have this intuition like
let's say they're running a thousand
GPUs, they can say we tend to see five
GPU XID 79s per day. The GPU falling off
the bus code. Or we see two or we see
one or we have a 256 GPU cluster and we
see a failure a week. At the beginning
it was two failures a week, now it's one
or less failures, right? From these
sorts of pieces of intuition you can you
can back out in your mind
what the GPU level MTBF is, in other
words, how the time between failures and
then apply that to say
in general, the way we do our ClusterMax
rankings like the higher up a
a provider is on the rankings, gold,
silver, bronze, gold or platinum tier,
the more reliable the clusters are going
to be, the less failures are going to
happen and the more hot spare nodes they
run to be able to recover from a a
failure quickly. So it's it I guess in
summary it's it's relatively complicated
to calculate good put, but the result is
like
yeah, on screen what you're showing
right now is a chart that that says
basically as you increase the number of
nodes and as you increase the failure
rate, uh you move into this like red
zone where jobs like can't even make
progress as opposed to
low cluster sizes or low failure rates
where jobs can make progress, they can
do useful work. Jordan, you mentioned
ClusterMax. I think we have the rankings
up here, but you mentioned ClusterMax
and I I I two questions, well, three.
The first I want to ask you, you know,
this is obviously ClusterMax. The first
question I had was you mentioned ECC
errors, you mentioned GPUs falling off
the bus. Aren't those Nvidia problems?
Aren't they common to most hyperscalers?
Is there actually a lot of variance
between those? And if if not, then what
are the failure modes that there is
actually a huge difference between tiers
of Neo clouds? Yeah, so there there
definitely is a difference between tiers
of Neo clouds. I can focus on the GPUs
or the network to explain this point.
Maybe it's worth going through both, but
when it comes to GPUs, different systems
run at different temperatures and
different power draw depending on the
environmentals in the data center. So
the simplest example would be air
cooling versus liquid cooling. Liquid
cooling is generally more consistent
over time. Air cooling creates hot spots
and it causes GPUs to fail more often.
And uh especially with the latest and
greatest, you know, B300s,
these GPUs are really hot. They're
really power hungry. And so, a simple
example might be a provider that's
running an air-cooled data center might
experience more failures because the
GPUs are running hotter when compared to
one that's using a DLC, a direct liquid
cooler to the chip. And so, they can
they
the system at a more steady state
temperature and power draw and and uh
experience less failures. Uh another
example is like the air quality in the
data center. So, this applies a lot to
the net net working at scale. If you're
training, let's say, 4,000 GPUs and the
cluster's 5,000 GPUs in size or
something, you're trying to launch a big
job. All 4,000 of those GPUs needs to be
uh in sync um as in order for training
to progress. They need to be running
collectives across the network. And so,
that means that every single network
link has to be up. And this is where
we'll hear terms like link flaps where a
given cable or a given NIC maybe having
issues like the connector maybe dirty or
the connector may just be failing, the
light maybe degrading, like there
there's a bunch of different issues that
can actually happen physically with a
cable. Uh but the point is that if that
happens, training's going to slow down,
stall, and then eventually fail. And so,
air quality in the data center is like a
a primary example of how you can
guarantee less link failures or or link
flaps because literally just like
cleaning the cables or getting dust in
there is is an issue. So, yeah, people
who run like clean data centers and
design the physical hardware are
generally expected to to have less hard
failures like that that I'm describing.
But in addition to that, there's there's
also operational issues that a lot of
pro- providers can have, which is to
say, if you constantly need to need to
be making changes on the network,
changes on the storage, changes on the
GPUs themselves because you're upgrading
firmware or you're changing drivers or
you're reconfiguring the network on the
physical layer because you're trying to
expand add somebody else into the
cluster. These are things that impact
your existing customers because it
requires taking downtime on the cluster.
Anybody who's run GPUs for like six or
more months has been contacted by their
provider before to say like, "Hey, can
you accommodate us doing something? We
need to reboot this. We need to unmount
your storage. We need to, you know,
maintenance window this weekend. Please
don't run jobs for this amount of time."
And that's covered in the SLA in the
contract. It's like, you know, let's
say, 8-hour maintenance windows over a
certain period of time. But providers
who are not experienced running this,
they these maintenance windows go longer
than expected. They happen more often
than needed. And those interruptions,
even if they're not like actual hard
failures in the data center, can still
cause you to have to, you know, stop
jobs or restart them or just generally
like not get as much useful work out of
your cluster as you're expecting. The
other thing, Jordan, you mentioned Torch
Pass, right? Let me let me share the
graph again. And you you mentioned that
that actually goes a long way towards
ameliorating the issues of having to
checkpoint and restart. So, the question
I would have is doesn't this equalize um
doesn't this equalize the performance
across Neo clouds? Couldn't it paper
over those those kind of differences or
is that not the case? Yeah, it it
potentially can. And and that's why
Torch Pass is a licensed product that
the Clockwork guys are selling to many
of these labs to try to, you know, get
people to pay a little bit of money in
order to be able to run on some of these
lower tier providers. I think it totally
helps, especially for um like
predictable failures like these
maintenance windows I'm talking about
where there might be a rolling upgrade
or ECCs on the like memory on the system
or like a reboot that's scheduled or
something. But as it can't Look, it it
can recover from hard failures, but it
can't necessarily accommodate for many
hard failures all at once. And and
nothing can accommodate for, you know, a
switch outage or a file system unmount
or like something major. And so, there's
a there's a level in which the software
framework on a properly run cluster will
help improve goodput and therefore
you'll have a better TCO. But it it it's
not like a silver bullet to solve all
potential issues from a provider. It's
just it's it's something that the Torch
Pass is the closest that we've seen to
what Frontier Labs are using at this
scale. And if everybody running 100,000
GPUs is using it, then what's the
threshold at which you need it? We think
it's generally just getting lower over
time as it becomes easier to adopt the
framework, the amount of code changes
you need to make is lower, and just the
amount you need to think about the
system infrastructure is lower. And so,
is that limit like a 2,000 GPU cluster
or 1,000 or 512? We know people running
fault tolerant frameworks on a 1,000
GPUs for for job sizes in like the 128
to 256 GPU range. So, it kind of feels
like a why not do it point at the at
this point? Why not explore? And that's
kind of why we wanted to introduce that
section of the article to just, you
know, motivate everybody from like the
licensed products like Clockwork Torch
Pass to the open source stuff like Torch
FT and and all the users or potential
contributors in the ecosystem to think
about this more. And yeah, yeah, help
help in some ways help the providers
improve or help accommodate for issues
at the providers' level that will allow
more people to be in the business. Let's
uh pivot a little bit more towards
talking specific dollars and cents. I
thought it might be interesting to talk
briefly through the differences here. Uh
you know, I see it's a very significant
difference. And I know below we actually
have some useful charts. So, Jordan, I
was wondering if you could just talk us
quickly through the difference. And then
I'll go to the um
the bar charts where you actually show
what accounts for that difference. Yeah,
let me uh let me steal the screen here
for a sec. This will be
potentially interesting. Um
As Dan was saying, there's there's a a
TCO cluster calculator scenario on
screen here where we started out by
saying this is going to be a cluster of
5,184 GB300 and VL72, latest and
greatest GPUs.
And what we did for this scenario is
just keep all the the pricing the same.
And we called the three providers gold
tier, hyperscaler, and silver tier. And
uh the pricing's four bucks an hour. And
so, there's differences in the pricing
of storage. There's differences in
network services and CPUs.
Um there's major differences in support
if you want to get good support from the
hyperscalers. But the biggest
discrepancy
when you think about the pricing
difference
is in this goodput tier where on the
gold tier providers, we come to a a
number of a 6.14% goodput premium.
Hyperscaler's at 10.53%
and silver tier's at 20.91%.
And as you said, Dan, like when you
scroll down, if I attribute this this
pricing discrepancy here, if I just do
silver versus gold tier, what this means
is that like 92%
of the difference in price is due to
goodput when I compare those two, not
storage, not debugging, not setup time.
And a large percentage of this
discrepancy about 40% when we look at
the hyperscalers. And so, what did we do
to arrive to those numbers? Well, we
when we click over to goodput expense,
the scenario that we went through was we
used fault tolerant frameworks like
Torch Pass for the gold tier. We used a
fault tolerant framework called
HyperPod, a checkpointless training to
represent what the hyperscaler might be
running in this case, AWS. And then the
silver tier has a checkpoint restart.
And the silver tier also has a a 15,000
MTBF, which means they're experiencing
slightly more failures than the gold
tier and the hyperscaler, which are at a
dozen MTBF, meantime between failure.
And that number is GPU hours. So,
um the uh maybe the more interpretable
way of doing this is like if there's
5,000 GPUs in the cluster, we expect
there to be a hard failure every 4.8
hours on the gold tier and hyperscaler,
uh but every 2.9 hours on the silver
tier. And so, the the calculation is
done, you know, based on a formula that
we created to say like basically how
long are you doing work after a failure
occurs and not identifying it? That's
wasted across the entire cluster. How
long do you actually need to fail over?
And then how long does it take you to
replace that failed node itself? Because
for as long as you can't use the failed
node, even if it's not part of that
training job, well, you're paying for it
to just like be out of service and not
used for other jobs, research,
inference, things like that. The other
thing that's that's really important
here is that we configured the average
job size to 4,000 GPUs on that 5,000 GPU
cluster and the blast radius to 64,
meaning that you uh
have 64 of the 72 GPUs in the rack that
are being used for this. And so, yeah,
you you add that all up, you multiply it
together, you take that in this case for
HyperPod checkpointless training of 5%
memory overhead because they need to in
order to provide fault tolerance, you
need to take some of the uh
um GPU memory away, uh which
impacts the batch size that you can run
at during training, basically. So, your
training is going to be slower. Uh
that's what that 5% memory overhead
does. And uh and that filters down,
right? So, uh 6% on the gold tier, 10%
on the hyperscaler, and 20% on the
silver tier. Why I wanted to do this
live is just because we can adjust this
to show things that are bigger. In the
case of a paper from Meta, uh
uh the Llama 3 behemoth runs with the
4.5 billion parameters. Uh they were
running 16,000 GPU jobs on a 20,000 GPU
cluster. And so, just to point out what
this would look like at this scale, if
you're running fault tolerant, you're
losing 21% to goodput. On the Torch Pass
scenario, 26% in HyperPod
checkpointless. And in a checkpoint
restart scenario,
80% of your cluster, you're effectively
having a failure every 0.8 hours on a
cluster that size. So,
you know, you're basically having a
failure right after you take a
checkpoint every on an hourly basis in
those scenarios. And so, it just goes to
show you like how sensitive these um
this
to how big the cluster is and how big
the jobs are, leading to the conclusion
of like that's the motivation for why
people are actually using these fault
tolerant training frameworks when
they're running at this scale. Yeah, and
and you guys concluded in the article
with with a very interesting gross
margin sensitivity. Let me put it up on
screen just to to keep keep uh
discussing dollars and cents. And Kong
Wen and Jordan, can you talk through a
little bit about how we how we can use
this to figure out effective margins and
how we can use this framework to think
about gross margin sensitivity? Yeah,
I'll I'll start and then Kong Wen can
can jump in, I guess, yeah. Um I think
they're key the key point is just like
however many failures you're
experiencing impact inference, too. I've
only talked about uh training so far,
but as you have more nodes down in the
cluster, you're able to serve less
customers total. That's the the basic
conclusion for inference providers. And
Kong Wen, you did this analysis, so like
what does that actually look like in
terms of their margins? Yeah. So, if I'm
bringing your attention to the column,
we can see it's token selling price,
dollars per M token. That refers to,
let's say, a provider and token, you
know, how much it is selling their
compute or the inference that they
provide on a dollar per million token
basis. And if I bring your attention to
the row, that is the two figures that I
managed to take from Jordan's
calculations. And the reason why I chose
this range of numbers is that, you know,
for his 200 doing about, you know, a
year you know, one-year contract today,
you know, maybe you can get somewhere
around, you know, $2 on the GPU rental
price.
Uh factoring into, you know, what Jordan
uh mentioned worked on on the good put
expense. What you're seeing there's very
little additional good good put expense
on top of the GPU rental price. So,
that's the $1.90 that you see on the
left. And if I can bring your attention
all the way to the right, where you can
see it goes all the way up to $3.00 and
10 cents. That would be, let's say, you
have a hyperscaler compute provider.
Yeah, your overall cost is up to 1.5
times more on the total good put expense
basis. This is what the margins can look
like. So, if let's say you are able to
sell your tokens for $3 today, and you
have, you know, CoreWeave or Platinum
supplier, Platinum compute provider,
offering you a $1.19 good put expense,
you know, you make pretty good margins
at 28%. But if let's say you're going to
a small hyperscaler compute provider,
the same $3 token that you're selling
can actually yield you a negative 25%
gross margin when you take into account
the total good put expense that Jordan
did out. Yeah, so to use to use real
numbers, I think you have around an 8 to
10% I want to say between if I look at
gold till versus versus
silver, right? It's about like I think
it even be 10 to 15%. Is that right,
guys? Maybe if you want to pick a couple
points, Kong Wen, to illustrate where
you would land in the column, right?
They could both charge 210, but um
should we compare 210 to 230? Like this
would be a gold and this would be a
silver. Is that about right, guys? I
think it can be
So, in inference, it's a little bit
different in terms of how you calculate
things.
And I think that's fair to say gold and
silver would be 210 to 230 or something
like that, but
I've seen a lot of inference providers
because it's a more like naturally fault
tolerant workload, single node
inference, they're willing to go way
down the list and use any spare GPUs
that they can find
as long as it's cheap. And then a lot of
them have have commented that, you know,
they kind of learned their lesson over
time that it's not that easy to make
money on cheap GPUs if they're never
online. You have to chase providers all
over the place to try to get them to fix
things or to get them to credit you back
for downtime or things like that. So,
it's I think in some ways it can affect
the margins of the business, in other
ways it can just affect your peace of
mind as you're trying to operate the
business in some some ways, too. So,
being able to not have good put expense
be a question mark of how much it's
going to cost you and have it be like
pretty reliably something that you can
actually consider and you can predict,
not to say it's ever going to be zero,
especially for big clusters and big jobs
as we're saying, but something that you
can accommodate for, I think, is the
goal for anybody who's trying to build
these like complicated systems with lots
of GPUs in them. So, it could be a
situation of pay 230 because you know
you're going to get 230 of good put
as opposed to paying 210 and then you
land in the 270 much later.
100%, yeah.
>> After much aggravation. Yeah. Yeah. And,
you know, potentially a long-term
contract in order to to like lock down
those GPUs right now. You're In some
ways you're kind of committed to these
providers. So, like I said, I think
inference is is in some ways a little
bit less sensitive to good put itself,
not to not the margins to good put, but
the workload itself is like in many
cases single node, so the blast radius
is just eight GPUs that fail at a time.
And the ability to adopt a software
framework that's fault tolerant is
almost required to run inference end end
points because you have to be able to
load balance and and retry requests that
have failed. If you're going to have a
thousand GPUs serving customers, some
customers are get routed to different
GPUs, right? That that's kind of like a
very basic feature, whereas people who
have been training models, even at
Frontier Labs where they've got all this
infrastructure built, or smaller
companies, academia, training smaller
models to learn things, they go to a
startup where they're like trying to
train the next generation of models and
they've got all these great ideas,
suddenly they need to become like
systems engineers to be able to actually
run it at scale.
Whereas previously they were supported
by a team of like, you know, 20 people
who are managing this fault tolerant
framework for the entire organization.
They don't even need to think about what
cluster they run on, let alone, you
know, which versions of software and
which versions of like the, you know,
GPU drivers and stuff they're actually
running on to make it work. Question
that I had was, you know, why is there
room for hyperscalers to, you know,
price a lot smaller on, you know, the
GPUs, the orchestration software, the
storage, you know, the support, you
know, why why why are they not, you
know, instantly competed out by, you
know, gold tier provider or a silver
tier provider? It's a good question. I
think um in some ways they are competed
out. Like you look at
how successful CoreWeave and Nebulous or
Crusoe or like Lambda even has been at
selling like all of their new GPU
capacity. They they are like sold out
for the near future. Um and they're get
they're now getting like long-term
five-year committed contracts measured
in the billions of dollars, which just
means the end of the business is going
to be around to stay. So, I think that's
a lesson that the hyperscalers have
learned. In fact, I know that's a lesson
that the hyperscalers have learned to
kind of look at that and say we missed
something here. People don't need these
like expensive feature-rich storage
options. They just need S3 to work or a
file system to work. They don't want to
be nickeled and dimed for every single
compute node and dashboard and support
ticket that they open. They they just
want a good experience, right? So, in
some ways like Neo Cloud were just being
successful in proving that that's not an
issue, but on the flip side, the
hyperscalers have also served sold
plenty of GPUs at relatively high
margins. Their revenues are increasing,
their gross margins are increasing. Like
they they're doing fine, too. I think
it's also hard to draw conclusions and
say that there's like clear winners and
losers in the Neo Cloud industry right
now when demand is so high and that like
masks over a lot of
um issues from both hyperscalers and Neo
Clouds, where Neo Clouds who had poor
reliability and lost customers have been
able to find replacement customers for
that capacity because there's so much
demand and they they're able to find
somebody to accommodate for it. And
hyperscalers who were pricing too high
have now seen a lot of people buying
those GPUs at high prices because they
can't get them anywhere else. And
hyperscalers who
um
were charging a lot of money for like
feature-rich storage, like their S3
object, you know, options. Well, those
features pay for themselves in some ways
with like high availability and
replication across
availability zones and stuff. Like
people are willing to pay a premium for
certain features in the hyperscalers.
And you're always going to have peace of
mind that AWS or Google or Azure like
knows how to run a clean data center.
Yeah. Yeah. Yeah, it's a bit off uh case
with like a rising tide lifts all boats.
Right now, demand is so strong.
You know, people can charge whatever
they want, you know, they're they're
going to find a customer for it for now.
For now, yeah. Are you calling the top
sometime soon, Kong Wen, or you riding
it out with us? Is it Is this time
different, Kong Wen?
This time is different. The famous
forward Ben said with me. Yeah, we're
calling back to previous podcast there.
Um that's our favorite question. Is this
time different? Well, uh speaking of
this time is different, I think we have
we wanted to share some interesting
evidence why this time really is
different.
>> Let's talk about flops and flops per
dollar here. Okay.
Um so, let let's talk about why this
time is different.
>> [music]
>> While Zane has appeared. I I like the
graphic. Very very cute. Yeah. Yeah, so
Zane, I mean, you you came from private
equity, and so I think equity research
is arduous. I'm not sure what we would
call private equity. Like I could think
of some non-PC stuff. We probably
shouldn't say it, but like
>> [laughter]
>> Yeah, for sure. For sure. I thought
arduous and and there's a lot of back
and forth as well. So, it's it's always
it's always like an iterative process.
Like one boss says one instruction set,
and then you go and carry that out, and
then you go back to the same boss or
maybe a different boss, and then, you
know, it's a it's an iterative process,
I would say. One thing about the models
is that I can like, you know, let's say,
you know, Ben you're from Amazon, so,
you know, you say like probably every PC
you do, 10 10 rows of model, you you
model 10 lines and then you're done. But
I see in private equity it's like a
thousand and nine
uh models, you know, 50 sheets, you
know, How is crazy? Yeah. Yeah.
It's It always depends on what's what's
required for that particular deal, but
yeah, it gets it gets pretty crazy at
times and I think it's granular is
another word to describe it.
Let's talk a little bit about the
specific tasks. So, from last week
you'll known at SemiAnalysis we have an
Agented Director of Research,
and we're talking about why this time is
different and I think in the prior slide
we were pretty good illustration of of
why this time is different. And you want
to go to that table of the tasks and
ROIs? Yeah, Zane, can you talk us
through this and what we're seeing here?
Yeah, so
this this table is broadly speaking like
the the cost for AI to do one of our
real workflows versus like humans,
right? And I think when we say like AI
just like token cost of course we're not
saying that we'll just fully throw it to
the
to cloud and then we'll not do anything.
But I think like for us to supervise and
throw in a proper prompt and to
to look at the results. This is roughly
the cost and the the time it takes for
tokens versus humans. Right. So, if I
can maybe the fourth item here is
something that that we'd be more
familiar with. So, initiating on a new
company, in this case we chose HPE
Hewlett Packard Enterprise. And in
particular, you know, we just wanted to
look at their road map and balance sheet
as well. So, say for a token cost it's
roughly $50 to do it in cloud. I think
for a human that's assuming about $50
an hour. I think this would take easily
like 40 hours to go through all the
different
like
annuals, quarterly's, earnings calls
scripts, uh presentation. I think 40
hours is is
is is not far off the mark. And so, if
we compare in terms of like ROI like
human cost over token cost it's about 36
times as well. And right below that you
see like four or five for the tasks that
that will be common. So, maybe one thing
that's fairly common in the public
markets as well as should be the
earnings recap. So, that's the model
earnings recap. And you know, in
particular wanted to look at some of the
up-and-coming technologies which is CXL
memory switching and then CPU as well.
So, when we look at that, yeah, it's um
it's not even a comparison that like 282
on the token side versus I think that
would have cost me about like $16 to do
in person. So, you can see that ROI
across all these various tasks that
we're looking at really pretty high. And
we're not trying to eliminate. We're
we're trying to refocus their time on
stuff that's not data entry, not control
F on various transcripts. We're we're
we're trying to think bigger and and and
spend our time on on higher value-add
stuff. And then also just cover more
ground cuz there's always a lot of
companies that you could have been
tracking, but you're not just because
it's too costly and you don't have the
time.
>> Yeah, yeah, for sure. And I think the
last item here I just to pull like past
annual financials and
>> [clears throat]
>> uh year-to-date financials as well,
right? So, that's maybe 5 years plus
like three or four quarters in this
case. That that's mainly like a data
entry job, just making sure stuff lines
up if you have line up and changes over
the years. But yeah, I think this would
have taken a regular human analyst maybe
like 3 hours, but um AI is able to do it
for us in just like this took probably
like uh like 3 minutes and uh $1.87 in
token costs. So, you can see the
disparity there. And it's just like you
said, um taking out the more menial
tasks like data entry so that we can
focus on other stuff as well. Let's talk
about how the value's also accrued. I
think there's multiple layers. What we
talked about a recent article is how
there's so much value being accrued.
We've already shown how the users are
accruing a lot of value. Kang Wan, can
you talk a little bit about how
Anthropic and the inference providers
have actually picked up a lot of value?
I think we've got a great margin slide
here. See, so when I'm thinking about
this side right
Yeah. So, as you can see a pretty clear
trend how Anthropic ARR has accelerated,
you know, I'm sure everyone heard the
you know, blockbuster numbers, you know,
Anthropic reached 30 billion ARR, you
know, over the last couple of months.
And this margin meeting will continue to
accrue to Anthropic as they provide the
application layer, you know, what we are
directly benefiting from.
You know, we forecast that they can go
up to almost 300 billion in revenue at
51% gross margins. You know, this this
seems like a pretty good business to me.
What what's really driving the margin
improvement actually is the fact that
the throughput has been increasing
continuously, whether through software,
whether it's through better hardware,
but they haven't been decreasing the
prices. They've just been offering more
expensive stuff the whole time. I think
Kang Wan is showing uh generation to
generation how things have improved so
much. And we can flash some of the
generation to generation graphs as well.
And so, it's been really interesting. I
think one and then we've also talked
about how good puts been improving,
right? So, there's a lot of value being
created in just pure good put. I think
the next thing that's worth discussing
is value accruing. Are the system
providers capturing their fair share of
value? Kang Wan, what do you think? I
think that's uh you know, a nuanced
question considering that we are still
quite early in the I would say the agent
AI revolution, right? So, then we we
were talking you know, a couple of
friends on Telegram you know, they're
saying like you know, the banks aren't
using AI at all, but you know, from from
where we see from our vantage point, you
know, it almost looks like a no-brainer
thing to to be using AI. So, for now it
it seems like if the profit pools keep
accruing to your your your inference
providers, it only makes sense for it to
to release back to the upper end of the
spectrum, right? Where you think about
your OEMs, you think about um your
system integrators, you think about your
hardware providers, you think about your
foundry equipment makers. So, right now
it seems like this is important for them
to move up. Let's look at the scatter
plot of that, right? How how is how are
things looking? This is the system
pricing, right? And what do you think of
the VR pricing? So, this trend line that
we're drawing out shows the cost per
flop across different generations of
when it's released. So, you can see H100
released at December '22 initially had a
about ATC per P flop of about 80 cents.
And you can see most most GPUs tend to
cluster tightly around this line until
we go to VR. So, we can see VR seems to
be a bit of anomaly compared to to you
know, what the trends we expect to see,
right? It seems to
have
fallen off quite sharply in terms of its
TCO per P flop,
you know, way below the trend line.
Even if you give it a 40% hike on the
summer price that we are modeling in
today, and
you know, the cost that we have put, it
seems to just barely reach the the trend
line. So, that's also another argument
that you know, maybe the hardware should
be accruing more of this value. Like I
think the big thing that that you guys
are talking about here is the
denominator is flops. And of course
flops are improving, but the the concept
of inference acts is that the amount of
useful work you get out of the GPUs is
actually exponentially more than the
flops increase. Like if flops go up 2x,
we're not seeing throughput go up 2x.
We're seeing in some cases it go up 15x
generation to generation because of all
of the improvements beyond flops. There
are flops improvements, but there are
efficiency improvements on the
interconnect network like 18 times
faster interconnect with NVLink going to
72 GPUs instead of just eight or the use
of prefill decode, uh disaggregation, or
the use of YDP, or the use of
multi-token prediction. All of this
software which has been optimized for
Blackwell first because it's the latest
and greatest is
you know, it it gets even better or
worse depending on your perspective if
you consider useful work on a benchmark
of tokens per second instead of just
flops. But make the point with flops and
I think it just gets stronger. I totally
agree. And the reason we did flops is
cuz we don't yet have inference acts for
VR. I think we could proxy it with
memory bandwidth. What you're going to
find it is this this you'd have to
honestly, Jordan, we'd have to make this
a log axis. That's how quickly that's
how fast the improvements in inference.
So, whatever point we're making here,
it's going to be even more powerful. Um
and I think there's you know, to your
point there's even more uh left on the
table from system vendors. I think
you're going to find that it's going to
be well below trend even on a on a
linear line on the log chart. Yeah, Kang
Wan, um you want to annotate some of
these points here and kind of illustrate
what we're what we've been thinking
here? Yeah, so this chart is similar to
what we just showed, so but we're still
thinking about it from the TCO
perspective. We're thinking about it on
a rental price per P flop. In essence,
this would
probably illustrate how inference
providers who are renting compute how
they would be thinking about what they'd
be willing to pay on a you know, rental
price per P flop basis. So, you can see
once again older generations of
Nvidia GPUs, they seem to be tightly
scattered around this trend line that we
have drawn out from P100 to B2s to B3s
and GB300s. But VR stands out as a very
unusual outlier. So, GB300s today, if
you deploy it at the current market rate
with the current server cost, you get
about 15.3% IRR.
If you are trying to recreate the same,
you know, IRR with VR server price at
15.3% over 5 years, it implies a rental
cost that gives you a rental cost per P
flop all the way down at about 28 cents
per P flop. So, that's way lower than
the trend line that we have drawn out
here. So, even if you hike your server
price by 40%, that gets you closer to 40
cents per P flop.
Even if you hike your server price and
more than double the rental, you know,
you get a good 38% IRR that seems to
still fall below the rental price per P
flop
trend that we have drawn out. Yeah, and
one So, what we did, uh we actually
combined this into a framework on the
next slide. And this is what we call one
chart to rule them all.
And the reason is because what we do is
there's two constraints, right? There's
a lower bound and upper bound. So, the
upper bound is uh Kang Wan just showed
you how if you're renting a GB300, then
you're paying a rental price per flop of
70 cents. So, you're obviously never
going to pay more for a VR. So, a VR has
17,500 peta uh uh
teraflops of FP8 dense. And so, that
works at about a $12, it works out to
about 70 cents. So, you never pay more
than that. On the flip side, a Neo Cloud
is never going to put in a VR system if
it's not above the hurdle rate. So, you
can see here, this orange curve actually
forms the supply curve in a way. It's
technically not a supply curve because
there's no quantity. Um
this shows you the variety of pricing.
And this shows you the IRR. On the
x-axis, you've got IRR. So, as you slide
along the orange curve, what you're
seeing is price is higher and the IRR
for the Neo Cloud is higher. So, in
other words, as you slide up into the
right along the orange curve, the
pricing power for the Neo Cloud is
stronger. As you slide, conversely, down
into the left, it it's weaker pricing
power for the Neo Cloud. And why why why
is this the one chart to rule them all?
Because there's another there's an
implicit third dimension here. And
that's the different curves. So, you can
see the gray line is if there's a 40%
hike in server price. So, a shift of the
curve up and down
is reflected is reflected
um because of the server price change.
So, when the server price changes, you
can see that for a given IRR 15%, you
have to charge more. So, at a 40% hike,
a Neo Cloud have to charge $6 to make
the same IRR. Um but what we show is
it's still even if they did that, it's
still well below trend. And uh the prior
chart column showed even with a 40%
hike, it's still well below trend in
flops. And it's probably even much
further below trend if we looked at an
inference throughput basis.
If you have a shift Well, so what this
shows you, this gap here between the top
left corner and the orange chart is the
value that the server provider is
leaving on the table. We already talked
about You know, I almost think we should
maybe edit this out or just not release
this because we certainly like our our
80 times ROI. So, we're almost arguing
against this, but I think we can I think
we can take a uh a 50% higher pricing
cuz the ROI is just so high. And I think
that's the point we're trying to make is
is there's so much value being created.
There There's so much talked about
memory price increase, but like just
think about all the value that's being
created. What do you think, Jordan? Is
this a confusing chart? Cuz I think it
takes a little while to
understand it. Yeah, I think I've been
so conditioned for the last few months
and understand some of it. I I would I
would stress to everybody looking at
this that they're making the point based
on rental price per petaflop ignoring
all of the improvements of inference
that have come with the latest
generation. So, if you just do this chip
by chip and the pricing that we've seen,
the result is like a few different
options. Jensen is feeling really,
really benevolent. Jensen is really,
really scared about his competition. Or
somebody doesn't really understand what
they're doing on the financial side. And
none of those three make sense to me.
So, I don't know what the reality is
here. I think um it's interesting to
consider that despite the fact that
people are are going to look at this and
see Groq was almost at a dollar an hour
just 6 months ago.
$8 an hour GPUs. They're going to like
visually look at that, not understand
not compute the fact that a GPU is so
much more expensive from a Neo Cloud.
But then they're going to turn around
and see Anthropic gross margins
improving, Neo Cloud gross margins
improving, and people funding a whole
bunch of projects with a ton of capex as
people keep making investments in this
space. So, we'll see. I mean, do you
want to motivate Jensen to hike the
price even higher? Is that a good result
for you, Dan? Well, if if if it was
uh
Blackwell's was B for benevolent, then
is it B for valiant? No, hike the
prices.
It's V for value.
V for value, okay. Yeah, actually V for
value, there we go. V for value. That's
a good soundbite.
I like V for value. Yeah. I mean, to
some extent I I think Jensen will spin
it as being benevolent, to be honest.
And and I think I think that's the
closest to the truth. I mean,
the guy is VR. He's very rich. So, I
don't know how much more That's another
good soundbite. So, yeah. I don't know
how much more money he needs to be
making.
>> [laughter]
>> That explains it actually, Jordan. I
think that's the explanation before he's
already VR. Yeah, it's it's already VR,
man. No, I think Yeah, I think I think
he he's got I think it's some
combination of them not understanding
the financials with the pricing and and
not pricing to value and instead pricing
to the component inputs and doing a 75%
markup standard. They do it for every
component. Doesn't matter if it's a
transceiver with no value or a GPU with
all the value, they're all marked up the
same. And then I think um I think he
he's more concerned about
TPU and Trainium being used to power two
of the best models in the world in
Claude and Gemini than he really would
like to admit. I think those are serious
players in the industry right now. And
um if he does jack the price and
everybody else doesn't, and there's some
world
12 to 18 months from now where there is
a lack of scarcity and you know, an
abundance of compute options for people
to choose from, then they will run to
the ones that are the cheapest per flop
or per
uh
you know, bit per second on memory
bandwidth or per token per second on a
real benchmark. I think I think Jensen
regrets pushing Anthropic into the
welcoming arms of AWS with Trainium and
then having that collaboration really
result in a uh world-class Trainium chip
that can run the biggest models in the
world and and others can use. And TPU is
already world-class. So,
uh intentionally do that to anybody else
in the future when you've got that. And
you've got pressure from Chinese chips.
And
you know, you've already admitted you
missed something by acquiring Groq and
doing the SRAM thing, which we're not
even considering here with the token for
value stuff. I mean, these are
unstructured thoughts at the end of the
podcast. But uh
That's what That's what jumped to mind
here. We'll see. Dan says Jensen jacked
the price. All Neo Clouds who receive
pricing from Jensen after today on,
please contact dan@semianalysis.com to
complain.
Yeah, we've got uh you know, your call
is important to us.
We call it like we see it.
>> Press one to request a callback. All
operators are currently experiencing
high call volume. Press two to file a
Jira ticket.
All right, back to the phone lines,
everyone. All right, so let's uh we're
signing off then, Jordan, unless there's
anything else you want to add. No, this
has been great, guys. I'm All right. I'm
excited to see the article in full now,
actually, after seeing this. And
hopefully we can publish both of these
roughly around the same time.
Should we literally title it that, why
this time is different? Or no, V for
value. Okay, I think we're going to
title it like Vera Rubin, V for value.
Yes, Vera Rubin is V for value. Vera is
V for value. Not not Vera and compares
to CPU. Vera, no. Yeah. All right. So,
signing off. Thanks for everyone for
joining us this week.
And we will uh
catch you next week. Catch you on the
next one, guys. Good job. All right.
Bye. Bye.
