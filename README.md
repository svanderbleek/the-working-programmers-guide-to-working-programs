# the working programmer's guide to working programs

"Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it" - Dijkstra

What if nand2tetris met deepspec? Can we find the appropriate jumping in point to build a verification stack from the language to os level with a specific vocus on creating a verification focused ide.

Two major goals are

* demonstrate the joy in the proof based approach to programming
* demonstrate the impact integrated tooling can have on productivity

The target audience is working programmers so there is no teaching the basics of writing programs. All introduced concepts are fully explained by building programs. Nothing done here is for ideological purity all choices are made to maximize the simple presentation of hard concepts.

The language built will be called Student with Desk the ide and Room the os.

## Influences

* nand2tetris
* digital circuit design for computer science students: an introductory textbook
* proof in vdm
* deepspec
* rems
* sail
* sel4
* certikos
* ironclad
* cakeml
* koika
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
* program logics for certified compiliers
* certified programming with dependent types
* concrete semantics
* decision procedures
* the calculus of computation
* type theory and formal proof
* turnstile
* hol
* coq
* dedukti
* andromeda
* twelf
* tutch
* carnap
* webassembly
* binaryen
* browsix
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

This is exploratory, some of it will go no where. There is a pragmatic focus with working so we don't go beyond that for any reason, we work with what we are given and make the least ammount of inventions to develop the verification chain and a verification focused ide. Currently that looks like webassembly with binaryen and browsix as our entry point versus the simulators of nand2tetris.

* Compiler Verification
  * Compositional CompCert https://www.cs.princeton.edu/~appel/papers/compcomp.pdf
  * Verified compilation on a verified processor
  * Verified Sequential Malloc/Free https://www.cs.princeton.edu/~appel/papers/memmgr.pdf
  * VST-Floyd: A separation logic tool to verify correctness of C programs https://www.cs.princeton.edu/~appel/papers/VST-Floyd.pdf
  * A Completely Verified Realistic Bootstrap Compiler
  * A Verified Compiler for an Impure Functional Language http://adam.chlipala.net/papers/ImpurePOPL10/ImpurePOPL10.pdf
  * A Certified Type-Preserving Compiler from Lambda Calculus to Assembly Language
  * The Next 700 Compiler Correctness Theorems http://www.ccs.neu.edu/home/amal/papers/next700ccc.pdf
  * correctness of a compiler for arithmetic http://jmc.stanford.edu/articles/mcpain/mcpain.pdf
* Verification Check
  * https://en.wikipedia.org/wiki/Verification_condition_generator
* interaction trees https://github.com/DeepSpec/InteractionTrees
* instruction semantics
  * https://www.cl.cam.ac.uk/~pes20/sail/
* nand2fpga
  * https://gitlab.com/x653/nand2tetris-fpga/
* rems https://www.cl.cam.ac.uk/~pes20/rems/
* deepspec https://deepspec.org/main
* foundation
  * Foundational analysis of computation
  * Evolving Algebras an attempt to discover semantics http://www.mit.edu/afs.new/sipb/user/golem/papers/898/asm-tutorial.pdf
  * Evolving algebras https://web.eecs.umich.edu/~gurevich/Opera/103.pdf
* logic
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
* primitive recursion
  * The efficiency of primitive recursive functions: A programmer's view https://www.sciencedirect.com/science/article/pii/S0304397515003539
* lisp
  * Typed Lisp https://alhassy.github.io/TypedLisp.html
  * scheme to depednent type theory https://github.com/gbaz/mess
* lambda calculus
  * LC Turing Machine https://www.cs.cmu.edu/~rwh/talks/cs50talk.pdf
  * Efficient Self-Interpretation in Lambda Calculus
  * On the representation of data in lambda-calculus
  * Lambda -> Types https://crypto.stanford.edu/~blynn/lambda/
  * Mikrokosmos Programming on the λ-calculus https://mroman42.github.io/mikrokosmos/tutorial.html
  * the mechanical evaluation of expressions https://www.cs.cmu.edu/afs/cs/user/crary/www/819-f09/Landin64.pdf
* javascript
  * json and synthesis https://grgv.xyz/inductive_program_synthesis/
  * Dependent types https://tiarkrompf.github.io/notes/?/dependent-types/
* hardware
  * hardware dsl https://github.com/sifive/Kami
* assembly
  * Typed assembly language https://en.wikipedia.org/wiki/Typed_assembly_language
  * from system f to typed assembly
  * proof theory for low level code http://www.riec.tohoku.ac.jp/~ohori/research/LogicalMachineRevOct2005.pdf
* webassembly
  * portability https://webassembly.org/docs/portability
  * import https://webassembly.github.io/spec/core/syntax/modules.html
  * tooling https://github.com/WebAssembly/binaryen
  * os https://browsix.org/
  * deepspec https://pldi20.sigplan.org/details/rems-deepspec-2020/11/-WebAssembly-sequential-and-concurrent-semantics
* rewrite systems
  * On Constructor Rewrite Systems and the Lambda-Calculus
* theorem provers
  * Learning logic and proof with an Interactive Theorem Prover https://www.andrew.cmu.edu/user/avigad/Papers/learning_logic_and_proof.pdf
  * Towards a practical programming language based on dependent type theory
  * Learning logic and proof with an Interactive Theorem Prover https://www.andrew.cmu.edu/user/avigad/Papers/learning_logic_and_proof.pdf
  * Towards a practical programming language based on dependent type theory
  * Parametric Higher-Order Abstract Syntax for Mechanized Semantics http://adam.chlipala.net/papers/PhoasICFP08/
  * Implementing Certified Programming Language Tools in Dependent Type Theory http://adam.chlipala.net/papers/ChlipalaPhD/
* hol
  * Mechanizing Programming Logics in Higher Order Logic https://www.cl.cam.ac.uk/archive/mjcg/Banffpaper.pdf
* os 
  * kit http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=CF1415D8926E00366C310FE5FC6D40A5?doi=10.1.1.42.3293&rep=rep1&type=pdf
  * flint http://flint.cs.yale.edu/flint/index.html
  * certikos http://flint.cs.yale.edu/certikos/
* vdm
  * proof in vdm https://www.overturetool.org/publications/books/proof-in-vdm/ProofinVDM.pdf
* system
  * ironclad https://www.microsoft.com/en-us/research/project/ironclad/
* verilog
  * Verilog development and verification project for HOL4 https://github.com/CakeML/hardware
  * lutsig http://www.cse.chalmers.se/~loow/papers/cpp2021.pdf
* bluespec
  * Formal Verification of Hardware Synthesis https://arxiv.org/abs/1301.4779
  * the essence of bluespec https://dl.acm.org/doi/abs/10.1145/3385412.3385965
  * koika https://github.com/mit-plv/koika
  
## Algorithms

* union find https://en.wikipedia.org/wiki/Disjoint-set_data_structure
* unification https://en.wikipedia.org/wiki/Unification_(computer_science)
* smt https://en.wikipedia.org/wiki/Satisfiability_modulo_theories
* skolemization https://en.wikipedia.org/wiki/Skolem_normal_form

## OS

* what is most micro os

## Protocols

* devices, io
* packets why not
* whatever -> upd -> tcp -> http whatever

## Applications

* desk ide
* md processor

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

## Verification

Try Cheri C example hack on nand2tetris as motivation for verification.

## Stack

The iot project outlines a full stack path through verification including hardware running risk-v https://github.com/mit-plv/bedrock2
