add_mlir_dialect_library(MLIRTensor
  TensorDialect.cpp
  TensorOps.cpp

  ADDITIONAL_HEADER_DIRS
  ${PROJECT_SOURCE_DIR}/include/mlir/Dialect/Tensor

  DEPENDS
  MLIRTensorOpsIncGen
  MLIRTensorAttrDefsIncGen

  LINK_COMPONENTS
  Core

  LINK_LIBS PUBLIC
  MLIRCastInterfaces
  MLIRIR
  MLIRSideEffectInterfaces
  MLIRSupport
  )
