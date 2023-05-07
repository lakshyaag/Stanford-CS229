#lecture
# Definition
Machine learning is defined as a computer's ability to learn without being programmed explicitly. To explain further, a computer learns from experiences $E$ through a set of tasks $T$, measured using some performance metric $P$. As $P$ improves while doing $T$, the computer is said to increase $E$. 

Broadly, machine learning can further be broken down into three methods, depending on the tasks:
1. [[Supervised learning]]
2. Unsupervised learning
3. Reinforcement learning

# [[Supervised learning]]
- If the predicted variable $y$ is a continuous variable, then the task is called **regression**
- If the predicted variable $y$ is a discrete variable, then the task is called **classification**
- Computer vision tasks are typically supervised, with the end goal being either object identification (*hot dog vs. not hot dog?*) or segmentation (bounding boxes around identified objects)

## Example
An example of a machine learning task would be to predict house prices given information about the size of the house. This can be further augmented using another metric (say, overall lot size) and so on, thereby creating a model that accepts multiple inputs and produces a single output.

![[Pasted image 20230507140329.png]]![[Pasted image 20230507140441.png]]

# Unsupervised learning
In unsupervised learning, the computer is just given a bunch of data with a vaguely-specified goal, which is usually to find interesting structures in the data.

## Example
- Clustering
- Word embeddings
- Large language models (LLMs)
# Reinforcement learning
These type of tasks deal with making sequential decisions, where each individual input impacts the next output (and subsequent ones, should the model be configured so).
![[Pasted image 20230507141803.png]]

