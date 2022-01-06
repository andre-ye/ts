---
layout: default
title: Module 1
parent: Winter
grand_parent: Biology
nav_order: 1
---

# Module 1 - Gene Expression, Development, Technologies

Winter Biology
{: .fs-6 .fw-300 }

---

## Navigation
- [Textbook Notes: Chapter 18, "Control of Gene Expression in Bacteria"](#textbook-notes-chapter-18-control-of-gene-expression-in-bacteria)
- [Textbook Notes: Chapter 19, "Control of Gene Expression in Eukaryotes"](#textbook-notes-chapter-19-control-of-gene-expression-in-eukaryotes)
- [Textbook Notes: Chapter 20.5, "Genome Editing"](#textbook-notes-chapter-205-genome-editing)
- [Amy Wagers: CRISPR-Cas9 to Address Duchenne Muscular Dystrophy](#amy-wagers-crispr-cas9-to-address-duchenne-muscular-dystrophy)
- [Neville Sanjana: Genetic Screens for Improving Cancer Therapy](#neville-sanjana-genetic-screens-for-improving-cancer-therapy)
- [Doudna: Genome Engineering with CRISPR-Cas9](#doudna-genome-engineering-with-crispr-cas9)
- [Documentary Notes: The Stem Cell Revolution](#documentary-notes-the-stem-cell-revolution)
- [Assigned Video Notes](#assigned-video-notes)


---

## Textbook Notes: Chapter 18, "Control of Gene Expression in Bacteria"

- Imagine seeing an orchestra; all the instruments play all at once, uncoordinated. It's not music.
- Similarly, if a bacterial cell expressed all its genes all the time, the organism would not function properly.
- Bacteria cells control the activity, or expression, of their genes.
- **Gene expression** is the process of converting information from DNA to molecules that function.

### Section-Specific Navigation

- [Introduction](#introduction)
- [18.1: An Overview of Gene Regulation and Information Flow](#181-an-overview-of-gene-regulation-and-information-flow)
  * [Mechanisms of Regulation](#mechanisms-of-regulation)
  * [Metabolizing Lactose - A Model System](#metabolizing-lactose-a-model-system)
- [18.2: Negative and Positive Control of Transcription](#182-negative-and-positive-control-of-transcription)
  * [A Gene Needed to Regulate Lactose Metabolism](#a-gene-needed-to-regulate-lactose-metabolism)
  * [Negative Control of Lactose Utilization Genes](#negative-control-of-lactose-utilization-genes)
  * [The Operon Model](#the-operon-model)
    + [Key Ideas from the Operon Model](#key-ideas-from-the-operon-model)
  * [Positive Control of Lactose Utilization Genes](#positive-control-of-lactose-utilization-genes)
    + [Positive Control by CAP Regulation](#positive-control-by-cap-regulation)
    + [Control by Inducer Exclusion](#control-by-inducer-exclusion)
  * [Why Has the *lac* Operon Model Been So Important Scientifically?](#why-has-the-lac-operon-model-been-so-important-scientifically)
  * [The *trp* Operon: A Twist on Negative Control](#the-trp-operon-a-twist-on-negative-control)
- [18.3: Global Gene Regulation](#183-global-gene-regulation)


### 18.1: An Overview of Gene Regulation and Information Flow
- Bacterial organisms in your intestine compete for space and nutrients.
  - The cell must use resources efficiently.
- The cell needs to orchestrate and regulate which proteins they produce in accordance with reactions from the environment.


#### Mechanisms of Regulation
- Gene expression can be controlled at any of the steps in the Central Dogma:
  - DNA to mRNA, *transcriptional control*. The cell only makes mRNAs for proteins it needs. Regulatory proteins affect RNA polymerase's ability to bind to the promoter and initiate transcription.
  - mRNA to protein, *translational control*. The cell prevents mRNAs for unneeded proteins from being translated. Regulation of mRNA's life span or ability is used.
  - protein to activated protein, *post-translational control*. Modifications required to activate proteins can be denied.
- All of these forms of control appear in bacteria, but this textbook will only focus on *transcriptional control*.

| Type | Speed | Energy |
|  |  |  |
| Transcriptional | Not too fast. | Saves energy of the cell because it controls gene expression before the cell spends too many resources on it. |
| Translational | Faster changes than transcriptional, because mRNA has already been made and the *amount* of proteins can be regulated. | More energy than transcriptional, because mRNAs are being made when they may not need to be. |
| Post-translational | The fastest response of all mechanisms; only one step is needed to inactivate or activate a protein. | Energetically inefficient; the entire protein needs to be made first. |

- Clear **tradeoff between efficiency and speed**.
- **Constutively transcribed** genes are ones that are transcribed all the time.
  - e.g. enzymes required for glycolysis.
- Genes are not just 'on' or 'off', instead, the *level* of expression varies.







#### Metabolizing Lactose - A Model System
- Jacques Monod and Francois Jacob used *E. coli* to study regulation of lactose metabolism.
- *E. coli* uses many sugars for ATP production; glucose is its preferred carbon source.
  - Lactose can also be used in the absence of glucose.
  - To use it, *E. coli* uses **galactoside permease* to transport the sugar into the cell.
  - Enzyme **beta-galactosidase** breaks down lactose into glucose and galactose.
- ***E. coli* produces a high level of beta-galactosidase only when lactose is present.***
  - Lactose regulates the gene for beta-galactosidase; lactose is an **inducer**, or a small molecule that triggers transcription of a gene.
- *E. coli* did not produce beta-galactosidase when *both* glucose and lactose were present.







### 18.2: Negative and Positive Control of Transcription
- Transcription of any gene can be regulated through:
  - **Negative control**. A **repressor** (a regulatory protein) binds to DNA and stops transcription.
  - **Positive control**. An **activator** (a regulatory protein) binds to DNA and *triggers* transcription.
- Genes are under both negative and positive control.







#### A Gene Needed to Regulate Lactose Metabolism
- Monod and Jacob isolated and analyzed mutants of *E. coli* unable to use lactose.
- Three types of mutants:
  - Cells unable to cleave lactose, even when lactose was in the medium and transported into cells. These mutants lacked functioning beta-galactosidase proteins. Genotype `lacZ-`
  - Cells failed to accumulate lactose in the cell. These mutants lacked galactosidase permease. Genotype `lacY-`
  - Cells can cleave lactose even if lactose is absent. Cells could produce beta-galactosidase and galactoside permease, but could not regulate their expression. Genotype `lacI-`
- **Constitutive mutants** are cells that produce a product *consistently* at all times instead of regulating its expression.
- **`lacI` prevents the transcription of `lacZ` and `lacY` when lactose is absent.**
  - `lacI` is supposed to act as a negative regulator; thus, lactose probably is an inducer, interacting with `lacI`.








#### Negative Control of Lactose Utilization Genes
- Leo Szilard suggested `lacI` codes for a *protein product* that represses transcription of `lacZ` and `lacY`.
  - Genetic mapping suggests `lacZ` and `lacY` are transcribed together.
- `lacI` produces a repressor protein that binds to DNA and overlaps the promoter for both the `lacZ` and the `lacY` genes.
  - This prevents RNA polymerase by interfering with the binding.
- Lactose binds to the repressor, changes its shape, and causes the repressor to release from its binding site in the DNA.
  - Lactose "releases" the "brake" (negative control repressor)
- Constitutive transcription happens when the functional repressor is absent (no "brake").
- **To test out this hypothesis of negative control;**
  - Added a functioning copy of `lacI` repressor to `lacI-` mutants.
  - Beta-galactosidase production stopped.
- **Lactose acts as an inducer by causing the repressor to release from DNA and ending negative control.**








#### The Operon Model
- Genes for beta-galactosidase and galactoside permease are controlled *together* and transcribed into a single mRNA.
  - An mRNA that codes for two or more polypeptides is a **polycistronic mRNA**.
  - (Most bacteria mRNAs are polycistronic; almost all eukaryotic mRNAs are not.)
- An **operon** is a set of coordinately regulated bacteria genes transcribed into *one* polycistronic mRNA.
  - Genes involved in lactose metabolism are the **lac operon**.
- `lacA` codes for the enzyme transacetylase; allows certain types of sugars to be exported from the cell when they are too abundant.







#### Key Ideas from the Operon Model
1. `lacZ`, `lacY`, and `lacA` genes are adjacent and transcribed as *one* mRNA. This is known as **cotranscription**.
2. The repressor protein encoded by `lacI` binds to a specific sequence in DNA and prevents transcription of the *lac* operon genes. `lacI` is expressed constitutively. The repressor binds to a DNA sequence in the *lac* operon called the **operator**.
3. The inducer (lactose) binds to the repressor and changes its shape, causing it to come off the DNA. Control over protein function like this is **allosteric regulation**.
  - Allosteric regulation: a small molecule binds to a protein and changes its shape and activity.
  






#### Positive Control of Lactose Utilization Genes
- Transcription of *lac* operon is reduced when glucose is present.







#### Positive Control by CAP Regulation
- **Catabolite activator protein (CAP)** exerts positive control on many operons in *E. coli*.
  - Is transcribed & transcripted constitutively.
- CAP binds to a regulatory sequence of DNA and *increases* the frequency of initiating transcription.
  - CAP promotes the association of the RNA polymerase holoenzyme w/ the promoter.
  - CAP can only be bound to cyclic AMP. When glucose level outside the cell is high, cAMP is inhibited.
  - When glucose level outside a cell is low, cAMP synthesis ramps up. This enables CAP to bind and promote transcription.
 






#### Control by Inducer Exclusion
- Glucose inhibits the transport of sugars other than glucose into the cell.
  - When glucose is abundant, galactoside permease is inhibited.







#### Why Has the *lac* Operon Model Been So Important Scientifically?
- Many bacterial genes and operons are under negative control by repressor proteins.
- Activator proteins often work by enhancing the binding of RNA polymerase to the promoter.
- Gene transcription is often regulated by contact between regulatory proteins and regulatory sequences in DNA.
- Post-translational control allows for a quick response to changing environments.
  - Activity of repressors can be altered allosterically.







#### The *trp* Operon: A Twist on Negative Control
- The *lac* operon breaks down lactose into component sugars.
  - Operons can also *create* compounds.
- The *trp* operon synthesizes the amino acid tryptophan.
- Each reaction in the multistep biochemical pathway are catalyzed by an enzyme encoded by a *trp* operon gene.
  - 5 enzymes are needed - corresponding to 5 *trp* operon genes.
  - All genes are needed to work together by trnascribing the genes into one polycistronic mRNA.
  - Control of transcription *is mediated by a repressor protein*.
- Genes for tryptophan synthesis should be expressed only when tryptophan is required.
  - Genes need to be turned on when tryptophan is *absent*, instead of when something is *present* (like the *lac* operon).
- The *trp* repressor binds to its operator only when it is bound by tryptophan (its regulator).
  - *lac* repressor binds to the *lac* operator only when it is *not* bound to its operator.
- The repressor no longer binds to the operator when the tryptophan level drops, and the *trp* operon genes are transcribed.
- This is a form of **negative feedback** control.
  - The final product of a pathway inhibits the production of the product.
- The *trp* operon has a **co-repressor** that works *with* the repressor to make it active during allosteric regulation.







### 18.3: Global Gene Regulation
- Sometimes, one cannot only turn on genes or even operons individually. Bacteria may need to coordinate change.
- **Global gene regulation** is the coordinated regulation of many genes.
  - A **regulon** is a set of separate genes and operons that contain the same regulatory sequences and are controlled by one type of regulatory protein.
  - Regulons can be under *negative* control by a repressor protein or under *positive* control by an activator protein.
  - SOS response regulon: damage to DNA sets off an SOS signal that induces transcriptions of many genes that code for enzymes needed for DNA repair.
- The SOS system is under control of one of *its own genes*.
  - *lexA* codes for the LexA protein, which represses transcription of SOS regulon genes when the cell is healthy; DNA damage makes LexA cleaved and inactivated.
  - Since *lexA* is *part* of the genes, it is also produced. By the time the DNA is repaired, the SOS regulon is restroed by active LexA.
- **Interactions between protein regulators and DNA sequences produce finely tuned control over gene expression.**

---

## Textbook Notes: Chapter 19, "Control of Gene Expression in Eukaryotes"

- Bacteria regulate gene expression b/c of changes in their environment.
- However, for eukaryotes, different types of cells must be maintained using the same set of genes.
  - All cells differ from each other, but have the same genes.
- Eukaryote cells must react to changes in the external  *and internal* environments.
- **Differential gene expression** - cells with the same genome can express different sets of genes, because cells at different times and locations are exposed to different signals.

### Section-Specific Navigation
- [Introduction](#introduction-2)
- [19.1: Gene Regulation in Eukaryotes - An Overview](#191-gene-regulation-in-eukaryotes-an-overview)
  * [Summary of Levels of Gene Expression in Eukaryotes](#summary-of-levels-of-gene-expression-in-eukaryotes)
- [19.2: Chromatin Remodeling](#192-chromatin-remodeling)
  * [Chromatin Structure](#chromatin-structure)
  * [Chromatin Structure is Altered in Active Genes](#chromatin-structure-is-altered-in-active-genes)
  * [How is Chromatin Altered?](#how-is-chromatin-altered)
    + [DNA Methylation](#dna-methylation)
    + [Histone Modification](#histone-modification)
    + [Chromatin-Remodeling Complexes](#chromatin-remodeling-complexes)
  * [DNA and Chromatin Modifications Vary and Can Be Inherited](#dna-and-chromatin-modifications-vary-and-can-be-inherited)
    + [Long-Lasting Epigenetic Marks Imposed During Development](#long-lasting-epigenetic-marks-imposed-during-development)
    + [Epigenetic Inheritance is Widespread](#epigenetic-inheritance-is-widespread)
- [19.3: Initiating Transcription](#193-initiating-transcription)
  * [Promoter-Proximal Elements Are Regulatory Sequences Near the Core Promoter](#promoter-proximal-elements-are-regulatory-sequences-near-the-core-promoter)
  * [Enhancers Are Regulatory Sequences Far from the Core Promoter](#enhancers-are-regulatory-sequences-far-from-the-core-promoter)
  * [The Role of Transcription Factors in Differential Gene Expression](#the-role-of-transcription-factors-in-differential-gene-expression)
  * [How Do Transcription Factors Recognize Specific DNA Sequences?](#how-do-transcription-factors-recognize-specific-dna-sequences)
  * [A Model for Transcription Initiation](#a-model-for-transcription-initiation)



### 19.1: Gene Regulation in Eukaryotes - An Overview
- Eukaryotes can control gene expression at *transcription, translation,* and *post-translation*.
  - There are, however, *more levels of control*.
- **Chromatin** - the sturcture formed by DNA wrapped around proteins.
  - Eukaryotic genes have promoters, but *before* transcription can begin, DNA containing the promoter needs to be *released* from interactions w/ the protein.
  - This allows the RNA polymerase to contact the promoter.
  - This is **chromatin remodeling**.
- **RNA processing** is required to produce a mature mRNA in eukaryotes (splicing introns, etc.)
  - Alternative splicing can include exons, which result in different gene products.
- **mRNA stability** can be regulated, such that certain mRNAs can have a shorter or longer life span.

#### Summary of Levels of Gene Expression in Eukaryotes
1. Chromatin remodeling - "opening" chromatin for the RNA polymerase
2. Transcription - produce the pre-mRNA
3. RNA processing - process the pre-mRNA to form mature mRNA
4. mRNA stability - make changes to the mRNA that can degrade mRNA life span, if necessary.
5. Translation - create a polypeptide corresponding to the mRNA sequence.
6. Post-translational modification - activate or deactivate proteins.


### 19.2: Chromatin Remodeling
- For a signal to trigger transcription of a gene, chromatid around the target gene must be remodelled.
- DNA is very tightly wrapped since there is so much information; this does not allow RNA polymerase to access it.
- It must be "unwrapped" such that it *can* be accessed and transcribed.

#### Chromatin Structure
- Eukaryotic DNA is associated with **histone** proteins (generally speaking; other proteins may be used as well).
- Chromatin looks like beads on a string; these beads are **nucleosomes**.
  - Each nucleosome is about 200 base pairs of DNA wrapped almost twice around 8 histones.
  - Histone protein called **H1** "seals" DNA to each set of histone proteins.
  - DNA is negatively charged (phosphate groups); histones are positively charged (lysines and arginines).
- Nucleosomes are linked to each other to form chromatin.
  - H1s interact with each other and other histones to produce a tightly packed structure.
- These fibers are attached at intervals along their length to framework proteins; this allows the chromosome to be organized.
- Each chromosome lies in its own territory of the interphase nucleus.
  - Parts fold into actively transcribed sites; location matters.
- Chromatin has important implications for gene expression control.

#### Chromatin Structure is Altered in Active Genes
- The interaction between DNA and histones **must be altered** for RNA polymerase to interact with it.
  - A gene cannot be transcribed *until* the condensed chromatin near the promoter is remodeled.
  - **Chromatin remodelling is the first step of eukaryotic gene expression.**
- **DNase** is an enzyme that cuts DNA at random locations. However it cannot cut DNA if it is wrapped with proteins; so it can only work with DNA if the DNA is "decondensed" or in *open configuration*.
  - Wintraub and Groudine experiment: compared chromatin structure of beta-globin and ovalbumin.
  - Beta-blogin is hemoglobin found in red blood cells, ovalbumin is a protein found in egg white. Beta-globin should be transcribed at high levels in blood cells, and the opposite for ovalbumin.
  - Findings: DNase cut beta-globin gene DNA much more than ovalbumin gene DNA. Hence, chromatin of beta-globin was *decondensed* and chromatin the ovalbumin gene was *condensed*.
- **Chromatin is decondensed in genes that are being transcribed**.
- By default, eukaryotic genes are "turned off" b/c they are normally wrapped tightly in chromatin.

#### How is Chromatin Altered?
- There are three ways to remodel chromatin: DNA methylation, histone modification, and chromatin-remodeling complexes.

###### DNA Methylation
- **DNA methyltransferases** add methyl groups to cytosine residues in DNA via **DNA methylation**.
- The sequence recognized by enzymes is a C next to a G (`ATAT[CG]TA`). The methylated sequences are abbreviated `CpG`.
- Methylated `CpG` sequences are recognized by proteins that **trigger chromatin condensation**.
  - Hence, actively transcribed genes **have fewer methylated CpG sequences near their promoters**.

###### Histone Modification
- Many enzymes add several chemical groups to histone protein amino acids.
  - Includes acetyl groups, methyl gruops, phosphate groups, and short polypeptides.
- Modifying histones alters the bond between DNA and histone proteins.
  - **This can condense or decondense chromatin**, depending on the modifications.
- Proposal: histone modification combinations set the state of chromatin condensation for a particular gene. **Histone code hypothesis**.
  - **histone acetyltransferases (HATs)** add acetyl groups to positively charged lysine residues of histones. This interferes with assembly nucleosomes in condensed chromatin.
    - Process known as **acetylation** - promotion of *decondensed* chromatin and active transcription. The "on switch".
  - **histone deacetylases (HDACs)** remove acetyl groups. This reverts chromatin into a condensed state. The "off switch".
  
###### Chromatin-Remodeling Complexes
- **Chromatin-remodeling complexs** are proteins that form macromolecular machines.
  - Harness energy in ATP to *reshape* chromatin.
  - Can cause nucleosomes to slide along DNA or knock histones off DNA to open chromatin for transcription.
- **Condensation state of chromatin is critical in determining whether transcription can occur or not.**

#### DNA and Chromatin Modifications Vary and Can Be Inherited
- Chromatin modifications vary from one cell type to another (e.g. skin and liver cell).
- When skin or liver cells divide, **DNA methylation and histone modification patterns are passed to duaghter cells.**
  - Daughter cells inherit patterns of gene expression via **epigenetic inheritance**. (inheritance of anything other than DNA sequences)
- Chromatin is modified early in its development to form a certain cell, like a skin cell.
- Epigentic mechanisms can record life events and are difficult to erase. Prenatal conditions can make long-lasting alterations in the chromatin of embryos that influence phenotypes.

###### Long-Lasting Epigenetic Marks Imposed During Development
- Experiment: what happens to rats born to mothers fed low-protein diets during pregnancy and nursing?
  - Animals have a greater risk of developing disorders similar to type 2 diabetes, even though a normal diet was provided after early deprivations.
- *Hnf4a* is a gene associated with diabetes; codes for a regulator of genes involved in glucose uptake.
  - Epigentic inheritence could be silencing *Hnf4a* expression.
- Results of analysis: **histone modifications of *Hnf4a* gene led to condensed chromatin** for rats born to malnourished mothers.
- A mother's nutritional status is repsonsible for chromatin modifications seen in offspring.

###### Epigenetic Inheritance is Widespread
- Environmental influences early in life can be recorded into patterns of chromatin condensation.
- Human mental retardation - Rett syndrome. Occurs when mutation l eads to absence of a protein that binds to methylated DNA to induce chromatin condensation.


### 19.3: Initiating Transcription
- The promoter in eukaryotes is where DNA and RNA polymerase bind to initiate transcription.
- **Core promoter** refers to the sequence RNA polymerase binds to.
  - **TATA box** is an intensively studied core promoter sequence.
- THe **TATA-binding protein (TBP)** binds to initiate transcription.
  - TBP is in a large protein complex.

#### Promoter-Proximal Elements Are Regulatory Sequences Near the Core Promoter
- **Regulatory** sequences are other DNA sequences *besides the core promoter* that allow control over the initiation of transcription.
  - Regulatory sequences in eukaryotes are like the operator and CAP binding site.
- How do yeast cells control metabolism of galactose?
  - When galactose is absent, *S. cerevisiae* cells produce small amounts of the five galactose-processing enzymes. When galactose is present, the opposite is true.
  - The regulatory protein binds to a regulatory sequence just upstream from the core promoter for *each* of the five genes.
- **Instead of being clustered into a single operon, co-regulated genes in eukaryotes have the *same* regulatory DNA sequence that binds to the same type of regulatory protein.**
  - These regulatory sequences exist in all eukaryotic genes.
- Regulatory sequences close to the promoter are **promoter-proximal elements**.
  - Different types of promoter-proximal elements are associated with each gene; eukaryotic cells can express certain genes but not others.

#### Enhancers Are Regulatory Sequences Far from the Core Promoter
- Researchers found a regulatory sequence required for enhanced transcription in one of the *introns*.
  - The regulatory sequence was thousands of bases away and downstream from the promoter.
  - These regulatory sequences far from the promoter (and can be in nontranscribed sequences) that activate transcription are **enhancers**.
  - Enhancers *occur in all eukaryotes*.
- Enhancers are composed of many short regulatory sequences that bind to a different specific regulatory protein.
- Enhancers work even if they are flipped from their normal orientation or moved to new locations near the gene.
- **Transcriptional activators** (or just **activators**) bind to enhancers to begin transcription.
  - Enhancers and activators are *positive control*, like a gas pedal.
- Regulatory sequences like enhancers that instead inhibit transcription re **silencers**.
  - When **repressors** bind to silencers, transcription is shut down.
  
#### The Role of Transcription Factors in Differential Gene Expression
- Enhancers and silencers are binding sites for activators and repressors that regulate transcirption; these proteins are **regulatory transcription factors**.
  - Hundreds of transcription factors binde to enhancers, silencers, and promoter-proximal elements.
- Different types of cells **express different genes b/c of different transcription factors**.
  - Genes encoding transcription factors are expressed inr esponse to signals from other cells (esp. during embryonic development).
- Formation of a muscle cell:
  1. As a cell in the early embryo, production of muscle cell-specific transcription factors begins.
  2. Transcription factors bind to regulatory sequences and turn "on" production of muscle-specific proteins.
- **Differential gene expression results primarily from production or activation of specific transcription factors.**

#### How Do Transcription Factors Recognize Specific DNA Sequences?
- Transcription factors must be able to recognize and bind to a DNA sequence.
  - DNA bases are partially exposed in the grooves of the DNA double helix. (major and minor grooves)
- Differences in chemical composition and shape of groves are recognized by transcription factors.
- A transcriptional factor important for development of muscle cells inserts amino acid side chains into the grooves of DNA.
  - Complementary interactions between amino acids and a particular sequence of base pairs in DNA.

#### A Model for Transcription Initiation
- Gene expression can be controlled at many levels, *but regulating the start of transcription is perhaps the most important.*
- **General transcription factors** interact w/ the core promoter and are not restricted to *particular genes* or cell types. 
  - "general": proteins are necessary for transcription to occur, but do not provide much regulation.
- TBP is a part of a large general transcription factor.
- The **mediator** acts as a bridge between regulatory transcirption factors, general transcription factors, and RNA polymerase II.
  - Plays an important role of integrating regulatory trnascription factors; delivers a signal to RNA polymerase for transcription initiation.
- Process:
  1. Activators bind to DNA. Chromatin-remodeling complexes and histone acetyltransferases are used, and chromatin decondenses.
  2. Some chromatin that is exposed includes the core promoter, promoter-proximal elements, and enhancers.
  3. Other activators bind to exposed enhancers and promoter-proximal events. DNA-bound activators bind to the Mediator.
  4. General transcription factors and RNA polymerase II assemble to the Mediator and associate with the core promoter.
  5. DNA strands are opened, RNA polymerase II begins transcription.
- Activators work to stimulate transcription, but *also* to bring chromatin-remodeling proteins to the right place.
- Chromatin remodeling proteins cannot recognize specific DNA sequences; transcriptional activators bind first to recruit them.
- DNA sometimes disassociates from histone proteins in nucleosomes, exposing regulatory sequences to activators.

---

## Textbook Notes: Chapter 20.5, "Genome Editing"

- Biotechnology tools often come in unexpected places.
- Precise genome editing was produced with the **CRISPR-Cas** system.

### Section-Specific Navigation
- [The Biology of the CRISPR-Cas System](#the-biology-of-the-crispr-cas-system)
- [Using the CRISPR-Cas System for Genome Editing](#using-the-crispr-cas-system-for-genome-editing)
- [What's Been Achieved with CRISPR-Cas Genomoe Editing?](#what-s-been-achieved-with-crispr-cas-genomoe-editing)
  * [CRISPR-Cas Genome Editing in Agriculture](#crispr-cas-genome-editing-in-agriculture)
  * [CRISPR-Cas Genome Editing in Ecosystems](#crispr-cas-genome-editing-in-ecosystems)


### The Biology of the CRISPR-Cas System
- While studying salt-tolerant archaean, investigators found short repeating DNA sequences.
  - These were separated by spacer sequences with no similarity to each other or other sequences.
  - This repeat-separated-by-spacer sequence is widespread in bacteria and archaea.
- The spacer sequences are not random bits of DNA, but **DNA of different viruses that could infect the cell.**
  - These viral spacer DNAs provided immunity against further infections.
- Repeats (bacterial DNA) are between 20-50 base pairs; spacers (viral DNA fragments) are between 30-70 base pairs.
- DNA sequences that protect against these viral infections are:
  - **C**lustered
  - **R**egularly
  - **I**nterspaced
  - **S**hort
  - **P**alindromic
  - **R**epeat
- The CRISPR locus is transcribed into long pre-crRNA.
  - crRNA: CRISPR RNA.
  - Pre-CRNA processed into shorter RNA fragments.
  - Each fragment (the crRNA) contains a spacer region that is an RNA copy of part of the viral genome, flanked by bacterially encoded repeat sequences.
- crRNA binds with tracrRNA (trans-activating CRISPR RNA), and are bound with the Cas protein (CRISPR-associated protein).
  - Cas proteins are endonucleases that cut DNA compelmentary to a crRNA.
- There are four different CRISPR systems; Cas9 is the simplest and most widely used for gene editing.
- The Cas protein could be guided to a genome sequence by complementary crRNA: **possibilities for editing the genome by cutting it into specific pieces.**

### Using the CRISPR-Cas System for Genome Editing
- Next step: simplify the CRISPR-Cas system for practical use.
- Chemically synthesized DNA was transcribed in vitiro to create a fusion of crRNA and tracrRNAs, producing **single guide RNA (sgRNA)**.
- Common method:
  1. Mix sgRNA with plasmid DNA that contains the gene for Cas9.
  2. Introduce this mixture of nucleic acids into the cell.
  3. When the Cas9 gene is expressed, it associated with the sgRNA.
  4. The sgRNA guides Cas9 to a complementary target sequence in the genome.
  5. Cas9 endonuclease makes double-stranded cuts in the DNA.
- Two ways to join broken DNA:

| **Nonhomologous end joining** | A double-strand break can be repaired by joining the broken DNA back together, but there will always be insertions or deletions (indels). If DNA is cut, it will disrupt viral function. |
| **Homology-directed repair** | An intact segment of DNA that is available is fitted into the double-strand break. |

- To use HDR, scientists need to introduce a DNA fragment into the cells along with the CRISPR-Cas machinery.
  - The DNA can be a modification of the original sequence.
- CRISPR-Cas genome editing is the next revolution in biology.

### What's Been Achieved with CRISPR-Cas Genomoe Editing?

#### CRISPR-Cas Genome Editing in Agriculture
- Animal and crop scientists have embraced CRISPR-Cas genome editing because of its ease, precision, and ability to introduce multiple genome changes at once.
- With CRISPR-Cas editing, nothing foreign is inserted into the genome.
- Crop genomes can be edited by disrupting genes.
- CRISPR-Cas-edited organisms are not currentlyr egulated.

#### CRISPR-Cas Genome Editing in Ecosystems
- CRISPR-Cas can be used in a genetic engineering process called "gene drive".
- CRISPR-Cas is used to spread, or drive, a particular form of a gene to a population in just a few generations.
- Converts organisms that begin development as heterozygotes into homozygotes for an altered allele.
- Perhaps populations of mosquitos that transmit malaria could be wiped out, but what are the side effects on ecosystems?

---

## Amy Wagers: CRISPR-Cas9 to Address Duchenne Muscular Dystrophy

### Duchenne Muscular Dystrophy is a genetic disease
- A progressive and incurable muscle disease.
- Affects 1/3,500 boys.
- Caused by any number of mutations in the DMD gene that cause a lack of production of the dystrophin protein.
- Without the protein, muscle fibers lack structural stability and degenerate.







### Using CRISPR-Cas9 to restore dystrophin function
- In preclinical mouse studies, a mouse with a mutation in the middle of the dystrophin-endoding gene was used.
  - Prevents expression of the dystrophin protein, although the disease is milder than in humans.
- CRISPR-Cas9 was used to make two cuts of the mutation, removing that section of the gene.
  - The gene could be read in the way that lacked the middle part but could have *partial function*.
- Gene function could be rescued; study measured increased force by muscles.







### A preclinical proof-of-concept
- A proof-of-concept test was done.
- To bring it forward as a real treatment for humans, more work needs to be done.
- Human cells need to be tested in a culture and in a mouse to be tested in a true organismal setting.







### CRISPR provides a tool for asking many questions at once
- Because of its programmability and versatility, it can impact many areas of biology.
  - Fundamental and applied.
- The CRISPR-Cas9 system has unprecedented throughput of interrogation.
  - Can ask, "does any gene in the genome play role in this process?"

---

## Neville Sanjana: Genetic Screens for Improving Cancer Therapy

- There has been development of immunotherapy, which has been exciting for cancer research.
- There are between 50%-80% of patients that do not respond to immunotherapy, though.
- Question: what are all genes in the genome that, when their function is loss, makes you no longer responsive to immunotherapy?







### How does any one gene influence disease?
- There are 20k genes in the genome, and 5 different guide sequences per gene. 10k CRISPR guides are created.
- These guides are introduced into cells, and each has a different set of the 10k guides.
  - Therefore, each cell has a different gene knocked off.
- Genetic screening allow anyone to have a question and analyze the impact of one gene.







### Identifying genes involved in immuntherapy evasion
- A human melanona cell was taken, and a different gene was knocked out.
- Which mutations enable the cell to evade T-cell immunotherapy?
- The top 2-most enriched genes in T-cell selection were the two essential components of major histone comaptability complexes - what allows the body to surveil for infected cells.
  - When these two proteins are disrupted, the T-cells no longer recognize cancerous cells.







### CRISPR an be an efficient pointer into the genome
- Cas9 is not just something that cuts DNA, it is a general pointer into a genome.
- Thinking of it in terms of CS: a computer is useless until a specific location in memory can be pointed to and changed.
- Once an efficient pointer is achieved, the sky is the limit.

---

## Doudna: Genome Engineering with CRISPR-Cas9
- The story begins with a bacterial immune system: how do bacteria fight off an immune infection?
- Many bacteria have - in their chromosome - a sequnece of *repeats* that are interspaced with sequences that are derived from viruses.
  - These have been noticed by microbiologists sequencing bacterial genomes.
  - These also occur with a series of genes that often encode proteins that have homology to enzymes that do things like DNA repair.
- **Hypothesis** - this system (CRISPR) could actually be an acquired immune system in bacteria that might allow sequences to be integrated from viruses and used to protect the cell from infection by the same virus.







### Acquiring Immunity in Bacteria
- Right after the publication of 3 papers that pointed out the incorporation of virus sequences of these genomic loci, began studying CRISPR.
- These CRISPR systems are acquired systems in bacteria; bacteria actually had aw ay to adapt to viruses that get into the cell.
- It involves detecting foreign DNA that gets injected from a virus that gets into the cell.

| **Step** | **Description** |
|  |  |
| 1. Adaptation | The CRISPR system allows integration of short pieces of those viral DNA molecules into the CRISPR locus. |
| 2. crRNA Biogenesis | The CRISPR sequences are transcribed into pieces of RNA that are used together with proteins encoded by the CAS genes (CRISPR-associated genes) to form interference complexes. |
| 3. Interference | These interference complexes use the information in the form of RNA molecules to base-pair with matching sequences in viral DNA, disabling the virus. |

- How are RNA molecules used to help cells regulate the expression of proteins?
- Begin studying the moelcular mechanisms by which this pathway operates.







### Cas9 and Streptococcus Pyogenes
- Emmanuelle Charpentier was interested in bacteria that are human pathogens.
- Studying *streptococcus pyogenes* that is a bacterium that can cause very severe infections in humans.
- This bug has a CRISPR system; there was a single gene encoding the Cas9 protein.
  - This protein has been shown to be required for the operation of the CRISPR system for streptococcus pyogenes.
  - No one had known what the function of Cas9 was, though.

#### Cas9 Is a Dual-RNA-Guided dsDNA Endonuclease
- After experiments, discovered that **Cas9 has the ability to interact with DNA and generate a double stranded break** in DNA at sequences that match the sequence in the *guide RNA*.
- The guide RNA base pairs with one strand of the double-helical DNA.
  - This RNA interacts with tracrRNA that forms a structure that recruits the Cas9 protein.
  - These two RNAs and the protein are required for the protein to recognize what would be viral DNAs in the cell; the protien cuts these.

#### Simplifying Cas9
- Instead of two RNAs, one can link together the two RNAs to form a single-protein and single-guiding-RNA system.
- The two RNAs would be linked together to create a **single guide RNA**.

#### Programmed Cas9 Cleaves DNA at Specified Sites
- Simple experiment to test whether this was a programmable DNA cleaving enzyme.
- Short single-guide RNAs were generated, these recognized sites in a circular DNA molecule.
- The plasmid DNA was incubated with Sal1 and the RNA-guided Cas9.
- Results: cleaved molecules of DNA are separated in an agarose gel, and a different sized-molecule is released from a doubly-digested plasmid.
  - The size of the DNA corresponds to cleavage at different sites directed by the guide RNA sequences.
  - A programmable DNA cutting enzyme has been achieved; it can be programmed with a hsort bit of DNA.







### Genome Editing Begins with dsDNA Cleavage
- There are many experiments showing that cells have ways to repair double-stranded DNA breaks that lead to changes in the genomic information of the DNA.
- After a double-stranded break is generated by any enzyme (including Cas9), the break is detected and repaired.
  - One repair pathway involves **nonhomologous end-joining**; the ends are chemically ligated together. There is a small insertion or deletion.
  - Another repair pathway involves **homology directed repair**; a donor DNA molecule can be integrated into the genome at the site of the break to introduce new genetic information.
- If there were a tool to allow scientists or researchers to introduce double-stranded breaks at a particular site, you can edit genes.
  - For example, fix a mutation or generate a mutation in a DNA sequence.
- The power of technology: **we can generate double-stranded breaks that we choose** by programming Cas9.







### Genome Targeting Technologies
- Challenge: how to generate the breaks in the first place?

| Zinc Finger Nuclease (ZFN) and TAL Effector Nuclease | Programmable way to generate double-stranded breaks; rely on **protein-based recognition** of DNA sequences. Proteins are modular and can be generated in different combinations to recognize different DNA sequences. **Requires a lot of protein engineering.** |
| CRISPR/Cas9 | An **RNA-programmed** nuclease; a single protein can be used with a guide RNA. |

- This is the missing piece of the "Biology IT Toolbox".
  - DNA structure/sequencing
  - Restriction enzymes
  - Polymerase Chain Reaction
  - **Genome Editing** - enabling facile genome editing!







### Summary: CRISPR-Cas9 Technology and Applications
- A 2-component system that relies on RNA-DNA base pairing for recognition.
- The system is quite striaghtforward to do **multiplexing**.
  - Program with multiple guide RNAs to cut out multiple segments.
- There has been a large explosion in genetics and biology for creative and interesting applications.
- Applications:

| Biology | Cell lines, model organisms |
| Biotechnology | Making changes in crop plants and fungi |
| Biomedicine | Using CRISPR as a tool to come up with novel solutions to disease. |

- The future of CRISPR-Cas9-mediated genome engineering:
  - Human gene therapy
  - Agriculture
  - Synthetic biology
  - Programmable RNA targeting
  - Ecological vector control (mosquito sterilization, etc.)
  - Viral gene disruption (pathogen gene disruption)
  - Screens for drug targets

---

## Documentary Notes: The Stem Cell Revolution

### Chapter 3: Not All Cells Are Equal
- It is incredibly important we have all stem cell systems working; one cannot substitute for another.
- The blood-forming system make blood only; same for brain systems, skeletan muscles, etc.
- THe specialization of funciton is a feature of stem cells; the *embryonic stem cell* comes from the early embryo (~ 100 cells).
- Inside the early embryos are pluripotent stem cells; they can differentiate to make every sort of cell in the body.
	- They can become a new source of cells.
- It was an unusual type of cancer that gave a rise to embryo stem cells; teratocarcinoma.
- When things go wrong, we can see how the body works; to make the connections requires a conceptual leap.
- Most tumors are a nasty cariacture of a particular tissue; tumors have different tissues inside them, like teeth, etc.; a cariacture of a developing embryo.
	- There are in some cells that have the ability to differentiate.
- If there are tumor cells, you can grow them in the culture; growing cells that have the ability to develop into every other cell.
- It was a huge achievement; stem cells must have been kept undifferentiated to produce new stem cells.
	- The cells *wanted* to develop and differentiate; yet somehow they needed to be held back.
- These tumor cells were almost *identical* to embyronic cells, but simply in the wrong environment.
- Are cells from tumors normal? - yes.
- Teratocarcinoma cells modelled early embyronic development.
- Embyronic stem cells were taken directly from embryos; they could differentiate.
- The mouse produced was using embyronic stem cells.
- in vitro fertilization treatment.
- The usage of embryos is quite controversial.
- Pluripotent states - can make all sorts of cell types.








### Chapter 4: The Discovery of iPS Cells
- A tool of *reversing* cells, and perhaps we can avoid using human embyros to get stem cells.
- Yamanaka - had difficult patients suffering from spinal cord injuries, and there is no treatment.
	- Began interested in basic research, perhaps able to treat and help those patients.
- We know that each cell in our value contains something that determines its cell identity; the genes in the nucleus are expressed differently. Genes that are turned off are locked away in the chromatin.
- Yamanaka questioned if a cell must remain locked in a differentiated state.
- Begins with a list of over 100 transcription factors - operated alone, or in combination.
	- Distinguished 24 most likely candidates for transcription factors.
	- Found 4 (Oct 4, Sox2, Klf 4, and cMye) essential transcription factors.
- The four transcription factors began to turn on embyronic stem cell genes; we can thus turn somatic cells back into embyronic cells.
	- Only four factors are needed to "reset".
- We don't need embryos, but we can make ES-like stem cells; induced Pluripotent Cells (iPS).
- It was surprising that only four transcription factors are needed; it is a massive change in the nucleus.
- Work is based partially on precedented experiments.







### Chapter 5: Where could it lead?
- Because stem cells have changed the way we understand it, they have raised new questions about ethics, religion, and government.
- As soon as iPS cells have succeeded, new issues have been generated.
- Because iPS cells are pluripotent, they can be used to make sperm and eggs; thus, a human can be created from a piece of skin. It's possible in theory; keep an eye on this research.
- Be careful what you wish for; should stem cell research stop? - It's too late.
- Making iPS cells is simple for anyone with some biological training; but there needs to be more discussion with government, the public, and other entities.
- Science is morally neutral; they are tools, but any tool that is not being used sits there.
	- The people that put things to use make the moral choice.
- Progress in stem cell research has become very rapid.

---

## Assigned Video Notes

### Operons and Gene Regulation in Bacteria
[Access here](https://www.khanacademy.org/science/ap-biology/gene-expression-and-regulation/regulation-of-gene-expression-and-cell-specialization/v/operons-and-gene-regulation-in-bacteria){:target="_blank"}
- DNA regulation: if you look at an organism's genome, not all the genes are being translated & transcripted at the same time.
  - e.g. immune and muscle cells have the exact same DNA,
- Even unicellular organisms do not want to transcribe all their genes at the same time; different types of genes serve different purposes that may or may not need to be expressed.
- RNA polymerase attaches to the *promoter*; polymerase transcribes the gene.
  - Each promoter is associated with a gene in eukaryotes.
  - In prokaryotes, multiple genes may be grouped together that only have one promoter, or *regulatory DNA sequence*.
  - RNA polymerase attaches to this and transcribes multiple genes as a bundle.
  - Promoter + gene forms an **operon**.
- The operon is transcribed into one strand of mRNA, which is translated into several proteins.
- A repressor attaches to a series of DNA after the promoter, blocking polymerase from doing transcription.
  - The operator is a sequence where the repressor can attach.
- The repressor may only be able to do its job if other molecules - **corepressors** - are attached to it.
- An **activator** allows *more* transcription. Small molecules that turn the *activator* on are **inducers**.

### Lac Operon
[Access here](https://www.khanacademy.org/science/ap-biology/gene-expression-and-regulation/regulation-of-gene-expression-and-cell-specialization/v/lac-operon){:target="_blank"}
- *Lac* operon deals with lactose; e.g. `lacZ` codes for an enzyme that cleaves it into simpler sugars.
- If there's no lactose, there is no need to translate enzymes needed. Lac repressor prevents the RNA polymerase from transcribing.
- If there *is* lactose, *allolactose* (version of lactose) acts as an inducer of transcription. It binds to the lac repressor, which can no longer bind to the operator site.
  - Allows RNA polymerase to transcribe the genes.
- Glucose is preferred by the cell, though.
- CAP site; the Catabolite Activator Protein, in the presence of cAMP, binds to the cap site and allows further transcription.
  - If you have high glucose, cAMP is inhibited.
- If there is both glucose and lactose,
  - There will be allolactose, so the RNA polymerase will be able to transcribe.
  - However, there is low cAMP, which cannot bind to the CAP, which will not bind to the CAP site and act as an activator.

### Jacob Monod lac operon
[Access here](https://www.khanacademy.org/test-prep/mcat/biomolecules/dna/v/jacob-monod-lac-operon){:target="_blank"}
- An eye cell and a skin cell have the exact same DNA, but different genes are expressed.
- Usually, protein regulation happens at the transcription level; it's the most efficient.
- Lac operon found in *E. coli*.
- `Lac Z`, `Lac Y`, and `Lac A` genes help break down lactose into glucose and galactose.
- Default: these genes are not expressed.
- The RNA polymerase attaches to the promoter; on the operator site, a repressor sits and blocks the RNA polymerase.
- When there is lactose in the cell, the lactose attaches to the repressor protein and makes it come off the operator site.
  - RNA polymerase moves and transcribes all the genes.


