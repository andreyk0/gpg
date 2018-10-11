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
sec   rsa4096/D29DD5BF0A0D164A 2018-06-17 [SC]
      81D36A78EEBDAABF9909CBF5D29DD5BF0A0D164A
uid                 [ultimate] Andrey Kartashov <andrey.kartashov@gmail.com>
ssb   rsa4096/837FE28F9FFF0E6C 2018-06-17 [E]
ssb   rsa4096/202DA9BAE8F0FE08 2018-06-17 [S] [expires: 2023-06-16]
ssb   rsa4096/57168B0669B88036 2018-06-18 [A] [expires: 2023-06-17]

```

## Older, deprecated
```
sec   rsa2048/3C35F6BBA50B5999 2014-04-18 [SC]
      246B104427ED6E2401318FDA3C35F6BBA50B5999
uid                 [ultimate] Andrey Kartashov <akartashov@gilt.com>
ssb   rsa2048/04B837F5FCE5491E 2014-04-18 [E]
```
