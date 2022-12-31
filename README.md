# Import Public key and encrypt a message

Import key:
```bash
curl https://raw.githubusercontent.com/andreyk0/gpg/master/81D36A78EEBDAABF9909CBF5D29DD5BF0A0D164A.pub | gpg --import
```

Encrypt a test message:
```bash
echo test |  gpg --encrypt --armor --recipient 81D36A78EEBDAABF9909CBF5D29DD5BF0A0D164A > test.gpg
```

# GPG keys

```bash
gpg --list-secret-keys --keyid-format long
```

## Current
```
sec   rsa4096/0xD29DD5BF0A0D164A 2018-06-17 [SC]
      Key fingerprint = 81D3 6A78 EEBD AABF 9909  CBF5 D29D D5BF 0A0D 164A
uid                   [ultimate] Andrey Kartashov (Earnest) <akartashov@earnestanalytics.com>
uid                   [ultimate] Andrey Kartashov <andrey.kartashov@gmail.com>
ssb   rsa4096/0x837FE28F9FFF0E6C 2018-06-17 [E]
ssb   rsa4096/0x202DA9BAE8F0FE08 2018-06-17 [S] [expires: 2023-06-16]
ssb   rsa4096/0x57168B0669B88036 2018-06-18 [A] [expires: 2023-06-17]
ssb   rsa4096/0x5CC858C93DB02839 2022-12-31 [S] [expires: 2032-12-28]
ssb   rsa4096/0xBA6FD54D2021844F 2022-12-31 [E]
ssb   rsa4096/0x609BDBB2C279BAAF 2022-12-31 [A] [expires: 2032-12-28]
```

## Older, deprecated
```
sec   rsa2048/3C35F6BBA50B5999 2014-04-18 [SC]
      246B104427ED6E2401318FDA3C35F6BBA50B5999
uid                 [ultimate] Andrey Kartashov <akartashov@gilt.com>
ssb   rsa2048/04B837F5FCE5491E 2014-04-18 [E]
```
