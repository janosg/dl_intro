# Logistics

The following page contains everything you need to know to take the class for credit. Please read it carefully before approaching us with questions.

## Communication

All communication related to the course should be via zulip.

If you have not signed up for the `bonn-econ-teaching` zulip workspace yet, use this [link](https://bonn-econ-teaching.zulipchat.com/join/wuyru5foek3s3vb6tdkjubwc/) to do so. You will then automatically be subscribed to the `dl-intro` stream.

If you are already signed up from a previous course, please subscribe to the `dl-intro` stream.

Questions that do not contain any private information or sensitive data should be asked in a public stream such that everyone benefits from the answer.

**We will announce relevant information about the lectures and course logistics on zulip. If you do not sign up or check your messages, you might miss something important!**

## Office hours

If you have a question or problem that is better discussed in person, we can do so
right after the lecture.


## Instructors

```{eval-rst}
+--------------------------------------------------------------------+-------------------------------------------------------------------+
+ .. figure:: _static/images/janos.jpg                               + .. figure:: _static/images/mariam.png                             +
+     :width: 200px                                                  +     :width: 200px                                                 +
+                                                                    +                                                                   +
+     `Instructor: Janoś Gabler <https://github.com/janosg>`_        +     `TA: Mariam Petrosyan <https://github.com/mpetrosian>`_       +
+--------------------------------------------------------------------+-------------------------------------------------------------------+
```

## Distribution of materials

All materials can be downloaded from the [course webpage](https://dl-intro.readthedocs.io).

## Grading

The grade is determined entirely by a final project. The final project consists of a practical application of deep learning methods (you can choose the topic) and  written answers to questions that we will distribute in due time.

In the written answers you can achieve up to 25 points. In the application you can achieve up to 75 points. The points are added and translate into grades as follows:

| Grade | Minimum number of points |
| ----- | ------------------------ |
| 1.0   | 98                       |
| 1.3   | 93                       |
| 1.7   | 87                       |
| 2.0   | 82                       |
| 2.3   | 77                       |
| 2.7   | 71                       |
| 3.0   | 66                       |
| 3.3   | 61                       |
| 3.7   | 55                       |
| 4.0   | 50                       |

### How do we grade the application

The grade will be a holistic assessment of your project. We look at the following criteria:

- Is there a `README.md` that tells me how the repository is structured and how I can run the project?
- Does the code run?
- Is the code readable and well documented?
- How challenging is the task?
- How complete and correct is the solution?

A final project will be about as much work as two or three of the exercise notebooks you will see in class.

### How do we grade the written answers

We are looking for precise answers to the questions within the specified word limits. Answers that are too long will not get full points. Answers that contain the correct answer but also wrong or redundant information will not achieve full points.

### How will the project be submitted

Final projects are submitted in a GitHub repository created by GitHub classroom. Follow this [invitation](https://classroom.github.com/a/R1vgPUT1) to create the repository which you can then clone to your computer.

If you do not know yet what git is and how it works, don't worry. You will learn this during the lecture.


### How should the code be structured

You can choose whether you want to work in jupyter notebooks, `.py` files or a mix thereof. You are also free to use a workflow system such as [pytask](https://github.com/pytask-dev/pytask) or [kedro](https://github.com/kedro-org/kedro). We think that in practice you should always use such a workflow system, but we do not have the time to teach them in this class.

The only **strict requirement** is that there is a simple way to run your entire project and produce all results you need, either by running **one** notebook (that potentially imports functions from many files) or by running **one** command (such as pytask) from the command line.

If there is no simple way of producing all results or it is not documented in the README, we will deduct points.

### Where to put the written answers

The written answers to the questions have to be in the `README.md` file of your repository.

### Which libraries can you use

You can use any python library you want. If you need packages that are not installed in the course environment, your project needs to contain an `environment.yml` file with all packages you use.

If you use libraries that are not part of the course environment and do not provide an environment file, we will deduct points.

### Examples of final project applications

(to be written)


## Deadlines

- Between **April 3** and **April 10** you must **register for the class** via basis. Otherwise, you cannot take the class for credit! It happens to multiple students every year and the examination office does not make exceptions. Please also look at the [official dates](https://www.vwlpamt.uni-bonn.de/pruefungsamt-en/pdf/summer-semester-2023/time-table-summer-semester-2023) from the examination office for details.
- The **topic of of your final project** needs to be submitted until **Tuesday, July 11** by writing it down at the top of the README.md file of your repository. This is to make sure that you have a topic and to make sure that you have created your repository and know how to push materials to it.
- The deadline for the **final project** is **Sunday, September 10, 23:00**. The projects we download via GitHub classroom will not contain any changes you push after the deadline.

## Calendar

| Lecture| Date       | Comment                                            |
|--------| -----------|----------------------------------------------------|
| 1      | 2023-04-03 |                                                    |
| -      | 2023-04-10 | EASTER MONDAY - NO LECTURE                         |
| 2      | 2023-04-17 |                                                    |
| 3      | 2023-04-24 |                                                    |
| -      | 2023-05-01 | LABOR DAY - NO LECTURE                             |
| 4      | 2023-05-08 |                                                    |
| 5      | 2023-05-15 |                                                    |
| 6      | 2023-05-22 | Guest lecture entrepreneurship                     |
| -      | 2023-05-29 | PENTECOST MONDAY - NO LECTURE                      |
| 7      | 2023-06-05 |                                                    |
| 8      | 2023-06-12 |                                                    |
| 9      | 2023-06-19 |                                                    |
| 10     | 2023-06-26 |                                                    |
| 11     | 2023-07-03 |                                                    |
| 12     | 2023-07-10 | Will most likely be rescheduled (Scipy Conference) |


## Tentative Lecture Plan (this will change!)


- **Lecture 1**: Overview, logistics and installation
- **Lecture 2**: Python, Jupyter, Git and Markdown basics
- **Lecture 3**: Intro to huggingface ecosystem and different NLP tasks
- **Lecture 4**: Classification with sklearn
- **Lecture 5**: Tokenization
- **Lecture 6**: Text classification via feature extraction
- **Lecture 7**: Text classification via fine-tuning
- **Lecture 8**: Feedforward neural networks from scratch
- **Lecture 9**: (Pre-)training neural networks
- **Lecture 10**: RNNs, attention and transformers
- **Lecture 11**: Model architectures and loss functions
- **Lecture 12**: Final Projects tips / Bonus lecture
