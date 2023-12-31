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
	* If, of the many possible bases of classification, a particular one is desired, it can generally be transferred to the perceptron by a *forced learning* session or by an *error correction* training process. 
	* If left to its own resources the perceptron can still divide up into classes the patterns presented to it, on a classification basis of its own forming. This formation process is commonly referred to as *spontaneous learning*.
1. The Mark I Perceptron implemented a simple neural network made of three layers of units that were connected in progression: 'Sensory or S-units, Association or A-units, Response or R-units'. 
1. The input layer (also called the 'retina') was a 20-by-20-pixel camera, featuring 400 photoreceptors in total. 
1. These sensory units were randomly or topologically connected, with fixed weights, to a layer of 512 associative units. 
1. The associative units were themselves connected to eight response units (R- units, or output) with weights that could be adjusted automatically (these 'weights' were analogue potentiometers that could be also controlled by hand).
1. Like Warren McCulloch and Walter Pitts's artificial neurons, associative and response units operated according to a threshold value: they would sum up their input values and fire only if the sum was above a given threshold The operator's manual described it as a sort of implementation of the Hebbian rule, but this is perhaps a generous interpretation:
	* *The A-units, however, differ from the others in that when they do switch on, the excitation which they transmit to the R-units has a value which is dependent on the comparative success which that A-unit has had in contributing to the switching of its R-unit in the past. These values form the memory of the perceptron.*
1. In this intricate tangle of wires, one has only to remember that the parameters that could be trained were the potentiometers linking A-Units with R-Units. 
1. In total, 512 x 8 = 4096 parameters. To be precise, the Mark I Perceptron was running eight simple perceptrons in parallel, each one for a dedicated pattern to be recognised. 
1. Given a retina of 20-by-20 pixels, each simple perceptron featured 400 parameters. 
1. In any case, in terms of algorithmic complexity, this was already a big number of variables to be computed by incremental approximation with the resources of the time. 
1. Today, to give an idea of the different scale of complexity, three lines of Python code suffice to run the perceptron algorithm on a desktop computer, whereas a large model such as GPT4 comprises of around 1 trillion parameters (which requires a large data centre for training and deployment).  
1. The randomness of the initial connections and weights was crucial for Rosenblatt to demonstrate that the perceptron displayed a capacity of self- organisation, even when initialised from a chaotic state. 
1. Rosenblatt was enthusiastic about the perceptron's computing resolution, remarking: 'It is clear that with an amazingly small number of units -- in contrast with the human brain's 1010 nerve cells -- the perceptron is capable of highly sophisticated activity.' 
1. The architecture of the perceptron could vary and assume different configurations with more layers and functions.
1. It was already clear in Rosenblatt's papers that guessing the optimal configuration of the computing network was a craft of its own, forming part of the experimental practice.  
1. Guessing a good architecture for the perceptron was only half of the problem; the other half was to design a training algorithm and errorcorrection technique to find the optimal value of the parameters expressed by the network connections. 
1. The training procedure was based on the assumption that if a solution to the classification problem existed (if the set of images could be linearly separated in two groups), the parameters would converge to the optimal values in a finite number of steps. 
1. A main algorithm to train the perceptron was the following procedure of step-by- step approximation, which is basically an automated version of the technique of differential calculus:
	1. Start off with a perceptron having random weights and a training set.
	2. For the inputs of an example in the training set, compute the perceptron's output.
	3. If the output of the perceptron does not match the output that is known to be correct for the example:
		* If the output should have been 0 but was 1, decrease the weights that had an input of 1.
		* If the output should have been 1 but was 0, increase the weights that had an input of 1.
	4. Go to the next example in the training set and repeat steps 2--4 until the perceptron makes no more mistakes.
1. Today's deep learning employs more refined algorithms (such as gradient descent), but the trial-and-error principle remains the same: 
	1. *present an image to the neural network;*
	1. *check if the output is correct;*
	1. *if not, increase or decrease the parameters by a small value;*
	1. *repeat the procedure until the neural network computes the correct output.*
