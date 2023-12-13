All csv files can be following the lonk below: 
Rhiju Das, Shujun He, Rui Huang, Jill Townley, Rachael Kretsch, Thomas Karagianes, John Nicol, Grace Nye, Christian Choe, Jonathan Romano, Maggie Demkin, Walter Reade, and Eterna players . (2023). Stanford Ribonanza RNA Folding. Kaggle. https://kaggle.com/competitions/stanford-ribonanza-rna-folding

## RNA reactivity
RNA reactivity is a measure of how likely an RNA molecule is to undergo chemical reactions, such as hydrolysis, acylation, or modification by specific reagents. RNA reactivity depends on several factors, such as the local structure, the base composition, the solvent environment, and the presence of catalytic agents. RNA reactivity can be used to probe the structure and function of RNA molecules, as well as to design and synthesize novel RNA-based molecules for various applications1234

Some examples of RNA reactivity are:

- RNA hydrolysis: This is the cleavage of RNA by water molecules, which can occur spontaneously or be catalyzed by metal ions or enzymes. RNA hydrolysis can break the phosphodiester bonds between nucleotides, resulting in shorter RNA fragments or mononucleotides. RNA hydrolysis can also affect the bases, leading to deamination, depurination, or ring opening. RNA hydrolysis is a major factor in the degradation and instability of RNA molecules4
- RNA acylation: This is the reaction of RNA with acylating agents, such as anhydrides or acid chlorides, which can attach an acyl group to the 2’-OH group of the ribose sugar. RNA acylation can be used to label and modify RNA molecules for various purposes, such as mapping RNA structure, enhancing RNA stability, or introducing functional groups for further conjugation. RNA acylation is influenced by the steric and inductive effects of the nucleotides and the acylating agents2
- RNA chemical probing: This is the use of chemicals that react with RNAs in a structure-dependent manner. For example, some chemicals can modify or cleave only unpaired or accessible bases, while others can target specific base pairs or motifs. By comparing the reactivity of different regions of an RNA molecule under different conditions, one can infer its secondary and tertiary structure, as well as its interactions with other molecules. RNA chemical probing is a powerful tool for studying the structure and function of RNAs
## RNA Chemical probing

RNA chemical probing uses chemicals that react with RNAs. Importantly, their reactivity depends on local RNA structure e.g. base-pairing or accessibility. Differences in reactivity can therefore serve as a footprint of structure along the sequence. Different reagents react at different positions on the RNA structure, and have different spectra of reactivity.Recent advances allow the simultaneous study of the structure of many RNAs (transcriptome-wide probing) and the direct assay of RNA molecules in their cellular environment (in-cell probing).

Structured RNA is first reacted with the probing reagents for a given incubation time. These reagents would form a covalent adduct on the RNA at the site of reaction. When the RNA is reverse transcribed using a reverse transcriptase into a DNA copy, the DNA generated is truncated at the positions of reaction because the enzyme is blocked by the adducts. The collection of DNA molecules of various truncated lengths therefore informs the frequency of reaction at every base position, which reflects the structure profile along the RNA. This is traditionally assayed by running the DNA on a gel, and the intensity of bands inform the frequency of observing a truncation at each position. Recent approaches use high-throughput sequencing to achieve the same purpose with greater throughput and sensitivity.

The reactivity profile can be used to study the degree of structure at particular positions for specific hypotheses, or used in conjunction with computational algorithms to produce a complete experimentally supported structure model.

Depending on the chemical reagent used, some reagents, e.g. hydroxyl radicals, would cleave the RNA molecule instead. The result in the truncated DNA is the same. Some reagents, e.g. DMS, sometimes do not block the reverse transcriptase, but trigger a mistake at the site in the DNA copy instead. These can be detected when using high-throughput sequencing methods, and is sometimes employed for improved results of probing as mutational profiling (MaP).

Positions on the RNA can be protected from the reagents not only by local structure but also by a binding protein over that position. This has led some work to use chemical probing to also assay protein-binding.

## DMS_MaP and 2A3_MaP chemical mapping experiments

DMS_MaP and 2A3_MaP are two methods for performing chemical mapping experiments on RNA molecules. Chemical mapping is a technique that uses chemicals that react with RNA in a structure-dependent manner, and then measures the reactivity of each nucleotide using high-throughput sequencing. Chemical mapping can reveal information about the secondary and tertiary structure of RNA, as well as its interactions with other molecules.

DMS_MaP is a method that uses dimethyl sulfate (DMS) as the chemical probe. DMS modifies the N1 position of adenine and the N3 position of cytosine, which are usually unpaired or exposed in RNA structures. DMS_MaP uses mutational profiling (MaP) to quantify the DMS modification rates at each nucleotide. MaP is a technique that introduces random mutations during reverse transcription, and then maps the mutations to the original RNA sequence using bioinformatics tools. The mutation rates reflect the reactivity of each nucleotide to DMS, and thus indicate the structural features of RNA12

2A3_MaP is a method that uses 2-aminobenzoyl-3-nitrotyrosine (2A3) as the chemical probe. 2A3 is a fluorescent dye that can be attached to the 2’-OH group of ribose in RNA. 2A3 reacts with guanine and uracil bases, which are usually paired or stacked in RNA structures. 2A3_MaP also uses MaP to quantify the 2A3 modification rates at each nucleotide. The mutation rates reflect the reactivity of each nucleotide to 2A3, and thus indicate the structural features of RNA3

Both DMS_MaP and 2A3_MaP are examples of multidimensional chemical mapping (MCM) methods, which measure how the reactivity of one nucleotide changes in response to modifications at another nucleotide. MCM methods can provide more information about RNA structure than conventional one-dimensional chemical mapping methods, which only measure the reactivity of each nucleotide independently. MCM methods can also capture structural heterogeneity and dynamics of RNA molecules, which are important for their function2


## Problem and solution

The current work the DNABERT from Hudding face is involved to solve the regression problrm. For this pupposes CLS mask emmbeding of the RNA secuences was used as output vector and was passed into regressional head. 

For the sake of saving GPU resourses traing was done using the small chunk of data. 

The MAE error for  this model was: 0.2887
