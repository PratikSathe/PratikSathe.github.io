---
layout: post_math
title:  "Measurements in Q#"
date:   2020-12-18 10:38:35 -0800
categories: jekyll qsharp
permalink: "/qsharp/single-qubit-measurement-tutorial"
---

> This blog post is written as part of the [Q# Advent Calendar – December 2020](https://devblogs.microsoft.com/qsharp/q-advent-calendar-2020/).

Quantum computing has gained a lot of attention, especially recently. This attention is well-deserved. For many problems, quantum computers promise solutions which are far more efficient than what classical computers are even capable of. A (prime :grinning:) example is prime factorization, which can be solved by the famous quantum algorithm called [Shor's algorithm](https://en.wikipedia.org/wiki/Shor%27s_algorithm) exponentially faster than any known classical algorithm. They are also well suited for simulating quantum systems, and has immense potential to solve problems in physics and chemistry. Quantum computers can also be used to solve optimization problems (using, e.g. quantum annealing), and speed up machine learning algorithms (quantum machine learning).

Most experiments for studying quantum phenomena are rather sophisticated. Traditionally, such experiments are made available only to students of physics, chemistry or electrical engineering, during their senior undergraduate years at the earliest. It is remarkable that this is no longer the case! It is now possible for almost anyone to write some code in a quantum programming language (such as [Microsoft's Q#](https://docs.microsoft.com/en-us/quantum/overview/what-is-qsharp-and-qdk)), and to run it on an real quantum computer offered by various companies or to simulate it on their own computer. Additionally, a number of high-quality free resources are being made available for free, to teaching quantum computing and quantum programming. 

The [quantum katas](https://github.com/Microsoft/QuantumKatas) are such a resource, consisting of a set of tutorials and programming exercises. The katas start with tutorials covering the basic concepts of quantum computing, such as the math needed (complex numbers and linear algebra), the concepte of qubits, and quantum gates. Each tutorial can be run using Jupyter notebooks, and includes demonstrations as well as small coding exercises in Q#, and are perfect for someone to learn quantum computing hands on. The katas also contain programming exercises to help cement these concepts, and to make on prificient in writing code in Q#.
{: .text-justify}

One of the important concepts in quantum computing is measurements. Measurements in quantum physics are markedly different that measurements in classical physics. Importantly, quantum measurements are probabilistic, and can result in different outcomes each time. In classical computing, ultimately, the final outcome of any computation is the state of the logical bits at the end of the logic circuit. In contrast, the final state (or wavefunction) of the qubits at the end of a quantum circuit is not useful _unless_ a measurement is done on the qubits. In other words, measurements are necessary in order to access the information held by the qubits, and consequently, quantum circuits typically end with a measurement operation. (There isn't a single 'truth table' when it comes to quantum logic circuits). Naturally, measurements are an important part of quantum circuits.

To demestify these concepts, we recently created [a tutorial on measurements in single qubit systems](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitSystemMeasurements). The tutorial starts with a discussion of the outcome probabilities for a measurement, and provides a demonstration of the use of the `M` operation in Q# for measuring in the computational basis. Although measurements are usually done in the computational basis (i.e., the $\|0\rangle$ and $\|1\rangle$ basis), one can also implement measuremnts in other bases, such as the $\|\pm\rangle$ basis, which can be implemented using the `Measure`. Measurements in non-computational bases can be useful in cases to distinguish between different states of a qubit. Specifically, if an input qubit is specified to be in either of two given states, a measurement in an appropriate basis can be used for identifying the correct state of the qubit. We end the tutorial by discussing measurements in arbitrary bases, which can be understood by using the projection formalism for measurements.

I am glad to have participated in the Microsoft mini-mentorship program, during which I got to work on creating this tutorial, which is my first contribution on Github! I learned a lot during this process. I learned how to code in Q#, and how to create unit tests. I also learned about the power of Github, and have already started using it for my personal projects. I am thankful to Mariia Mykhailova for guiding me through this process. 

 We hope that you enjoy learning from this tutorial. Over the next few weeks, we plan to create a follow-up tutorial soon, introducing measurements on multi-qubit systems.
 {: .text-justify}

<!-- ---------------
add /** Page content */
.page-content { padding: 30px 0; flex: 1; text-align: justify;} /*added text-align: justify;*/
--------------
 -->

<!-- 
Let me start by creating a list of things I want to include in the tutorial:
- General intro
- Measurements in quantum mechanics
- Measurements in quantum computing
- What I learned during this process:
	- Github
	- Q# 
	- unit testing
 -->

<!-- Jekyll also offers powerful support for code snippets:
 -->
<!-- {% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %} -->

<!-- Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
 -->