# GitHub Push to 0.10.10 Branch - TODO List

## Objective
Push the compilation fixes for Debian 13 compatibility to the GitHub repository 0.10.10 branch.

## Status
- [x] Created 0.10.10 branch
- [x] Pushed Makefile.debian13

## Files to Push with Compilation Fixes

### Core Fixed Source Files
- [x] Makefile.debian13 - Debian 13 build system (COMPLETED)
- [ ] bdt/ExtendedAttribute.cpp - Fixed header path (attr/xattr.h → sys/xattr.h)
- [ ] bdt/FileDigest.cpp - Fixed OpenSSL 3.x API (EVP_MD_CTX_destroy → EVP_MD_CTX_free)
- [ ] bdt/FileMetaParser.cpp - Fixed Python 3 API (PyString → PyUnicode migration)
- [ ] bdt/Inode.cpp - Fixed header path and errno (ENOATTR → ENODATA)
- [ ] bdt/stdafx.h - Added errno.h include
- [ ] bdt/PriorityTape.h - Fixed C++20 const-correctness (operator() const)

### Documentation
- [ ] COMPILATION_TODO.md - Comprehensive documentation of all fixes

## Next Steps
1. Push all fixed source files to 0.10.10 branch
2. Push documentation
3. Verify all files are in repository
4. Test compilation on fresh clone

## Notes
- All compilation errors have been resolved
- 45 object files compile successfully with zero errors
- Project is now compatible with Debian 13, OpenSSL 3.x, Python 3, and C++20
