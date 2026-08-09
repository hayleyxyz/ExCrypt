add_library(ExCrypt STATIC
        src/excrypt.h
        src/excrypt_aes.c
        src/excrypt_aes.h
        src/excrypt_bn.c
        src/excrypt_bn.h
        src/excrypt_bn_key.cpp
        src/excrypt_bn_mod.cpp
        src/excrypt_bn_pkcs1.cpp
        src/excrypt_bn_rsa.cpp
        src/excrypt_bn_sig.c
        src/excrypt_des.c
        src/excrypt_des.h
        src/excrypt_des_data.h
        src/excrypt_ecc.c
        src/excrypt_ecc.h
        src/excrypt_md5.c
        src/excrypt_md5.h
        src/excrypt_mem.cpp
        src/excrypt_mem.h
        src/excrypt_parve.c
        src/excrypt_parve.h
        src/excrypt_rc4.c
        src/excrypt_rc4.h
        src/excrypt_rotsum.c
        src/excrypt_rotsum.h
        src/excrypt_sha.c
        src/excrypt_sha.h
        src/excrypt_sha2.c
        src/excrypt_sha2.h
        src/exkeys.cpp
        src/exkeys.h
        src/fp61.hpp
        src/rijndael.c
        src/rijndael.h)

target_include_directories(ExCrypt PUBLIC src)

if(WIN32)
    target_link_libraries(ExCrypt PUBLIC bcrypt)
endif()
