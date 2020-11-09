# IS893: Advanced Software Security

## Logistics
- Instructor: [Kihong Heo](https://kihongheo.kaist.ac.kr) (허기홍, kihong.heo@kaist.ac.kr)
- TAs: Changhoon Song (송창훈, songch@kaist.ac.kr), Myojoon Kil (길묘준, myojoonkil@kaist.ac.kr)
- Time: Mon/Wed 09:00-10:15
- Office hour: by appointment
- Location: Zoom

## Course Description
This course covers advanced topics in software security. Students will be exposed to
techniques that are gaining increasing attention in the software security research
communities through research papers and programming assignments. Students will have
opportunities to develop their scientific communication skills through writing their
own project proposals and presenting their solutions.

## Grading
- Homework: 40%
- Paper Presentation: 30%
- Project: 30%

## Textbook
- Lecture slides will be provided
- Paul C. van Oorschot, [Computer Security and the Internet: Tools and Jewels](https://people.scs.carleton.ca/~paulv/toolsjewels.html), Springer, 2020
- Andreas Zeller et al., [The Fuzzing Book](https://www.fuzzingbook.org)
- Benjamin C. Pierce, [Types and Programming Languages](https://www.cis.upenn.edu/~bcpierce/tapl), MIT Press, 2002
- Aaron R. BradleyZohar Manna, [The Calculus of Computation](https://link.springer.com/book/10.1007/978-3-540-74113-8), Springer, 2007
- Xavier Rival and Kwangkeun Yi, [Introduction to Static Analysis: an Abstract Interpretation Perspective](https://mitpress.mit.edu/books/introduction-static-analysis), MIT Press, 2020

## Homework
This course includes programming assignments through which students will learn how to design and implement dynamic and static program analyzers.

- We will use Github/Github Classroom to provide skeleton code and manage submissions.
Make sure you have a Github account and get the [student developer pack benefits](https://education.github.com/pack).
Moreover, student should get familiar with `git`.
If you are new to `git`, see this [book](https://git-scm.com/book/en/v2).
All submissions will be managed using Github.
For each assignment, a unique invitation URL for Github Classroom will be posted in this page.
Once you accept the invitation, a private repository for your assignment will be created.
You can push as many commits as you want before the deadline. We will grade the final commit of your `master` branch.
The late homework policy is as follows:
  - 80% credit for one day late
  - 50% credit for two days late
  - NO credit given after two days late

- Students will use the [OCaml](https://ocaml.org) programming language for the assignments. For more details of OCaml, see the following meterials:
  - [Real World OCaml](https://dev.realworldocaml.org/index.html)
  - [Commercial Users of Functional Programming](http://cufp.org/2017)
  - [OCaml for the Masses](https://queue.acm.org/detail.cfm?id=2038036)
  - [Why OCaml](https://blog.janestreet.com/why-ocaml/)
  - [Why Functional Programming Matters](https://dl.acm.org/doi/10.1093/comjnl/32.2.98) [<img src="icons/youtube.png" width="16" />](https://youtu.be/1qBHf8DrWR8)
  - [Functional Programming in 40 minutes](https://youtu.be/0if71HOyVjY)
  - [Functional Programming in OCaml (Cornell CS3110)](https://www.cs.cornell.edu/courses/cs3110/2019sp/textbook/)

- Students will use the [LLVM](https://llvm.org) infrastructure and implement various tools that analyze programs written in LLVM IR code.
LLVM IR code can be generated from many source languages such as C/C++/Obj-C, Swift, Rust, Scala, Haskell, etc.
For more details of LLVM, see this [document](https://llvm.org/docs).

- Students will use the [Z3](https://github.com/Z3Prover/z3) theorem prover that automatically prove logical contraints (e.g., safety conditions)
generated by your analyzer from LLVM IR.

## Academic Integrity Violation
Students who violates academic integrity will get an F.

## Schedule (tentative)
|#|Topics|Reading|Presentation|Tools|Homework|
|-|------|-------|------------|-----|--------|
|-|[Presentation Schedule](https://docs.google.com/spreadsheets/d/1XWGdLnSZEkEaK1olUEcjb9SKhbfpW5-roQ6asPTfBhE/edit?usp=sharing)|||||
|-|[Project Guideline](slides/project.pdf)||||[<img src="icons/github-classroom.png" width="16" />Project](https://classroom.github.com/a/lBCHIeFq)|
|0|[Functional Programming in OCaml](slides/lecture0.pdf)|||
|1|[Introduction](slides/lecture1.pdf)||||[<img src="icons/github-classroom.png" width="16" />HW0: Hello-world](https://classroom.github.com/a/2pyTXU7M)|
|2|[**Part 1: Basic Concepts**](slides/lecture2.pdf)||||[<img src="icons/github-classroom.png" width="16" />HW1: OCaml Programming](https://classroom.github.com/a/O7rd_BBa)|
|3|Exploitation|[ASLR/CCS04](https://dl.acm.org/doi/10.1145/1030083.1030124)<br>[ROP/CCS07](https://dl.acm.org/doi/10.1145/1315245.1315313)<br>[COOP/S&P15](https://ieeexplore.ieee.org/document/7163058)<br>[KOOBE/USENIXSEC20](https://www.usenix.org/conference/usenixsecurity20/presentation/chen-weiteng)<br>|[ROP/정재황](slides/ROP.pdf)<br>[KOOBE/김현수](slides/KOOBE.pdf)<br>[ASLR/강우석](slides/ASLR.pdf)<br>[COOP/홍재민](slides/COOP.pdf)|[GSA](https://github.com/michaelbrownuc/GadgetSetAnalyzer)|
|4|Software Integrity|[CFI/CCS05](https://dl.acm.org/doi/10.1145/1102120.1102165)<br>[DFI/OSDI06](https://dl.acm.org/doi/10.5555/1298455.1298470)<br>[Conti/CCS15](https://dl.acm.org/doi/10.1145/1102120.1102165)<br>[CPI/OSDI14](https://www.usenix.org/conference/osdi14/technical-sessions/presentation/kuznetsov)<br> [CFB/USENIXSEC15](https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/carlini)<br>[TypeArmor/S&P16](https://ieeexplore.ieee.org/document/7546543)|[CFI/이대진](slides/CFI.pdf)<br>[TypeArmor/신명근](slides/typearmor.pdf)<br>[CPI/류혜원](slides/CPI.pdf)|[LLVM-CFI](https://clang.llvm.org/docs/ControlFlowIntegrity.html)||
|5|**Part 2: Dynamic Approaches**||||
|6|Runtime Monitoring|[ASan/USENIXATC12](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf)<br>[SoftBound/PLDI09](https://dl.acm.org/doi/abs/10.1145/1542476.1542504)|[ASan/이대진](slides/ASan.pdf)<br>[SoftBound/정재황](slides/SoftBound.pdf)|[LLVM-ASAN](https://clang.llvm.org/docs/AddressSanitizer.html)|[<img src="icons/github-classroom.png" width="16" />HW2: SmaLLVM Sanitizer](https://classroom.github.com/a/x9oGnjpJ)|
|7|[Fuzzing](slides/lecture3.pdf)|[DeepXplore/SOSP17](https://dl.acm.org/doi/10.1145/3132747.3132785)<br>[NEZHA/S&P17](https://ieeexplore.ieee.org/abstract/document/7958601)<br>[NAUTILUS/NDSS20](https://www.ndss-symposium.org/ndss-paper/nautilus-fishing-for-deep-bugs-with-grammars)|[NEZHA/홍재민](slides/NEZHA.pdf)<br>[NAUTILUS/강우석](slides/NAUTILUS.pdf)<br>[DeepXplore/류혜원](slides/DeepXplore.pdf)|[AFL](https://lcamtuf.coredump.cx/afl/)<br>[LLVM-LibFuzzer](https://llvm.org/docs/LibFuzzer.html)|[<img src="icons/github-classroom.png" width="16" />HW3: SmaLLVM Fuzzer](https://classroom.github.com/a/nHXGLmbx)||
|8|[Cause Reduction](slides/lecture4.pdf)|[C-Reduce/PLDI12](https://dl.acm.org/doi/10.1145/2345156.2254104)|[C-reduce/김현수](slides/Creduce.pdf)|[C-Reduce](https://embed.cs.utah.edu/creduce/)|[<img src="icons/github-classroom.png" width="16" />HW4: SmaLLVM Delta](https://classroom.github.com/a/EpKCdIFz)|
|9|[Fault Localization](slides/lecture5.pdf)|[CBI/PLDI05](https://dl.acm.org/doi/10.1145/1065010.1065014)<br>[CCC/PLDI11](https://dl.acm.org/doi/10.1145/1993316.1993550)||[CBI](https://research.cs.wisc.edu/cbi/)|
|10|[**Part 3: Static Approaches**](slides/lecture6.pdf)|[Astree/PLDI03](https://dl.acm.org/doi/abs/10.1145/781131.781153)|||
|11|[Data-flow Analysis](slides/lecture7.pdf)||||[<img src="icons/github-classroom.png" width="16" />HW5: SmaLLVM Dataflow](https://classroom.github.com/a/Vff2oy-c)|
|12|[Logic and Constraint Languages](slides/lecture8.pdf)||||||
|13|[Constraint-based Analysis](slides/lecture9.pdf)|[Securify/CCS18](https://dl.acm.org/doi/10.1145/3243734.3243780), [Ethainter/PLDI20](https://dl.acm.org/doi/abs/10.1145/3385412.3385990)|||[<img src="icons/github-classroom.png" width="16" />HW6: SmaLLVM Constraint-based analyzer](https://classroom.github.com/a/rw7SrKBp)||
|14|[Type Systems](slides/lecture10.pdf)|[CCured/TOPLAS05](https://dl.acm.org/doi/10.1145/1065887.1065892)<br>[TypeEq/CCS17](https://dl.acm.org/doi/abs/10.1145/3133956.3133998)||[CheckerFramework](https://checkerframework.org)|HW7: SmaLLVM Type Checker|
|15|Symbolic Execution|[Dart/PLDI05](https://dl.acm.org/doi/abs/10.1145/1065010.1065036)<br>[KLEE/OSDI08](https://dl.acm.org/doi/10.5555/1855741.1855756)||[KLEE](http://klee.github.io)||
|16|Project Presentation||
