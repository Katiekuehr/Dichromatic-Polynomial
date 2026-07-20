# The Dichromatic Polynomial

The chromatic polynomial is well-studied in literature; it is a polynomial in $x$ and encodes the number of ways an undirected graph can be colored with $x$ colors where no two adjacent vertices share the same color. The dichromatic polynomial is an analogue for directed graphs (digraphs) and builds on the acyclic coloring of a digraph introduced by Neumann-Lara (1982), where an acyclic coloring is a digraph coloring such that no monochromatic cycles exist in the graph. Harutyunyan (2012) showed that, given a number of available colors $x$, the nummber of acyclic colorings of a graph can be encoded into a polynomial in $x$. The code provided here allows to calculate the dichromatic polynomial of an arbitrary digraph using contraction and deletion relations as introduced in Moreno et al (2021).

## How to use
You can skip the #code section in the notebook or the python file and skip to #TO USE. 

### Input
Input the digraph as 
- Adjacency matrix format $(A_{ij} = 1$ if $ij$ is an arc, $0$ else): `dichromatic_poly(edge_matrix).as_expr()`
- .d6 format (see Brendan McKay's library ![here](https://users.cecs.anu.edu.au/~bdm/data/digraphs.html) ) as ``dichromatic_poly(parse_d6("&EIC`OHa")).as_expr()``
- Upper triangular form (tournaments only) (0-1 string of the form $"v_1v_2 \ldots v_1v_n v_2v_3 \ldots v_2v_n \ldots v_{n-1}v_n"$ where an entry is $1$ if the arc $v_iv_j$ exists and 0 if the arc $v_jv_i$ exists): `dichromatic_poly(parse_tournament('011000')).as_expr())`

### Output:
- Dichromatic Polynomial
- Dichromatic Number
- d6 string
- Graph visual

### References
González-Moreno, D., Hernández-Ortiz, R., Llano, B., & Olsen, M. (2022). The Dichromatic Polynomial of a Digraph. Graphs and Combinatorics, 38(3), 85. https://doi.org/10.1007/s00373-022-02484-0 \
Harutyunyan, A. (2012). Brooks-Type results for colorings of digraphs [PhD].\
Neumann-Lara, V. (1982). The dichromatic number of a digraph. Journal of Combinatorial Theory, Series B, 33(3), 265–270. https://doi.org/10.1016/0095-8956(82)90046-6
