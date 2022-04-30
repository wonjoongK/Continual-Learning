
# Related Learning Paradigms

> _이 포스팅은 [DSAIL@KAIST](http://dsail.kaist.ac.kr/)의 능력자 중 한명인 [Yunhak Oh](https://yunhak0.github.io/)형의 도움을 받아 작성되었습니다_

<br/>

## Definition of Continual Learning(Lifelong Learning)
> ### Five key characteristics of LL:
* continuous learning process
* knowledge accumulation and maintenance in the KB
* the ability to use the acuumulated past knowledge to help future learning
* the ability to discover new tasks
* the ability to while working or to learn on the job

> ### Objective  
To optimize the performance of the new task, but it can optimize any task by treating the rest of tasks as the previous tasks

> ### Evaluation Methodology
* A large number of tasks
* Task sequence
* Progressive experiments

<br/>

## Transfer Learning(Domain Adaptation)
> ### Description
* Source domain: Normally has a large amount of labeled training data
* Target domain: Has little or no labeled training data
* Goal: To use the labeled data in the source domain to help learning in the target domain

> ### Difference from lifelong learning
* Transfer leraning is not concerned with continuous laerning or knowledge accumulation
* Not unidirectional
* Typically involves only two domains(source, target)
* Does not identify new tasks to be learned during model application

<br/>

## Multi-task Learning(MTL)
> ### Description
* MTL learns multiple related tasks simultaneously, aiming at **achieving a better performance by using the relevant information shared** by multiple tasks
* Prevents overfitting in the individual tasks, has a better generalization ability
* Online multi-task learning aims to learn the tasks sequentially and accumulate knowledge over time and leverage the knowledge

> ### Difference from lifelong learning
* Similarity is that they both aim to use some shared information 
* Optimizes **several tasks simultaneously**
* Does not accumulate any knowledge over time and not have the concept of countinuous learning

<br/>


## Online Learning
> ### Description
* Training data points arrive in a sequential order, a new data points arrives then the model quickly updated to produce the best model
* Goal: to optimize the performance on given learning task
* Typically memory and run-time efficient (not re-training using all the available data)

> ### Difference from lifelong learning
* Online learning still **performs the same learning task** over time
* Its objective is just to learn more efficiently with the data arriving incrementally

<br/>

## Reinforcement Learning
> ### Description
* Problem where an agent learns actions through trial and error interactions with a dynamic environment
* Goal: to learn an optimal policy that maps states to actions that maximizes the long run sum of rewards

> ### Difference from lifelong learning
* Learning is **limited to one task and one environment**
* No concept of accumulating knowledge to help future learning tasks

<br/>

## Meta Learning
> ### Description
* Aims to learn a new task with only small number of training examples using a model trained on many other similar tasks
* Goal: to transfer knowledge across tasks, the model learnmed from the meta learner enables the base learner to learn effectively with only a very small set of training examples
* Meta-learning basically treats learning tasks as learning examples

> ### Difference from lifelong learning
* Meta learning trins a meta-model from a large number of tasks to quickly adapt to a new task with only a few examples
* One key assumption made by most meta-learning techniques is that the trianing tasks and new tasks are from the same distribution, which is a major limits
* In the evaluation, previous tasks are often artificially created to have the same distribution as the new tasks

