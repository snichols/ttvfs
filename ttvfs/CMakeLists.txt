
set(ttvfs_code
    VFSBase.cpp
    VFSDebug.cpp
    VFSDir.cpp
    VFSDirInternal.cpp
    VFSDirView.cpp
    VFSFile.cpp
    VFSFileFuncs.cpp
    VFSLoader.cpp
    VFSRoot.cpp
    VFSSystemPaths.cpp
    VFSTools.cpp
)

set(ttvfs_headers
    ttvfs.h
    VFSArchiveLoader.h
    VFSBase.h
    VFSDebug.h
    VFSDefines.h
    VFSDir.h
    VFSDirInternal.h
    VFSDirView.h
    VFSFile.h
    VFSFileFuncs.h
    VFSInternal.h
    VFSLoader.h
    VFSRefcounted.h
    VFSRoot.h
    VFSSystemPaths.h
    VFSTools.h
)

add_library(ttvfs ${ttvfs_code} ${ttvfs_headers})

install(TARGETS ttvfs DESTINATION lib)
install(FILES ${ttvfs_headers} DESTINATION include/ttvfs)