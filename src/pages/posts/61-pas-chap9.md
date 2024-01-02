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

### 10. An organization of the external environment in a meaningful way
1. In 1958, two years after the Dartmouth workshop on AI, *The New York Times* granted bold headlines to the project of a new 'thinking machine': the artificial neural network 'perceptron'. Its inventor, the psychologist Frank Rosenblatt (at the time only thirty years old), and its sponsor, Marshall Yovits of the US Office of Naval Research, were looking for good press to justify the expenditure of taxpayer money. 
1. In praise of the invention, the newspaper cartoonishly reported that 'the Navy revealed the embryo of an electronic computer that it expects will be able to walk, talk, see, write, reproduce itself and be conscious of its existence'. 
1. It was fanfare for the military, yet some of the article's exaggerations predicted the creepy future achievements of deep neural networks. For instance, the article was eerily prescient regarding face recognition and natural language processing that would emerge half a century later: 'Later Perceptrons will be able to recognize people and call out their names and instantly translate speech in one language to speech or writing in another language.'

### 12 JH Break

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

### 20. The Mark I Perceptron
1. The first implementation of the perceptron was a computer simulation written in the SHARE programming language and run, in 1957, on an IBM 704, one of the first commercial mainframes. In the earliest tests, the computer was fed a series of punched cards, and apparently, after fifty trials, it 'taught itself to distinguish cards marked on the left from cards marked on the right'. 
1. Rosenblatt considered this proof that a more complex architecture of the perceptron could be designed to recognise more complex patterns. Shortly after *The New York Times* article, this idea took the form of a bulky piece of hardware which would be completed only in 1960: the legendary Mark I Perceptron which now rests at the Smithsonian National Museum of American History in Washington, DC. 
1. The Mark I was the same digital computer that had been used by John von Neumann in the 1940s to make calculations for the Manhattan Project; however, in this implementation, it was extended by the analogue module of the Perceptron. 
1. Though it was a thousand times slower than the IBM 704, this hardware--software hybrid allowed a programmer to rewire the network by hand, which was faster than rewriting a program. 
1. The operator's manual described it in this way:
	* *The Mark I Perceptron is a pattern learning and recognition device.*
	* *It can learn to classify plane patterns into groups on the basis of certain geometric similarities and differences.*
	* *Among the properties which it may use in its discriminations and generalizations are position in the retinal field of view, geometric form, occurrence frequency, and size.*
	* *If, of the many possible bases of classification, a particular one is desired, it can generally be transferred to the perceptron by a *forced learning* session or by an *error correction* training process.*
	* *If left to its own resources the perceptron can still divide up into classes the patterns presented to it, on a classification basis of its own forming. This formation process is commonly referred to as *spontaneous learning*.*
1. The Mark I Perceptron implemented a simple neural network made of three layers of units that were connected in progression: 'Sensory or S-units, Association or A-units, Response or R-units'. 

### 22 JH Break 

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

### 24 JH Break

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

### 26 JH Break

1. This is still a case of brute force approximation, the logic of which has become even more 'brute' in large models featuring trillions of parameters. 
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

### 30. Brain models and experimental method

1. The simple perceptron was not the first artificial neural network but the first *adaptive* one -- meaning it was able not just to recognise patterns but to learn how to recognise them (and to be rewired in different configurations in order to *learn differently*). 
1. Although its achievements were primitive, it is considered, nevertheless, the first classifier algorithm. 
1. As previously illustrated, the neural network architecture was already known: in order to demonstrate the capacity of self-organisation and adaptation of brain neurons, Rosenblatt intended to initiate the perceptron with random values. 
1. Rosenblatt then applied an errorcorrection algorithm to gradually adjust these values and have them converge towards an optimal equilibrium with external data, achieving in this way 'intelligence' as a spontaneous order emerging from chaos.  
1. The hype around neural networks and self-organising theories (see chapter 6) initially caused ill feeling and envy among the 'artificial intelligentsia', especially in the circles of symbolic AI that were competing for the same military funds. 
1. In order to counteract this negative response, in 1961 Rosenblatt went on to systematise his research in the lengthy monograph *Principles of Neurodynamics*, which, while little studied, remains the best source to understand the origins of artificial neural networks. 

### 32 JH Break

