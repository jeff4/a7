---
layout: ../../layouts/MdPostDescLayout.astro
title: 'Chapter 9'
LastUpdatedDate: 2024-01-10
CreatedDate: 2023-12-25
description: 'Matteo Pasquinelli'
author: 'Jeff'
tags: []


---
## The Invention of the Perceptron
### Quotes
* Frank Rosenblatt, interview in *The New Yorker* (1959): 'Our success in developing the perceptron means that for the first time a non-biological object will achieve an organization of its external environment in a meaningful way ... My colleague [Marshall Yovits] disapproves of all the loose talk one hears nowadays about mechanical brains. He prefers to call our machine a self-organizing system, but, between you and me, that's precisely what any brain is.'
* Frank Rosenblatt (1964): 'The role of experimentation becomes increasingly important as the systems to be considered grow in complexity, while the amount that can be accomplished by purely logical reasoning falls increasingly short of a complete understanding of the system's performance. This does not mean that an abandonment of theoretical analysis is advocated but, rather, in the spirit of Galileo, that theory must be matched by experiment at all times, and that from the interaction of theory and experiment will emerge the knowledge of the proper steps which must follow.'
* Simon Schaffer (2011): "Faults are defaults, yet instruments perform. A principle of science studies is that dissensus is instructive, not pathological, and that agreement is not inevitable, but to be explained.  Instruments' adequate function needs comparable analysis. Then 'the big question' is how it's judged that instruments are working and, indeed, what they are."

### An organization of the external environment in a meaningful way
1. In 1958, two years after the Dartmouth workshop on AI, *The New York Times* granted bold headlines to the project of a new 'thinking machine': the artificial neural network 'perceptron'. Its inventor, the psychologist Frank Rosenblatt (at the time only thirty years old), and its sponsor, Marshall Yovits of the US Office of Naval Research, were looking for good press to justify the expenditure of taxpayer money. 
1. In praise of the invention, the newspaper cartoonishly reported that 'the Navy revealed the embryo of an electronic computer that it expects will be able to walk, talk, see, write, reproduce itself and be conscious of its existence'. 
1. It was fanfare for the military, yet some of the article's exaggerations predicted the creepy future achievements of deep neural networks. For instance, the article was eerily prescient regarding face recognition and natural language processing that would emerge half a century later: 'Later Perceptrons will be able to recognize people and call out their names and instantly translate speech in one language to speech or writing in another language.'
1. In the same year, *The New Yorker* featured more sober coverage in the form of an interview with Rosenblatt, who clarified that the perceptron was not 'a mechanical brain', as the hype claimed, but a self-organising machine that could likewise provide 'an organization of its external environment in a meaningful way'. Paraphrasing the Hebbian principle of neuroplasticity ('Neurons that fire together, wire together'), the magazine gave an accurate account, for the time, of the working of an artificial neural network:
	* The distinctive characteristic of the perceptron is that it interacts with its environment, forming concepts that have not been made ready for it by a human agent. 
	* Biologists claim that only biological systems see, feel, and think, but the perceptron behaves as if it saw, felt, and thought. Both computers and perceptrons have so-called memories; in the latter, however, the memory isn't a mere storehouse of deliberately selected and accumulated facts but a free, indeterminate area of association units, connecting, as nearly as possible at random, a sensory input, or eye, with a very large number of response units.
	* If a triangle is held up to the perceptron's eye, the association units connected with the eye pick up the image of the triangle and convey it along a random succession of lines to the response units, where the image is registered. 
	* The next time the triangle is held up to the eye, its image will travel along the path already travelled by the earlier image. 
	* Significantly, once a particular response has been established, all the connections leading to that response are strengthened, and if a triangle of a different size and shape is held up to the perceptron, its image will be passed along the track that the first triangle took. 
1. What kind of artificial neural network was the perceptron? 
1. Rosenblatt struggled to explain the workings of perceptrons in simple terms and later lamented that media hype spoiled 'scientific confidence'. At the Cornell Aeronautical Laboratory in Buffalo, New York, it was filed as 'Project PARA: Perceiving and Recognising Automaton'. 
1. The Navy -- the main backer of the project -- was essentially interested in the automation of target classification, such as the reconnaissance of enemy vessels through radar, sonar, or visual data.
1. Rosenblatt also planned to design, aside photoperceptrons, a whole class of devices operating with the same logic which included phonoperceptrons (to recognise words in audio communications) and radioperceptrons (to recognise objects in radar and sonar signals). 
1. Technically speaking, the perceptron was a statistical neural network for pattern recognition -- that is, a self-organising computing network for the classification of stimuli in a binary way, as briefly mentioned in previous chapters.

### The Mark I Perceptron
1. The first implementation of the perceptron was a computer simulation written in the SHARE programming language and run, in 1957, on an IBM 704, one of the first commercial mainframes. In the earliest tests, the computer was fed a series of punched cards, and apparently, after fifty trials, it 'taught itself to distinguish cards marked on the left from cards marked on the right'. 
1. Rosenblatt considered this proof that a more complex architecture of the perceptron could be designed to recognise more complex patterns. Shortly after *The New York Times* article, this idea took the form of a bulky piece of hardware which would be completed only in 1960: the legendary Mark I Perceptron which now rests at the Smithsonian National Museum of American History in Washington, DC. 
1. The Mark I was the same digital computer that had been used by John von Neumann in the 1940s to make calculations for the Manhattan Project; however, in this implementation, it was extended by the analogue module of the Perceptron. 
1. Though it was a thousand times slower than the IBM 704, this hardware--software hybrid allowed a programmer to rewire the network by hand, which was faster than rewriting a program. 
1. The operator's manual described it in this way:
	* The Mark I Perceptron is a pattern learning and recognition device. 
	* It can learn to classify plane patterns into groups on the basis of certain geometric similarities and differences. 
	* Among the properties which it may use in its discriminations and generalizations are position in the retinal field of view, geometric form, occurrence frequency, and size. 
	* If, of the many possible bases of classification, a particular one is desired, it can generally be transferred to the perceptron by a forced learning session or by an error correction training process. 
	* If left to its own resources the perceptron can still divide up into classes the patterns presented to it, on a classification basis of its own forming. This formation process is commonly referred to as spontaneous learning.
