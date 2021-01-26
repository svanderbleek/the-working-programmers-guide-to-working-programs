# the working programmer's guide to working programs

"Simplicity is a great virtue but it requires hard work to achieve it and education to appreciate it" - Dijkstra

What if nand2tetris met deepspec? Can we find the appropriate jumping in point to build a verification stack from the language to os level with a specific vocus on creating a verification focused ide.

Two major goals are

* demonstrate the joy in the proof based approach to programming
* demonstrate the impact integrated tooling can have on productivity

The target audience is working programmers so there is no teaching the basics of writing programs. All introduced concepts are fully explained by building programs. Nothing done here is for ideological purity all choices are made to maximize the simple presentation of hard concepts.

## Computation system

We design a computation system able to execute programs stored in io on finite hardware. The standard model of hardware provisions registers of T size types and O size types of operators, where cardinality of O is drastically smaller than T, and provide M * T registers and P * O operators. This is a turing machine model we can also use any equivalent model if it will be easier for verification purposes.

## Effective progress

The idea behind a computation system making effective progress in a general theory of computation is that a processor P adapts the hardware H capabilities C to running an abstract machine M evaluating a language L. Specs bind C to P with proofs of M sufficiency for C and that P C implements M faithfully. This formal relationship among parts will be extended with the case of P defining an operating system and what that means for the relations. Our model of computation is effective progress, obtaining an incrementally verifiable proof within finite bounds of io and processing tokens.

## Influences

"Young man, in mathematics you don't understand things. You just get used to them." - von Neumann

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
* kit
* the little typer
* the little prover
* software abstractions
* tla+
* verisoft
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
* type and formal proof
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
* reduceron
* fpga
* lisp machines
* lilith
* zarf
* lem

## Research

This is exploratory, some of it will go no where. There is a pragmatic focus with working so we don't go beyond that for any reason, we work with what we are given and make the least ammount of inventions to develop the verification chain and a verification focused ide. Currently that looks like webassembly with binaryen and browsix as our entry point versus the simulators of nand2tetris.

* How to Believe a Machine-Checked Proof https://www.brics.dk/RS/97/18/BRICS-RS-97-18.pdf
* bisumulation
  * Bisimilarity as a theory of functional programming
* theorem transfer
  * transfer principle https://en.wikipedia.org/wiki/Transfer_principle
* optimization
  * optimization validation http://homepages.inf.ed.ac.uk/da/papers/optval/
  * improvement theory http://www.cse.chalmers.se/~dave/papers/hoots97.pdf
* verification interacting synthesis
  * https://ptolemy.berkeley.edu/projects/embedded/research/vis/doc/VisUser/vis_user/node2.html
  * Computational Tree Logic
* concurrency
  * https://web.archive.org/web/20200504155703/https://www.cl.cam.ac.uk/~gw104/winskel-nielsen-models-for-concurrency.pdf
  * petri https://en.wikipedia.org/wiki/Petri_net
  * kahn https://en.wikipedia.org/wiki/Kahn_process_networks
* ku machine
  * http://web.archive.org/web/20080913062038/http://research.microsoft.com/~gurevich/Opera/78.pdf
* types
  * logical and data types https://www.researchgate.net/profile/Zhaohui_Luo/publication/243770570_Computation_and_Reasoning_A_Type_Theory_for_Computer_Science/links/54d0dc6b0cf29ca81103f26a.pdf
* reification
  * THE ROLE OF DATA REIFICATION IN PROGRAM REFINEMENT
* finiteness
  * the finiteness of developments https://www.math.cmu.edu/~wgunther/FD.pdf
  * The input/output complexity of sorting and related problems https://hal.inria.fr/inria-00075827/document
* rewrite
  * Computing with Rewrite Systems 
* proof carring code
  * http://www.cs.jhu.edu/~fabian/courses/CS600.624/proof-carrying-code.pdf
* sequent
  * A sequent calculus machine for symbolic computation systems 
* high level
  * High-level verification of system designs
* circuit
  * constructing correct circuits http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.97.2678
* One Instruction Set
  * https://www.cs.drexel.edu/~bls96/oisc/
* Compiler Verification
  * A Minimalistic Verified Bootstrapped Compiler http://www.cse.chalmers.se/~myreen/cpp2021-bootstrap-myreen.pdf
  * Compositional CompCert https://www.cs.princeton.edu/~appel/papers/compcomp.pdf
  * Verified compilation on a verified processor
  * Verified Sequential Malloc/Free https://www.cs.princeton.edu/~appel/papers/memmgr.pdf
  * VST-Floyd: A separation logic tool to verify correctness of C programs https://www.cs.princeton.edu/~appel/papers/VST-Floyd.pdf
  * A Completely Verified Realistic Bootstrap Compiler A Completely Verified Realistic Bootstrap Compiler
  * A Verified Compiler for an Impure Functional Language http://adam.chlipala.net/papers/ImpurePOPL10/ImpurePOPL10.pdf
  * A Certified Type-Preserving Compiler from Lambda Calculus to Assembly Language
  * The Next 700 Compiler Correctness Theorems http://www.ccs.neu.edu/home/amal/papers/next700ccc.pdf