1. However, an essay from 1964, 'Analytic Techniques for the Study of Neural Nets', better illustrates Rosenblatt's research perspective. 
1. In this later text, in order to defend the experimental nature of artificial neural networks, Rosenblatt polemically mobilised the Galilean method against the Aristotelian one, which, in his view, was still used in other studies of brain models. Symbolic AI theorists, for instance, believed in the possibility of encoding the mind's rules into the machine's rules straightforwardly, without experimental testing:
	* *For the two millennia which followed Aristotle, it was believed that the fundamental truths of nature could be revealed through the application of pure reason, that it was the philosopher, rather than the experimenter, who might discern the necessary order of nature through the sheer power of his intellect...*
	* *Then, at the beginning of the seventeenth century, the publication of Galileo's 'Discourses on Two New Sciences' gave voice for the first time to the doctrine of the experimental method.* 
	* *Galileo's work, advocating a clear alternative to Aristotelian rationalism, engendered a period of scientific growth and discovery in the physical sciences which has not yet run its course*
	* *It may happen, by coincidence, that these results have application in the engineering domain, but for present purposes we propose to work not as inventors, but as discoverers, and the kind of theorizing which leads to scientific discovery is apt to be quite different from the kind of theorizing which is useful for engineering synthesis.*

### 33 JH Break

1. The way in which Rosenblatt claimed the role of 'discoverer' rather than 'inventor' can be considered naive but it was somehow a defence of the experimental and scientific method against the 'engineer mentality' of many cyberneticians. 
1. Rosenblatt professed the experimental culture of artificial neural networks research in particular against the selfproving logic of symbolic AI. In the introduction to *Neurodynamics*, similarly, Rosenblatt echoed McCulloch's method of 'experimental epistemology' to assert that:
	* *a perceptron is first and foremost a brain model, not an invention for pattern recognition.*
	* *As a brain model, its utility is in enabling us to determine the physical conditions for the emergence of various psychological properties.*
	* *It is by no means a 'complete' model, and we are fully aware of the simplifications which have been made from biological systems; but it is, at least, an analysable model.*
1. Siding with brain scientists rather than computer engineers was for Rosenblatt a way to contend the tentative, partial, and incomplete nature of the perceptron as an *experimental model*. 
1. In a similar fashion to Hayek, Rosenblatt maintained that a model of the brain is always an implementation, that is, a simplification and exaggeration of some of its traits, as he explained:
	* *Perceptrons are not intended to serve as detailed copies of any actual nervous system.* 
	* *They are simplified networks, designed to permit the study of lawful relationships between the organization of a nerve net, the organization of its environment, and the 'psychological' performances of which the network is capable.*
	* *Perceptrons might actually correspond to parts of more extended networks in biological systems...More likely, they represent extreme simplifications of the central nervous system, in which some properties are exaggerated, others suppressed.*
1. The perceptron was a machine constituted by numerous parameters to be adjusted in order to approximate a result. 

### 38 JH Break

1. If scientific experiments usually rely on testing models of few parameters, Rosenblatt's neural network can be regarded as an experimental simulation par excellence, given the increasing number of parameters to be determined. 
1. This experimental dimension was missing from symbolic AI, whose algorithms were instead often based on the opposite assumption -- that a limited number of rules could project unlimited intelligence without much acknowledgement of the critical role that implementation plays.27 The perceptron's numerical parameters were not a *representation* of the world as in symbolic AI; they were simply relational and partial elements in the construction of a *non-isomorphic model* of the world. 
1. This feature would escalate in deep learning, with algorithmic models such as GPT4 today featuring trillions of parameters. 
1. In fact, despite the seeming simplicity of its architecture, a neural network requires a number of operations that exponentially increases just by adding a few layers and connections. 
1. Writing the history of computation from the point of view of algorithmic complexity -- that is, the size of calculations and resource usage -- statistical neural networks such as the perceptron marked a hurdle that, at the time, could not be successfully crossed due to the lack of computing power.

### 40. From symbolic logic to vector space

1. The first international symposium on the newly established field of AI took place in November 1958 at the National Physical Laboratory in Teddington, West London, under the title 'Mechanisation of Thought Processes'. 
1. This event played a key role in the history of AI, but it has been rarely studied; here, for reasons of space, only Rosenblatt's contribution is considered. 
1. Rosenblatt took part in the symposium to clarify and defend the mathematical intuition behind the perceptron -- that is, the theorem of statistical separability of data in a multidimensional space. 
1. Standing apart from the rigid computationalism of other AI scholars who attended the symposium, Rosenblatt explained that the mathematics of the perceptron had much more in common with 'the mathematics of particle physics', namely statistics, than with the 'mathematics of digital computers'. 
1. In modelling the brain, Rosenblatt urged his colleagues to depart from the paradigm of digital computation because 'Boolean algebra, or symbolic logic, is well suited to the study of completely describable logical systems, but breaks down as soon as we attempt to apply it to systems on which complete information is not available'. 
1. In favour of his thesis, Rosenblatt mobilised also the authority of von Neumann, who had passed away just the year before. As seen already in chapter 7, von Neumann, in one of his last lectures, stressed:
	* *Logics and mathematics in the central nervous system...must structurally be essentially different from those languages to which our common experience refers...* 
	* *When we talk mathematics, we may be discussing a secondary language, built on the primary language truly used by the central nervous system.*
	* *Thus the outward forms of our mathematics are not absolutely relevant from the point of view of evaluating what the mathematical or logical language truly used by the central nervous system is* 

