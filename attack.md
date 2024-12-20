# Attack Resistance Defense Mechanism

**Q1: What is attack resistance?**
Attack resistance is a formal approach aimed at analyzing security defense mechanisms (e.g., ASLR, ISR,...) and cryptographic obfuscation methods with the goal of ascertaining whether they are secure. At a high level, attack-resistance is based on ideas from cryptography, such as computational or information-theoretic indistinguishability, as applied to system security and side-channel defense mechanisms, information-flow and program obfuscation methods.

More formally, attack-resistance is defined in terms of computational indistinguishability, wherein, we say that a defense mechanism D is deemed attack resistant iff the following is true: for any probabilistic polynomial time attacker (PPT) A and for a meaningful combination of D with any program P, the combination D+P is computationally indistinguishable from an ideal program IP. (In a variant of this notion of attack-resistance, we are also exploring the idea of SAT-based attackers wherein the attacker is weaker than a general PPT attacker, but strong enough to be relevant in practical settings.)

The key insight is that in our setting the protected program P and the ideal program IP may have the same exploitable bug (e.g., buffer overflow). However, the difference between P and IP is that a PPT attacker A has a way to exploit the bug in the vulnerable program P, but does not have a way of exploiting the same bug in the ideal program IP. The value of the defense mechanism D then is to protect P such that the attacker A's probability of successfully launching an attack on the combination P+D is vanishingly small, as a function of a security parameter (e.g., the number of bits of a random seed used by the defense mechanism D). I.e., for any PPT attacker A, P+D is computationally indistinguishable from the ideal program IP.

**Q2: What is the notion of attack-resistance useful for?**
The notion of attack resistance is useful for establishing security properties of defense mechanisms. Often security researcher present defense mechanisms without sufficient formal analysis. Insufficient formal analysis can lead to the deployment of insecure defense mechanisms. 

**Q3: What attacker model do we use in order to establish attack-resistance of defense or obfuscation methods?**
Depending on context, we use one of the two attacker models described below:

PPT attacker: Here the attacker is a probabilistic polynomial time (PPT) Turing machine, i.e., the attacker can execute any PPT algorithm as an attack to accomplish her objective.

SAT attacker: Here the notion is that the attacker is limited to attacks where in order to accomplish her objective she has to break problems that are considered hard for SAT solvers.

**Q4: Which defense mechanisms have been shown to be attack resistant?**
We applied our analysis to certain variants of address space layout randomization (ASLR) and instruction set randomization (ISR), and showed that these variants are attack resistant in the sense described above.

**Q5: What are the future goals of this project?**
We want to apply our approach to other defense mechanisms (e.g., DieHarder), side-channel defenses, as well as to cryptographic obfuscation methods.

# People


## Principal Investigators
- [Vijay Ganesh](https://vganesh1.github.io/){:target="_blank"}, Georgia Institute of Technology
- [Martin Ochoa](http://dblp.uni-trier.de/pers/hd/o/Ochoa:Mart=iacute=n){:target="_blank"}, Singapore University of Technology and Design
- [Sebastian Banescu](https://www.in.tum.de/i04/banescu/){:target="_blank"}, Quantstamp Inc


## Researchers
- [Gilles Barthe](https://software.imdea.org/people/gilles.barthe/){:target="_blank"}, IMDEA Software
- [Mayank Varia](http://www.mvaria.com/){:target="_blank"}, Boston University
- [Cynthia Disenfeld](https://dblp.org/pid/57/11135.html) , University of Toronto


# Publications and Slides

- **Martin Ochoa, Sebastian Banescu, Cynthia Disenfeld, Gilles Barthe, and Vijay Ganesh**  
Reasoning about Probabilistic Defense Mechanisms against Remote Attacks  
**The Second IEEE European Symposium on Security and Privacy (IEEE EuroS&P 2017), Paris, France, April 28, 2017.**  
[[pdf](https://arxiv.org/abs/1701.06743){:target="_blank"}][[bib](https://dblp.uni-trier.de/rec/journals/corr/OchoaBDBG17.html?view=bibtex){:target="_blank"}][[Slides](https://ece.uwaterloo.ca/~vganesh/Publications_files/TalkSlides-vg2017-EuroSP-AttackResistance2017.pdf){:target="_blank"}]  

- **Vijay Ganesh, Sebastian Banescu, and Martin Ochoa**  
The Meaning of Attack-Resistant Programs  
**International Workshop on Programming Languages and Security (PLAS at ECOOP 2015), Prague, Czech Republic, July 6, 2015.** 
*Presentation-only at International Workshop on Foundations of Computer Security (FCS at CSF 2015), Verona, Italy, July 13, 2015.*  
[[pdf](https://arxiv.org/pdf/1502.04023v2){:target="_blank"}][[bib](https://dblp.uni-trier.de/rec/journals/corr/GaneshBO15.html?view=bibtex){:target="_blank"}]  

- **Vijay Ganesh, Michael Carbin, and Martin Rinard**  
Cryptographic Path Hardening: Hiding Vulnerabilities in Software through Cryptography  
**Off-the-Beaten-Path Workshop @ POPL 2012, Philadelphia, PA, USA, January 22, 2012.**  
[[pdf](https://arxiv.org/abs/1202.0359?context=cs){:target="_blank"}][[bib](https://dblp.uni-trier.de/rec/journals/corr/abs-1202-0359.html?view=bibtex){:target="_blank"}]


