# Matrix Market test data

Nine sparse matrices that ArrayFire's sparse tests read, from the
[SuiteSparse Matrix Collection](https://sparse.tamu.edu), formerly the University of Florida
Sparse Matrix Collection.

## License

The matrices are licensed under CC BY 4.0
(https://creativecommons.org/licenses/by/4.0/) by the SuiteSparse Matrix Collection. The BSD
license of this repository (`LICENSE`) does not apply to this folder.

## The files are unchanged

Each file is the collection's Matrix Market file, byte for byte, with its metadata header
(name, id, date, author, editor, kind) intact. Only each matrix's main `<name>.mtx` is
included: the collection's archives also hold extra vectors for some matrices, which the tests
don't use.

## Citation

As the collection asks, please cite it when you use these matrices:

- Timothy A. Davis and Yifan Hu. 2011. The University of Florida Sparse Matrix Collection. ACM
  Transactions on Mathematical Software 38, 1, Article 1 (December 2011), 25 pages.
  https://doi.org/10.1145/2049662.2049663
- Scott P. Kolodziej, Mohsen Aznaveh, Matthew Bullock, Jarrett David, Timothy A. Davis, Matthew
  Henderson, Yifan Hu, and Read Sandstrom. 2019. The SuiteSparse Matrix Collection Website
  Interface. Journal of Open Source Software 4, 35 (March 2019), 1244.
  https://doi.org/10.21105/joss.01244

The header of each file names its own authors and editors.

## The matrices

| Matrix | Collection id | Kind | ArrayFire test |
|---|---|---|---|
| [JGD_Kocay/Trec4](https://sparse.tamu.edu/JGD_Kocay/Trec4) | 2138 | combinatorial problem | `test/matrixmarket.cpp`, `Sparse.FailIntegerMTXRead` |
| [HB/bcsstm02](https://sparse.tamu.edu/HB/bcsstm02) | 57 | structural problem | `test/matrixmarket.cpp`, `Sparse.ReadRealMTXFile` |
| [HB/young4c](https://sparse.tamu.edu/HB/young4c) | 281 | acoustics problem | `test/matrixmarket.cpp`, `Sparse.ReadComplexMTXFile` |
| [LPnetlib/lpi_vol1](https://sparse.tamu.edu/LPnetlib/lpi_vol1) | 730 | linear programming problem | `test/sparse_arith.cpp`, `SparseSparseArith.LinearProgrammingData` |
| [LPnetlib/lpi_qual](https://sparse.tamu.edu/LPnetlib/lpi_qual) | 727 | linear programming problem | `test/sparse_arith.cpp`, `SparseSparseArith.LinearProgrammingData` |
| [Sandia/oscil_dcop_12](https://sparse.tamu.edu/Sandia/oscil_dcop_12) | 1123 | subsequent circuit simulation problem | `test/sparse_arith.cpp`, `SparseSparseArith.SubsequentCircuitSimData` |
| [Sandia/oscil_dcop_42](https://sparse.tamu.edu/Sandia/oscil_dcop_42) | 1153 | subsequent circuit simulation problem | `test/sparse_arith.cpp`, `SparseSparseArith.SubsequentCircuitSimData` |
| [QCD/conf6_0-4x4-20](https://sparse.tamu.edu/QCD/conf6_0-4x4-20) | 1596 | theoretical/quantum chemistry problem | `test/sparse_arith.cpp`, `SparseSparseArith.QuantumChemistryData` |
| [QCD/conf6_0-4x4-30](https://sparse.tamu.edu/QCD/conf6_0-4x4-30) | 1597 | theoretical/quantum chemistry problem | `test/sparse_arith.cpp`, `SparseSparseArith.QuantumChemistryData` |

Each file is at `matrixmarket/<group>/<name>/<name>.mtx`, the layout ArrayFire's tests expect.
