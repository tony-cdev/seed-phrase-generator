CXX = g++
CC  = gcc

TARGET = walletgen

CXXFLAGS = -O2 -std=c++17 -Wall -Wextra -I. -Icrypto
CFLAGS   = -O2 -std=gnu99 -Wall -Wextra -I. -Icrypto


CXXFLAGS = -O2 -std=c++17 -Wall -Wextra -I. -Icrypto
CFLAGS   = -O2 -std=gnu99 -Wall -Wextra -I. -Icrypto


CPP_SRCS = main.cpp recovery.cpp address_generator.cpp address_checker.cpp
CPP_OBJS = $(CPP_SRCS:.cpp=.o)

# =========================
# Trezor crypto (C)
# =========================
SRCS = \
crypto/ed25519-donna/curve25519-donna-32bit.c \
crypto/ed25519-donna/curve25519-donna-helpers.c \
crypto/ed25519-donna/modm-donna-32bit.c \
crypto/ed25519-donna/ed25519-donna-basepoint-table.c \
crypto/ed25519-donna/ed25519-donna-32bit-tables.c \
crypto/ed25519-donna/ed25519-donna-impl-base.c \
crypto/ed25519-donna/ed25519.c \
crypto/ed25519-donna/curve25519-donna-scalarmult-base.c \
crypto/ed25519-donna/ed25519-sha3.c \
crypto/ed25519-donna/ed25519-keccak.c \
crypto/bignum.c crypto/ecdsa.c crypto/curves.c \
crypto/secp256k1.c crypto/nist256p1.c \
crypto/rand.c crypto/rand_impl.c \
crypto/hmac.c crypto/bip32.c crypto/bip39.c crypto/pbkdf2.c \
crypto/base58.c crypto/base32.c crypto/address.c crypto/script.c \
crypto/ripemd160.c crypto/sha2.c crypto/sha3.c crypto/hasher.c \
crypto/aes/aescrypt.c crypto/aes/aeskey.c crypto/aes/aestab.c crypto/aes/aes_modes.c \
crypto/blake256.c crypto/blake2b.c crypto/blake2s.c crypto/groestl.c \
crypto/rc4.c crypto/nem.c crypto/segwit_addr.c crypto/cash_addr.c \
crypto/memzero.c crypto/shamir.c crypto/hmac_drbg.c crypto/rfc6979.c crypto/slip39.c

OBJS = $(SRCS:.c=.o)


all: $(TARGET)

# C
crypto/%.o: crypto/%.c
	$(CC) $(CFLAGS) -c $< -o $@

crypto/aes/%.o: crypto/aes/%.c
	$(CC) $(CFLAGS) -c $< -o $@

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c $< -o $@

$(TARGET): $(OBJS) $(CPP_OBJS)
	$(CXX) $^ -o $@ $(LDFLAGS)


clean:
	rm -f *.o $(TARGET)

clean-crypto:
	rm -f crypto/*.o crypto/*/*.o
