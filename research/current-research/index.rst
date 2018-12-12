.. title: Current Research
.. slug: current-research
.. date: 2018-01-18 10:07:37 UTC-05:00
.. tags: Neuroscience, Electrophysiology, Taste, Dynamical Systems, Python
.. category: Research
.. link: 
.. description: Current research page
.. type: text

Taste stimuli, in contrast to other sensory modalities (like vision or hearing), are unique in the degree of behavioral information they carry - an animal necessarily has to decide to consume or reject a taste in the mouth. In my PhD thesis research with Prof. Donald Katz, I study large-scale neural activity patterns in the primary taste cortex of awake, behaving rodents in the context of their consumption decisions. This work has involved the open-source technological development of both an affordable hardware system that can perform large-scale multi-electrode recordings in rodents and analysis software that can process the large streams of neural voltage data flowing in from the hardware. To learn more about these technological projects, please read our `Scipy 2017 paper </publications/mukherjeeetal2017_scipy.pdf>`_.  

Continue reading below for the main findings from my thesis research.

"Noisy" dynamics holds behavioral significance
==============================================

Studying sensory systems from a single neuron perspective is a common tradition in neuroscience. The stimulus is typically presented to the animal multiple times and the responses of individual neurons are averaged across these repeated presentations to get a sense of each neuron's "mean representation". Response variability, both across neurons and trials, is dismissed as "noise".

Using probabilistic graphical models (with Bayesian inference techniques) to go beyond individual neurons and model the dynamics of large neural populations in the taste cortex, we showed that the variability in their stimlus responses is anything but noise. In fact, we discovered a surprisingly strong correlation between the wildly variable emergence of consumption decision-related firing in taste cortex populations and the timing of the animals' actual consumption behaviors on individual trials. For a deep dive into these results, please read our `Journal of Neuroscience paper </publications/sadaccaetal2016_jneuro.pdf>`_.    

Sudden transitions, not gradual ramps, underlie consumption decisions
=====================================================================

Classical decision-making theory posits that animals arrive at optimal decisions through a process of "gradual accumulation of evidence". These results are primarily based on studies in primates and humans performing decision-making tasks that need a large amount of prior training. In the decision to consume or egest a taste in the mouth, that animals need almost no training to perform, we showed that sudden, coherent shifts in population activity patterns, despite being variably timed across trials, are strongly predictive of the timing of the decision. In fact, we went on to show that traditional trial-averaged analyses of the responses of individual neurons *artifactually impose* an appearance of gradual accumulation of evidence in these data. Read more in our `Journal of Neuroscience paper </publications/sadaccaetal2016_jneuro.pdf>`_.

Read this `Science paper`_ for similar conclusions about neural responses in a visual decision-making task and browse through this `Journal of Computational Neuroscience paper`_ for a mechanistic model of how stochastically switching neural circuits can produce better decisions than linear ramping circuits.   

The brain might not be divided into separable processing areas
==============================================================

Systems neuroscience, right from the pioneering studies of Hubel and Wiesel, has divided the brain into separable processing "areas" - sensory areas (like the primary visual cortex) that "encode" incoming stimuli are thought to be largely distinct from areas involved in decision-making (like frontal or temporal areas) and motor action (like motor cortex). This modular view of the brain has gained traction in recent years with the advent of deep artificial neural networks for computer vision - some of the most succesful deep nets, just like the brain, tend to encode stimulus features in superficial layers while more abstract, classification-related computations happen in deeper layers.

Taste stimuli, however, land on the tongue replete with both chemical (identity-related) and behavioral (palatability-related) information. Accordingly, sensory cortical responses to tastes reflect both stimulus identity and palatability (the decision-related variable that labels foods as being "yummy" or "yucky"). Fascinatingly, taste cortex neuronal populations separate out these encoding and processing related computations in separate temporal "epochs" - the transitions between these epochs of firing, despite being stochastic, correlate with the timing of consumption decisions. Thus, stimulus encoding and higher computations related to tastes are separated in the brain in time, but not in anatomy.

Using precisely-timed optogenetic perturbations, we went on to show that neurons in the taste cortex are functionally involved in generating the animal's consumption decisions, but only in a temporally-specific manner. We found that identical optogenetic perturbations produced drastically different effects on decision-making and behavior depending on the state of the brain just before the perturbation. You can read more about these results in our `bioRxiv preprint`_       

.. _Science paper: https://doi.org/10.1126/science.aaa4056

.. _Journal of Computational Neuroscience paper: https://doi.org/10.1007/s10827-013-0452-x

.. _bioRxiv preprint: https://www.biorxiv.org/content/early/2018/12/03/486043.full.pdf
    
