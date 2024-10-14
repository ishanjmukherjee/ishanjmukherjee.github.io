---
layout: post
title: "Book review: Genius Makers"
permalink: /genius-makers
date: 2024-08-25
---

_Comments on [Substack](https://decisiontree.substack.com/p/genius-makers)._

<img src="/assets/images/genius-makers-cover.jpg" alt="Cover of Genius Makers, by Cade Metz" width="210">

Overall, Cade Metz’s *Genius Makers* is a useful and brisk history of artificial intelligence. The majority of the book focuses on neural networks, with only the first couple chapters devoted to [good old fashioned AI](https://en.wikipedia.org/wiki/GOFAI). Here are some of my notes from the book.

# The economics of open-source

One reason for open-sourcing your work is that people build upon it, and you can profit off of the improved performance. In *Genius Makers*, Metz explains Google’s rationale for open-sourcing the ML library TensorFlow:

> After deploying the software in its own data centers, Google had open-sourced this creation, freely sharing the code with the world at large. This was a way of exerting its power across the tech landscape. If other companies, universities, government agencies, and individuals used Google’s software as they, too, pushed into deep learning, their efforts would feed the progress of Google’s own work, accelerating AI research across the globe and allowing the company to build on this research.

As long as it sets an industry standard, companies need not fear open-sourcing software they have spent millions of dollars writing. On [Dwarkesh Patel’s podcast](https://www.dwarkeshpatel.com/p/mark-zuckerberg), Mark Zuckerberg said:

> We take a lot of the low-level infrastructure and we make that open source. Probably the biggest one in our history was our [Open Compute Project](https://tech.facebook.com/engineering/2021/11/open-compute-project/) where we took the designs for all of our servers, network switches, and data centers, and made it open source and it ended up being super helpful. Although a lot of people can design servers the industry now standardized on our design, which meant that the supply chains basically all got built out around our design. So volumes went up, it got cheaper for everyone, and it saved us billions of dollars which was awesome.

If Meta open-sources its models, developers will build upon them for free. If models become 10% more efficient as a result, Meta saves “billions or tens of billions of dollars”.  

A more whimsical example of standardization from [a *Diff* post](https://www.thediff.co/archive/sharing-and-owning-standards/): Dungeons & Dragons released “a [generic role-playing system](https://en.wikipedia.org/wiki/D20_System) that could be grafted on to other themes, like superheroes, spies, and Star Wars”. While this increased competition (the number of new tabletop gaming companies tripled in two years, while the number of employees per company halved), it made a lot more people interested in tabletop gaming and knowledgeable about the basics (20-sided dice, storytelling). 

A second reason companies open-source software is to [commoditize the complement](https://www.joelonsoftware.com/2002/06/12/strategy-letter-v/). TensorFlow makes AI research easier and Google can profit off of this research, yes, but TensorFlow also drives revenues for Google's [TPU chips](https://en.wikipedia.org/wiki/Tensor_Processing_Unit). Ditto for [JAX](https://en.wikipedia.org/wiki/Google_JAX). And as Metz writes in *Genius Makers*, Nvidia has had a deep learning research wing since early on. Nvidia's hope was that if its research made deep learning easier/more fruitful, demand for its GPUs (which are used in deep learning) would increase. Ben Thompson of Stratechery [explains](https://stratechery.com/2023/ai-and-the-big-five/) that by open-sourcing models like Llama and supporting the development of the ML library PyTorch, Meta makes AI-generated content cheaper to produce. This means more content for its social media platforms, from Facebook to Instagram. 

Similarly, Google's open-source Angular framework makes it easier to build websites, and it’s websites people need a search engine *for* in the first place. Google Chrome's richly-featured Dev Tools is also a push towards making web programming easier. Another browser, Mozilla, hosts one of the world's best collections of resources on web programming, [MDN](https://developer.mozilla.org/en-US/). The [top financial contributors](https://openwebdocs.org/sponsors/) to MDN are Google, Microsoft, Igalia and Canva. All these companies stand to gain if more people build websites. Google and Microsoft make browsers and search engines, Igalia makes browsers, and Canva helps create graphics and wireframes. Until [recently](https://web.archive.org/web/20230304141510/https://openwebdocs.org/sponsors/), JetBrains also sponsored MDN. JetBrains makes IDEs, which are essential infrastructure for web development.

In [this *Diff* post](https://www.thediff.co/archive/bullshit-jobs-is-a-terrible-curiosity-killing-concept/), Byrne Hobart explains how [ElevenLabs](https://elevenlabs.io/) commoditizes its complement. Its core product “converts text into voice, for arbitrary voices”. So why is it launching [a tool to isolate voice content from background noise](https://venturebeat.com/ai/elevenlabs-launches-free-ai-voice-isolator-to-take-on-adobe/)? In part because “\[i\]f ElevenLabs can dominate text-to-voice (still very much an open question) it's in their interest to make voice samples as abundant and cheap to acquire as possible”. It’s these samples that will get fed into ElevenLabs’ core product.

Gwern has a lot more examples of complement commoditization in [this post](https://gwern.net/complement#examples).

A final reason why open-sourcing work helps is that talent is more likely to work for you. Academics, used to measuring their impact in publications, may feel ill at ease in a closed-source company. 

Metz notes Zuckerberg was able to nab [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun) for [Facebook AI Research](https://en.wikipedia.org/wiki/Meta_AI) (FAIR) despite not being able to articulate a use case for AI within the company. Earlier, he had tried and failed to acquire DeepMind for this very reason: Demis Hassabis, the DeepMind founder, couldn’t see what Zuckerberg was trying to do with AI. One of the reasons Zuckerberg fared better with LeCun was his almost ideological commitment to open-sourcing AI research, and allowing LeCun to keep in touch with academia by spending part of his time at NYU.

# Frank Rosenblatt, inventor of the perceptron

After inventing the perceptron — arguably the first nontrivial machine learning algorithm — Frank Rosenblatt pivoted to running brain experiments on rats. 

> After one group of rats learned to navigate a maze, he would inject their brain matter into a second group. Then he would drop the second group into the maze to see if their minds had absorbed what the first group had learned.

And, yes, this did mean killing rats. From Rosenblatt’s [paper](https://www.pnas.org/doi/pdf/10.1073/pnas.55.3.548):

> To obtain this extract, the donor rats were killed by decapitation. … At least some of these \[recipient\] rats appear to be suffering adverse after-effects from the injection (including injuries and phenol poisoning in several cases).

# Genius foundries

Both Rosenblatt and [Marvin Minsky](https://en.wikipedia.org/wiki/Marvin_Minsky) were from [Bronx Science](https://en.wikipedia.org/wiki/Bronx_High_School_of_Science), the NYC public high school that has produced “eight Nobel laureates, six Pulitzer Prize winners, eight National Medal of Science winners, and three recipients of the Turing Award”. 

Minsky doles out high praise to Bronx Science — compared to [Phillips Andover](https://en.wikipedia.org/wiki/Phillips_Academy) and even Harvard, the work was more challenging and the students were “people you could discuss your most elaborate ideas with and no one would be condescending”.

A bit like how both the polymath genius [John von Neumann](https://en.wikipedia.org/wiki/John_von_Neumann) and his collaborator [Eugene Wigner](https://en.wikipedia.org/wiki/Eugene_Wigner) happened to be contemporaries at the [Fasori Gymnnasium](https://en.wikipedia.org/wiki/Fasori_Gimn%C3%A1zium) in Budapest. Fasori was pretty influential to von Neumann — if only to the extent that it brought him the math teacher László Rátz, who got von Neumann world-class tutors from the University of Budapest.

# Geoff Hinton's remarkable pedigree

You may already know that Geoff Hinton, one of the grandfathers of neural networks, is the great-great-grandson of George Boole (of Boolean algebra). But the rest of his family was star-studded too: his [great-grandfather](https://en.wikipedia.org/wiki/Charles_Howard_Hinton) was a science fiction writer who coined the word “tesseract”, his great-uncle got inspired by his father’s four-dimensional fantasy to invent the jungle gym, and Geoff Hinton’s cousin was one of the few women to work on the Manhattan Project. Sir George Everest, after whom the mountain is named, was also a relative. 

Geoff Hinton’s father was impressive too — he was an entomologist and a Fellow of the Royal Society. But he doesn’t seem to have been a model parent. “Work really hard and maybe when you’re twice as old as me, you’ll be half as good,” he told Hinton. 

Of course, Hinton did okay. When his AlexNet paper had 60,000 citations, he said it was fifty-nine thousand more times than any paper his father ever wrote. He won a third of [the Turing awarded for deep learning](https://www.nytimes.com/2019/03/27/technology/turing-award-ai.html). The \\$1 million in prize money was split with the co-winners, Yann LeCun and Yoshua Bengio, but Hinton got to keep the extra cent. However, far before AlexNet, when Hinton had only just finished his thesis, “\[t\]he old bastard died … Not only that, he got a cancer with a high genetic linkage. The last thing he did was increase my chances of dying.”

# Hinton's puzzle

Geoff Hinton has a delightful puzzle about arranging two pieces to form a pyramid.

![](/assets/images/geoff-hinton-pyramid-puzzle.jpg)
*Geoff Hinton and Sara Sabour hold two pieces which can be arranged to form a pyramid. Via [The New York Times](https://www.nytimes.com/2017/11/28/technology/artificial-intelligence-research-toronto.html).*

Hinton shows how to solve the puzzle in [this talk](https://youtu.be/x5Vxk9twXlE?si=2uqU9UU-W1wvsGGw&t=366).

In general, Hinton comes across as hilarious. He calls the issue with his spine, which prevents him from sitting down, a “long-standing problem”.

# Yann LeCun designed the first AI accelerator

I didn’t know that Yann LeCun has an impressive background in electrical engineering. In fact, he may have designed the first bespoke chip for training neural nets, what the cool kids call an [AI accelerator](https://en.wikipedia.org/wiki/AI_accelerator):

> \[In the mid-1990s\] LeCun and his colleagues also designed a microchip they called ANNA. … Instead of running their algorithms using ordinary chips built for just any task, LeCun’s team built a chip for this one particular task. That meant it could handle the task at speeds well beyond the standard processors of the day: about 4 billion operations a second.

It would be almost 25 years before Nvidia started making GPUs (which exploited ML’s [embarrassing parallelizability](https://en.wikipedia.org/wiki/Embarrassingly_parallel)) and Google invented the TPU (which speeded up matrix computations by dealing in integers rather than floating-point numbers). And where did LeCun do this research? That most hallowed institution of American dynamism — [Bell Labs](https://en.wikipedia.org/wiki/Bell_Labs), profiled in Jon Gertner’s book *The Idea Factory*.

Speaking of neural networks pioneers who were also electrical engineers, I recently learned from a [*Diff* issue](https://www.thediff.co/archive/longreads-open-thread-90) about [Marcian Hoff](https://en.wikipedia.org/wiki/Marcian_Hoff), who helped invent the world’s first microprocessor.

# The only\* truly biology-inspired neural network

Despite their name, neural networks have little to do with the architecture of the animal brain. A few years ago, a machine learning engineer worked through a neurobiology textbook and wrote a series of blog posts on comparisons between biological and artificial neural networks. It's worth [checking out](https://zswitten.github.io/2019/08/04/neuroscience-neural-networks-0.html). The gist is: you can make hand-wavy analogies between them, but improvement in artificial neural nets has been driven by research on the nets themselves, rather than by sifting through biology textbooks for inspiration. 

Except, a specific flavor of neural nets — [convolutional neural nets](https://en.wikipedia.org/wiki/Convolutional_neural_network) (CNNs) — *were* inspired by biology. First, I'll note how important CNNs are. They're the primary architecture for working with images. Innovations made in CNNs have often trickled into other architectures tailored towards different problem classes. It was a CNN named [AlexNet](https://en.wikipedia.org/wiki/AlexNet) that destroyed the competition in a 2012 [image recognition contest](https://en.wikipedia.org/wiki/ImageNet) and ushered in an AI summer. 

A CNN works by chopping up an image into squares, and analyzing each square separately to find broader patterns in the big picture. Consider, for example, the task of classifying 128 x 128 pictures as “cat” or “dog”. It turns out that rather than looking at the whole image at once, if a net looks at all possible 5 x 5 patches within images separately, it can learn to recognize edges and splotches of color. These edges/splotches can make up ever more complex patterns, like eyes/whiskers/ears. 3Blue1Brown has a great [video](https://www.youtube.com/watch?v=aircAruvnKk) on this. Chris Olah has a neat (but more technical) [blog post](https://distill.pub/2017/feature-visualization/).

The precursor to the CNN — the [neocognitron](https://en.wikipedia.org/wiki/Neocognitron) (objectively the coolest name in all ML) — was inspired by the human visual cortex, as “different sections of the visual cortex process different sections of the light captured by your eyes”.

Amusingly, the clever CNN architecture was built and forgotten in the 1980s. The problem was that LeCun’s nets could recognize digits in 32 x 32 pixels on checks, but they didn’t work for higher resolutions. Classifications also took inordinately long. LeCun was despondent: he called ANNA “the first (and maybe the last) neural net chips to actually do something useful”.

![](/assets/images/xkcd-1425.png)
*[xkcd 1425](https://www.xkcd.com/1425/)*

Obviously, he was wrong. We live in an age in which [xkcd 1425](https://www.xkcd.com/1425/) is comically outdated. But what changed? The [bitter lesson](http://www.incompleteideas.net/IncIdeas/BitterLesson.html) reared its head. Hardware improvements, like GPUs, made training large nets much faster and cheaper. Geoff Hinton put it this way: “No one ever thought to ask: ‘Suppose we need a million times more \[computing power\]?’”

# Fostering a domestic technical industry

It’s strange how Canada dropped the ball on deep learning. Geoff Hinton worked in Toronto and attracted the likes of [Ilya Sutskever](https://x.com/ilyasut) and [Alex Krizhevsky](https://www.bloomberg.com/profile/person/21862614), who went there for grad school. Yoshua Bengio worked in Montreal and drew [Ian Goodfellow](https://en.wikipedia.org/wiki/Ian_Goodfellow) (who had competing offers from Stanford and Berkeley). Bengio, in particular, is incredibly keen on staying in Canada — he has repeatedly refused offers from big tech companies like Microsoft to move to the US and work in the industry. Hinton, too, had an affinity for Toronto: when he worked there, his salary was lower than what his pension would have been, meaning that he was effectively paying the university to be allowed to teach.

Despite the devotion of these first-rate researchers, it’s the US that is undoubtedly the world's leading AI country. Next come the UK and China, then Canada — *maybe*.

Canada did try some things. In 2017, Hinton’s [Vector Institute](https://vectorinstitute.ai/) was established with \\$130 million in funding from the likes of Google and Nvidia to incubate Canadian AI startups. Justin Trudeau promised \\$93 million in support of AI research centers. Canada is also less cagey about granting visas to AI researchers, especially those who come from Middle Eastern countries like Iran, such as Sara Sabour. Yet, all this seems to have been too little, too late.

Why was it hard to convert the academic hubs into successful AI companies? What, specifically, went wrong? A detailed case study would have lessons for countries trying to kickstart their own AI industries, most notably [the UAE](https://time.com/6958369/artificial-intelligence-united-arab-emirates/) and [India](https://www.ft.com/content/414e912f-c50c-4bc8-b3a2-b9ac36c34ebb) (see [this press release](https://pib.gov.in/PressReleasePage.aspx?PRID=2012375) from India’s Ministry of Electronics & IT).

*Genius Makers* provides subtle hints on what can work, when it describes why Baidu was confident it could put self-driving cars on the road faster than Google could, despite launching its project years after Google.

> This wasn’t because Baidu had better engineers or better technology. It was because Baidu was building its car in China. In China, government was closer to industry. As Baidu’s chief operating officer, \[Qi Lu\] was working with five Chinese municipalities to remake their cities so that they could accommodate the company’s self-driving cars.

(Another reason: China is less reticent about providing its companies its citizens' data.)

Government intervention in industry, when handled by competent people, can be *good*. For a specific example, Byrne Hobart’s “[Lessons from the East Asian Economic Miracle](https://byrnehobart.medium.com/lessons-from-the-east-asian-economic-miracle-5f8d0f2354d9)” is a great look at how MITI helped Japanese industry flourish.

# The PR of deep learning

It seems that the phrase “deep learning” started getting used mainly to glam up the field of neural nets, which hadn’t until then produced practical results:

> When Hinton gave a lecture at the annual NIPS conference, then held in Vancouver, on his sixtieth birthday, the phrase “deep learning” appeared in the title for the first time. It was a cunning piece of rebranding. Referring to the multiple layers of neural networks, there was nothing new about “deep learning.” But it was an evocative term designed to galvanize research in an area that had once again fallen from favor.

I don’t know exactly how much the rebranding helped, but here’s an illustrative example from the book. [Russ Salakhutdinov](https://www.cs.cmu.edu/~rsalakhu/), who was to become “one of the world’s leading connectionist researchers”, got drawn into deep learning in part by Hinton’s use of the evocative phrase “deep belief networks” for neural nets. Objectively, deep learning became hot. By 2016, the Microsoft vice president was [complaining](https://www.wired.com/2016/11/giant-corporations-hoarding-worlds-ai-talent/#:~:text=Even%20the%20big%20players%20talk,of%20acquiring%20an%20NFL%20quarterback) that an AI researcher cost as much as an NFL quarterback.

On branding, consider also the motivation for OpenAI’s early projects: a world-class Dota model, and a robotic arm to solve the Rubik’s cube. 

> Both projects were also conspicuous stunts, a way for OpenAI to promote itself as it sought to attract the money and the talent needed to push its research forward. The techniques under development at labs like OpenAI were expensive—both in equipment and in personnel—which meant that eye-catching demonstrations were their lifeblood.

# Google's 20 percent time

Google’s “20 percent time” — the practice of allowing employees to work one day a week on whatever side projects they want, which may or may not spin into new products — makes a few appearances in *Genius Makers*.

Most notably, Google’s [AI lab](https://en.wikipedia.org/wiki/Google_Brain) began as Jeff Dean’s 20 percent time project — a collaboration with [Andrew Ng](https://en.wikipedia.org/wiki/Andrew_Ng) (of Coursera fame) to write a [cat video classifier](https://www.wired.com/2012/06/google-x-neural-network/). (By the way, here are the [Jeff Dean facts](https://www.informatika.bg/jeffdean).)

For his 20 percent time project, [Varun Gulshan](https://sites.google.com/view/varungulshan/home) created a neural net to make diabetes diagnoses from retinal scans. It seems that a descendant of the net is [currently used](https://health.google/caregivers/arda/) to support three thousand screenings weekly, many of them in India.

This program has also given Google the following products: AdSense, Gmail and Google News. However, it seems to have been effectively killed now. *Inc* weighs the evidence [here](https://www.inc.com/bill-murphy-jr/google-says-it-still-uses-20-percent-rule-you-should-totally-copy-it.html).

# Gary Marcus' startup

Gary Marcus, [deep learning skeptic](https://garymarcus.substack.com/p/two-years-later-deep-learning-is), has sold an AI company. His Geometric Intelligence was bought by Uber. According to a [*Wired* article](https://www.wired.com/2016/12/uber-buys-mysterious-startup-make-ai-company), it was supposed to be Uber's pivot “from a ride-hailing company into an outfit that does self-driving cars and trucks, hardcore machine learning, even flying automobiles”, much like Amazon went from online bookseller to cloud computing behemoth. Marcus’ deep-learning-mixed-with-expert-systems approach was supposed to work better than pure deep learning because “there’s not enough data describing the rare situations that lead to accidents”. According to *Genius Makers*, four months after starting at San Francisco, “without much explanation, Marcus left the company and returned to New York, resuming his role as the world’s leading critic of deep learning”.

As far as I know, modern autonomous driving technology, which works mostly fine and is improving, works almost entirely on deep learning.

# How Goodfellow invented GANs

Ian Goodfellow invented generative adversarial networks (GANs). The story of how he did so is amusing:

Neural nets had proved successful in classifying images. In 2013, Goodfellow and his labmates at Montreal were trying to create a neural net that could *generate* images. His colleagues proposed to “statistically analyze each image that emerged from their neural network”, “compare these stats to what they found in real photos”, and train the nets to minimize deviations. Goodfellow offered a “radically different solution”:

> What they should do, he explained, was build a neural network that learned from another neural network. The first neural network would create an image and try to fool the second into thinking it was real. The second would pinpoint where the first went wrong. The first would try again. And so on. If these dueling neural networks dueled long enough, he said, they could build an image that looked like the real thing. Goodfellow’s colleagues were unimpressed. His idea, they said, was even worse than theirs. …
> 
> When he walked into his one-room apartment later that night, his girlfriend was already in bed. She woke up, said hello, and then went back to sleep. So he sat down at a desk next to the bed, in the dark, still slightly drunk and with his laptop screen shining on his face. “My friends are wrong\!” he kept telling himself as he pieced his dueling networks together using old code from other projects and training this new contraption on several hundred photos while his girlfriend slept beside him. A few hours later, it was working as he had predicted it would. The images were tiny, no bigger than a thumbnail. And they were a bit blurry. But they looked like photos. It was, he later said, a stroke of luck. “If it hadn’t worked, I might have given up on the idea.” In the paper he published on the idea, he called them “generative adversarial networks,” or GANs. Across the worldwide community of AI researchers, he became “the GANfather.”

LeCun, justifiably, called GANs “the coolest idea in deep learning in the last twenty years”. When Geoff Hinton heard this, he “pretended to count backwards through the years, as if to make sure GANs weren’t any cooler than backpropagation, before acknowledging that LeCun’s claim wasn’t far from the truth”.

Goodfellow was also an early pioneer of adversarial robustness research. And, of course, he was the lead author of the [canonical deep learning textbook](https://www.deeplearningbook.org/).

# Why NIPS was renamed

NeurIPS is one of the top ML research conferences. It used to be called NIPS, for “Neural Information Processing Systems”.

> After many researchers protested that the name contributed to an environment that was hostile to women, the conference organizers changed the name to NEURips.

# Elon Musk at OpenAI

Elon Musk was an early investor in OpenAI. In February 2018, however, he left the company. I know that one of the reasons he cites now is concern about existential risk. However, at the time, he cited two more reasons: to avoid conflicts of interest, as “his other businesses were now competing for the same talent as OpenAI”, and because robots were delivering underwhelming performance on Tesla’s factory floors.

# Demis Hassabis, child prodigy

Demis Hassabis co-founded the AI company DeepMind. At one point, he was the second-highest-rated under-fourteen chess player in the world. At twenty-one, he won the Pentamind “mind sports” olympiad, which included “everything from chess and Go to Scrabble, backgammon, and poker”. He won for four of the next five years — the year he didn’t win, he hadn’t entered. Hassabis has also won a world team championship for the board game *Diplomacy*. Geoff Hinton says of him:

> He’s got three things. He’s very bright, he’s very competitive, and he’s very good at social interactions. That’s a dangerous combination.

Hinton says of his cofounder Shane Legg (who has been interviewed on [Dwarkesh Patel’s podcast](https://www.dwarkeshpatel.com/p/shane-legg)):

> He’s not as bright, not as competitive, and not as good at social interactions. But then, that applies to almost everybody.

Hinton has high praise for Hassabis’ operational skills in particular: “He ran AlphaGo like Oppenheimer ran the Manhattan Project. If anybody else had run it, they would not have gotten it working so fast, so well.”

Hassabis also helped Peter Molyneux, OBE and IGN’s [18th greatest video game designer of all time](https://www.ign.com/top/game-creators/18.html), design an [amusement park sim](https://en.wikipedia.org/wiki/Theme_Park_\(video_game\)) that sold 10 million copies.

I’m glad that Hassabis didn't waste his talents on chess, and instead focused on AI. In this, he’s remarkably like the economist and former child chess prodigy Tyler Cowen, who [gave up](https://www.bloomberg.com/news/articles/2011-05-26/tyler-cowen-americas-hottest-economist) chess and philosophy because they had “little stability and poor benefits”. This [Kenilworth chess club profile](https://archive.is/4ADB) of Cowen also has him point out [Kenneth Rogoff](https://en.wikipedia.org/wiki/Kenneth_Rogoff), the grandmaster who consciously gave up chess for economics. As another example of giving up your immediate comparative advantage, Leopold Aschenbrenner was told by Cowen that he was an extremely promising young economist (David Thorstad [says](https://reflectivealtruism.com/2022/12/11/existential-risk-pessimism-and-the-time-of-perils-part-5-an-existential-risk-kuznets-curve/) that a paper Aschenbrenner wrote at seventeen was worthy of publication in a top journal), but that it’d be a mistake to go into economics research. Aschenbrenner took the advice, and now [runs an AI hedge fund](https://www.dwarkeshpatel.com/p/leopold-aschenbrenner) (after stints at the FTX Future Fund and the OpenAI Superalignment team).

# Superintelligence research at DeepMind

The proto-believer in AI superintelligence at DeepMind seems to have been Shane Legg. And it was none other than “self-educated philosopher and self-described artificial intelligence researcher” Eliezer Yudkowsky who introduced Legg to superintelligence, when both of them were working with a New York-based startup called Intelligensis in the early 2000s.

But soon, Hassabis was converted, too. One of the clauses in Google’s contract for acquiring DeepMind was the creation of “an independent ethics board that would oversee the use of DeepMind's AGI technology, whenever that might arrive”.

Amusingly, Ilya Sutskever, the OpenAI cofounder, was *not* an early believer in artificial general intelligence: when he met with Hassabis and Legg, the DeepMind duo “explained what they were trying to do. They were building AGI—artificial general intelligence—and they were beginning with systems that played games. As he listened, Sutskever thought they’d lost touch with reality. AGI was not something serious researchers talked about.” He declined their DeepMind job offer and worked instead at Google, where he helped build Translate. Fast forward to today, Sutskever has left OpenAI to start a [company](https://ssi.inc/) explicitly premised on AI superintelligence being a very real possibility.

# Neuroscience research at DeepMind

By 2020, DeepMind was swimming in Google’s money (not unjustifiably; its reinforcement learning algorithm to reduce power consumption across Google’s data center network was saving Google hundreds of millions of dollars). Demis Hassabis hired “a team of more than fifty neuroscientists to investigate the inner workings of the brain” in addition to the hundreds of computer scientists who worked there. Hassabis himself has a PhD in neuroscience. His research linking memory to imagination was a *Science* [top 10 breakthrough of the year 2007](https://www.science.org/doi/10.1126/science.318.5858.1844a).

DeepMind’s neuroscience team and Adam Marblestone presented a [tutorial on neuroscience and AI](https://sites.google.com/view/neurips-2020-tutorial-neurosci/home) at the 2020 NeurIPS conference.

# Why every company is an AI company now

> This is how the tech industry works. The largest companies are locked in a never-ending race toward the next transformative technology, whatever that might be. Each is intent on getting there first, and if someone beats them to it, then they are under even more pressure to get there, too, without delay. With the acquisition of Geoff Hinton and his start-up, Google had gotten to deep learning first. By the middle of 2013, Zuckerberg decided he had to get there, too, even if he was racing for only second place. It didn’t matter that Facebook was merely a social network. It didn’t matter that deep learning was not an obvious fit for anything beyond ad targeting and image recognition on this social network. It didn’t matter that the company didn’t really do long-term research. Zuckerberg was intent on bringing deep learning research to Facebook.

# The high of work

There are nice examples of researcher obsessiveness sprinkled throughout the book which complement the anecdotes I am currently reading in Cal Newport’s *Deep Work*. For example, Hinton “rated ideas on how much weight he had lost because he had forgotten to eat”. The “best Christmas present Hinton’s family could ever give was an agreement to let him go back into the lab and do a little more research”.

Navdeep Jaitly obsessed over his speech recognition project at Google:

> He forgot his own limits. He worked each evening until eleven o’clock or midnight. When he got home, his wife would hand him the baby, who was up most of the night with colic. But it wasn’t hard to repeat the same cycle the next day. “It was addictive,” he says. “The results kept getting better.”

# Location, location, location

Navdeep Jaitly’s audio recognition project at Google ended up being a grand success. It was one of deep learning’s earliest victories. In less than a week, the project’s neural net had better accuracy than the state-of-the-art speech recognition [expert system](https://en.wikipedia.org/wiki/Expert_system) on Android phones. Android quietly made the switch to Jaitly’s neural nets. At the time, its phones carried a chip for removing background noise. This was helpful for the expert system. After the switch, their chip supplier called — the chip was no longer boosting audio recognition performance. The neural net was so good that it had learned to deal with noise.

For all its glory, however, the team began incredibly ragtag:

> Each GPU card was equipped with a fan that whirred incessantly as it struggled to keep the hardware from overheating, and \[Vincent Vanhoucke\] worried that someone would get fed up with the noise and shut the machine down without realizing what it was for. He put it behind the printer so that anyone who heard the whirring of the fans would blame the printer for all the noise.

This environment nicely mimics the makeshift victories of MIT's famous [Building 20](https://en.wikipedia.org/wiki/Building_20). According to Cal Newport’s *Deep Work*, it was a temporary timber workspace where “\[w\]alls and floors could be shifted and equipment bolted to the beams” as needed for collaboration between the “haphazard combination of different disciplines” housed within it, ranging from “nuclear science to linguistics to electronics”. The building gave the world Chomsky grammars, the navigational radar, the atomic clock, [this stop-action shot of a bullet going through an apple](https://edition.cnn.com/style/article/harold-edgerton-bullet-apple-snap/index.html) and [Bose speakers](https://en.wikipedia.org/wiki/Amar_Bose). Holed up in a closet-sized room in the building, Rainer Weiss [came up](https://www.quantamagazine.org/rainer-weiss-remembering-the-little-room-in-the-plywood-palace-20170615/) with the experiment that was the precursor to LIGO. Building 20 [has been described](https://www.nytimes.com/1998/03/31/science/last-rites-for-a-plywood-palace-that-was-a-rock-of-science.html) as one of America’s two prominent wartime “shrines of the triumph of science” (along with the atomic bomb research installation at Los Alamos). At one time, “more than 20 percent of the physicists in the United States (including nine Nobel Prize winners) had worked” in Building 20\.

[Walter Brattain](https://en.wikipedia.org/wiki/Walter_Houser_Brattain) and [John Bardeen](https://en.wikipedia.org/wiki/John_Bardeen), too, invented the transistor in a small lab. Shuji Nakamura, who did [Nobel-winning](https://www.nobelprize.org/prizes/physics/2014/nakamura/facts/) without a PhD (I mention this only because his lack of a PhD was a chip on Nakamura’s shoulder), [invented](https://www.youtube.com/watch?v=AF8d72mA41M) the blue LED out of a cramped Nichia lab. Nvidia was [started](https://blogs.nvidia.com/blog/nvidia-dennys-trillion/) in a Denny’s because “\[i\]t had all the coffee you could drink and no one could chase you out”. The number of startups that began in garages is practically infinity — HP, Apple, Microsoft, Google, Dell, Amazon, Disney, even [Harley-Davidson](https://www.harley-davidson.com/us/en/content/expert-advice/harley-davidson-early-history.html) and [Mattel](https://en.wikipedia.org/wiki/Mattel). In *The Formula*, Joshua Robinson and Jonathan Clegg describe how the Formula One [team](https://en.wikipedia.org/wiki/Team_Lotus) that invented the monocoque chassis was started out of a block of stables. The first [Y Combinator](https://www.ycombinator.com/) companies, I think, were run out of similarly scrappy settings.

You need offices that could be featured in *Architectural Digest* ([Apple](https://en.wikipedia.org/wiki/Apple_Park), [Nvidia](https://www.youtube.com/watch?v=qDg_3eqssig), [Facebook](https://www.archdaily.com/901572/facebook-expands-menlo-park-headquarters-with-mpk-21-building-by-gehry-partners), [Square](https://www.officelovin.com/2022/06/a-look-inside-san-francisco-chronicles-new-san-francisco-office/)) only for expanding a company. *Starting* a company requires, to use a Newport phrase, “a laptop and a flat surface to put it on”.