murmurhash
===========

MurmurHash3 general hash bashed lookup function implementation

## about

[MurmurHash](http://en.wikipedia.org/wiki/MurmurHash) is a non-cryptographic hash function suitable
for general hash-based lookup. This implementation implements version 3
of MurmurHash.

## install

[clib](https://github.com/clibs/clib):

```sh
$ clib install jwerle/murmurhash.c
```

## example

```c

#include <stdlib.h>
#include <string.h>
#include <murmurhash.h>

int
main (void) {
  uint32_t seed = 0;
  const char *key = "kinkajou";
  uint32_t hash = murmurhash(key, (uint32_t) strlen(key), seed); // 0xb6d99cf8
  return 0;
}
```

## api

```c
uint32_t
murmurhash (const char *key, uint32_t len, uint32_t seed);
```

Returns a murmur hash of `key' based on `seed' using the MurmurHash3 algorithm.

## license

MIT