### 42 JH Break

1. Von Neumann argued that there is less 'logical depth' in the brain than in a computer, which may require millions of successive logical steps to imitate a simple thought process (known as the problem of 'combinatorial explosion' mentioned above). 
1. Following von Neumann, Rosenblatt similarly concluded that 'in dealing with the brain, a different kind of mathematics, primarily statistical in nature, seems to be involved [as the] brain seems to arrive at many results directly, or *intuitively*, rather than analytically'. 
1. It is clear from these passages that Rosenblatt intended to conceptualise the perceptron not as a logical but as a statistical machine -- that is, as a machine quite different from the paradigm of Boolean and binary computation that was emerging in those years. 
1. The genealogy of the perceptron points to a technological lineage that is related but clearly distinct from that of the digital computer.  
1. The invention of the perceptron, in fact, condenses influences that proceeded from diverse disciplines such as neurology, psychology, engineering, cybernetics, mathematics, and statistics. 

### 44 JH Break

1. Rosenblatt's book *Neurodynamics* is the best source to evidence such a conurbation of ideas. 
1. Aside from von Neumann, in *Neurodynamics* Rosenblatt credited the contributions of Nicolas Rashevsky, McCulloch and Pitts, as well as: 
	* Minsky for the idea of the logical neural network;
	* Albert Uttley for the probabilistic model of distributed memory;
	* Ross Ashby for the theory of self-organisation in machines;
	* Donald Hebb and Hayek for selfreinforcement in neural pathways;
	* Gestalt theorists for holistic perception and distributed memory, among others. 
1. But, how exactly did the perceptron constitute a breakthrough in the relation to this tradition? 
1. In a nutshell, as a technical form, the perceptron was an electromechanical computing network, but as a mathematical form, it expressed a novel trick: its adjustable parameters represented coordinates in a multidimensional vector space. 
1. This intuition has less to do with neurophysiology than with statistics. 
1. Rosenblatt's innovation was, as we will see below, to apply the statistical technique of multidimensional analysis (which had dominated US psychology in the 1950s) to image recognition. 
1. This technique has since then defined the logical form at the core of machine learning. 
1. The mathematical 'trick' to solve image recognition via multidimensional analysis can be reconstructed in this way. 
1. Each digital image in a training dataset is a two-dimensional matrix of numerical values that represent pixels. 
1. In addition to being a two-dimensional matrix, each image can also be defined as a single point in a multidimensional space whose coordinates are the values of each pixel. 

### 46 JH Break

1. For example, given the resolution of the Mark I Perceptron, an image of 20-by-20 pixels is equivalent to a single point in a multidimensional space of 400 dimensions. 
1. The projection of digital images onto a multidimensional space discloses unexpected properties. 
1. In such multidimensional space, for example, points that are closer together designate similar images, while points that are further apart designate dissimilar images. 
1. Furthermore, following the progression of a value along a single dimension, images can be arranged according to a specific gradient of similarity. 
1. In such a multidimensional space, pattern recognition can be performed, then, by separating a cluster of points (which represent a class of similar images) from all the others (which represent different images). 
1. A boundary (or 'hyperplane' in technical terms) can then be drawn to separate this dataspace in two regions, in order to declare which images belong to a class and which do not. 
1. The separation of the dataspace into two regions is called binary classification (from which also the term 'classifier algorithm' derives).
1. Rosenblatt's theorems of statistical separability argued that a perceptron could automate this act of classification on its own and find a hyperplane to linearly separate the vector space into two regions: one containing the images corresponding to the pattern to be 'learned', the other not. 
1. The parameters of the mathematical function of the hyperplane are the weights of the network connections. 
1. The weights of the perceptron plot the hyperplane and adjust its inclination across the hyperspace until the two clusters are perfectly separated. 

### 48 JH Break

