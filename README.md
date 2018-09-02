# MyNotes

## CGRA Mapping techniques

### Problem Formulation ILP

1. [An Architecture-Agnostic Integer Linear Programming Approach to CGRA Mapping](http://cgra-me.ece.utoronto.ca/downloads/dac2018.pdf) [DAC '18]
2. Mapping Multi-Domain Applications onto Coarse-Grained Reconfigurable Architectures[IEEE Trans. on CAD (2011)]
Support floating point operations in CGRA, ILP formulation and heuristic based mapping method
3. [SPKM : A Novel Graph Drawing based Algorithm for Application Mapping onto Coarse-Grained Reconfigurable Architectures.](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.127.7463&rep=rep1&type=pdf)[DAC 2008]
    - graph mapping based approach
    - formulate  the  application  mapping  problem  onto  CGRA considering the routing PEs, the shared resource constraints and complex PE interconnection
    - develop  an  integer  linear  programming  (ILP)  solution obtain  the  optimal  application  mapping 
    - propose a graph drawing based approach to map applications onto  CGRAs  which  can  map  4.5X  more  randomly  generated application DAGs than previous approach, while using less rows 62% of time, without any mapping time penalty
    - Bench marks : fft,dist1,bdlist2,n_complex_update,hydro,inner, state, laplace, wavelet, prewitt, compress, GSR, average
    - Authors : Jonghee W. Yoon, Aviral Shrivastava, Sanghyun Park, Minwook Ahn,Reiley Jeyapaul, and Yunheung Paek
4.  A Graph Drawing Based Spatial Mapping Algorithm for Coarse-Grained Reconfigurable Architectures.[IEEE Trans. on VLSI(Nov 2009)]
    - model several CGRA details, e.g., irregular CGRA topologies, shared resources and routing PEs in their compiler and develop a graph drawing based approach, Split-Push Kernel Mapping (SPKM), for mapping applications onto CGRAs
    - Bench marks : fft,bdlist2,mpeg2_enc,n_complex_update,inner,iccg, state, laplace, wavelet, prewitt, average
    - Authors: Jonghee W. Yoon, Aviral Shrivastava, Sanghyun Park, Minwook Ahn, and Yunheung Paek
5.  [A General Constraint-centric Scheduling Framework for Spatial Architectures](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.649.1577&rep=rep1&type=pdf) [SIGPLAN(June 2013)]
    - expresses spatial scheduling as a constraint satisfaction problem using Integer Linear Programming (ILP) with 20 constraints
    - Benchmarks : over TRIPS, DySER, and PLUG architectures: ammp_1/2,art_1/2/3, bzip_1, equake_1,gzip,martiz_1, parser_1,add,fft,mm,stencil,spmv,nnw,kmeans,needle,ethernet,ethane,ipv4,seattle 

### Graph based

1.  [Modulo Graph Embedding: Mapping Applications onto Coarse-Grained Reconfigurable Architectures](http://cccp.eecs.umich.edu/papers/parkhc-cases06.pdf) [IEEE/ACM CASES 2006]
  - introduces a software pipelining technique for mapping loop bodies onto CGRAs, referred to as modulo graph embedding
. - Benchmarks : blowfish, channel, dct, fft, fir, fsed, sharp, sobel, viterbi
2. [ Graph Minor Approach for Application Mapping on CGRAs] (https://www.comp.nus.edu.sg/~tulika/TRB6-13.pdf) [ ACM TRETS 7]

3.  A Graph-Based Spatial Mapping Algorithm for a Coarse Grained Reconfigurable Architecture Template[Inf. in Ctrl., Auto.and Robo 2012] 


### Simulated Annealing

1.  [Optimization by Simulated Annealing S. Kirkpatrick, C. D. Gelatt, and M. P. Vecchi](https://pdfs.semanticscholar.org/beb2/1ee4a3721484b5d2c7ad04e6babd8d67af1d.pdf)[1983]

1. [DRESC: A Retargetable Compiler for Coarse-grained Reconfigurable Architectures](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=EF884B4BE279B4BF58B595B0736F3F40?doi=10.1.1.5.6251&rep=rep1&type=pdf) [FPL 2002]
  - simulated annealing strategy is used to dEcide whether to accept the new placement or not
  - benchmarks: idct,fft, corr, latanal
2. [SPR: An Architecture-adaptive CGRA Mapping Tool](https://www2.ee.washington.edu/faculty/hauck/publications/SPR.pdf) [ACM FPGA 2009]
  - SPR’s placer uses Simulated Annealing 
  - Benchmarks: Motion Estimation,Smith-Waterman,2-D Convolution,Matched Filter,Matrix Multiply,CORDIC,K-Means Clust.,Blocked FIR
  
 
  

### Modulo Scheduling
1. [DRESC: A Retargetable Compiler for Coarse-grained Reconfigurable Architectures](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=EF884B4BE279B4BF58B595B0736F3F40?doi=10.1.1.5.6251&rep=rep1&type=pdf) [FPL 2002]
2. [Edge-Centric Modulo Scheduling for Coarse-Grained Reconfigurable Architectures](https://courses.cs.washington.edu/courses/cse591n/09sp/Papers/Park2008ecm.pdf)[IEEE/ACM PACT 2008]
  - take an edge-centric approach to modulo scheduling that foc uses on the routing problem as its primary objective. With edge-centric modulo scheduling (EMS), placement is a by-product of the routingprocess, and the schedule is developed by routing each edge in thedataflow graph.

### Heuristic based

### Boolean satisfiability based
1.[SAT-based compilation to a non-vonNeumann processor](http://delivery.acm.org/10.1145/3200000/3199790/p675-chaudhuri.pdf?ip=137.132.65.142&id=3199790&acc=ACTIVE%20SERVICE&key=FF6731C4D3E3CFFF%2EBB5EB8D2067C1662%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1535900877_1ef0d715ffaa37fa675b75188e8336af)[ICCAD 2017]

## CGRA memory mapping related papers

1. Conflict free loop mapping for CGRA with multibank memory [Shouyi Yin,Shaojun Wei(TPDS'17)]
2. Efficient memory partitioning for parallel data access in multidimensional arrays[Chenyue Meng, Shaojun Wei(DAC'15)]
    - Mapping data elements in multidimensional array to new position in memory banks to realize multiple simultaneous accesses.
    - Find linear transformation vector(α) such that each data element in given pattern is assigned with a distinctive number(memory bank number)after the transformation.
3. Efficient Memory Partitioning for Parallel Data Access via data reuse [FPGA'16]

## Notes

1. The problem of mapping an application onto a CGRA to minimize the number of resources giving best performance has been shown to be NP-complete - C. O. Shields, Jr., “Area efficient layouts of binary trees in grids,” Ph.D.dissertation, Dept. Comput. Sci., Univ. Texas, Dallas, 2001.