* classics 
  * correctness of a compiler for arithmetic http://jmc.stanford.edu/articles/mcpain/mcpain.pdf
  * towards compiler implementation correctness proofs 10.1145/5397.30847
* Verification Check
  * https://en.wikipedia.org/wiki/Verification_condition_generator
* interaction trees https://github.com/DeepSpec/InteractionTrees
* instruction semantics
  * https://www.cl.cam.ac.uk/~pes20/sail/
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
  * A Reduction Theorem for Predicate Logic
  * Computation-oriented reductions of predicate to propositional logic
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
  * Processor verification using efficient reductions of the logic of uninterpreted functions to propositional logic
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
  * lisp machine https://www.cs.utah.edu/~mflatt/past-courses/cs6510/public_html/lispm.pdf
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
  * Kami: a platform for high-level parametric hardware specification and its modular verification https://dl.acm.org/doi/abs/10.1145/3110268
* assembly
  * Typed assembly language https://en.wikipedia.org/wiki/Typed_assembly_language
  * from system f to typed assembly
  * proof theory for low level code http://www.riec.tohoku.ac.jp/~ohori/research/LogicalMachineRevOct2005.pdf
  * Safe functional systems through integrity types and verified assembly
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
* abstract stack
  * An Abstract Stack Based Approach to Verified Compositional Compilation 
* microarchitecture
  * http://goto.ucsd.edu/~rjhala/papers/microarchitectural_verification_by_compositional_model_checking.html
  * Automated Formal Verification of Processors Based on Architectural Models
  * Model Stack for the Pervasive Verification of a Microkernel-based Operating System
  * Verification-Aware Microprocessor Design
* dataflow architecture
  * https://en.wikipedia.org/wiki/Dataflow_architecture
  * http://csg.csail.mit.edu/pubs/memos/Memo-261-1/Memo-261-2.pdf
  * j machine https://en.wikipedia.org/wiki/J%E2%80%93Machine
  * https://course.ece.cmu.edu/~ece740/f13/lib/exe/fetch.php?media=onur-740-fall13-module5.2.1-dataflow-part1.pdf
  * Naiad: a timely dataflow system https://dl.acm.org/doi/10.1145/2517349.2522738
  * fmj dataflow language http://www.fmjlang.co.uk/fmj/FMJ.html
  * https://cacm.acm.org/magazines/2019/6/237005-heterogeneous-von-neumann-dataflow-microprocessors/fulltext
* risc
  * A Practical Methodology for the Formal Verification of RISC Processors https://dl.acm.org/doi/10.1023/A%3A1008622002590
  * risc semantics in haskell https://github.com/mit-plv/riscv-semantics
* fpga
  * reduceron https://github.com/tommythorn/Reduceron
  * https://gitlab.com/x653/nand2tetris-fpga/
  * A FORMAL VERIFICATION METHODOLOGY FOR REAL-TIME FPGA https://library.ndsu.edu/ir/bitstream/handle/10365/26685/A%20Formal%20Verification%20Methodology%20for%20Real-time%20FPGA.pdf?sequence=3&isAllowed=y
* isa
  * End-to-End Verification of ARM® Processors with ISA-Formal https://alastairreid.github.io/papers/cav2016_isa_formal.pdf
* verification stack
  * Integrating Formal Verification into an Advanced Computer Architecture Course
  * kit and the short stack https://link.springer.com/article/10.1007%2FBF00243135
  * Model Stack for the Pervasive Verification of a Microkernel-based Operating System
  * Formal Verification of a Small Real-Time Operating System
* cakeml
  * Proof-grounded bootstrapping of a verified compiler Producing a verified read-eval-print loop for CakeML
* design for verifiability
  * Design for verifiability https://link.springer.com/chapter/10.1007/0-387-97226-9_20
  * Using Formal Techniques for Design for Verifiability https://si2.epfl.ch/~demichel/si.epfl.ch/files/content/sites/si/files/shared/Logic%20Synthesis/slides/EPFL%20LSV%20Workshop%202015_Rolf%20Drechsler.pdf
  * improving hardware designs while simplifying their proof http://webcache.googleusercontent.com/search?q=cache:Rv0hrLcRuLkJ:citeseerx.ist.psu.edu/viewdoc/download%3Bjsessionid%3D5021E76374FD1A652C5E9C4BDA3A32AF%3Fdoi%3D10.1.1.104.2960%26rep%3Drep1%26type%3Dpdf+&cd=3&hl=en&ct=clnk&gl=us
  * verifiability and analysis as a first-order constraint https://www.arch.cs.ucsb.edu/zarf
  * Verification Driven Formal Architecture and Microarchitecture Modeling
* rtl
  * http://ucsbarchlab.github.io/PyRTL/


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