1. In the case of the simple perceptron (with 400 weights between association and output units), the hyperplane would be defined by a linear equation with 400 unknowns. 
1. The values of this equation (which are the weights of the neural network) are found by the training algorithm through the stepby-step procedure of approximation abovementioned.  
1. The perceptron is a crucial episode in the history of cultural techniques: it entails not just a process of digitisation of the picture plane into a two- dimensional numerical matrix but its vectorisation into a statistical matrix of multiple dimensions. 
1. With this method, the human faculty of image recognition was translated and reduced to a problem of mathematical optimisation in a vector space. 
1. Since then, however, its influence has gone far beyond image recognition: vectorisation in multiple dimensions has been applied to all kinds of data and has come to represent the epistemic form of the 'intelligence' that machine learning embodies in general, which is a form of *statistical intelligence*. 
1. The characteristic of 'intelligence' that is anthropomorphised in AI systems is essentially the trick of projecting data on a multidimensional space in order to perform operations of clustering, classification, and prediction. At its core, machine learning exhibits the quality of geometric and spatial 'intelligence'.

### 50. The new vectors of mind

1. During the 1950s, psychometrics emerged as an influential subfield in the departments of psychology across US universities. 
1. It represented quite a reductionist turn in the study of the psyche, as it was mainly concerned with the quantification and statistical measurement of personality traits, cognitive abilities, and work skills. 
1. Eventually, it became a common practice for many students to render data from psychological tests into vectors in order to calculate similarities, covariances, and find patterns of different sorts.  
1. Tracing the origins of the perceptron, the AI scholar Jonathan Penn has recently found that Rosenblatt already employed psychometric techniques of multidimensional analysis in his doctoral research, with the purpose of examining personality profiles. 
1. In 1953, Rosenblatt asked two hundred students of Cornell University to answer a questionnaire about their childhood using a numerical scale for each answer, pursuing the typical postulate of psychometrics that 'personalities can be classified objectively'. 
1. In the tradition of the psychometrics of Alfred Binet, Lewis Terman, Charles Spearman, and especially Louis Leon Thurstone, Rosenblatt analysed the results through a method of factor analysis in order to compute the similarity between the numerical matrices of each questionnaire. 
1. In this way, the twenty-five-year-old Rosenblatt intended to prove the mathematical presence of clusters of similar answers and, therefore, to demonstrate, as a psychometrician of sound faith would do, the existence of distinguishable personalities.  

### 51 JH break

1. It was probably towards the end of his PhD that Rosenblatt noticed that the numerical matrices of cognitive tests looked identical to the numerical matrices of digital images and began to consider applying the same techniques of multidimensional analysis to visual pattern recognition. 
1. It is apparent that Rosenblatt's perceptron was computing patterns of similarity in numerical images in the same way in which psychometrics was computing patterns of similarity in the numerical matrices of psychological profiles.
1. This is another example of the spurious and experimental genealogies of AI, which points, however, to a specific and intriguing modality of technological innovation in which metrics anticipates automation: Rosenblatt, in fact, repurposed the tools that were used to quantify a cognitive task for the automation of the cognitive task itself.  
1. During his PhD, Rosenblatt had another idea that served as a precursor to the perceptron: he planned to automate statistical analysis with a new calculating machine that was then called the Electronic Profile Analyzing Computer (EPAC). 
1. The journal *American Scientist* described it in this way: 
	* *An 'idiot brain', an electronic computer that can solve only one type of problem, has been designed and built by a 25-year-old psychology student at Cornell University.*
	* *The machine is helping its inventor, Frank Rosenblatt to prepare data for his Ph.D. thesis at the University.* 
	* *A problem that would take 15 minutes to solve with a desk computer can be solved by the machine in two seconds. Rosenblatt is testing the idea that personalities can be classified in a scientific and objective way.*
1. Predating the Mark I Perceptron, Rosenblatt's EPAC was a first experiment in the automation of multidimensional analysis, a task which was commonly assigned to human 'computers' (often women) in the psychology laboratories of the time. 
1. In the same way in which Babbage put a calculating engine in place of a human computer, it could be said that Rosenblatt put a computer in place of a statistician, shaping machine learning as it is understood today. 

### 52 JH break

