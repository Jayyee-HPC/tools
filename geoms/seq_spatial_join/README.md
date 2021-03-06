# geospatial_join_work_stealing

Repository for geo-spatial join using work stealing.

Version: 0.01

 1. What is geo-spatial join?
 2. What is work stealing?
 3. Directory Structure.
 4. Prerequisties.
 5. Installation.
 6. External Links.

## 1. What is geo-spatial join? ##

[ParADP](https://www.cs.mu.edu/~satish/ParADP_for_loadbalancing_in_spatial_join.pdf)

>Spatial join involves two spatial layers, namely, _R_ and _S_. Performing spatial join queries with predicate _Intersects_, _Contains_, _Overlap_, etc, on _R_ and _S_ generates a collection of pairs _(r,s)_, where _r_ in _R_, _s_ in _S_ that satisfy the join predicate. For example, "find all roads that cross a river" is an _Intersects_ query. 

>A spatial join can be performed in two phases: 1) filter phase and 2) refinement phase. In the filter phase, the minimum bounding rectangles (MBR) of geometries are utilized to generate a collection of candidate pairs where each pair consists of cross-layer geometries whose MBRs have spatial overlap. These candidate pairs are further refined in the second phase using the actual geometric representations. 

## 2. What is work stealing? ##

_Work Stealing_ is a popular approach for dynamic load balancing in distributed systems, in which an idle processor steals computational threads or jobs from other processors.

To efficiently compute on a multiple instruction, multiple data (MIMD) style parallel computer, a scheduling algorithm must ensure that enough concurrent threads are alive to keep all processors busy while the consumption of system resources (mainly memory) are not overdrawn. To reduce communication, the scheduling algorithm should try to maintain related threads on the same processor. 

## 3. Directory Structure. ##

[inclue](https://github.com/Jayyee-HPC/geospatial_join_work_stealing/tree/main/include)
Headers

[src](https://github.com/Jayyee-HPC/geospatial_join_work_stealing/tree/main/src)
Source files

[tests](https://github.com/Jayyee-HPC/geospatial_join_work_stealing/tree/main/tests)
Test files

Object files will be in bin folder. 

_makefile_ and executable _prog_ are in 
[main dir](https://github.com/Jayyee-HPC/geospatial_join_work_stealing/tree/main).

## 4. Prerequisties. ##

GEOS 3.8.x 
[GEOS](https://github.com/libgeos/geos/tree/3.8)

g++ 7.1.0 or later (support for c++17 needed).

## 5. Installation. ##

_make_ if prerequisties are met. 

_prog_ is the excutable file.

```
./prog /path/to/file
```

## 6 Exteranal Links. ##

[Homepage of our lab](https://www.cs.mu.edu/~satish/)

[Work stealing queue](https://github.com/taskflow/work-stealing-queue)