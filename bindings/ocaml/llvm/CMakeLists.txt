add_ocaml_library(llvm
  OCAML llvm
  C     llvm_ocaml
  LLVM  core support)

configure_file(
  "${CMAKE_CURRENT_SOURCE_DIR}/META.llvm.in"
  "${LLVM_LIBRARY_DIR}/ocaml/META.llvm")

install(FILES "${LLVM_LIBRARY_DIR}/ocaml/META.llvm"
        DESTINATION "${LLVM_OCAML_INSTALL_PATH}")