1. During his PhD, Rosenblatt aimed to empower psychometrics with the help of a computer, but it was psychometrics, in fact, that helped to calculate the matrices of artificial neural networks and contributed to forge a new -- statistical this time -- model of the synthetic mind.  
1. It is of historical relevance that the perceptron advanced the automation of statistical tools precisely in the same years when they were becoming a predominant method in US psychology. 
1. This institutionalisation of statistics in US psychology between 1940 and 1955 has been studied and confirmed also by the German psychologist Gerd Gigerenzer. 
1. In addition, Gigerenzer has noticed another critical phenomenon, the transformation of the tools of psychological analysis into a theory of the mind in its own right:
	* *The statisticians' conquest of new territory in psychology started in the 1940s...*
	* *By the early 1950s, half of the psychology departments in leading American universities offered courses on Fisherian methods and had made inferential statistics a graduate program requirement.*
	* *By 1955, more than 80% of the experimental articles in leading journals used inferential statistics to justify conclusions from the data...I therefore use 1955 as a rough date for the institutionalization of the tool in curricula, textbooks, and editorials...*
	* *In experimental psychology, inferential statistics became almost synonymous with scientific method.  Inferential statistics, in turn, provided a large part of the new concepts for mental processes that have fueled the so-called cognitive revolution since the 1960s.*
	* *Theories of cognition were cleansed of terms such as restructuring and insight, and the new mind has come to be portrayed as drawing random samples from nervous fibers, computing probabilities, calculating analyses of variance (ANOVA), setting decision criteria, and performing utility analyses.*
	* *After the institutionalization of inferential statistics, a broad range of cognitive processes, conscious and unconscious, elementary and complex, were reinterpreted as involving 'intuitive statistics'.*
1.  Gigerenzer provides a realistic periodisation that is compatible with the adoption of statistical techniques also in the artificial neural networks research. 

### 53 JH Break

1. Considering Rosenblatt's PhD (1956) and his first paper on the perceptron (1957), the 1950s are indeed the years in which statistical tools of multidimensional analysis made an interdisciplinary leap and were applied to artificial neural networks and the automation of pattern recognition. 
1. It is through this path that psychometrics entered the history of AI and imparted a statistical mentality to it. 
1. These advancements come as no surprise considering that, at the beginning of the century, psychology had already attempted to quantify human intelligence in a statistical way. 
1. Indeed, the automation of intelligence in the twentieth century was prepared by its measurement in the nineteenth century, by the establishment of a standard metrology of cognitive abilities (such as solving a puzzle or recognising a picture) rather than the study of the mind's logic. 
1. As pointed out by the historian of science Simon Schaffer:
	* *Since the Enlightenment, neurology, anthropology and physiology have often relied on such measures: oxygen flow, pulse rate, galvanic activity, phrenological charts, cerebral thermometry or -- most pervasively -- cranial capacity have all been used as markers of underlying brain activity and thus intellectual, social and moral rank.*
	* *No doubt the instruments used to make such measures then become the source of neurological metaphor.* 
	* *But this kind of cerebral metrology embraces a wider history than that which links craniometry with more recent strategies of intelligence testing and psychometrics.*
1. To what extent could the performance of a machine be judged as 'intelligent' -- that is, commensurable (measurable in the same terms) with human intelligence? 

### 54 JH break

1. Since the Turing test, machines have been judged as 'intelligent' by comparing their behaviour with social conventions. Cybernetics investigated this question in a different way, that is, by postulating a common 'mechanism' (whatever logical or physiological) between humans and machines. 
1. But in the decades prior to cybernetics and computer science, psychometrics had already turned human intelligence into a quantifiable (and potentially computable) object. 
1. In the early twentieth century, Spearman, for instance, proposed the statistical measurement of 'general intelligence' (or g factor) as the correlation between unrelated tasks in a skill test. 
1. For Spearman, these correlations mathematically demonstrated the existence of an underlying cognitive faculty that common sense would refer to as 'intelligence'. 
1. Spearman's analysis was based on two factors: general intelligence (g) and specific ability (s). 
1. A few decades later, Thurstone criticised Spearman's reduction of intelligence to only two factors and proposed the consideration of multiple factors, listing up to seven intelligence attributes or 'primary mental abilities'. 
1. There was enthusiasm about the flexibility of these statistical techniques which could potentially escalate the number of their dimensions and model the most complex aspects of mind and the world. 

### 55 JH break