1. Once again, the problem is finding the most efficient procedure that converges to the final result in the fewest number of steps. 
1. The design of the training algorithm is a further level of abstraction and problem-solving, which is distinct from the structure of the neural network. 
1. On this view, what many still call 'artificial intelligence' is just a technique of mathematical optimisation. 
1. This is still a case of bruteforce approximation, the logic of which has become even more 'brute' in large models featuring trillions of parameters. 
1. Eventually, it is remarkable that at the heart of the most advanced techniques of 'artificial intelligence', one finds approximation procedures not dissimilar to those that constituted calculus since antiquity (see chapter 1). 
1. What was the Mark I Perceptron capable of? In terms of pattern recognition, not much. 
1. It was able to distinguish a black square on the left of the visual field from one on the right, and to distinguish simple letters if they were aligned on the centre of its 20-by-20 visual matrix. 
1. Its capacity for pattern recognition (as Marvin Minsky and Seymour Papert demonstrated in their famous criticism, explained below) was primitive and restricted to continuous figures. 
1. Rosenblatt and his team were aware of its limitations, but they speculated that architectures with more layers (as deep learning eventually proved) could perform more complex tasks of recognition:
	* *It seems reasonable to expect that a machine similar to the Perceptron with a logical depth of three or more (obtained by two or more layers of A-Units, with each layer providing the excitation for the next) would be even more powerful than the Perceptron.*
1. It should be noted that in 1958, Rosenblatt already envisioned spatial constraints similar to the filters that grounded the idea of convolution neural networks at the origin of deep learning. 
1. Specifically, in *Neurodynamics*, he mentioned David Hubel and Torsten Wiesel's study of the cat's cortex and their topological constraints, which would later inspire Kunihiko Fukushima's 'neocognitron' neural network (1980), Yann LeCun's architecture known as 'LeNet' (1989), and finally AlexNet (2012). 
1. Rosenblatt was also aware of the logical limits of statistical neural networks in imitating human intelligence, writing: 'Statistical separability alone does not provide a sufficient basis for higher order abstraction. 
1. Some system, more advanced in principle than the perceptron, seems to be required at this point.' 
1. To date, lacking a complete theory of statistical learning, artificial neural networks and deep learning are still at the epistemic stage of *experiments*. In other words, they are machines of unknown potentialities and unpredictable failures.

### Brain models and experimental method

1. The simple perceptron was not the first artificial neural network but the first adaptive one -- meaning it was able not just to recognise patterns but to learn how to recognise them (and to be rewired in different configurations in order to learn differently). Although its achievements were primitive, it is considered, nevertheless, the first classifier algorithm. As previously illustrated, the neural network architecture was already known: in order to demonstrate the capacity of self-organisation and adaptation of brain neurons, Rosenblatt intended to initiate the perceptron with random values. Rosenblatt then applied an errorcorrection algorithm to gradually adjust these values and have them converge towards an optimal equilibrium with external data, achieving in this way 'intelligence' as a spontaneous order emerging from chaos.  The hype around neural networks and self-organising theories (see chapter 6) initially caused ill feeling and envy among the 'artificial intelligentsia', especially in the circles of symbolic AI that were competing for the same military funds. In order to counteract this negative response, in 1961 Rosenblatt went on to systematise his research in the lengthy monograph Principles of Neurodynamics, which, while little studied, remains the best source to understand the origins of artificial neural networks. However, an essay from 1964, 'Analytic Techniques for the Study of Neural Nets', better illustrates Rosenblatt's research perspective. In this later text, in order to defend the experimental nature of artificial neural networks, Rosenblatt polemically mobilised the Galilean method against the Aristotelian one, which, in his view, was still used in other studies of brain models. Symbolic AI theorists, for instance, believed in the possibility of encoding the mind's rules into the machine's rules straightforwardly, without experimental testing:






