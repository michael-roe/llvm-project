add_mlir_dialect_library(MLIRStandardOps
  IR/Ops.cpp
  EDSC/Builders.cpp
  EDSC/Intrinsics.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/StandardOps

  DEPENDS
  MLIRCallOpInterfacesIncGen
  MLIRControlFlowInterfacesIncGen
  MLIRStandardOpsIncGen
  )
target_link_libraries(MLIRStandardOps
  PUBLIC
  MLIRControlFlowAnalysis
  MLIREDSC
  MLIRIR
  LLVMSupport
  )
