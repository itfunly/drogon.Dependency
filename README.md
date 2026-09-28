# drogon.Dependency

Dependency of [drogon framework](https://github.com/drogonframework/drogon) writed by c++

## 依赖项目及github地址

[botan](https://github.com/randombit/botan)

```git
    git submodule add -f --depth 1 https://github.com/randombit/botan dependency.src/brotli
```

[brotli](https://github.com/google/brotli)

```git
    git submodule add -f --depth 1 https://github.com/google/brotli dependency.src/brotli
```

[c-ares](https://github.com/c-ares/c-ares)

```git
    git submodule add -f --depth 1 https://github.com/c-ares/c-ares dependency.src/c-ares
```

[cpptrace](https://github.com/jeremy-rifkin/cpptrace)

```git
    git submodule add -f --depth 1 https://github.com/jeremy-rifkin/cpptrace dependency.src/c-ares
```

[drogon](https://github.com/drogonframework/drogon)

```git
    git submodule add -f --depth 1 https://github.com/drogonframework/drogon dependency.src/drogon
```

[hiredis](https://github.com/redis/hiredis)

```git
    git submodule add -f --depth 1 https://github.com/redis/hiredis dependency.src/hiredis
```

[jsoncpp](https://github.com/open-source-parsers/jsoncpp)

```git
    git submodule add -f --depth 1 https://github.com/redis/hiredis dependency.src/hiredis
```

mariadb

openssl

[spdlog](https://github.com/gabime/spdlog)

```git
    git submodule add -f --depth 1 https://github.com/gabime/spdlog dependency.src/spdlog
```

sqlite3

[trantor](https://github.com/an-tao/trantor)

```git
    git submodule add -f --depth 1 https://github.com/an-tao/trantor dependency.src/spdlog
```

[yaml-cpp](https://github.com/jbeder/yaml-cpp)

```git
    git submodule add -f --depth 1 https://github.com/jbeder/yaml-cpp dependency.src/yaml-cpp
```

[zlib](https://github.com/madler/zlib)

```git
    git submodule add -f --depth 1 https://github.com/madler/zlib dependency.src/zlib
```

cmake命令

``` bat

rem -------------------------- start of cmake envirment

    set vs2006dir=D:/Program Files/Microsoft/Visual Studio 2026/
    set vs2006di2=D:\Program Files\Microsoft\Visual Studio 2026\
    set winsdkdir=C:\Program Files (x86)\Windows Kits\10\
    set winsdkdi2=C:/Program Files (x86)/Windows Kits/10/
    set winsdkver=10.0.26100.0
    set vc2006ver=14.51.36231
    set platform=x64

    set gitroot=D:/Documents/GitHub
    set mariadbroot=D:/application/mariadb
    set diaPath=D:/application/mSys/ucrt64/bin/dia.exe
    set GraphvizPath=D:/application/Graphviz/bin/dot.exe
    set doxygenPath=D:/application/DOXYGEN/doxygen.exe
    set pkgPath=D:/application/mSys/ucrt64/bin/pkg-config.exe

    set defaultDll=msvcrt.lib vcruntime.lib msvcprt.lib kernel32.lib user32.lib gdi32.lib winspool.lib shell32.lib ole32.lib oleaut32.lib uuid.lib comdlg32.lib advapi32.lib
    set defaultLib=/LIBPATH:\"%winsdkdir%lib\%winsdkver%\ucrt\%platform%\" /LIBPATH:\"%winsdkdir%Lib\%winsdkver%\ucrt_enclave\%platform%\" /LIBPATH:\"%winsdkdir%lib\%winsdkver%\um\%platform%\" /LIBPATH:\"%vs2006di2%VC\Tools\MSVC\%vc2006ver%\lib\%platform%\"


    set output=output
    set dstdir=dstdir

    set wincmd=
    set wincmd=%wincmd% -DCMAKE_C_COMPILER="%vs2006dir%VC/Tools/MSVC/%vc2006ver%/bin/Host%platform%/%platform%/cl.exe"
    set wincmd=%wincmd% -DCMAKE_CXX_COMPILER="%vs2006dir%VC/Tools/MSVC/%vc2006ver%/bin/Host%platform%/%platform%/cl.exe"
    set wincmd=%wincmd% -DCMAKE_AR="%vs2006dir%VC/Tools/MSVC/%vc2006ver%/bin/Host%platform%/%platform%/lib.exe" 
    set wincmd=%wincmd% -DCMAKE_CXX_FLAGS_RELWITHDEBINFO="/O2 /Ob1 /DNDEBUG"
    set wincmd=%wincmd% -DCMAKE_CXX_STANDARD_LIBRARIES="%defaultDll%"
    set wincmd=%wincmd% -DCMAKE_C_FLAGS="/DWIN32 /D_WINDOWS"
    set wincmd=%wincmd% -DCMAKE_C_FLAGS_RELWITHDEBINFO="/O2 /Ob1 /DNDEBUG"
    set wincmd=%wincmd% -DCMAKE_C_STANDARD_LIBRARIES="%defaultDll%"  
    set wincmd=%wincmd% -DCMAKE_EXE_LINKER_FLAGS="/machine:%platform% /SAFESEH:NO /NODEFAULTLIB:LIBCMT %defaultLib% %defaultDll%"
    set wincmd=%wincmd% -DCMAKE_EXE_LINKER_FLAGS_DEBUG="/debug /INCREMENTAL"
    set wincmd=%wincmd% -DCMAKE_EXE_LINKER_FLAGS_MINSIZEREL=/INCREMENTAL:NO
    set wincmd=%wincmd% -DCMAKE_EXE_LINKER_FLAGS_RELWITHDEBINFO="/debug /INCREMENTAL /NODEFAULTLIB:LIBCMT %defaultLib% %defaultDll%"
    set wincmd=%wincmd% -DCMAKE_LINKER="%vs2006dir%VC/Tools/MSVC/%vc2006ver%/bin/Host%platform%/%platform%/link.exe"   
    set wincmd=%wincmd% -DCMAKE_MODULE_LINKER_FLAGS="/machine:%platform% /SAFESEH:NO  /NODEFAULTLIB:LIBCMT %defaultLib% %defaultDll%" 
    set wincmd=%wincmd% -DCMAKE_MODULE_LINKER_FLAGS_DEBUG="/debug /INCREMENTAL"
    set wincmd=%wincmd% -DCMAKE_MODULE_LINKER_FLAGS_MINSIZEREL=/INCREMENTAL:NO
    set wincmd=%wincmd% -DCMAKE_MODULE_LINKER_FLAGS_RELWITHDEBINFO="/debug /INCREMENTAL"
    set wincmd=%wincmd% -DCMAKE_MT="%winsdkdi2%bin/%winsdkver%/%platform%/mt.exe"
    set wincmd=%wincmd% -DCMAKE_RC_COMPILER="%winsdkdi2%bin/%winsdkver%/%platform%/rc.exe"
    set wincmd=%wincmd% -DCMAKE_RC_FLAGS=-DWIN32
    set wincmd=%wincmd% -DCMAKE_RC_FLAGS_DEBUG=-D_DEBUG    
    set wincmd=%wincmd% -DCMAKE_SHARED_LINKER_FLAGS="/machine:%platform% /SAFESEH:NO  /NODEFAULTLIB:LIBCMT %defaultLib% %defaultDll%" 
    set wincmd=%wincmd% -DCMAKE_SHARED_LINKER_FLAGS_DEBUG="/debug /INCREMENTAL"
    set wincmd=%wincmd% -DCMAKE_SHARED_LINKER_FLAGS_MINSIZEREL=/INCREMENTAL:NO
    set wincmd=%wincmd% -DCMAKE_SHARED_LINKER_FLAGS_RELWITHDEBINFO="/debug /INCREMENTAL"
    set wincmd=%wincmd% -DCMAKE_STATIC_LINKER_FLAGS="/machine:%platform% /SAFESEH:NO /NODEFAULTLIB:LIBCMT %defaultLib% %defaultDll%"




    set makecmd=
    set makecmd=%makecmd% -DCMAKE_CXX_STANDARD=20
    set makecmd=%makecmd% -DCMAKE_CONFIGURATION_TYPES=RelWithDebInfo 
    set makecmd=%makecmd% -DZLIB_LIBRARY_DEBUG=%gitroot%/zlib/%dstdir%/lib/libzd.lib
    set makecmd=%makecmd% -DZLIB_LIBRARY_RELEASE=%gitroot%/zlib/%dstdir%/lib/libz.lib
    set makecmd=%makecmd% -DSQLITE3_INCLUDE_DIRS=%gitroot%/sqlite3
    set makecmd=%makecmd% -DSQLITE3_LIBRARIES=%gitroot%/sqlite3/sqlite3.lib
    set makecmd=%makecmd% -DPKG_CONFIG_EXECUTABLE=%pkgPath%
    set makecmd=%makecmd% -DMYSQL_INCLUDE_DIRS=%mariadbroot%/include/mysql
    set makecmd=%makecmd% -DMYSQL_LIBRARIES=%mariadbroot%/lib/libmariadb.lib
    set makecmd=%makecmd% -DJSONCPP_INCLUDE_DIRS=%gitroot%/jsoncpp/%dstdir%/include
    set makecmd=%makecmd% -DJSONCPP_LIBRARIES=%gitroot%/jsoncpp/%dstdir%/lib/jsoncpp.lib
    set makecmd=%makecmd% -DHIREDIS_INCLUDE_DIR=%gitroot%/hiredis/%dstdir%/include
    set makecmd=%makecmd% -DHIREDIS_LIBRARY=%gitroot%/hiredis/%dstdir%/lib/hiredis.lib
    set makecmd=%makecmd% -DDOXYGEN_DIA_EXECUTABLE=%diaPath%
    set makecmd=%makecmd% -DDOXYGEN_DOT_EXECUTABLE=%GraphvizPath%
    set makecmd=%makecmd% -DDOXYGEN_EXECUTABLE=%doxygenPath%
    set makecmd=%makecmd% -DCMAKE_INSTALL_PREFIX=%gitroot%/bin
    set makecmd=%makecmd% -DC-ARES_INCLUDE_DIRS=%gitroot%/c-ares/%dstdir%/include
    set makecmd=%makecmd% -DC-ARES_LIBRARIES=%gitroot%/c-ares/%dstdir%/lib/cares.lib
    set makecmd=%makecmd% -DBotan_INCLUDE_DIRS=%gitroot%/botan/%dstdir%/include/botan-3
    set makecmd=%makecmd% -DBotan_LIBRARIES=%gitroot%/botan/%dstdir%/lib/botan-3.lib
    set makecmd=%makecmd% -DTrantor_DIR=%gitroot%/trantor/%dstdir%/lib/cmake/Trantor
    set makecmd=%makecmd% -DBROTLI_INCLUDE_DIR=%gitroot%/brotli/%dstdir%/include
    set makecmd=%makecmd% -DBROTLICOMMON_LIBRARY=%gitroot%/brotli/%dstdir%/lib/brotlicommon.lib
    set makecmd=%makecmd% -DBROTLIDEC_LIBRARY=%gitroot%/brotli/%dstdir%/lib/brotlidec.lib
    set makecmd=%makecmd% -DBROTLIENC_LIBRARY=%gitroot%/brotli/%dstdir%/lib/brotlienc.lib
    set makecmd=%makecmd% -DMARIADB_INCLUDE_DIRS=%mariadbroot%/include/
    set makecmd=%makecmd% -Djsoncpp_DIR=%gitroot%/jsoncpp/%dstdir%/LIB/cmake/jsoncpp
    set makecmd=%makecmd% -Dunofficial-libmariadb_DIR=%mariadbroot%/lib
    set makecmd=%makecmd% -Dunofficial-sqlite3_DIR=%gitroot%/sqlite3
    set makecmd=%makecmd% -Dyaml-cpp_DIR=%gitroot%/yaml-cpp/%dstdir%/lib/cmake/yaml-cpp
    set makecmd=%makecmd% -DZLIB_INCLUDE_DIR=%gitroot%/zlib/%dstdir%/include
    set makecmd=%makecmd% -DBUILD_BROTLI=TRUE
    set makecmd=%makecmd% -DBUILD_C-ARES=TRUE
    set makecmd=%makecmd% -DBUILD_CTL=TRUE
    set makecmd=%makecmd% -DBUILD_DOC=TRUE
    set makecmd=%makecmd% -DBUILD_EXAMPLES=TRUE
    set makecmd=%makecmd% -DBUILD_MYSQL=TRUE
    set makecmd=%makecmd% -DBUILD_ORM=TRUE
    set makecmd=%makecmd% -DBUILD_REDIS=TRUE
    set makecmd=%makecmd% -DBUILD_SHARED_LIBS=TRUE
    set makecmd=%makecmd% -DBUILD_SQLITE=TRUE
    set makecmd=%makecmd% -DBUILD_YAML_CONFIG=TRUE
    set makecmd=%makecmd% -DBUILD_POSTGRESQL=FALSE
    set makecmd=%makecmd% -DUSE_COROUTINE=TRUE
    set makecmd=%makecmd% -DUSE_SPDLOG=TRUE
    set makecmd=%makecmd% -DUSE_SUBMODULE=FALSE
    set makecmd=%makecmd% -DCMAKE_HAVE_LIBC_PTHREAD=FALSE
    set makecmd=%makecmd% -DCOMPILER_HAS_DEPRECATED=TRUE
    set makecmd=%makecmd% -DCXX_FILESYSTEM_NO_LINK_NEEDED=TRUE
    set makecmd=%makecmd% -DCXX_FILESYSTEM_STDCPPFS_NEEDED=TRUE
    set makecmd=%makecmd% -DCXX_FILESYSTEM_CPPFS_NEEDED=TRUE
    set makecmd=%makecmd% -DCXX_FILESYSTEM_HAVE_FS=TRUE
    set makecmd=%makecmd% -DCXX_FILESYSTEM_HEADER=filesystem
    set makecmd=%makecmd% -DCXX_FILESYSTEM_NAMESPACE=std::filesystem



cd /d %gitroot%/drogon

cmake -S. -B %output% %makecmd% %wincmd%
```

