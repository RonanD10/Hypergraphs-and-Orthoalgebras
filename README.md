# Hypergraphs-and-Orthoalgebras
A repository of the programs used in my summer project about hypergraphs and orthoalgebras. In particular, the programs are mostly for displaying graphs of certain algebras, and for checking validity of candidate orthoalgebras.

It is necessary to have Graphviz installed in order to display the graphs. Info on Graphviz can be found here: https://graphviz.readthedocs.io/en/stable/manual.html.

# Table of Contents
- [Displaying Hasse diagrams](#displaying-hasse-diagrams)
  * [Powesets - ps_hasse](#powersets-ps_hasse)
  * [Orthoalgebras (and Boolean algebras) - oa_hasse](#orthoalgebras-(and-boolean-algebras))
- [Checking Orthoalgebras - oa_check](#checking-orthoalgebras)
- [Generating Orthoalgebras - oa_gen](#generating-orthoalgebras) 
- [Displaying Hypergraphs hg_show] (#displaying-hypergraphs)


## Displaying Hasse diagrams

### Powersets - ps_hasse
This program allows you to generate the Hasse diagram of a powerset. For example:

```python 

list = powerset([1,2]) # returns [[1,2],[1],[2],[]]
ps_hasse(list, 2) # returns Hasse diagram of list
```
Returns 

![alt text](https://github.com/RonanD10/Hypergraphs-and-Orthoalgebras/blob/master/example1.png)

### Orthoalgebras (and Boolean Algebras) - oa_hasse
This program allows you to generate the Hasse diagram of an orthoalgebra (or a Boolean algebras). For example:

![alt text](https://github.com/RonanD10/Hypergraphs-and-Orthoalgebras/blob/master/example2.png)

A note about the datatypes `NEG`, `COMP`, and `OPLUS`. Suppose the orthoalgebra in question contains <img src="https://render.githubusercontent.com/render/math?math=n"> elements. 
- `NEG` is an <img src="https://render.githubusercontent.com/render/math?math=n">-element list such that it contains only the elements <img src="https://render.githubusercontent.com/render/math?math=0,1,2,...,n-1">. 
- `COMP` is a symmetric <img src="https://render.githubusercontent.com/render/math?math=n \time n"> matrix with each element either <img src="https://render.githubusercontent.com/render/math?math=0"> or <img src="https://render.githubusercontent.com/render/math?math=1">. If `COMP[i,j] == 1`, then elements <img src="https://render.githubusercontent.com/render/math?math=i"> and <img src="https://render.githubusercontent.com/render/math?math=j"> are compatible.
- `OPLUS` is a symmetric <img src="https://render.githubusercontent.com/render/math?math=n \times n"> matrix with entries satisfying
  * if `COMP[i,j] == 1`, then `OPLUS[i,j]` <img src="https://render.githubusercontent.com/render/math?math={= i \oplus j}">, where <img src="https://render.githubusercontent.com/render/math?math={\oplus}"> is the partial binary operation in the orthoalgebra
  * if `COMP[i,j] == 0`, then `OPLUS[i,j] = -1`, i.e. an element not in the orthoalgebra. 


## Checking Orthoalgebras - oa_check
This program allows you to check if an algebra (in the datatype defined above) is an orthoalgebra (or a Boolean algebra) or not. It does this by checking the axioms in the definition an orthoalgebra.

Examples:

A valid orthoalgebra.

![alt text](https://github.com/RonanD10/Hypergraphs-and-Orthoalgebras/blob/master/example3.png)


An invalid orthoalgebra.

![alt text](https://github.com/RonanD10/Hypergraphs-and-Orthoalgebras/blob/master/example4.png)

## Generating Orthoalgebras - oa_gen



## Displaying Hypergraphs - oa_show



