# Text Generation: Science Fiction Synopsis

## Artificial Intelligence Course at Allegheny College

**Instructor:** Janyl Jumadinova

## Table of Contents

- [Summary](#summary)
- [Objectives](#objectives)
- [Code of Conduct](#code-of-conduct)
- [Learning](#learning)
- [Assignment Specification](#assignment-specification)

  - [Data Gathering](#data-gathering)
  - [Text Generation using Tensorflow](#text-generation-using-tensorflow)
  - [Text Analysis](#text-analysis)
  - [Supplemental Production](#supplemental-production)

- [Planning](#planning)

- [Project Progress](#project-progress)

- [Project Walkthrough](#project-walkthrough)

- [Project Demonstration](#project-demonstration)

- [Required Deliverables](#required-deliverables)

- [Assignment Assessment](#assignment-assessment)

- [System Commands](#system-commands)

  - [Using Docker](#using-docker)
  - [Using Gradle](#using-gradle)
  - [Automated Checks with GatorGrader](#automated-checks-with-gatorgrader)

- [Receiving Assistance](receiving-assistance)

## Summary

Designed for use with [GitHub Classroom](https://classroom.github.com/), this repository contains the starter files for Laboratory 3 assignment in Computer Science 310.

This laboratory assignment invites you to work individually to implement a learning agent for a text generation application. You are also responsible for writing a detailed report, stored in the file `writing/report.md`. This is a Markdown file that must adhere to the standards described in the [Markdown Syntax Guide](https://guides.github.com/features/mastering-markdown/).

## Objectives

To learn how to use a `tensorflow` software library and a neural network algorithm for the natural language processing tasks. To gain understanding of natural language processing techniques that can be used for text generation and text analysis. To evaluate the performance of the machine learning algorithm used for the natural language processing tasks. To reflect on the design and development of the algorithm and to highlight ethical issues raised in the generated text.

## Code of Conduct

Throughout the completion of this project you must adhere to the community guidelines that we developed as a class. In addition to reporting any violations of the code of conduct, please make sure that you attest to the fact that you followed the code of conduct. Students who think that the class should revise some aspect of the guidelines must use the GitHub issue tracker for that repository to suggest, discuss, and implement any required changes.

## Learning

To review material on neural networks please read section 4.1.from the [Dive into Deep Learning](https://d2l.ai/chapter_multilayer-perceptrons/mlp.html) book and section 7.5 from the [Artificial Intelligence: Foundations of Computational Agents](https://artint.info/2e/html/ArtInt2e.Ch1.html) textbook. To learn about `tensorflow` and its use you may follow [tensorflow tutorials](https://www.tensorflow.org/tutorials). To see how to use Google's colab environment to run Tensorflow applications, please refer to [its documentation](https://colab.research.google.com/notebooks/intro.ipynb).

If you have not done so already, please read all of the relevant [GitHub Guides](https://guides.github.com/) that explain how to use many of the features that GitHub provides. In particular, please make sure that you have read the following GitHub guides: [Mastering Markdown](https://guides.github.com/features/mastering-markdown/), [Hello World](https://guides.github.com/activities/hello-world/), and [Documenting Your Projects on GitHub](https://guides.github.com/features/wikis/).

## Assignment Specification

One of the grand challenges in AI is developing a system that can comprehend and manipulate language as well as humans do. Automated text generation uses computational linguistics and artificial intelligence to automatically generate natural language texts that satisfy certain communicative requirements. Deep learning algorithms have recently achieved a great success on natural language processing tasks such as machine translation, dialogue response generation, summarization, and other text generation tasks.

In this multi-week lab project, each individual will use neural network based algorithm with `tensorflow` to create an agent that is able to generate text. The specific text to be generated is a synopsis for a science fiction show as today's technology tends to be yesterday's science fiction. During this lab, you are invited to create an agent that is able to generate a synopsis for a science fiction show or movie that may help us think through different possibilities of (future) technology use. Then, you will analyze your generated text both autonomously and manually and assess its ability to spark discussions on ethical issues surrounding technology.

### Data Gathering

To generate relevant science fiction text you first need relevant data. There are many TV shows or movies that might provide text that wold be useful for your task. "Black Mirror" show on Netflix and movie "Her" are good examples as they contain storylines involving the technology that seems feasible (or at least represents a foreseeable straight line from our current capabilities) and takes it a step further. This allows the viewers to ask important questions about possibilities of such technologies. What kinds of regulations would exist in a world that had this technology? What would the terms of service for this technology look like? What social norms would form? What kinds of ethical decisions would individual actors have to make?

**Your first task is to gather useful textual data.** For example, you can get the subtitle (.str) files from [tv-subs website](https://www.tv-subs.net/), where each file contains the transcript of an episode, or you can search for synopsis data on [kaggle](https://www.kaggle.com). You may need to do some pre-processing to get a dialog of each episode without extraneous text. An example of getting a single string which contains the whole dialog of the Black Mirror episode as a paragraph can be found at [this repository](https://github.com/pcalderon0711/black-mirror-sentiment-analysis/blob/master/blackmirrorsentiment.ipynb). While the goal of this example tool is to conduct sentiment analysis of Black Mirror episodes, the return dialog method provides Python code for extracting dialog from subtitle files.

### Text Generation using Tensorflow

**Once you have the relevant data, you are to use `tensorflow` and a machine learning algorithm of your choice that is based on the idea of neural networks to automatically generate synopsis for a science fiction show.** While your generated text does not need to be structurally or grammatically correct, it should produce some phrases that can be used to extract meaning of what the episode of a show might be about. You should run experiments to evaluate and improve your implementation.

There are many examples and tutorials for generating text using `tensorflow`. There are also some existing projects that provide tools to automatically generate text. For example, [textgenrnn project](https://github.com/minimaxir/textgenrnn) uses recurrent neural network and allow you to train the model on new text relatively easily (see basic example code in the repository). A more recent approach is to use unsupervised learning, `tensorflow` and neural networks to create an AI-based text-generation model, called GPT, which is trained on huge amounts of text all around the internet. [gpt-2 simple](https://github.com/minimaxir/gpt-2-simple) is a Python package which provides many functionalities for model management and generation control, allowing you to easily fine tune GPT-2 on your text.

You will need to either install `tensorflow` locally or via Docker, please refer to the [official website](https://www.tensorflow.org/install) for instructions for both. Alternatively, you can run `tensorflow` applications directly in a browser using Google's Colaboratory platform. Since training and testing natural language models is computationally expensive, with big models running for hours or days on a regular CPU machine, use of GPU is encouraged. Google's Colaboratory platform allows you to execute programs using `tensorflow` on GPU for free. Go to [colab's website](https:// colab.research.google.com), click on "File", "New notebook". Now you can write the code and run it in the web browser. You can also download the program either as a notebook (.ipynb file) or as a Python program (.py file) by going to "File", "Download".

### Text Analysis

**After you have an automatically generated text, you will automatically analyze it.** Here, you are free to select any natural processing task, as long as it extracts some information about your generated text. For example, you can get information about POS or NER or perform a sentiment analysis on your generated text. Fell free to explore and use one of the natural language processing libraries, such as [nltk](https://www.nltk.org/) or [nlp](https://nlp.stanford.edu/) to easily accomplish these tasks. You need to then run experiments to evaluate this part of your implementation.

### Supplemental Production

Finally, to "sell" your script's synopsis, you are to produce a supplemental production, which could be a tangible product or a visual artifact. Please feel free to utilize the resources of the ALIC's fab lab for this task. For example, perhaps you find a 3D printer model on sites such as [thingiverse](https://www.thingiverse.com/) that speaks about your synopsis. You can 3D print it and demonstrate it during your presentation. Or, maybe you want to etch the words of your synopsis on wood or another material. You can use a laser cutter to easily accomplish this task. Or, you may use text to speech library to develop an agent that can speak the text of the synopsis. Or perhaps, you decide to create a digital art. Possibilities are limitless but keep it to something that is feasible to do in a short amount of time.

## Planning

Please read and reflect on the project requirements and explore the types of available data you can use. Based on the project requirements, create a rough timeline for when you expect each task to be completed. Before the class time on October 25th, submit your project timeline. Then, you should try to stick to your timeline or adjust it as you work on the project. Regular work on the lab is required and your grade will be reduced if there is a lack of regular commits or lack of commits during work lab days.

## Project Progress

By the class time on Friday, October 29th, you should write and commit one paragraph in the appropriate section of your report document describing all of the tasks you have accomplished. By that time, you should at least obtain your data, perform any needed data pre-processing to get it ready for the machine learning algorithm, and to investigate and select machine learning implementation.

## Project Walkthrough

During the lab session on Wednesday, November 3rd, each individual will participate in the project walk-through process. Project walkthrough is an informal process where the instructor leads the process of reviewing the progress of the project and the written code is reviewed for technical accuracy with the objective of ensuring that the project is moving in the right direction and identifying improvements to the quality of the project. The purpose of this walkthrough is to motivate continuous progression on the project, identification of any conceptual issues, and detection of any technical errors. When the walkthrough is finished, the author of the project is responsible for taking the necessary actions to correct the identified issues.

By this project walkthrough, each person should have implemented, if not all then most of the text generation task, have run some preliminary tests, and have started investigating text analysis component of the project. During the walkthrough, each author will lead the walkthrough process, which should last 5-10 minutes for each project and outline the following:

- Describe the chosen data and the chosen algorithm.
- Explain the written code.
- Discuss the evaluation of text generation.
- Identify the steps left to complete for this project.

## Project Demonstration

At the beginning of the lab session on Wednesday, November 10th, each team will be given an opportunity to demonstrate their project. When the lab session starts, teams will be given a few minutes to set up their demonstrations and get them running. Then, class members will participate in an interactive demonstration session, where everyone will be able to view each demonstration.

## Required Deliverables

- _Project Planning_: October 25th by 11:30am
- _Project Progress_: October 29th by 11:30am
- _Project Walkthrough_: November 3rd, 3pm - 4:50pm
- _Code and Report_: November 10th by 3pm
- _Project Demonstration_: November 10th, 3pm - 4:50pm

This assignment invites you to submit the following deliverables through your team repository.

1. Planning/timeline portion of the report due on October 25th by 11:30am.
2. Progress portion of the report due on October 29th by 11:30am.
3. Participation in project walkthrough during the lab on November 3rd.
4. A properly completed and commented source program(s). Please make sure your source code is located inside "src" directory in your lab03 repository.
5. A production artifact to supplement your automatically generated synopsis.
6. The completed report, stored in `/writing/report.md` and written in Markdown, that contains the planning and progress portions as described above, and provides answers in all remaining sections (follow the prompts inside the report document).
7. Participation in project walkthrough during the lab on November 3rd.
8. Participation in project demonstration during the lab on November 10th.

Lab session on October 27th will be used for lab work. Lab session on October 13th will be used for demonstrations.

## Assignment Assessment

The grade that a student receives on this assignment will have the following components.

- **GitHub Actions CI Build Status [up to 5%]:**: For lab03 repository associated with this assignment students will receive a checkmark grade if their last before-the-deadline build passes. This is only checking some baseline writing and commit requirements. An additional reduction will given if the commit log shows a cluster of commits at the end clearly used just to pass this requirement. An addition reduction will also be given if there is no commit during lab work times. All other requirements are evaluated manually.

- **Mastery of Verbal Explanation during Walkthrough and Demonstration [up to 10%]:**: Since the timely project development and the ability to communicate technical details of a project is crucial to building successful software applications, a portion of students' lab grade will be determined based on the quality of the project walkthrough and demonstration.

- **Mastery of Technical Writing [up to 15%]:**: Students will also receive a checkmark grade when the responses to the writing questions presented in the `report.md` reveal a proficiency of both writing skills and technical knowledge. To receive a checkmark grade, the submitted writing should have correct spelling, grammar, and punctuation in addition to following the rules of Markdown and providing conceptually and technically accurate answers.

- **Integration of Supplemental Production Artifact [up to 10%]:**: Since sparking interest in technological innovation is crucial to the success of the technology, a part of your grade will be based on the creativity of your supplemental production and its ability to enhance the attractiveness of your project.

- **Mastery of Technical Knowledge and Skills [up to 60%]**: Students will receive the largest portion of their assignment grade when their project implementation reveals that they have mastered all of the technical knowledge and skills developed during the completion of this project. As a part of this grade, the instructor will assess aspects of the project including, but not limited to, the completeness and the correctness of the program(s), the use of effective source code comments and Git commit messages, the effective experimental analysis.

All grades for this project will be reported through a student's gradebook GitHub repository.

## System Commands

### Using Docker

Once you have installed [Docker Desktop](https://www.docker.com/products/docker-desktop), you can use the following `docker run` command to start `gradle grade` as a containerized application, using the [DockaGator](https://github.com/GatorEducator/dockagator) Docker image available on [DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

The aforementioned command will use `"$(pwd)"` (i.e., the current directory) as the project directory and `"$HOME/.dockagator"` as the cached GatorGrader directory. Please note that both of these directories must exist, although only the project directory must contain something. Generally, the project directory should contain the source code and technical writing of this assignment, as provided to a student through GitHub. Additionally, the cache directory should not contain anything other than directories and programs created by DockaGator, thus ensuring that they are not otherwise overwritten during the completion of the assignment. To ensure that the previous command will work correctly, you should create the cache directory by running the command `mkdir $HOME/.dockagator`.

If you are running your program on a Windows Operating System, you should run the following command instead, replacing the word "user" with the username of your machine:

```bash
docker run --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator
```

Here are some additional commands that you may need to run when using Docker:

- `docker info`: display information about how Docker runs on your workstation
- `docker images`: show the Docker images installed on your workstation
- `docker container list`: list the active images running on your workstation
- `docker system prune`: remove many types of "dangling" components from your workstation
- `docker image prune`: remove all "dangling" docker images from your workstation
- `docker container prune`: remove all stopped docker containers from your workstation
- `docker rmi $(docker images -q) --force`: remove all docker images from your workstation

### Using Gradle

Since the above `docker run` command uses a Docker image that, by default, runs `gradle grade` and then exits the Docker container, you may want to instead run the following command so that you enter an "interactive terminal" that will allow you to repeatedly run commands within the Docker container.

In Linux and Mac OS:

```bash
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

In Windows OS (replace `user` with your machine's username):

```bash
docker run -it --rm --name dockagator -v "%cd%":/project -v "C:\Users\user/.dockagator":/root/.local/share gatoreducator/dockagator /bin/bash
```

Once you have typed this command, you can use the [GatorGrader tool](https://github.com/GatorEducator/gatorgrader) in the Docker container by typing the command `gradle grade` in your terminal.

## Automated Writing and Commit Checks with GatorGrader

In addition to meeting all of the main requirements outlined in the assignment sheet, your submission must pass the following checks mainly related to writing and the number of commits that [GatorGrader](https://github.com/GatorEducator/gatorgrader) automatically assesses. If [GatorGrader's](https://github.com/GatorEducator/gatorgrader) automated checks pass correctly, the tool will produce the output similar to the one below.

```
✔  The file analyzer.py exists in the src directory
✔  The file report.md exists in the writing directory
✔  The report.md in writing has at least 500 word(s) in total
✔  The report.md in writing has exactly 11 of the 'heading' tag
✔  The repository has at least 30 commit(s)
✔  The analyzer.py in src has exactly 0 of the 'TODO' fragment
✔  The report.md in writing has at least 2 of the 'code_block' tag
✔  The report.md in writing has at least 1 of the 'list' tag
✔  The report.md in writing has exactly 0 of the 'TODO' fragment
✔  The generator.py in src has exactly 0 of the 'Your Name' fragment
✔  The analyzer.py in src has exactly 0 of the 'Your Names' fragment
✔  The generator.py in src has exactly 0 of the 'TODO' fragment
✔  The report.md in writing has exactly 0 of the 'Add Your Name' fragment
✔  The file generator.py exists in the src directory
```

## Receiving Assistance

If you are having trouble completing any part of this project, then please talk with either the course instructor during the lab session. Alternatively, you may ask questions in the Slack workspace for this course. Finally, you can schedule a meeting during the course instructor's office hours.
