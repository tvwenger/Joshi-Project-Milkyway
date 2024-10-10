# Constraining Galactic Structure with Simulation Based Inference

## Project Objectives

### 0. Logging research progress

   **Status: Ongoing**
   
   *Learning objective*: Recognize the importance of tracking research objectives, progress, and questions.

   *Criteria for success*: Keep organized, meticulous notes of your research.

   <details>
   The most important part of the research process is probably being able to effectively communicate about the project. This means being able to explain to a random stranger on the street what you're doing, why it's important, and what it means. This is only possible if YOU know what you're doing. To this end, I ask that you keep diligent notes about everything you do related to this project. These notes don't have to be in any specific format, although it would be useful if they were saved in some what that I could also access them (like a google doc). Keep a record of what you do (e.g., I read this paper, I wrote a program that does this, I got confused about this topic, etc.), keep a record of what you want to do next (e.g., I need to write a program that does this other thing, I need to read about this topic, etc.), and, most importantly, keep track of all of the questions that come up (what does this acronym mean, how does this physical thing relate to this other physical thing, etc.). These notes will be invaluable to you as you work on the project. I often get distracted by other tasks and come back to a project after a few days or weeks only to have forgotten what exactly I was doing and what I needed to do next. Without these notes, I would have been lost!
   </details>

### 1. Start writing the "paper"

   **Status: Ongoing**

   *Learning objective*: Develop effective written communication skills

   *Criteria for success*: Start a draft of the introduction/background section of a "paper"

   <details>
   I hope that this project will ultimately result in a publication, but no matter what it will benefit YOU to start writing a "paper" or "final report" for the project right now, before you do anything else. In particular, I want you to focus on the "introduction" section of a paper, where you outline the major research questions and goals of the project. This will immensely benefit you because it will be something that you can look back on when you're knee-deep in data analysis and programming and you've forgotten what the "big picture" of the research project is. Don't worry about the formatting, the specific content, or anything like that now. Just write a paragraph or two about the project, and go back and read/edit it once in a while as you develop a stronger grasp on our research objectives. And it's OK if you don't know what the research questions/goals are yet - that's something we can talk about, which will guide your writing!
   </details>

### 2. Background research

   **Status: Ongoing**

   *Learning objective*: Develop a basic physical understanding of the algorithms and data sets that we'll be working with.

   *Criteria for success*: Be able to describe "simulation based inference" and the components of our model at a basic level

   <details>
   The first step for any project is to understand what's been done before. In this case, other people have figured out everything we need to know about the physics and algorithms. Here are some resources to get you started, although I hope you will do your own internet-searches to fill in the gaps and answer some questions. Take note of any questions or confusing topics that you come across along the way, and we can talk about them together.

   * Wikipedia: https://en.wikipedia.org/wiki/Milky_Way
   * The WISE Catalog of Galactic HII Regions. This paper provides an overview of the dataset that we'll be using. https://ui.adsabs.harvard.edu/abs/2014ApJS..212....1A/abstract
   * Simulation based inference: https://www.pnas.org/doi/10.1073/pnas.1912789117
   * Trigonometic Parallaxes of High-mass Star-forming Regions: in this paper, the authors are able to measure the distances and kinematics of some star forming regions in order to map out some of the structures that we're looking for. It's not directly related to this project, but it covers many of the topics that will be relevant to our work (Galactic rotation, spiral structure, etc.). https://ui.adsabs.harvard.edu/abs/2019ApJ...885..131R/abstract
   </details>

### 3. Preparing your research environment.

   **Status: COMPLETE**

   *Learning objective*: Introduce yourself to programming in a python environment

   *Criteria for success*: Introduce yourself to programming in a python environment

   <details>
   We're going to have to write some computer programs. The first step in this journey will be installing the necessary software on your computer and writing your first python program. There are many ways to set up a python environment, the specifics of which depend on what kind of computer you have, what operating system you use, etc. In general, Google/ChatGPT will probably be more helpful than I. Look up some tutorials, watch some youtube videos, and try to write a "hello world" program in python. Here are some suggestions:
   
   - If you have a Windows computer, I recommend installing a linux operating system (I like "Ubuntu") in a Virtual Machine. This will allow you to start developing linux-related skills, which is important because most professional research activities use a linux-based environment. This isn't a requirement yet, but will likely be necessary later on in this project.
   
   - For python, I like to use "miniconda", which is a "package manager" that makes installing python and a bunch of useful "packages" easy: https://docs.anaconda.com/free/miniconda/index.html
   
   - For writing code, I like to use VSCode, which is just a nice editor with some handy formatting features: https://code.visualstudio.com/
   </details>

