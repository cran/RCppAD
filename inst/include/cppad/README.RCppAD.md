# RCppAD patches on top of CppAD 20260000.0

Applied by `tools/update-cppad.sh` (re-run after each upstream refresh):

1. `configure.hpp` — from `tools/configure.hpp.in` (ColPack/Eigen/ADOLC/IPOPT off).
2. `utility/error_handler.hpp` — `REprintf` + `Rf_error` (no `cerr`/`exit`).
3. `local/var_op/atomic_op.hpp`, `core/ad_pack.hpp`, `core/fun_construct.hpp` —
   `std::cout` → `RCppAD::cppad_trace_stream()`.

Helper: `inst/include/RCppAD/cppad_trace_stream.hpp`.
