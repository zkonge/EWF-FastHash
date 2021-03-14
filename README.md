# EWF-FastHash
Fast Expert Witness Compression Format (EWF) hash calculator

## Requirements

1. Python 3.6+
2. Any system supports `libewf-python`

Just run `pip install libewf-python`.

## Usage

Notice: Older Python version may support less hash method(s).  

```
usage: ewf_fasthash.py [-h]
                       [--hash {blake2b,blake2s,md4,md5,md5-sha1,mdc2,ripemd160,sha1,sha224,sha256,sha384,sha3_224,sha3_256,sha3_384,sha3_512,sha512,sha512_
224,sha512_256,shake_128,shake_256,sm3,whirlpool}]
                       [--block-size BLOCK_SIZE] [--parallelism PARALLELISM] [-V]
                       name

Fast EWF(E01) hash calculator

positional arguments:
  name                  EWF file name (1 name enough).

optional arguments:
  -h, --help            show this help message and exit
  --hash {blake2b,blake2s,md4,md5,md5-sha1,mdc2,ripemd160,sha1,sha224,sha256,sha384,sha3_224,sha3_256,sha3_384,sha3_512,sha512,sha512_224,sha512_256,shake_1
28,shake_256,sm3,whirlpool}
                        Hash type you want to use. (default: md5)
  --block-size BLOCK_SIZE
                        Block size(byte) read from disk, larger means faster, but cost more memory. (default: 536870912(512Mib))
  --parallelism PARALLELISM
                        Thread count, improve decompress performance, but large number have negative effect on read performance. (default: 3)
  -V, --verbose         Show more information for debugging.
```

