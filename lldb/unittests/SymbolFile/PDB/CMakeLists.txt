add_lldb_unittest(SymbolFilePDBTests
  SymbolFilePDBTests.cpp

  LINK_LIBS
    lldbCore
    lldbHost
    lldbSymbol
    lldbPluginObjectFilePECOFF
    lldbPluginSymbolFileDWARF
    lldbPluginSymbolFilePDB
    lldbUtilityHelpers
  LINK_COMPONENTS
    Support
    DebugInfoPDB
  )

set(test_inputs
   test-pdb.exe
   test-pdb.pdb
   test-pdb-function-level-linking.exe
   test-pdb-function-level-linking.pdb
   test-pdb-splitted-function.exe
   test-pdb-splitted-function.pdb
   test-pdb-types.exe
   test-pdb-types.pdb)

add_unittest_inputs(SymbolFilePDBTests "${test_inputs}")
