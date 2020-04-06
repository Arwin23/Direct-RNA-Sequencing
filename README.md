# **Direct-RNA-Sequencing**

### Description
This document repository is meant to serve as the start of collection of ideas, information, documentation, protocols and other resources for direct-rna-sequencing of viral samples using the ONT platform.


##### Open Questions
  - What's the expected viral load from an infected persons nasal/oral sample?
    - See [SARS-CoV-2 (COVID-19) by the numbers](https://elifesciences.org/articles/57309)
     - They say that the max observed values following diagnosis are:
        - Nasopharynx, 10^6 to 10^9 RNAs per swab
        - Throat, 10^4 to 10^8 RNAs per swab
        - Stool, 10^4 to 10^8 RNAs per gram
        - Sputum, 10^6 to 10^11 RNAs per mL

  -  Its seems that cultivation in a host is necessary to obtain a virus from the patient sample that is being investigated. What if viral particles can be isolated from patient sample based on the physical characteristics of virions, so that the virome can be obtained from the enriched viral particles?
    - See [Labratory Preocedures to generate viral metagenomes](https://www.nature.com/articles/nprot.2009.10) 
    
    > They say "This protocol is a description of the processes we have successfully used to: (i) concentrate viral particles from various types of samples, (ii) eliminate contaminating cells and free nucleic acids and (iii) extract, amplify and purify viral nucleic acids. Overall, a sample can be processed to isolate viral nucleic acids suitable for high-throughput sequencing in ∼1 week."





### Workflow

#### 1. RNA Extraction from Respiratory Specimens

##### Overview of Methods
- RNA Extraction suggested by CDC:
> Performance of the CDC 2019-nCoV Real-Time RT-PCR Diagnostic Panel is dependent upon the amount and quality of template RNA purified from human specimens. The following commercially available RNA extraction kits and procedures have been qualified and validated for recovery and purity of RNA for use with the panel:
    - Qiagen QIAamp® DSP Viral RNA Mini Kit or QIAamp® Viral RNA Mini Kit
    - Qiagen EZ1 Advanced XL
    - Qiagen EZ1 DSP Virus Kit and Buffer AVL (supplied separately) for offboard lysis
    - Qiagen EZ1 Virus Mini Kit v2.0 and Buffer AVL (supplied separately) for offboard lysis
    - QIAGEN QIAcube
    - Roche MagNA Pure LC
    - Roche MagNA Pure Total Nucleic Acid Kit
    - Roche MagNA Pure Compact
    - bioMérieux NucliSENS® easyMAG® Instrument
    - bioMérieux EMAG® Instrument
    
- Other kits:
    - [BioVision](https://www.biovision.com/documentation/datasheets/K1462.pdf) 
    - [ZymoResearch] 
    - [MyLab]
      
- RNA Extraction used by Labs that did DRS with ONT. Viral samples were from cell culture.
    - [Peter Doherty Lab](https://github.com/helix-phoenix/SARS-CoV-2_Sequencing/tree/master/protocols/ONT-Native_RNA) 
      > Nucleic acids were prepared from infected cellular material, following inactivation with linear acrylamide and ethanol. RNA was extracted from a modest cell pellet (~200mg) using manually prepared wide-bore pipette tips and minimal steps to maintain RNA length for long read sequencing, and a QIAamp Viral RNA Mini Kit (Qiagen, Hilden, Germany). Carrier RNA was not added to Buffer AVL, with 1% linear acrylamide (Life Technologies, Carlsbad, CA, USA) added instead. Wash buffer AW1 was omitted from the purification stage, with RNA eluted in 50 μl of nuclease free water, followed by DNase treatment with Turbo DNase (Thermo Fisher Scientific, Waltham, MA, USA) 37°C for 30 min. RNA was cleaned and concentrated to 10 μl using the RNA Clean & Concentrator-5 kit (Zymo Research, Irvine, CA, USA), as per manufacturer’s instructions
    - [Narry Kim's Lab](https://www.biorxiv.org/content/10.1101/2020.03.12.988865v2.full.pdf)
      > Total RNA from SARS-CoV-2-infected Vero cell was 314 extracted by using TRIzol (Invitrogen) followed by DNaseI (Takara) treatment. 
    
 - What Else?  
 
 - Twist SARS-CoV-2 RNA controls
    - The viral genome of 30,000 basepairs is provided in synthetic form.
    - Synthetic Viral Genome provided as six RNA fragments, each 5kb long.
    - RNA fragments are pooled in a 100uL solution 
    - The no. of fragments available are 1 Million per uL or a total of 100 Million per 100uL pool
    - Total fragments in 100uL pool = 0.16 fmol 
    - Total amount of RNA in 100uL pool = 1.7 ng 
    - All fragments in the pool are expected to be equimolar ratio and ~ weigh the same: 
        - so 0.026 fmol per 5kb RNA fragment
        - 0.28 ng per 5kb RNA fragment
        


#### 2. Barcoding 

Multiplexing samples lets you get more out of each flowcell. ONT shop has 96 barcode ligation kit that is suitable for DNA

  - Barcoding the cDNA 
    - [CDC Protocol](https://github.com/helix-phoenix/SARS-CoV-2_Sequencing/blob/master/protocols/CDC-Comprehensive/CDC_SARS-CoV-2_Sequencing_200325-2.pdf)
    
    - Salis Lab 
      - [A Massively Parallel COVID-19 Diagnostic Assay for Simultaneous Testing of 19200 Patient Samples](https://t.co/x2c2v8uvw3?amp=1) 
      - [Primers & Spike-in Controls](https://t.co/9cWzQrfz5P?amp=1)
      
  - Barcoding the RNA (is this possible?)
 
#### 3. Adaptor Ligation
#### 4. Sequencing
##### Overview of Approaches
   - Direct RNA Sequencing of poly-A tailed RNA specimens in sample [example protocol](https://github.com/helix-phoenix/SARS-CoV-2_Sequencing/tree/master/protocols/ONT-Native_RNA)
   - ARCTIC [Protocol](https://artic.network/ncov-2019)
   - Direct RNA Sequencing of all RNA specimens in sample with 5' helicase-adaptor ligation ??
   - ARCTIC Protocol on >5kb length cDNA ??

#### 5. Bioinformatics
  
 
  








--------------------------------------










### References

The following ONT sequencing protocols, checklists and job-aids are primarily designed for the Oxford Nanopore [MinION](https://nanoporetech.com/products/minion), and have been kindly shared by research groups throughout the world (please see individual protocols for attribution and citing purposes). Even so, most of these protocols should scale to larger ONT instruments without significant modifications.

#### CDC NCIRD/DVD ONT Sequencing Protocol
This protocol was developed, tuned and validated by the Viral Discovery laboratory at CDC/NCIRD, where it was used to generate the first 16 SARS-CoV-2 genome sequences from the United States. In practice, it has been used for situations with a relatively low or predictable volume of samples, and is often used in conjunction with Sanger-based tiling to resolve any potential sequencing or assembly issues.
- [Singleplex and Multiplex Protocols for ONT/Illumina](./protocols/CDC-Comprehensive)

#### ARTIC Network nCoV-2019 Sequencing [Protocol](https://artic.network/ncov-2019)
This protocol was developed and released by the fine folks at [ARTIC Network](https://artic.network), and was subsequently refined based on comments from [Itokawa et al](https://www.biorxiv.org/content/10.1101/2020.03.10.985150v1.full.pdf), which identified potential issues and proposed an alternate L18 primer.

- [Sequencing protocol](https://www.protocols.io/view/ncov-2019-sequencing-protocol-bbmuik6w) / [Single sample sequencing protocol](https://www.protocols.io/view/ncov-2019-sequencing-protocol-single-sample-bdbfi2jn)

- [Stepwise simplified protocol from ONT*](./protocols/ONT-COVID-19_Tiling)

- Primer schemes: [V1](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V1) / [V2](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V2) [(ref)](https://www.biorxiv.org/content/10.1101/2020.03.10.985150v1.full.pdf) / [V3](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V3)

- [ARTIC on Illumina - Complete Walk-through - Grubaugh/Andersen/Loman labs](https://docs.google.com/document/d/1PilT4w5jHO-ROsE8TL5WBGa0wSCdTHAsNl1LIOYiTgk/mobilebasic)

- Integrated bioinformatics (RAMPART) - documentation below under bioinformatics methods.

#### Doherty Institute VIDRL Sequencing Protocols
The Victorian Infectious Diseases Reference Laboratory ([VIDRL](https://www.vidrl.org.au/)) at the [Peter Doherty Institute for Infection and Immunity](https://www.doherty.edu.au/) released two protocols for the ONT MinION, which they successfully used to sequence early Australian SARS-CoV-2 samples.
- [Native RNA Sequencing Protocol](./protocols/ONT-Native_RNA) [(ref)](https://www.biorxiv.org/content/10.1101/2020.03.05.976167v1.full.pdf)

- [SISPA Sequencing Protocol](./protocols/ONT-SISPA)


##### Challenges in Extraction & Scaling: [Source](https://docs.google.com/document/d/1ra3L84yKwz3TU1xdRgDMQU3A0ZCGZmljeyqCI179KtQ/edit)
- Performing sequencing requires genomic material to be extracted from a physical sputum sample in a multi-step process where reagents and liquids are mixed, transferred into a thermocycler, and then processed for readouts. 

- Given the volume of tests that need to be done, this process must be automated. Robotic liquid handling systems are important for scaleup, but are typically very expensive and out of reach for most labs. 

- The key issues being faced in this category include:
  - Lack of extraction capability and instrumentation bottlenecks
  - Lack of trained staff, skilled technicians, and training capability for existing and new tests, especially for high-throughput platforms which have complex protocols
  - Lack of large-scale high complexity physical testing capacity (facilities, automation platforms/robotics) in public service (much of the installed base is operating in commercial settings)
  - Supply chain limitations on approved clinically validated viral RNA kits also require broadening the approved viral RNA methodologies and kits. For example, on March 10, Politico reported that all validated viral RNA extraction kits (i.e. the ones from Qiagen) were on backorder.
  - Multiple labs have reported successful changes to alternative unapproved solutions. Current short list of reported alternates includes (but additional validation of quality required):
    - OmegaBiotek Mag-Bind Viral RNA 96 kits (and amenable to liquid handling automation)
    - Switching to vet rated Qiagen kits (limited stock available)
    - Ambion vRNA kits (limited EU stock)
    - Zymo Research Direct-zol + Trizol inactivation (limited EU availability, available in USA)
    - Analytic Jena Innuprep kits + FeliX robot for automated 96 well extractions