1. In 1935, Thurstone published a book by the visionary title *The Vectors of Mind*, which aimed to provide students with an accessible introduction to multifactor analysis, moving psychol- ogy closer and closer to the mentality of statistics.46 Such a quantitative measure of intelligence, abstracted from social circumstances and deprived of any historical contexts, supported, however, a meritocratic social order and helped consolidate, among others, the questionable practice of measuring the intelligence quotient (IQ). 
1. These techniques were, and still are, instrumental to maintaining social hierarchies and racial segregation, and in disciplining the workforce. 
1. It must be remembered that the pseudoscience of psychometrics was founded by the English statistician Francis Galton with the racist and eugenicist agenda of demonstrating a correlation between intelligence and ethnicity. 
1. It is perhaps no coincidence that a system for mathematically discriminating between humans of different classes and 'races' has been subsequently used to equate humans to machines.  
1. Spearman's g factor contributed to the reification of 'intelligence' as a new scientific 'object' that could be statistically measured. 
1. As mentioned above, Gigerenzer has also noticed a similar process of reification of a tool of inquiry into a paradigm of thought in the field of psychology -- a process which he defines as 'tool-to-theory heuristics'. 
1. As he noted, in the psychology of the mid-twentieth century, the 'statistical tools' of psychometrics eventually 'turned into theories of mind' in psychology. 

### 56 JH break

1. Together with Daniel Goldstein, Gigerenzer has described how the adoption of statistical tools gradually also popularised the computational metaphor of the mind, adding to its plausibility. 
1. According to them, it was specifically the influence of statistical tools such as the Neyman--Pearson theory of hypothesis testing and Roland Fisher's analysis of variance (ANOVA) that helped to consolidate the metaphor of the mind as a computer in the second half of the twentieth century. 
1. The transformation of a tool of inquiry into a model of the mind is exemplified also by the case of the perceptron, in which a statistical technique implicitly became a brain model (and, ultimately, a model of collective knowledge). 
1. The invention of statistical neural networks implied, in their construction, the 'mind as an intuitive statistician' and, conversely, also made statistics the model of the new artificial mind. 
1. Statistical tools have become since then not only a model of 'intelligence' in psychology but also a model of 'artificial intelligence' in the development of labour automation. 
1. Eventually, a whole statistical view of the world and society underwent a process of automation, so to speak, as it became increasingly normalised and naturalised through AI.

### 60. Hacking the vector space

1. In their 1969 book *Perceptrons*, Marvin Minsky and Seymour Papert demonstrated in mathematical terms that Rosenblatt's simple perceptron was unable to recognise certain patterns, questioning in this way its capacity for generalisation to other tasks of human intelligence. 
1. Specifically, the book argued that certain images, once projected onto the multidimensional space, could not be linearly separated by the simple perceptron: in particular, the perceptron could not discriminate connected from disconnected figures. 
1. The theorem was illustrated with odd-shaped images that could lead the perceptron to misfire a wrong classification, and the cover of the book featured two intricate spirals that could also deceive the human eye (while they looked identical at first sight, one was continuous and the other composed of two distinguished spirals). 
1. In logical terms, the theorem explained that a perceptron reduced to only two input neurons could 'learn' the AND, OR, and NOT logic functions but not the more complex XOR (exclusive-OR). 
1. For the first time, the vector space of an artificial neural network was 'hacked' and its vulnerability exposed. 
1. Minsky and Papert's conclusions were true only for the simplest class of perceptrons (which featured only one layer of neurons), but they were received as valid for all configurations of artificial neural networks and had a devastating effect on the whole research field. 

### 61 JH break

1. This initiated the first 'winter of AI' -- which was in fact the imposition of the 'MIT winter' on other research communities. 
1. Minsky and Papert's attitude was somewhat baronial and recalcitrant: they manifestly sought to divert military funding back to MIT -- not exactly a needy institution -- and to demonstrate that artificial neural networks did not constitute true 'artificial intelligence', as other techniques would reveal the virtuous path towards this goal. 
1. It should be remembered that already in his 1961 monograph *Neurodynamics*, Rosenblatt proposed different configurations of 'multi-layer perceptrons' that could overcome these limitations, but a convergence theorem could not be proven, and an efficient training algorithm (such as gradient descent) was not yet known. 
1. As the computer scientist Richard Forsyth has noted, however, only two years after the publication of *Perceptron*, in 1971, it was proven that 'a simple Mark I Perceptron, modified to incorporate an expansion recorder, could be taught to solve the exclusive-OR problem' but 'it had no effect on the widespread belief among computer scientists that neurocomputing was something that had been tried and had failed'.
1. Among other aspects, Minsky and Papert noticed (as also had Rosenblatt) that artificial neural networks are not able to distinguish well between figure and ground: in their computation of the visual field, each point gains somehow the same priority -- which is not the case with human vision. 
1. This happens because artificial neural networks have no 'concept' of figure and ground, which they replace with a statistical distribution of correlations (while the figure--ground relation implies a model of causation). 
1. The problem has not disappeared with deep learning: it has been discovered that large convolutional neural networks such as AlexNet, GoogleNet, and ResNet-50 are still biased towards texture in relation to shape. 

