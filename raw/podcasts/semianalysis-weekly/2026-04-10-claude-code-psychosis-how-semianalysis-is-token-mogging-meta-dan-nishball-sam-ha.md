---
title: "Claude Code Psychosis: How SemiAnalysis Is Token Mogging Meta(Dan Nishball, Sam Harshe,Jordan Nanos)"
source_kind: "youtube_video"
source_url: "https://www.youtube.com/watch?v=MhedMJqzReo"
webpage_url: "https://www.youtube.com/watch?v=MhedMJqzReo"
published_at: "2026-04-10"
author: "SemiAnalysis Weekly"
transcript_source: "youtube-auto-captions"
collected_at: "2026-04-18T17:18:37.182658+00:00"
tags:
  - "know"
  - "right"
  - "it-s"
  - "yeah"
  - "think"
  - "actually"
  - "model"
  - "kind"
  - "going"
  - "people"
  - "using"
  - "time"
---

# Claude Code Psychosis: How SemiAnalysis Is Token Mogging Meta(Dan Nishball, Sam Harshe,Jordan Nanos)

Jordan Nanos (@jordannanos) Daniel Nishball (@dnishball) and Sam Harshe (@sharshe02) break down how SemiAnalysis is deploying Claude Code agents across its Singapore office at a scale that outpaces Meta on a per-employee basis. 

They cover the practical workflow changes, the trust and reliability questions that come with AI-generated analysis, and what it actually takes to build an agent swarm that does useful work. The conversation also gets into cybersecurity risks and where AI model development is headed next.

00:00 - Introduction and Team Dynamics
09:10 - The Evolution of Agent Utilization
14:49 - Conference Insights and Research Efficiency
15:58 - AI's Role in Learning and Analysis
21:13 - Trust and Reliability in AI Outputs
27:04 - Market Impact and Adoption of AI Tools
32:14 - Cybersecurity and AI: Opportunities and Challenges
39:32 - Future of AI Models and User Experience

## Summary
- Thank you.
- The And the key thing, right?
- So um you know, and the thing is, right?
- I like that.
- Like, here you go, right?

## Metadata
- **Author:** SemiAnalysis Weekly
- **Published:** 2026-04-10
- **Source:** https://www.youtube.com/watch?v=MhedMJqzReo
- **Webpage:** https://www.youtube.com/watch?v=MhedMJqzReo
- **Transcript Source:** youtube-auto-captions

## Transcript

