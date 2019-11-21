# Automatic Fact Verification and Misinformation Detection

Great thanks to Franziska Roesner @ UW for her course CSE599B: Technology-enabled misinformation

# Info

This is a computer science course, expecting some knowledge of machine learning

## What we will learn
* Describing and categorising misinformation
* How technology is misused
* Mitigating misinformation
* Detecting misinformation on the web
* Monitoring user reactions
* Detecting lies through style
* Checking factual claims
* How to identify suspicious accounts and networks

## Assessment

Three assignments, worth 30%, 30%, and 40% of the final grade. The final assignment should be written as a research paper, and may be submitted to an academic venue.

# Week 1

## Day 1: What is this?

* [Intro slides](1+intro.pdf)
* [War of the Worlds broadcast](https://www.youtube.com/watch?v=Xs0K4ApWl4g&feature=youtu.be&t=11m01s) ; [NYT manipulation quiz](https://www.nytimes.com/interactive/2018/09/04/technology/facebook-influence-campaigns-quiz.html)
* [Why ‘fake news’ is a Flawed Term](https://gate-socmedia.group.shef.ac.uk/why-fake-news-is-a-flawed-term/)
* Part 1 : introduction and examples [link](1-cse599b-18au.pdf)
* Part 2 : describing the misinformation space [link](2-cse599b-18au.pdf)
* [Exercise 1](exercise%201.pdf) : Personal experience study 


## Day 2: Measuring the problem

* Present exercise 1
* Research case studies. [Ecosystem or Echo-System? Exploring Content Sharing across Alternative Media Domains](https://faculty.washington.edu/kstarbi/Starbird-et-al-ICWSM-2018-Echosystem-final.pdf) ; [Acting the Part: Examining Information Operations Within #BlackLivesMatter Discourse](https://faculty.washington.edu/kstarbi/BLM-IRA-Camera-Ready.pdf) ; ["Who Shared It?": How Americans Decide What News to Trust on Social Media](http://mediainsight.org/PDFs/Trust%20Social%20Media%20Experiments%202017/MediaInsight_Social%20Media%20Final.pdf) ; [4chan](http://www.4chan.org)
* Measuring the problem, including the [AMI model](https://rm.coe.int/information-disorder-toward-an-interdisciplinary-framework-for-researc/168076277c) (pages 4-19)
* Backfire effect and confirmation bias. Slides [link](4-cse599b-18au.pdf) [link](5-cse599b-18au.pdf)
* [Exercise 2](exercise%202.pdf) : Case study

## Day 3: False video

* Present exercise 2
* Video fakes [slides](6-cse599b-18au.pdf)
* [Early deepfakes](http://niessnerlab.org/projects/thies2016face.html)
* [Recent deepfakes](https://web.stanford.edu/~zollhoef/papers/SG2018_DeepVideo/page.html)
* Reading: [Deepfakes and Synthetic Media: What should we fear? What can we do?](https://blog.witness.org/2018/07/deepfakes/)
* [Exercise 3](exercise%203.pdf): fake image

## Day 4: Micro-targeting
* Present exercise 3
* Micro targeting [slides](7-cse599b-18au.pdf)
* Panopticon: give yourself a [privacy check](https://panopticlick.eff.org)
* Article: [Attacks on privacy on Facebook](https://arxiv.org/pdf/1803.10099.pdf)
* [Web Tracking FAQ](http://trackingexcavator.cs.washington.edu/faq.html)
* [Exercise 4](exercise%204.pdf): compare how you can be tracked

## Day 5: Bots and fake content
* Present exercise 4
* Bots and abusive labour markets [slides](8-cse599b-18au.pdf), "Dirty jobs" [paper](https://www.usenix.org/legacy/event/sec11/tech/full_papers/Motoyama.pdf), [slides](https://cseweb.ucsd.edu/~dok027/papers/Kim_TopicModeling_Freelance.pdf)
* Neural language generation: [GPT-2](https://openai.com/blog/better-language-models/) (openly available), [Grover](https://arxiv.org/abs/1905.12616) (better than human) -- and a [GPT-2 blog post](https://towardsdatascience.com/openai-gpt-2-understanding-language-generation-through-visualization-8252f683b2f8).
* Assignment 1 [pdf](assignment%201.pdf) Due end of September 6th ([DeepFaceLab tutorial](dfl))

# Week 2

## Day 1
* Go through assignment (thanks!)
* Defences: [data mining](https://arxiv.org/pdf/1708.01967.pdf); [Fake News Challenge reflections](https://arxiv.org/pdf/1806.05180.pdf); [training your own fake news detection](https://towardsdatascience.com/i-trained-fake-news-detection-ai-with-95-accuracy-and-almost-went-crazy-d10589aa57c); [shades of truth and political fact checking](http://www.aclweb.org/anthology/D17-1317); [the FEVER dataset](https://arxiv.org/pdf/1803.05355.pdf) and [the FEVER challenge](https://www.fever.ai)

## Day 2
* [Peace and Conflict lab](https://pcnlab.asc.upenn.edu/)
* Neuroscience perspectives: [Persuasion, influence and value](https://www.annualreviews.org/doi/abs/10.1146/annurev-psych-122216-011821), [Testable and non-testable beliefs](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0124596),  [Asymmetic decision making](https://pubsonline.informs.org/doi/10.1287/mnsc.2015.2233)
* Cognitive biases: [List of 67](https://www.neurosciencemarketing.com/blog/articles/cognitive-biases-cro.htm)
* Perspectives - small exercise: [pdf](day2-perspectives.pdf)

## Day 4
* NLP intro [slides](1b%20-%20nlp%20outline.pdf)
* Tokens and tokenisation [slides](1f%20-%20tokenization.pdf) 
* Naive Bayes classification [slides](2c%20-%20ngrams%20exercise%20(movie%20reviews).pdf), sentiment [notebook](reviews.ipynb) 

## Day 5
* Sentiment with LSTM [blog + notebook](https://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/)
* Stance detection [slides](dast-slides.pdf) (first half)
* Fake news challenge [link](http://www.fakenewschallenge.org/)
* HMM for predicting truth [slides](dast-slides.pdf) (second half)

## Project 2
* Due 18 November; 40% of the final mark. [Description](project2.pdf)

# Week 3

## Day 1
* Fact Checking for Journalists [slides](https://centerforcooperativemedia.org/wp-content/uploads/sites/5/2014/10/NJ-Fact-Checking-Workshop-Slides.pdf)
* Crowdsourcing: [for single values](https://www.ft.com/content/bfb7e6b8-d57b-11e1-af40-00144feabdc0), [for rare info](https://www.reddit.com/r/whatisthisthing/)
* Fact checks on social media content [Not fake food](https://www.youtube.com/watch?v=vSBSzWmjXO0)
* Advanced search - Power searching with Google [tutorial](http://www.powersearchingwithgoogle.com/) - learn site:, filetype: operators; how to use ""; each country and search engine is different
* Finding dead/deleted files: [archive.org](http://web.archive.org/) [cachedview.com](https://cachedview.com/) - check out Uber's "Four Septembers" cherry-picking article and its disappearance

## Day 2
* Continue "Fact Checking for Journalists" workshop [slides](https://centerforcooperativemedia.org/wp-content/uploads/sites/5/2014/10/NJ-Fact-Checking-Workshop-Slides.pdf)
* Discuss the initial article in [INFEKTION](https://en.wikipedia.org/wiki/Operation_Infektion); go through AMI and the 7 steps - How would you classify this? Who would you contact? What's the evidence? What are the questions?

## Day 3
* Fact extraction: [paper](http://eprints.whiterose.ac.uk/91378/1/Identification%20and%20verification.pdf), [colab](https://colab.research.google.com/drive/1owZ8tVXgpUnFSMScfNaZq0AsnSXrtuuf), [spaCy](https://spacy.io/), [wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page), [exercise](factextr-assn.pdf)

## Day 4
* Triple extraction presentations
* Fact check: AMI+investigation for Pizzagate [news video](https://www.youtube.com/watch?v=XlxROGN_Nos), [news report](https://www.washingtonpost.com/local/pizzagate-from-rumor-to-hashtag-to-gunfire-in-dc/2016/12/06/4c7def50-bbd4-11e6-94ac-3d324840106c_story.html), [wikipedia](https://en.wikipedia.org/wiki/Pizzagate_conspiracy_theory)
* Fact check: AMI+investigation for SHIELD headwear [promo video](https://www.youtube.com/watch?v=cp95GUaw2oY), [video review](https://www.youtube.com/watch?v=i5UkXEM4aNU)
