# MyNotes

## CGRA Mapping(Scheduling, Placing and routing) techniques

### Problem Formulation - ILP

1. [An Architecture-Agnostic Integer Linear Programming Approach to CGRA Mapping](http://cgra-me.ece.utoronto.ca/downloads/dac2018.pdf) [DAC '18] 
2. Mapping Multi-Domain Applications onto Coarse-Grained Reconfigurable Architectures[IEEE Trans. on CAD (2011)] - local link (file:///D:/research/Papers/lee2011.pdf)
    - Support floating point operations in CGRA, 
    - ILP problem formulation and heuristic based mapping method
      
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
.   - Benchmarks : blowfish, channel, dct, fft, fir, fsed, sharp, sobel, viterbi
2. [Graph Minor Approach for Application Mapping on CGRAs***] (https://www.comp.nus.edu.sg/~tulika/TRB6-13.pdf) [ ACM TRETS 7]

3.  A Graph-Based Spatial Mapping Algorithm for a Coarse Grained Reconfigurable Architecture Template[Inf. in Ctrl., Auto.and Robo 2012] 


### Simulated Annealing

1.  [Optimization by Simulated Annealing S. Kirkpatrick, C. D. Gelatt, and M. P. Vecchi](https://pdfs.semanticscholar.org/beb2/1ee4a3721484b5d2c7ad04e6babd8d67af1d.pdf)[1983]

1. [DRESC: A Retargetable Compiler for Coarse-grained Reconfigurable Architectures***](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=EF884B4BE279B4BF58B595B0736F3F40?doi=10.1.1.5.6251&rep=rep1&type=pdf) [FPL 2002]
    - simulated annealing strategy is used to decide whether to accept the new placement or not
     - benchmarks: idct,fft, corr, latanal
2. [SPR: An Architecture-adaptive CGRA Mapping Tool](https://www2.ee.washington.edu/faculty/hauck/publications/SPR.pdf) [ACM FPGA 2009]
     - SPR’s placer uses Simulated Annealing 
    - Benchmarks: Motion Estimation,Smith-Waterman,2-D Convolution,Matched Filter,Matrix Multiply,CORDIC,K-Means Clust.,Blocked FIR
  
 
  

### Modulo Scheduling
1. [DRESC: A Retargetable Compiler for Coarse-grained Reconfigurable Architectures***](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=EF884B4BE279B4BF58B595B0736F3F40?doi=10.1.1.5.6251&rep=rep1&type=pdf) [FPL 2002]
2. [Edge-Centric Modulo Scheduling for Coarse-Grained Reconfigurable Architectures***](https://courses.cs.washington.edu/courses/cse591n/09sp/Papers/Park2008ecm.pdf)[IEEE/ACM PACT 2008]
     - take an edge-centric approach to modulo scheduling that foc uses on the routing problem as its primary objective. With edge-centric modulo scheduling (EMS), placement is a by-product of the routingprocess, and the schedule is developed by routing each edge in thedataflow graph.

### Heuristic based

### Boolean satisfiability based
1.[SAT-based compilation to a non-vonNeumann processor](https://dl.acm.org/citation.cfm?id=3199790)[ICCAD 2017]

## CGRA memory mapping related papers

1. Conflict free loop mapping for CGRA with multibank memory [Shouyi Yin,Shaojun Wei(TPDS'17)]
2. Efficient memory partitioning for parallel data access in multidimensional arrays[Chenyue Meng, Shaojun Wei(DAC'15)]
     - Mapping data elements in multidimensional array to new position in memory banks to realize multiple simultaneous accesses.
     - Find linear transformation vector(α) such that each data element in given pattern is assigned with a distinctive number(memory bank number)after the transformation.
3. Efficient Memory Partitioning for Parallel Data Access via data reuse [FPGA'16]
4.Memory access optimization in compilation for coarse-grained reconfigurable architectures, TODAES 2011
5.Memory-Aware Loop Mapping on Coarse-Grained Reconfigurable Architectures, TVLSI 2016
6. An Efficient Memory Organization for High-ILP Inner Modem Baseband SDR Processors, 2009
7.Optimizing the data placement and transformation for multi-bank CGRA computing system, DATE 2018

## Reconfigurable Architectures

1. Xputer (1991), PADDI (1992), PADDI-2 (1993), rDPA/KressArray (1995), Colt (1996),  MATRIX (1996), RaPID (1996), Garp (1997), RAW (1997),PipeRench (1998), REMARC (1998), CHESS (1999), Pleiades (2000), Chameleon/Montium (2000), DReaM (2000), [MorphoSys (2000)](https://ieeexplore.ieee.org/document/859540/), Chimaera (2000), SmartMemories (2000), Imagine (2002), [ADRES (2003)](https://courses.cs.washington.edu/courses/cse591n/06au/papers/fpl_03_mei.pdf), [DART (2003)](https://pdfs.semanticscholar.org/2178/c299bcf8f45660397b0ee70792f5bb027c04.pdf),[ACT XPP (2003)](https://slideheaven.com/pact-xppa-self-reconfigurable-data-processing-architecture.html), [WaveScalar (2003)](https://courses.cs.washington.edu/courses/cse471/07sp/readings/WaveScalarArch.pdf), [TRIPS (2004)](https://www.cs.utexas.edu/ftp/dburger/papers/ieee_micro04_itdlp.pdf), [Kim(2004)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.455.4917&rep=rep1&type=pdf),  [STA (2004)](https://pdfs.semanticscholar.org/7407/43d768d1b438820eae1023f36b9745b81271.pdf),  [Galanis(2005)](https://pdfs.semanticscholar.org/4225/a8c3c85a04f08fdeaa04d93f24696ea4a354.pdf),  [Astra (2006)](https://ieeexplore.ieee.org/document/4101073/),[CRC (2007)](https://pdfs.semanticscholar.org/78c0/79e9bdd7d99be0c92f97e96cdfbb5667c65b.pdf),  TCPA (2009),  [PPA (2009)](http://delivery.acm.org/10.1145/1670000/1669160/p370-park.pdf?ip=137.132.65.142&id=1669160&acc=ACTIVE%20SERVICE&key=FF6731C4D3E3CFFF%2EBB5EB8D2067C1662%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1535903413_2fdb6ad6b0cf8b4616657934bfe2a289),  [CGRA express (2009)](http://delivery.acm.org/10.1145/1630000/1629433/p271-park.pdf?ip=137.132.65.142&id=1629433&acc=ACTIVE%20SERVICE&key=FF6731C4D3E3CFFF%2EBB5EB8D2067C1662%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1535903279_0a875238683e127dbbe7845573102a64),  [EGRA (2011)](https://ieeexplore.ieee.org/document/5439942/),  [DySER (2012)](https://ieeexplore.ieee.org/document/6235947/),  [FPCA (2014)](https://ieeexplore.ieee.org/document/6861574/),[HARTMP (2016)](http://delivery.acm.org/10.1145/2980000/2972181/p1598-souza.pdf?ip=137.132.65.142&id=2972181&acc=ACTIVE%20SERVICE&key=FF6731C4D3E3CFFF%2EBB5EB8D2067C1662%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1535902924_3ee2ea83d2745a4657db287dcf3e5c74)
## Notes

1. The problem of mapping an application onto a CGRA to minimize the number of resources giving best performance has been shown to be NP-complete - C. O. Shields, Jr., “Area efficient layouts of binary trees in grids,” Ph.D.dissertation, Dept. Comput. Sci., Univ. Texas, Dallas, 2001.

## Building ccf
1. Error
In member function ‘void CGRA::calcRFConfig()’:
../src/CGRA.cpp:113:55: error: ‘log’ was not declared in this scope
           rfConfig[i*SizeY + j] = pow(2, ceil(log(diff)/log(2)));
                                                       ^
../src/CGRA.cpp:113:63: error: ‘ceil’ was not declared in this scope
           rfConfig[i*SizeY + j] = pow(2, ceil(log(diff)/log(2)));
                                                               ^
../src/CGRA.cpp:113:64: error: ‘pow’ was not declared in this scope
           rfConfig[i*SizeY + j] = pow(2, ceil(log(diff)/log(2)));

added #include <math.h> tp CGRA.cpp

2.Error:
build/ARM/proto/packet.pb.h:364:6: error: "PROTOBUF_INLINE_NOT_IN_HEADERS" is not defined [-Werror=undef]
 #if !PROTOBUF_INLINE_NOT_IN_HEADERS
Fix:
https://www.mail-archive.com/gem5-dev@gem5.org/msg21326.html
http://reviews.gem5.org/r/3779/diff/1/#1

## Benchmarks

1. HLS

Add directive PIPELINE to for loop
give input and output arrays as arguments in function, dont use pointers
Get power - Use HLS verilog sources + tcl script(HLS will generate tcl script to generate necessary IPs, run the tcl script in vivado tcl console to generate ips) to synthesize design in vivado.

2. Odroid A7/A15

ssh odroid@10.42.0.32
pw: odroid


Add following .h file to C file 
#include "../enable_arm_pmu-master/armpmu_lib.h"

rdstc() function will return current cycle count

build executable with -lm(to support math.h)

go to enable_arm_pmu-master
run sudo ./load_module script to enable necessary registers

run the executable with 
taskset -c 0/1/2/3 for arm cortex7
taskset -c 4/5/6/7 for arm cortex15