### 62. ANNs may continue to have a bias towards distinguishing textures vs. shapes

1. It may happen that they discriminate between the images of an elephant and a cat, for instance, not according to their shape but according to the texture of their skin and fur, respectively. 
1. The texture-over-shape bias occurs because even convolutional neural networks (which are specifically designed to extract edges, features, and details) still compute a statistical distribution of the whole data and not only of its 'meaningful' parts (as the human mind does, according to the Gestalt school). 
1. This was all the more true in the case of Rosenblatt's simple perceptron back then, but this problem of resolution in the rendering of common knowledge extends probably also to large foundation models such as the contemporary GPT. 
1. One can argue that Minsky and Papert conceived the first adversarial method for hacking an 'intelligent machine' and designed the corresponding 'adversarial patches', as they are called today -- the doctored pictures that can fool deep neural networks for image recognition. 
1. As a hack, it was quite successful in that it managed to derail military funding and neural networks research until the late 1980s. 

### 63 JH Break

1. Beyond the issues at stake in the controversy, Minsky and Papert nonetheless contributed to a critique of the knowledge paradigm that artificial neural networks embody and to the divulgation of the limitations of multidimensional modelling.
1. However, there is a tendency in the AI community, including in critical AI studies, to take sides in the 'perceptrons' controversy, mobilising viewpoints and philosophical traditions that would, alternatively, justify either symbolic or connectionist AI as the more rational or progressive paradigm, or as the more capable of causal thinking. 
1. Other readings conflate both schools under the same instrumentalist agenda of the military and its power genealogy. 
1. This book has proposed a different approach, namely to study and evaluate these AI lineages from the (externalist) perspective of labour automation, rather than as an (internalist) problem of computational logic, task performance, and human likeness. 
1. Neither deductive algorithms nor statistical techniques excel in mimicking human intelligence, because there is no inner logic to discover in human intelligence. 
1. Human cognition and machine tasks can be studied and compared because intelligence, whether 'natural' or 'artificial', is extroverted, contextual, and situated by constitution. 
1. Machines can be perceived as 'thinking' because they mimic the theatre of the human.  
1. The adoption of statistical tools by machine learning is a counterproof, in all its controversial legacy, that the master algorithm of 'artificial general intelligence', understood as the dream of technological singularity and *alpha machine* by a large community of engineers and computer scientists, is precisely a statistical illusion projected by data. 
1. In other words, the master algorithm does not exist as algorithm, but only as an originary extended social form.

### 70. The social calculus of knowledge

1. In the 1980s, in his book *The Vision Machine*, it was the French theorist Paul Virilio who would rediscover the then little-known case of the perceptron as part of the industrial and military spectrum of projects for the 'automation of perception'. 
1. Yet these military origins should not distract from seeing the perceptron in the larger genealogy of labour automation, social control, and knowledge extractivism. 
1. Alongside the known automation of manual and mental labour, the perceptron pioneered the automation of a different kind of labour: the *labour of perception*, or *supervision*. 
1. This is the task of surveilling machines (*Maschinenarbeit* in Marx) but also workspaces and assembly lines with a clear disciplinary function when it takes place under the eye of the authority, such as masters, guards, and policemen. 
1. As the media scholar Jonathan Beller has summarised, 'to look is to labour' and has been so for a long time; but 'to look is to organise labour' as well, and the eye of the master has been doing so all along. 
1. Optical media such as cinema and photography have often been involved in the automation of the gaze and the surveillance of labour in the past, and experiments of pattern recognition such as the perceptron have simply articulated these previous regimes of machine vision to a further stage.  
1. As seen in chapter 2, the industrial age pursued the mechanisation of manual labour with tooling machines and steam engines, and, with Babbage, the mechanisation of mental labour under the form of hand calculation and symbol manipulation (which are still quite 'manual' activities, as the names indicate). 

### 71 JH break

