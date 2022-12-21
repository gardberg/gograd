## :fish_cake: gograd :fish_cake:

A simple scalar automatic differentiation engine in Go!

Implements basic scalar operations and backpropagation.

Inspired (entierly copied) from Karpathy's [micrograd](https://github.com/karpathy/micrograd).

---

### Log

Created new go module with 'go mod init gograd'

cmd+k, shift+v to preview a .gv file.

### Todo

- [x] Basic scalar operations
- [x] Gradient tracking
- [x] Backpropagation
- [x] Topological sort
- [x] Add DAG visualization
  - [x] Add operator nodes
- [ ] Create a proper directory & package structure
- [ ] Add tests comparing results with an established autograd engine
  - [x] Add basic non-comparative tests
- [ ] Add tests as GitHub workflows (?)
- [ ] Investigare implementation of general `Pow` operation
- [ ] Add activation function(s)
- [ ] Add example of NN training
- [ ] Add overhead to enable import as a Go package

---

### Notes

When we call `a.Backward()` on a `Value` struct, we want to calculate the derivative of `a` with respect to itself and all of its children, i.e. all `Values` (nodes) used in calculating `a`.