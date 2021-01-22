# the working programmer's guide to working programs

"Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it" - Dijkstra

What if nand2tetris met deepspec? And took the browser to be the OS, built a language with a similar approach Rescript uses, built a quick ide with language server protocol support, used ideas like turnstile for tooling around building out language features, provided interactive theorem proving style programming features, and more. The idea is to to bootstrap a learning environment for Software Verification or Programming Language Foundations in Agda, with everything as simple as possible to demonstrate the concepts, and crucially be able to chain verification using a proof first approach.

Two major goals are

* demonstrate the joy in the proof based approach to programming
* demonstrate the impact integrated tooling can have on productivity

The target audience is working programmers so there is no teaching the basics of writing programs. All introduced concepts are fully explained by building programs.

The language built will be called Student. The idea is what is the simplist language that allows us to prove anything useful in the verification chain. From there we wish to add extensions to be able to prove more complicated things while integrating interactivity into a minimal in browser IDE running on our OS.

## Inspiration

* nand2tetris
* deepspec 
* sel4
* the little typer
* the little prover
* software abstractions
* tla+
* handbook of practical logic and automated reasoning
* fundamental proof methods in computer science
* rescript
* proofs = programs
* ml for the working programmer
* software foundations
* programming language fundamentals in agda
* concrete semantics
* decision procedures
* the calculus of computation
* turnstile
* twelf
* tutch
* carnap
* webassembly
* language server protocol
* haskell
* idris
* ml
* lisp
* vim
* emacs
* xi
* vimium

## Research

* Categorical Abstract Machine https://en.wikipedia.org/wiki/Categorical_abstract_machine
* Autosubst https://www.ps.uni-saarland.de/Publications/documents/SchaeferEtAl_2015_Autosubst_-Reasoning.pdf
* Human readable machine verifiable proofs for teaching constructive logic https://kilthub.cmu.edu/articles/journal_contribution/Human-Readable_Machine-Verifiable_Proofs_for_Teaching_Constructive_Logic/6606203
* Advanced Topics in software verification https://www.cse.unsw.edu.au/~cs4161/
* Advanced operating systems http://www.cse.unsw.edu.au/~cs9242/current/
* python
  * Pedagogical first-order prover in Python https://github.com/eprover/PyRes
* lisp
  * Typed Lisp https://alhassy.github.io/TypedLisp.html
  * scheme to depednent type theory https://github.com/gbaz/mess
* lambda calculus
  * Efficient Self-Interpretation in Lambda Calculus
  * Lambda -> Types https://crypto.stanford.edu/~blynn/lambda/
  * Compilers -> HOL https://crypto.stanford.edu/~blynn/compiler/
* javascript
  * json and synthesis https://grgv.xyz/inductive_program_synthesis/
  * Parser https://tiarkrompf.github.io/notes/?/just-write-the-parser/ 
  * Microprocessor https://tiarkrompf.github.io/notes/?/dependent-types/
  * Dependent types https://tiarkrompf.github.io/notes/?/lets-build-a-microprocessor/ 
  * resolution automated proof system https://rmarcus.info/blog/2015/09/02/vulcan.html
* assembly
  * Typed assembly language https://en.wikipedia.org/wiki/Typed_assembly_language
* verification
  * Verified compilation on a verified processor
  * Verified Sequential Malloc/Free https://www.cs.princeton.edu/~appel/papers/memmgr.pdf
  * VST-Floyd: A separation logic tool to verify correctness of C programs https://www.cs.princeton.edu/~appel/papers/VST-Floyd.pdf
  * A Completely Verified Realistic Bootstrap Compiler
## Algorithms

* union find https://en.wikipedia.org/wiki/Disjoint-set_data_structure
* unification https://en.wikipedia.org/wiki/Unification_(computer_science)
* smt https://en.wikipedia.org/wiki/Satisfiability_modulo_theories
* skolemization https://en.wikipedia.org/wiki/Skolem_normal_form