1. In the mid-twentieth century, mainframe computers extended the automation of mental labour as calculation and symbol manipulation in state administration, large companies, and scientific research. 
1. Compared to this history, the labour of supervision was mechanised in a different way. 
1. A novel aspect of the perceptron (and of pattern recognition algorithms in general) lies in the fact that a machine, for the first time, sought to automate so high a speculative faculty as the act of recognising -- that is interpreting -- an image, as opposed to the manipulation of symbols of given meaning. 
1. Rosenblatt defined the perceptron as a machine for the 'interpretation of the environment', arguing that the 'conceptualization of the environment is the first step towards creative thinking', and under this respect, in fact, the perceptron can be defined also as an *interpretation machine*.  
1. In today's technical jargon of machine learning, the perceptron is a *classifier* -- that is, an algorithm for statistically discriminating among images and assigning them a class or category (also known as a 'label') in a given cultural taxonomy. 
1. This, perhaps the most important aspect of the classifiers, has nothing to do with their *internal logic* but with the association of their output to an *external convention* that establishes the meaning of an image or other symbol in a given culture. 
1. Gestalt theory, cybernetics, and symbolic AI each intended to identify the *internal laws* of perception, but the key feature of a classifier such as the perceptron is to record *external rules* -- that is, social conventions. 

### 72 JH Break

1. Ultimately, an artificial neural network is an *extroverted machine*, a machine projected towards the outside, because the interpretation of an image, for example, is always affected more by experience and external social factors than by internal physiological circuits.  
1. A classification algorithm such as the perceptron does not automate reasoning understood as a capacity of *symbolic manipulation*, but rather as *situated knowledge* which is part of the cultural heritage of a given context. 
1. The act of image recognition or pattern classification is a specific kind of mental labour: it is a profoundly social act that mobilises, at the same time, tacit and explicit know-how, scientific and traditional taxonomies, and vernacular and technical grammars -- in short, knowledgemaking as a historical and often conflicting process. 
1. Although the industrial task of machine supervision can be highly codified, pattern recognition 'in the wild' remains a gesture of open interpretation rather than a strict rule-based procedure. 
1. For these reasons, a machine which is designed to automate such an epistemic mess (see the project of selfdriving cars) encounters, then as now, great difficulties. 
1. Moreover, the recent debates on gender, class, and racial bias in machine learning systems for face recognition reminds us what semioticians, philosophers of language, and art historians have always known: that image interpretation is an act that bears unresolvable political implications. 
1. In this regard, critical AI scholars Michael Castelle and Tyler Reigeluth have proposed to compare machine learning to the theory of learning as a social process by the Soviet psychologist Lev Vygotsky.58 The semiotic structure of the classifier, which is basically an *imitation machine*, confirms what Vygotsky argued: that there is no inner logic to discover in intelligence, because intelligence is a social process by constitution.
1. In conclusion, Rosenblatt's initial experiment to automate pattern recognition with a small matrix of 400 dimensions resulted, after the design of convolutional neural networks in the 1980s and the rise of deep learning in the 2010s, in the algorithmic modelling of vast inventories of spontaneous knowledge, mass communication, and cultural heritage. 

### 73 JH Break

1. The perceptron was an experiment of visual pattern recognition that thereafter was extended to the analysis of non-visual data, into a novel 'pattern recognition' across datasets of cultural, social, and scientific kind. 
1. In the age of deep learning, the architecture of the multilayered perceptron ended up being not a model of the biological brain but of the collective mind, eventually expressing its original ontology shaped by psychometrics. 
1. In fact, probably the most crucial moment in the history of AI is when, with Rosenblatt's perceptron, artificial neural networks inherited the techniques of multidimensional analysis from psychometrics and statistics. 
1. This made possible not only pattern recognition but also the computation of data of much-higher dimensions -- a feature that would come to be key, half a century later, in the age of 'big data'. 
1. As is well known, the unfortunate term 'big data' does refer to data that are not only vast in size but diverse in terms of typology -- rendered in statistics as 'dimensions'. 
1. Nowadays, companies such as Google, Amazon, Facebook, and Twitter, for example, collect data that define an extensive manifold of dimensions about their users, such as location, age, gender, nationality, language, education, job, number of contacts, along with political orientation, cultural interests, and so on. 

### 74 JH Break

1. The variety of social dimensions that these platform companies can analyse is vertiginous, exceeding the imagination of any well-trained statistician. 
1. The rise of machine learning algorithms is, then, also the response to the *dimensionality explosion* of social data rather than simply to an issue of information overload.  
1. Eventually, in the past decade, machine learning has grown into an extensive *algorithmic modelling of collective knowledge*, a 'social calculus' that aims to encode individual behaviours, community life, and cultural heritage under the form of vast architectures of statistical correlations. 
1. This has helped establish a monopolistic regime of knowledge extractivism on a global scale and new techniques for the automation of labour and management. As with only a few other artefacts of our epoch, AI has come to exemplify a unique concentration of power as knowledge.

***