### 4. More Research!

   **Status: Ongoing**

   *Learning objective*: Familiarize yourself with background research

   *Criteria for success*: Craft a "bibliography" file with summaries of background research and how it relates to your current project

   <details>
   Here are some additional papers that you might find useful. Use the ADS to find even more papers. I suggest following the references in these papers. Note that for background research, it is not essential to completely understand what the authors have done. Instead, focus on the introduction (broad background information), discussion (what are their results and how does it relate to the big picture question), and conclusions (summary). The details of their analysis might be important if we are trying to reproduce or replicate what they've done.
   
   - The Southern HII Region Discovery Survey: https://ui.adsabs.harvard.edu/abs/2021ApJS..254...36W/abstract
   
   - Kinematic Distances: A Monte Carlo method: https://ui.adsabs.harvard.edu/abs/2018ApJ...856...52W/abstract
   
   -- In particular, there are some equations that might be useful for you (eqs 3 - 5)
   </details>


### 5. Simulating HII region position-velocity diagrams

   **Status: Ongoing**

   *Learning objective*: Understand the relationship between Galactic structure and position-velocity data

   *Criteria for success*: Generate a "synthetic" Galactic longitude-velocity diagram for a population of simulated HII regions

   <details>
   There are three parts to this objective: (1) generate a 3D positions of a population of simulated HII regions. Use whatever distribution you like, or try different distributions (e.g., spherical, disk-like, logarithmic spiral arms). Make a 3D plot of these positions to verify that your program is working correctly! (2) Calculate the velocity vector for each HII region. Use whatever Galactic rotation model you like, or try different models (e.g., flat, the model from the Reid et al. (2019) paper, etc.). Make some plots to verify that your program is working correctly! (3) Derive the "observed" velocities of these nebulae, in the local standard of rest (LSR) frame. First project the 3D velocity vector onto the line-of-sight, then transform that radial velocity to the LSR frame. Generate a Galactic longitude-velocity diagram for these points to verify that your program is working!
   
   -> This is a lot of programming! Take it one step at a time. Think about your strategy first and write it down (like writing an outline of a paper). Break down the problem (e.g., I need to calculate Z from X) into small chunks (e.g., I need to calculate Y from X and then calculate Z from Y), make each of those chunks its own function or program (e.g., calc_Y and calc_Z), and think about how you can test that each of those functions or programs is working as intended!
   </details>


### 6. Preparing your research environment - Part 2

   **Status: New**

   *Learning objective*: Prepare software environment

   *Criteria for success*: Fork `galstruct` repository, submit a pull request

   <details>
   We're going to be writing some code for this project! In particular, we will be collaborating on a software package: https://github.com/tvwenger/galstruct

   Learn how to use Github to fork a repository, make changes on a branch, commit those changes, and submit them as a pull request to the repository.
   </details>

### 7. Understanding the `galstruct` model

   **Status: New**

   *Learning objective*: Understand the components of the `galstruct` model

   *Criteria for success*: Create a table describing each model parameter

   <details>
   It's time to dig in to `galstruct`! To get started, familiarize yourself with the `galstruct` model: https://github.com/tvwenger/galstruct/tree/master/galstruct/model

   Create a list of the model parameters, learn how the model parameters are related to the model. Describe the model parameters briefly in a table format -- we'll need to include this in the paper.
   </details>

### 8. Simulation Based Inference

    **Status: New**

    *Learning objective*: Learn how to use the python package `sbi`

    *Criteria for success*: Run the `galstruct` `learn_likelihood.py` program

    <details>
    We're going to use the python package `sbi` for this project. Here is a link to the documentation: https://sbi-dev.github.io/sbi/latest/

    Familiarize yourself with this software, and take notes about what parts you understand or do not understand so we can discuss them.

    Ultimately, you will need to update the `learn_likelihood.py` program to work with the latest version of `sbi`. See what you can do, and we'll work on it together!
    </details>