I just have a lot of things I prepared
to show and tell and that I'm going to
share. Um, this is our our intern.
>> [laughter]
>> Oh [laughter] my goodness. I'm like,
"Hey, you know, I know you guys say we
don't need interns, but like the script
is flipped. The intern's the boss now.
Like Yeah, man. How the turns have
tabled.
Hello everyone. Welcome back to
Semianalysis episode number eight. Uh,
we're going to talk about all of the
ways in which Claude code psychosis can
be used for profit today. Uh, with me is
Mr. Daniel Nishball again, back at it,
calling in from Singapore. We're going
to We're going to run through exactly
how many agents the team has built at
our biggest office. And uh, new member
of the team, Sam Harsh, calling in from
San Francisco, just south of me. Uh,
guys, welcome to the show. Thank you.
Excited to be here. Awesome. Cool. So,
look, it's been a big week for Claude
code. We We've been using it a lot. We
put out
some bait. Dylan tweeted today about how
we've been spending on Claude code, how
we're consuming more than twice the
amount of tokens per employee that Meta
is. Clearly have much more psychosis
than those guys do. And we also uh,
token mogging, I believe was the
technical term. And then we also We also
saw a nice release from Mythos from
Anthropic, which uh, yeah, we can run
run through in a little bit of detail.
Dan, what's new, man? You were You were
just telling me you got the agents ready
to go.
Yeah, yeah. We're um, we've been
stockpiling I think equipment at a scary
pace, mostly because Ray's been scaring
us into, you know, buying everything
like laptops, iPhones, and Mac minis,
right? Yeah. So, you know, we've got we
got two of them in the office, which
we've been kind of um, playing around
with stuff. Probably move them to proper
service at some point. But it's all
about like how how we're using Claude
code, right? And um,
you know, a lot of people say Claude
code means you don't need interns
anymore. You know, it's sort of like I
would say the flip the script is kind of
flipped, right? Let me sort of show you
uh, you know, our intern. So,
um, you know, like the script is kind of
flipped, right? Now now the intern is
the boss uh, of the agent swarm. And so
this is this is Terrence. He's a NTU.
You know, there are three universities
in Singapore. NTU is is a great AI
program. So, he's actually um, an AI and
uh, accounting major, right? Dual
majors. His job is teaching the agents
how to how to do um,
you know, actual financial modeling. Um,
so I'll kind of introduce you to a
couple of the agents so we've been
using. Um, so let me
>> While you're doing this, while you're
doing this, while while you pull this
up, that was just a a picture from We
got to see the nice back of Terrence's
head and he had five different terminals
up on across three different screens, I
think. So, now we get a live demo. Yeah,
yeah. So, this is the kind of stuff
Terrence does all day, right? Like he's
the boss. So, this is um, you know, this
is uh, what we call Wags. It's our
agentic director of research. You know,
the problem statement is, you know, we
got to cover a really broad industry
across networking and TCO, you know,
four to five switching relay companies,
dozens of optical transceiver supply
chain companies. And we can't just do a
full model on um,
you know, each of each of these
companies per quarter, right? So, you
know, what this is, right? Is uh, you
know, on the left you'll see uh, this is
what we call you know, Wags is a
director of research doing supervisory
function. And what what now we're doing
is we're actually uh, initial initiating
coverage in AOI, right? So, the key
problem is
you know, if we talk about like agents
before we, you know, kind of step back
and talk about why we're doing this, you
know, you're you're mainly limited by
context, right? And so you see in the
bars, you know, things are actually
filling up already. And you know, the
problem is, you know, by the time you
actually load in all the context you
need to know how to grab this info, how
to scrape stuff, how to do all that,
you've actually really overwhelmed the
context, right? Like so this is read all
the transcripts, process them, generate
summaries. This is grab all the news
digest. And then well, event engine. And
then let's see, brief agent's metadata.
And then model agent's not here.
Actually wrapping up now. But a model
agent, which would have been here, is
responsible for actually building the
model, right? But the problem is all of
these fill up fill their context up with
the sort of task at hand, right? And so
what we do is we structure this Oh, it's
so it's actually finished. So, let's see
I can show the show you I'll show you
like a little bit of process. I said,
"Okay, let's initiate, you know, here is
the the kind of steps we're going to
take, conference summaries. Here's key
takeaways from the coverage. And then
here's a final scorecard deliverable."
I'll just ask it like, "Hey Wags, oops.
Hey Wags, can you summarize all all of
the agents you used and what they did?"
Yeah. The And the key thing, right? The
one the one agent that we keep pretty
much pristine is the company agent. And
what the company agent does is actually
reads in all the results, all the
summaries, right? And then you can
actually ask it questions. It's
important to have that in the context,
but not necessarily how we got to it,
right? And so here, you know, you can
sort of see see what they did. And I
guess you know, I'll I'll take a step
back and say like, you know, why why did
we build this, right? Other than, you
know, covering more ground, right? And
you know, one really silly problem
statement, you know, in my past like
life before this, I was in investing,
public markets. And you know, I built
like so many of these models and covered
like a lot of companies. And you know,
it it seems silly in this day and age
that there's nothing to even
um,
you know, in a reliable way ingest
financial data, right? Like by the time
you ingest financial data, you actually
spend more time, you know, checking it
and fixing it. You might as well type it
in in the beginning, right? And it's
only kind of now this has allowed us,
right? So, anyway, you know, point is
we're going to we're going to have this
initiate. We're going to be able to ask
it questions. We want the analysts to
spend more time on reviewing, editing,
thinking, drawing connections. And the
less of data entry, less of telling us
what happened, but you know, why it
happened and what it means.
And so, you know, like our our analyst
team is is fixing my view. It just means
we we cover more ground and cover it
smarter. Make sense? Sam, what are your
impressions watching this happen? Have
you been using agents at this level? Um,
not at this level. Um, it's a bit
bewildering to me, certainly. I was
burning some tokens yesterday. It felt
good to uh, break that in under the
Semianalysis banner for the first time.
Um, but nothing like this. Uh, it
strikes me that
if you're using that much context on
each agent, I don't know, maybe it'd be
better to be a bit more aggressive with
spinning up sub agents. How do you think
about like how you're structuring this
whole thing and passing information from
node to node um, to make it all go as
quickly and reliably as possible. Yes.
Um, yeah, so it's a good question,
right? You know, one one one problem
we're here is So, one problem we had um,
is um,
like moving moving data sort of between
the agents, right? And um,
so what we have to do is the way the way
it sort of works is cuz they can only
talk to sort of the the lead agent,
right? So, what we have to do is we have
each of them doing like a very discrete
part of the process. Um, and so you can
see I've woken up a company agent. And
company agent is actually when it when
it wakes up, right? When we finish the
initiation process, it actually saves a
whole index file or it saves a whole
file like of what we create. Like, you
know, there's a model, there's the
earnings transcripts, there's the
company briefs. And then, you know, when
you when you wake up the company agent,
it's it's told to ingest all this stuff,
right? It's ingest all this context. So,
I mean, I'll just sort of see if this
What was the large uh, you know, optical
contract that AOI won and what impact
did it have on their financials? I mean,
there's a lot of good products in this
already. Like Quarter has a good
product, but it generally only will scan
you know, it'll scan earnings
transcripts and it won't necessarily
have like all this other stuff in in its
context. I'm not even sure this is going
to work cuz I just initiated it on it,
but
you know, it it it again, it's broadly
how do you keep the right amount of
context and the right amount of
information in the right in the right
agent. And
you know, uh, like I said, we have an
agent for earnings, we have an agent for
events, we have an agent for just
updating financials.
Um, does that answer your question?
Yeah, that gives some good insight. I'll
need to go to school on this these next
few days, but good to see the expert at
work.
Here. So, actually see see look at this,
right? So, if I, you know, like just
imagine how long it would take my
analyst like, you know, I just ran this.
Probably started 5 minutes before the
podcast, right? And you know, think of
how long it would take your analyst to,
you know, go through initiate on this
and come up with this answer. Is it
okay? AOI landed 324 million, you know,
million 1.2, likely Meta, Amazon, mostly
forward-looking. You know, obviously
like, you know, I'll have to check this
against the actual thing, right? You
know, we're still developing it. But
let's see how much this cost.
Okay? This cost me $3.52.
So, you can see why like um, you know,
what we've written about is we've
written about um, you know, probably I
think there was some initiation work I
did in other sites. So, maybe the total
cost is like 10 or 15 dollars. But it's
either this or I have an analyst spend
like a day on it. Um, and so you can you
can imagine if it was like 10 or 12
dollars or 15 or 20, I'd still do it,
right? And that's kind of why I think,
you know, the end demand, the end ROI is
so strong. And it's why you're seeing
that that inflection in in GPU rental
price, which we talked about last time.
Dan, can you talk about how quickly you
learned this? Like from going from cuz
I've been using coding agents for a
while and I feel like I'm almost more
cautious than you or slowly dipping my
toe toe into agents or open claw sort of
stuff. Like how did
you weren't using this even 3 months
ago, right? Yeah, yeah. I mean I mean 3
months ago, it was sort of like
um,
you know, we we were we were like we we
we had like a Chinese New Year break,
right?
And you know, we really uh, like wound
down a lot of projects that we were on.
And so we had a little bit of head space
to to get into this, right? Cuz the
ironic thing is, you know, we were so
busy, we didn't have time to like, you
know, like learn new stuff to keep us
get us less busy. So, anyway, you know,
with that break, we just started playing
around a bit. Uh, and you know, I think
what really helped is um,
you know, this the the concept of like,
you know, how you want to build like
like a research team. Like what tasks
are and then how you would sort of like,
you know, divide So, it also started
like this also started from uh,
you know, if I if uh, if I were to sort
of uh,
let me let me just switch windows real
quick.
It also started from like a collection
of discrete like very discrete things we
wanted to do.
Uh, and I'll show you a couple of
discrete things. And And what we
realized is there are a lot of discrete
tasks. Like I mean there's two two
important things to realize, right?
There are like a lot of discrete tasks.
Um so I'll just fire up Claud. So here
I'll show you the skills we built. There
are a lot of discrete um things that you
wanted to do. But you know, to get it
you know, build that into something
that's an ongoing like living agent
living coverage and not just like, you
know, let's let's build this project,
let's build that project, let's build
something that'll compound itself and
build and actually like use all these
functions, right? So all of these skills
are used by by Wags, event summary,
earnings, fin model build, press news,
pure monitor is all is all built upon
and these were all started out as very
very discrete things like, "Hey, can you
summarize an event? Hey, can you build
me a financial model? Like can you do a
press news monitor?" And they all
stemmed out of out of things we were
doing that were like really manual that
that we couldn't have even imagine, you
know, doing now, right? Like, "Hey, I
want to know what is all the press
announcements from Broadcom ahead of the
OFC for instance."
>> Yeah, makes sense, man. Um okay, you
talked about the the job of an intern
being different. Has your job changed
meaningfully?
Like you do you feel like you have to
spearhead learning this stuff even
though in some ways maybe younger people
who are going through school right now
might be more AI native and more better
prepared to learn how to do some of this
stuff? Well, I would I would say for me
a lot of this is um you know, really
trying to
uh I think I think all the analysts get
it, right? Cuz they they've all done
this kind of tasks and I think for me
it's it's really trying to figure out
like what is the what is the end goal,
right? What do we want to get to? Like
what what do we need to be as a team,
right? And where we need to be is we
need to be in a place where, you know,
we can cover like 60, 80, 100 companies,
right? Um without that creating so much
baggage that we lose sight of what's
really going on. And so making sure that
that that, you know, Wags and everything
it it it does things
you know, just in such a streamlined way
that that that it really enables that
that sort of cadence. And I'll sort of
give you one more example of uh you
know, another another agent family
within, you know, it's actually within
Wags. Uh what do we call uh Oh, there
are families now. Yeah, yeah, so so
Claudia is our conferences chief.
We we uh we actually we we as a company
attend over 50 to 60 conferences, right?
So
um you know, and the thing is, right?
When we attend uh do you cover now? So
the thing is, right? Most of the time we
actually spend it in meetings these
days, right? In targeted demos. Uh I
know Jordan you were like GTC, probably
back-to-back meetings with all the Neo
Clouds and I I went to like three
>> sections the whole time. I was just
there having meetings with people in
person cuz they happened to be there,
too. Yeah, exactly. You know, when every
time I go into a conference, kind of you
remark all these amazing sessions that I
want to go to and then I go to exactly
zero of them, right? So I mean you can
see you know, you can see there are 621
sessions at GTC. There is 830
presentations of which I went to exactly
zero, right?
You know, what what's the problem here?
>> to be clear. Like I was at GTC while Dan
was at OFC a couple of episodes ago we
talked about that. I actually like got
the debrief kind of live on that podcast
cuz like you know, I tried to read some
notes, but I hadn't talked to you about
it since you'd gone. Yeah, yeah, and and
and so you're you're like kind of not
exactly, you know, always like able to
view every
um presentation and then it just becomes
like an obstruction, right? Having to
stop whatever you're doing and like,
"Okay, now I got to go to the website
and dig through that and everything and
and then I might get interrupted, right?
And so you know, once once we have the
file users, what Claudia helps us do
like, you know, presentations, YouTube
links, we transcribe it, index the
talkability index of each conference for
uh speakers and then what I can do is,
you know, I can say hey if I'm
researching CPO and DWM for CPO, it's
like, "Hey, find me you know, all every
talk that discussed CPO and particular
use of DWM for CPO." I'm like, "Well,
here it is, right?" And so if I want to
do, you know, research project on CPO,
you know, this is this is kind of the
starting point, right? Um and I'll sort
of show you uh let me see. I'll show you
another
um output that we did uh a couple cool
things. You know, I told like, "Hey, you
know,
tell me what to what to do for
ScalaCross." And so so here it is. So
Julian's actually leading our work on
ScalaCross. He just joined us uh last
week or actually this week is his first
week. And so now I've got a bunch of uh
stuff for Julian to read. I'm like, "Go
read this and tell me what it says."
>> So the agent is going to brief an
analyst to brief you is the workflow?
Yes.
>> Yeah, I like that. I like that. Yes,
yes, yes.
>> Sam, when you hear when you hear Dan
say, "We got to cover 60 to 80
companies." And you think about like
joining SemiAnalysis and what it was
like coming up to speed trying to figure
out, you know, what's a Neo Cloud,
what's a Neo Lab, what's a tokenomics
model cover? Like do you feel like you
could have done this without AI or how
long would it have taken to do without
Claud code effectively?
It would have been a qualitatively
different experience. Yeah, I I was
thinking about this a couple days ago
because I think maybe there are some
skills that I've left behind that it
would be good to pick back up with the
upgraded tool of Claud code. But yeah, I
mean right now my first thought when I
have something new to learn is just like
spin up Claud and get into it that way.
To the point where I built a skill for
Claud that added the content of my
conversations with it to a flashcard app
so that I could go back through all the
lessons from the Neo Clouds because I
realized that all of my learnings were
in conversations with Claud and those
those were going to be hard to surface
if I wasn't a bit more deliberate about
keeping track of them. So yeah, it was
completely Claud based and I don't know
how I would have done it otherwise. So
what do you guys think about the
trustworthiness cuz it did cross some
space for me. It was roughly November
when we started pushing on on people.
Doug was definitely like spearheading
that at SemiAnalysis to get people to
use it. And we now kind of implicitly
trust the output by default and then
have to double-check things when it's
potentially wrong. Whereas before I feel
like everybody implicitly like did not
trust every output and had to keep
prodding the model to get it to a point
where it would be trustworthy. Um do you
guys think there is some level at which
this stuff can get better? I'm thinking
about the Mythos release that Mhm.
came out today which is to or a couple
of days ago which is to say like
I feel like at some in some level I am
the constraint now using Claud which is
to say
the instructions that I give the model
are the constraint. It just like it
wants to write code. It wants to do
analysis. It like the model wants to
build web apps for me. And I just need
to I just need to get out of its way so
that it can build the thing that I want.
And I'm like it's it's strange to think
about how the coding models can really
get much better from here in certain
scenarios.
Does that make sense to you guys? Like
do you think that
there's a meaningful gap in your Claud
code experience where the model really
needs to get better at a specific task
that it's just really bad at right now?
Yeah, yeah, and it's it's almost like
training a human analyst, right? Because
one of the common problems that I
actually see and I was just, you know,
troubleshooting this today is when it
does a model, right? And it doesn't
always like balance the balance sheet.
So I was kind of looking at Let me share
a screen real quick on this example
here. Okay, let's see. Screen. Yeah, so
if you look at this thing here, right?
You can see if if you were to zoom in,
right? You would see the balance sheet
doesn't actually balance.
So the asset liabilities, right? And so
this is sort of thing where I'm like
telling us, "Okay, man, how can you how
can you input something that doesn't
balance?" So I got to go back and, you
know, we got to go figure out like was
it mixing up fact set, MCP? Was it
mixing up SEC filings? And then, you
know, we we're building more of a
supervisory function with Wags. So
actually every time a model finishes
initiating, it has to go through these
checks. So that's what, you know,
Terrence's job is to like kind of whip
uh whip the agent, whip Wags and to make
sure that, you know, we don't see this.
And it's just like teaching an analyst
team, really. So that's one of the
things.
>> Yeah, but it's not necessarily just like
teaching an analyst team because that
type of mistake is not one that an
analyst would ever make. And uh That's a
good point. And they don't forget. The
analysts like that these these that the
challenge is the memory because, you
know, once you once once the sub agent,
you know, shuts down, like that's it.
The context is gone, right? You have to
memorialize everything in a memory, but
then you can't have like an endless
memory file. So like having those
learnings, right? Persist over time is
one of the biggest challenges actually.
Like the balance sheet problem is not a
new one, right? You know, mostly we've
solved it, right? But, you know, we we
have to be vigilant for these things. It
may take us another couple weeks or
months to iron out everything, but you
know, that's um you know, it's it's it's
like learning stuff. It's learning as we
go.
>> Yeah. Can you can you talk a little bit
about like based on your personal
experience what you think the impact is
going to be on the broader market? Last
week the core research guys were
commenting on how kind of shocked they
are that others like in their friend
groups who they consider smart and, you
know, plugged in are just like stuck in
different jobs or different mindsets
where they're not even trying this stuff
right now. And they're kind of like how
how do you get bigger adoption, more
people using it? Like my sense is that
everybody feels like there's going to be
a lot more growth of use of Claud tokens
this year just as not only more people
sign up, but also individual people
start to use it more. You guys agree
with that?
>> Yes.
Yeah. Sam, what do you think?
>> I think that it's reached the point
where
um I'd be comfortable introducing it to
my parents, grandparents even. I was
using it for work writing software about
a year ago. And as you said, it has
gotten a lot better at just getting
things right the first time. Like a year
ago you had to use test-driven
development, you had to be super careful
in managing context and a scaffolding
projects up step by step. But now it's
like good enough that it sort of uses
the terms that we use. You can just kind
of give it the same instructions that
you would give to an intern and it works
often enough. So there's some point at
which, you know, these quantitative
improvements in model quality, you know,
piecewise improvements on benchmarks
nets out into a qualitative
qualitatively different experience using
the model. And also a lot of that is
obviously the tooling that Anthropic has
built up around it, giving a nice
interface with the Claude co-work app
and so on. So, I think that it's only a
matter of time before these things are
not so intimidating tool that the code
people use and every finance bro, every
lawyer is just going to be relying on it
to do the bulk of their work. Yeah,
yeah. Big changes.
>> Yeah, I I agree. Yeah, I agree, Sam.
Like, you know, I I think about it feels
like everyone our circle is using it,
right? Like, everyone I met in in the
Bay is like using it, right? But but we
we know that like for Fortune 500, you
know, for all these companies like they
they probably don't even have approval
like IT approval. Like, you know, I
talked to a lot of a lot of fund
managers and they're still like only
starting to, you know, use it for like
just like, you know, summarize like
really small small time like single task
stuff. It's not really like a tool that
compounds and and improves over time.
And so, I really feel like if if, you
know, GPU prices are shooting up now and
like, you know, you can think of
everyone your your circle is like really
the tip of the spear, right? Can you
imagine if everyone at Meta or everyone
Amazon was using it like like I think
you guys had a great post as well,
right? Comparing the Meta uses per
employee how we're completely mogging
them right now. And and it's only going
to the gap's only going to become
bigger, right? But can you imagine if it
was like, you know, Unilever, P&G, if it
was like Boeing, all these companies,
right? Like we're using it, you know, in
such an embedded way. Like, you know,
the only way this gets relieved is like
honestly a lot of chip fabs, right?
Which,
you know, you can have to bring Jeff in
next next time for that. Yeah. Yeah.
Well, I think the the other thing is
that like we we have a relatively direct
impact on the company's revenue from
like the time at which we start
producing better products, better
research with these models, that flowing
through to people spending money on
SemiAnalysis research and signing up for
the products is like pretty is a pretty
direct clear link. Whereas, somebody
who's
six layers removed from a customer
working at P&G may have a different
experience of like
having their contribution to
um or or
In some ways, I think there's a lot of
people who if they were to get 50% more
efficient at their job, they'd just stop
working 50% earlier in the day as
opposed to doing 50% more. Whereas, it's
almost the exact opposite at
SemiAnalysis. One of the guys on the
team told me the other day that he had a
24-hour straight Claude code session. He
just like did not go to bed.
Yeah, I think I know who you mean and he
doesn't go to bed anyway, Jordan.
>> [laughter]
>> It's a different It's a different guy
who doesn't go to bed. Because I work
[clears throat] a lot with that guy in
my time zone, I think you know who it
is. It's a different guy, actually
somehow. Okay. Well, it's probably true
of the guy I'm thinking about as well.
He's not the only one. A lot of guys who
don't want to be want to be named. But
yeah, like it's certainly night owls.
This is affecting sleep patterns, but
it's it's I think it's like it's it's
been this unblock for these people who
have this like pent-up dam
of ideas that they want to get out into
the world or into the products that we
have to sell at SemiAnalysis, which is,
you know, it's just awesome, right? It's
been an awesome experience that people
can go from idea to like link sent in
Slack for others to click and view in
the span of an hour. I've had that
experience like multiple times this
week, right? The agenetic coding tracing
benchmark with the guys there. We had
the
dashboards for accelerator and for like
tracking some of the ClusterMax
participants and stuff. I mean, these
are things that we got the idea to do
and then two to three hours later we're
in a working format. And uh
it's really it's interesting to consider
what improved productivity would
actually do to companies that are not
named SemiAnalysis. I it's not clear to
me exactly that the productivity is
going to flow through directly to the
financials of a company if they spend a
lot more on Claude tokens. Yeah. I agree
with that. There's some funny way that
the quality of the models nowadays makes
me pessimistic about their adoption
long-term because it's become clear that
the bottleneck is not actually the
quality of the output. Like, for some
reason other than the fact that it's not
good enough, all these people at the
Fortune 500 companies are not using
them. It is good enough. It makes me
five times as productive and I'm still
figuring out the right tool set. But
yeah, something else, whether it's
apathy or foreign incentive structures
or whatever, is keeping everyone else
from hopping on board. So, what do you
think about the Mythos announcement that
had the comments about cybersecurity
issues and obviously the Nicholas
Carlini
uh YouTube video where he's kind of
reviewing some of the bugs that they
found in the Linux kernel and I think
the NFS driver, like stuff that's been
around for 10 plus years in running on
production systems with just a little
bit more focus and effort and a new
model. So, maybe I'll fire away with
some hot takes. I've been working most
of the day on a note and going through
the system card. It's weird to me how
good it is at coding. It's all-around
improvements are significantly less than
its improvements in coding and
cybersecurity in particular. The system
card says that they did not intend for
this to be the case. It sort of fell
out, which is a bit odd. I'm not sure to
what extent the yap about cybersecurity
is a marketing ploy. If I wanted people
not to use a model for malicious
cybersecurity uses, I would probably not
have this gigantic marketing campaign
talking about how good it is at finding
zero-day exploits.
I was speaking to a security researcher
at Stanford yesterday who said like,
"You're out to lunch as a researcher if
you're not worried long-term about you
know, agentic attacks from LLMs." But
he's he and all his friends are very
suspicious that this actually is a step
change in model quality. So, we'll see.
I mean, they've done a brilliant job of
making us all wait with bated breath for
it at least. Yeah, we're all excited,
for sure. I think there's I can throw
out two other examples of stuff that
seems similar to cybersecurity in this
case, which is like kernel authoring on
GPUs as well as like system architecture
for inference. We've been working on
both of those recently. There's like
been some progress in the GPU mode style
leaderboards for kernels where AI is
generating a lot of the best kernels in
a way that it wasn't even six months
ago,
which seems like a notable change
because generally the way this stuff
works is not that AI catches up,
overtakes humans and then suddenly
humans land a counterpunch and get
better than AI. Like, it generally is a
one-way street.
Mhm. So, it's it seems like the dam is
breaking there, but hasn't fully gotten
through yet or the people who have the
most experience with the kernels in
addition to using AI are able to, you
know, still win these competitions
instead of just anybody being able to
anybody who has enough budget for tokens
being able to just like spend the tokens
to author these kernels.
The other thing that that I was working
on like this week that the model seems
to really just not be able to do that
well is kind of the long-range tasks to
consistently keep digging into
documentation source code to be able to
find bugs even with the extra high
reasoning like effort turned on and like
lots of prodding, a lot of these models
will just kind of give up and tell you
to open a PR with the maintainers of the
repo and and not dig into the details of
like actually lying or the LLM to to fix
something that is clearly broken,
clearly have a log for. And I wonder if
cybersecurity, the use cases that
they're describing is not necessarily
something intrinsic about the models
understand like the weights having a
good encoding or understanding of how
these systems work. Seems like those
representations are already there. It's
almost more of a ability to train the
model to be persistent on long-range
tasks and then give it the right harness
and the right instructions and let it
go. And a lot of people kind of claiming
like, "Well,
if if you were to describe the exploit
in great detail that Mythos found, many
other models can also exploit that same
that same
vulnerability, right? And um that seems
like roughly correct to me, which is to
say like if it was explained in great
detail to me and I had all the source
code and I had enough time, I feel like
you could just, you know, give it enough
tries to do it. And so, why why wouldn't
a less capable model be able to
understand something that seems
relatively easy to understand when it's
explained to you by the model that found
it, if that makes sense?
Yeah, interesting. Does that imply to
you that like if we start building
better harnesses for other models, we
should be able to do something
analogous, right? If it's not some
fundamental improvement in model quality
per se, but it's something more like
agency or persistence, we should be able
to get that by other means. It just
seems like both are going to be
important. In other words, the model's
training includes like the post-training
includes the ability to use these
harnesses effectively, pursue these
tasks, get a reward signal. And the more
that you train it to do something
long-range coding related, the better
it's going to perform at that stuff. And
so, it's like you need to develop the
harness in addition to developing the
model. Yeah, we'll see. We'll see, man.
See. There's lots to think about here.
You guys have any any hot takes on
others? So, obviously Meta had a had a
big release with their avocado model
kind of catching up. It feels almost
like it was rushed to come out. They
kind of screwed up one of the charts
announcing some of their benchmark
performance and it was like just like,
you know, a tweet. Like, here you go,
right? And then suddenly it they're
showing up on all of these these things
that they did.
You know, anyway, my my impression
initially was like
um
they were they were almost surprised to
have a model that performs this well.
And even though they're not it's not
necessarily a counterpunch on my
personal usage of it so far, it's it's
not like as good as as the top two or
three naming like Opus, 5.4, and a
Gemini,
it does seem like it's in that ballpark
now. And just more RL, more data, off
they go. They certainly have the compute
and the team has produced this thing.
So, four horse race now?
Yeah, I think you would know better than
me, but that's how it seems from here.
That seems like they've done the hard
part just to get to this point and that
there's not a whole lot required. I
mean, easy for me to say sitting on a
freaking podcast, but like not not a
whole lot all things considered to
close.
>> you speak, man.
We got to send you down to Menlo Park
and start checking out what's what's
going on down there. I always happy to
go to Menlo Park.
Dan, let's let's leave it on that this
note actually. I'm really curious.
Everything you shared earlier in the pod
but what would it take to use a
completely separate model? What would it
take for you to switch off of Claude?
>> Yeah, I was just going to ask you guys
that because
you know,
it gets into like this question gets
asked a lot, right? You know,
philosophically like everyone's like
always catching up with each other then
then like does that mean that the moat
it is less high and so I wonder, you
know, does the moat become all
capabilities or it becomes like how you
capture the eyeballs and you know, how
you capture the users, right? And has
Claude code kind of captured like found
the right formula?
You know, and people get comfortable,
you know, and and I always thought like
chat GPT would be like everyone would
kind of have like their $10 thing and
they'd just be happy using it, but I
think you know, people have been
switching out of it like to to Gemini or
other things. So so I don't know. Do you
like I I I would think it'd be annoying
to switch off but
to switch out because you know, you'd
have to get all your
all your knowledge files to be like you
know, retransferred to another
uh
a set of agents and other set of models
that know how to work properly with it.
Uh like I have the same thought like I
like I would probably not want to go and
retry everything and then have two
models working, but like what what do
you guys think? Do you think, you know,
this becomes the way you differentiate
is not just like raw models like it's
just the ecosystem around it, the
incumbency and the you know, user
experience and the you know, user
history with it. What do you guys think?
Think like I'm I'm surprised I'm I think
at a high level it's easier to switch
models than you think in the ecosystem
of like using Claude code, but pointing
it at a Codex model would be like one
change to a URL
in your like config, but I think that
doesn't
>> the way you think? Would it work the way
you expect though or would it like now
you it would it would behave a different
way? I don't know what you gave the
example of the balance sheet stuff,
right? I feel like everybody using
Claude code right now has a lot of does
not have very high standards for the
model that it needs to pass to be wowed
by it and to keep using it. And so when
the thing doesn't work with the balance
sheet, you don't just throw it away and
stop doing it. You just like give it
another prompt and then it fixes the
issue, right? Mhm. And so I feel like
it's it's uh there's a lot of inertia
that would need to be overcome to
actually want to to be motivated to
switch to a new model. That's my
impression hearing people like you
describe their initial experience using
Claude code which is more of a change
not in the model you use use, but the
interface which is to say like it's not
a web browser on a remote machine with
like this chat application or interface.
It's like it's more about being able to
control your computer. Like that's the
change in the interface that Claude code
seems to enable or co-work or whatever.
That is motivating people to pay people
to install open claw for them.
Or something like
line up for open claw installs and and
teaching lessons, right? Cuz that that's
like the hurdle. Not
>> Do you know what the lead time for a Mac
Mini is in the US now? No.
It's like 3 months, but you know,
fortunately we're in Singapore so we're
closer. Huh?
You don't need a Mac Mini.
>> I know you don't, but it's like that's
what everyone's doing. You know, you go
to Apple store and say, "Oh, you're
doing this all this Claude code stuff."
You know, like yeah, we are.
But unfortunately it's only a month in
Asia. That's funny. I was thinking about
getting a Chromebook because I mean like
it doesn't matter whether the file
system is local at all almost all the
computes in the cloud anyway when I'm
using these models, so I might as well
just like run it out of
you know, a a notebook. Um
And we got to wait 3 months waiting for
the Mac Mini.
I can all guarantee you that Paul does
not listen to this.
It's okay. Paul's awesome. He he lets me
get the 48 gigabyte configuration. I'm
not complaining. He adds people to Slack
channels at a moment's notice at all
hours of the day when they are
restricted but are called Paul.
Yeah, better
[ __ ] Better call Paul. That is I'm
going to use that. Paul's Paul's
amazing. Let's go. Shout out Paul. If
he's listening to this, we love you,
Paul. Awesome.
All right, guys. This has been a fun
episode rambling a little bit. Hopefully
people found it interesting. Dan, I love
the demos. I love looking at the back of
Terrence's head. Shout out Terrence.
Shout out Paul. We appreciate you all
guys.
>> next time. We'll check out Terrence
another time. We need live demo. Live
demo of
five screens, six or seven agents just
all going. Yeah, that'd be fun. Sounds
good. Go guys. Thanks for coming. Good
job.
>> Bye. All right. Thank you.
