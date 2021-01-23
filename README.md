# the working programmer's guide to working programs

"Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it" - Dijkstra

What if nand2tetris met deepspec? And took the browser to be the OS, built a language with a similar approach Rescript uses, built a quick ide with language server protocol support, used ideas like turnstile for tooling around building out language features, provided interactive theorem proving style programming features, and more. The idea is to to bootstrap a learning environment for Software Verification or Programming Language Foundations in Agda, with everything as simple as possible to demonstrate the concepts, and crucially be able to chain verification using a proof first approach.

Two major goals are

* demonstrate the joy in the proof based approach to programming
* demonstrate the impact integrated tooling can have on productivity

The target audience is working programmers so there is no teaching the basics of writing programs. All introduced concepts are fully explained by building programs. Nothing done here is for ideological purity all choices are made to maximize the simple presentation of hard concepts.

The big decision is how to do the hardware. I'm not sure if circuits are the right place to start. Looking at nand2tetris course materials everything is based on simulators. So it seems being a simulator creates the deployment. I need to read through nand2tetris to see if this is the case or if the code ever jumps outside the simulation and targets actual machine instructions (wouldn't do that, probably runs on JVM? Targeting JVM bytecode could be seen as the same idea).

The whole thing should be portable to any real or idealized computer so that is where to start from. The question then becomes what to port to to make building and explaining this thing easy? Probably not something I build then, why not just port to a nice simulator that does verification? Then build a oberon style os on top. then build xi+emacs+vim and turnstile.

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
* type theory and formal proof
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

* logic
  * Foundational analysis of computation
  * Propositional with feedback https://en.wikipedia.org/wiki/Propositional_formula#Propositional_formula_with_%22feedback%22
  * https://math.stackexchange.com/questions/348379/why-is-propositional-logic-not-turing-complete
  * http://nand2tetris-questions-and-answers-forum.32033.n3.nabble.com/Project-Oberon-the-next-step-of-the-N2T-Journey-td4029517.html
* abstract machine
 * Categorical Abstract Machine
   * https://en.wikipedia.org/wiki/Categorical_abstract_machine
   * Camel: An extension of the categorical abstract machine to compile functional/logic programs
   * categorical abstract machine with typechecking and proof search http://boxbase.org/entries/2020/apr/27/cam_mk2/
   * The Linear Logical Abstract Machine https://reader.elsevier.com/reader/sd/pii/S1571066106001617?token=BDE50171214736DE16958B98A86E2B09769FD690ABD3B1695B11165B2AA2F6D3E302B47AB864E4F5A61852EB5C390B65
* Autosubst https://www.ps.uni-saarland.de/Publications/documents/SchaeferEtAl_2015_Autosubst_-Reasoning.pdf
* Human readable machine verifiable proofs for teaching constructive logic https://kilthub.cmu.edu/articles/journal_contribution/Human-Readable_Machine-Verifiable_Proofs_for_Teaching_Constructive_Logic/6606203
* Advanced Topics in software verification https://www.cse.unsw.edu.au/~cs4161/
* Advanced operating systems http://www.cse.unsw.edu.au/~cs9242/current/
* microprocessor 
  * To Reinvent microprocessor https://medium.com/@veedrac/to-reinvent-the-processor-671139a4a034
  * lets build a microprocesor javascript https://tiarkrompf.github.io/notes/?/lets-build-a-microprocessor/ 
* parser
  * Parser https://tiarkrompf.github.io/notes/?/just-write-the-parser/ 
* Provers
  * Pedagogical first-order prover in Python https://github.com/eprover/PyRes
  * Compilers -> HOL https://crypto.stanford.edu/~blynn/compiler/
  * resolution automated proof system https://rmarcus.info/blog/2015/09/02/vulcan.html
  * Learning logic and proof with an Interactive Theorem Prover https://www.andrew.cmu.edu/user/avigad/Papers/learning_logic_and_proof.pdf
  * Towards a practical programming language based on dependent type theory
  * Parametric Higher-Order Abstract Syntax for Mechanized Semantics http://adam.chlipala.net/papers/PhoasICFP08/
  * Implementing Certified Programming Language Tools in Dependent Type Theory http://adam.chlipala.net/papers/ChlipalaPhD/
