
set(ttvfs_zip_code
    VFSDirZip.cpp
    VFSFileZip.cpp
    VFSZipArchiveLoader.cpp
    VFSZipArchiveRef.cpp
    miniz.c
)

set(ttvfs_zip_headers
    VFSDirZip.h
    VFSFileZip.h
    VFSZipArchiveLoader.h
    VFSZipArchiveRef.h
    miniz.h
    ttvfs_zip.h
)

include_directories(${TTVFS_INCLUDE_DIRS})
add_library(ttvfs_zip ${ttvfs_zip_code} ${ttvfs_zip_headers})

install(TARGETS ttvfs_zip DESTINATION lib)
install(FILES ${ttvfs_zip_headers} DESTINATION include/ttvfs)