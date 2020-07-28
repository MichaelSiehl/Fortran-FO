# Fortran-FO
Keywords: Fortran 2018, Coarray Fortran, Fragmented Objects (FO), distributed objects, parallel programming

# Introduction
The intention here is to give a first brief overview about using Fortran (since the Fortran 2018 ISO standard) for applying and extending the Fragmented Objects model, which originated in the late 1980’s and early 1990’s. <br />
To get started with the basic ideas behind the Fragmented Objects (FO) model, you may start reading <br />
*‘Makpangou, Mesaac & Gourhant, Yvon & Narzul, Jean-pierre. (1998). Fragmented Objects for Distributed Abstractions’*. <br />
See also the Wikipedia article here: <br />
https://en.wikipedia.org/wiki/Fragmented_object <br />

# Motivation
Chances are that we are already approaching a new era of computers and computing in general: The introduction of *Explicit Data Graph Execution (EDGE)* computers: <br />
https://en.wikipedia.org/wiki/Explicit_data_graph_execution.<br />
<br />
So far, we can already review the first steps in hardware development:
1. Starting with the *University of Texas at Austin’s TRIPS* prototype processor: <br />
https://en.wikipedia.org/wiki/TRIPS_architecture
2. Followed by the experimental *Microsoft/Qualcomm E2* processor:<br />
https://www.theregister.com/2018/06/18/microsoft_e2_edge_windows_10/
3. and finally approaching *Intel’s Configurable Spatial Accelerator (CSA)* for dataflow graph execution: <br />
https://www.nextplatform.com/2018/08/30/intels-exascale-dataflow-engine-drops-x86-and-von-neuman/ <br />
https://patentscope.wipo.int/search/en/detail.jsf;jsessionid=ED24F9F36DA2A174901203FAAE3563CA.wapp2nB?docId=US222845669&recNum=614&office=&queryString=&prevFilter=&sortOption=Pub+Date+Desc&maxRec=69883930 <br />
<br />
One of the main features behind EDGE is to group a number of individual instructions into an entity that they call a ‘hyperblock’. These hyperblocks are then intended to execute in parallel.<br />
<br />
Thus, my basic motivation for applying a Fragmented Objects model with Fortran is to support the forming of hyperblocks with upcoming EDGE compilers: Intel is currently porting it’s ifort compiler to LLVM (http://lists.flang-compiler.org/pipermail/flang-dev_lists.flang-compiler.org/2019-May/000233.html), to me a first indication that the compiler may become an EDGE compiler in the near future.<br />
<br />
Nevertheless, while fragmented objects (FO) seem to be a promising candidate for a possible future of computing and programming for an approaching EDGE era, from a today’s Fortran 2018 view, the FO model is only very basically described and defined so far. Thus, I will also need to further refine the Fragmented Objects model here, to met with the already extended possibilities of Fortran 2018.<br />