* lisp
  * Typed Lisp https://alhassy.github.io/TypedLisp.html
  * scheme to depednent type theory https://github.com/gbaz/mess
* lambda calculus
  * LC Turing Machine https://www.cs.cmu.edu/~rwh/talks/cs50talk.pdf
  * Efficient Self-Interpretation in Lambda Calculus
  * On the representation of data in lambda-calculus
  * Lambda -> Types https://crypto.stanford.edu/~blynn/lambda/
  * Mikrokosmos Programming on the λ-calculus https://mroman42.github.io/mikrokosmos/tutorial.html
* javascript
  * json and synthesis https://grgv.xyz/inductive_program_synthesis/
  * Dependent types https://tiarkrompf.github.io/notes/?/dependent-types/
* hardware
  * hardware dsl https://github.com/sifive/Kami
* assembly
  * Typed assembly language https://en.wikipedia.org/wiki/Typed_assembly_language
* verification
  * Verified compilation on a verified processor
  * Verified Sequential Malloc/Free https://www.cs.princeton.edu/~appel/papers/memmgr.pdf
  * VST-Floyd: A separation logic tool to verify correctness of C programs https://www.cs.princeton.edu/~appel/papers/VST-Floyd.pdf
  * A Completely Verified Realistic Bootstrap Compiler
  * A Verified Compiler for an Impure Functional Language http://adam.chlipala.net/papers/ImpurePOPL10/ImpurePOPL10.pdf
  * A Certified Type-Preserving Compiler from Lambda Calculus to Assembly Language
  * The Next 700 Compiler Correctness Theorems http://www.ccs.neu.edu/home/amal/papers/next700ccc.pdf
* rewrite systems
  * On Constructor Rewrite Systems and the Lambda-Calculus
* theorem provers
  * Learning logic and proof with an Interactive Theorem Prover https://www.andrew.cmu.edu/user/avigad/Papers/learning_logic_and_proof.pdf
  * Towards a practical programming language based on dependent type theory
  * Learning logic and proof with an Interactive Theorem Prover https://www.andrew.cmu.edu/user/avigad/Papers/learning_logic_and_proof.pdf
  * Towards a practical programming language based on dependent type theory
  * Parametric Higher-Order Abstract Syntax for Mechanized Semantics http://adam.chlipala.net/papers/PhoasICFP08/
  * Implementing Certified Programming Language Tools in Dependent Type Theory http://adam.chlipala.net/papers/ChlipalaPhD/
  
## Algorithms

* union find https://en.wikipedia.org/wiki/Disjoint-set_data_structure
* unification https://en.wikipedia.org/wiki/Unification_(computer_science)
* smt https://en.wikipedia.org/wiki/Satisfiability_modulo_theories
* skolemization https://en.wikipedia.org/wiki/Skolem_normal_form

## Protocols

## Networked Applications

* Irma https://news.ycombinator.com/item?id=25881954

# Content

## The battle ahead

Peice by peice we will actack the formal verification problem. 

* logic level
* hardware level
* microprocessor level
* machine level
* the assembly level
* the os level
* abstract machine
* the ide level

This is a strategy for verifying deepspec guided by impelementation decisions. language exploration can result from this and we want self hosted tooling to support that.

Proof carrying code and the demonstration of verification is covered. Being able to exhibit proof carrying code that is checked indepdently is a strong sign of soundness.

## Hardware for constructive logic

Instead of a Nand presentation in classical logic we should be able to use constructive logic with intuitionistic support, here we can talk about proof program correspance and type checking logic.

* The core of each ATP-system is the inference machine which amounts to sort of a “microprocessor” for theorem proving Semantics–Based Translation Methods for Modal Logics
  *  normal form transformation (NFT) which serves to translate arbitrary first order formulae into clause-form which is the preferred language of most inference machines
  *  “logic morphisms” They basically aim at encoding semantical meta-knowledge for non-classical logics within the language of classical
logic.
  * Popular examples are the various resolution-based strategies [Rob65] as well as the connection-based methods like the extension-procedure

## Abstract Machine

* The linear logic abstract machine https://reader.elsevier.com/reader/sd/pii/S1571066106001617?token=BDE50171214736DE16958B98A86E2B09769FD690ABD3B1695B11165B2AA2F6D3E302B47AB864E4F5A61852EB5C390B65

## Machine Language
