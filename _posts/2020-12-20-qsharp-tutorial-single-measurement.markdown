---
layout: posts
title:  "Measurements in Q#"
date:   2020-12-20 00:00:01 -0800
categories: 
  - Blog
tags:
  - qsharp
  - quantumComputing
permalink: "/qsharp/single-qubit-measurement-tutorial"
---

> This blog post is written as part of the [Q# Advent Calendar – December 2020](https://devblogs.microsoft.com/qsharp/q-advent-calendar-2020/).


![Single qubit quantum measurement]({{site.baseurl}}/assets/circuit_diagram/measurement_figure.png "Single qubit quantum measurement")
*A typical quantum circuit starts with the state $|0\rangle$, operates some quantum gates on it, and ends in a measurement resulting in 0 or 1.*
{: style="color:gray; font-size: 100%; text-align: center;"}

Quantum computing has recently generated a lot of excitement, and for good reason. For many problems, the paradigm of quantum computation offers solutions which are far more efficient than what classical computers are capable of. A (prime :grinning:) example is prime factorization, which can be solved by [Shor's algorithm](https://en.wikipedia.org/wiki/Shor%27s_algorithm) exponentially faster than any known classical algorithm. Quantum computers also have great potential in solving physics and chemistry problems by simulating quantum systems (which was Feynman's [original motivation for quantum computers](https://link.springer.com/article/10.1007/BF02650179)). They can also be used to solve optimization problems (using, e.g. quantum annealing), and speed up machine learning algorithms (quantum machine learning). 

Most experiments for studying quantum phenomena are rather sophisticated. Traditionally, such experiments are made available only to students of physics, chemistry or electrical engineering, during their senior undergraduate years at the earliest. It is remarkable that this is no longer the case! It is now possible for anyone to learn and write some code in a quantum programming language (such as [Microsoft's Q#](https://docs.microsoft.com/en-us/quantum/overview/what-is-qsharp-and-qdk)), and to run it on a real quantum computer offered by various companies or to simulate it on their own computer. Additionally, a number of high-quality resources teaching quantum computing and programming are being prepared and made available for free. 

The [Quantum Katas](https://github.com/Microsoft/QuantumKatas) are one such resource, consisting of a set of tutorials and programming exercises. The learning path starts with tutorials covering the basic concepts of the math needed (complex numbers and linear algebra), and quantum computing (the concepts of qubits and quantum gates). Each tutorial can be run using Jupyter notebooks, and includes demonstrations as well as coding exercises in Q#, and are perfect for someone to learn quantum computing hands on. The katas also contain programming exercises to help cement these concepts, and to make one proficient in writing code in Q#.

One of the important concepts in quantum computing is measurements. Measurements in quantum physics are markedly different that measurements in classical physics. Importantly, quantum measurements are probabilistic and can result in different outcomes each time. (In terms of the _final output_, there isn't a single 'truth table' when it comes to quantum logic circuits). In classical computing, ultimately, the final outcome of any computation is the state of the logical bits at the end of the logic circuit. In contrast, the final state (or wavefunction) of the qubits at the end of a quantum circuit is not useful _unless_ a measurement is done on the qubits. In other words, measurements are necessary in order to access the information held by the qubits, and consequently, quantum circuits typically end with one or more measurement operations. Naturally, measurements are an important part of quantum circuits.

To demystify these concepts, we recently created [a tutorial on measurements in single qubit systems](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitSystemMeasurements). The tutorial starts with a discussion of the outcome probabilities for a measurement, and provides a demonstration of the use of the `M` operation in Q# for measuring in the computational basis. Although measurements are usually done in the computational basis (i.e., the $\|0\rangle$ and $\|1\rangle$ basis), one can also implement measurements in other bases, such as the $\|\pm\rangle$ basis using the `Measure` operation in Q#. Measurements in arbitary bases are also possible, and can be useful to distinguish between different states of a qubit. For example, if an input qubit is specified to be in either of two given states, a measurement in an appropriate basis can be used for identifying the correct state of the qubit. We end the tutorial by discussing measurements in arbitrary bases, which can be understood by using the projection formalism for measurements.

I am glad to have participated in the Microsoft mini-mentorship program, during which I got to work on creating this tutorial, which is my first contribution on GitHub! I learned a lot during this process. I learned how to code in Q#, and how to create unit tests. I also learned about the power of GitHub, and have already started using it for my personal projects. I am thankful to Mariia Mykhailova for guiding me through this process. 

 I hope that you enjoy learning from this tutorial. Over the next few weeks, I plan to create a follow-up tutorial, introducing measurements on multi-qubit systems.

<!-- ---------------
add /** Page content */
.page-content { padding: 30px 0; flex: 1; text-align: justify;} /*added text-align: justify;*/
--------------
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