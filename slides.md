---
theme: default
background: https://images.unsplash.com/photo-1572435555646-7ad9a149ad91?q=80&w=1920&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
title: Welcome to Slidev
highlighter: shiki
drawings:
  persist: false
mdc: true
layout: cover
transition: fade
---

# PGP

Segurança de dados ao seu alance

<div class="uppercase text-sm tracking-widest">
jaonoctus
</div>

<div class="abs-bl mx-14 my-12 flex">
  <img src="https://i.imgur.com/pISUX4M.png" class="h-8">
  <div class="ml-3 flex flex-col text-left">
    <div><b>Casa21</b></div>
    <div class="text-sm opacity-50">Workshop powered by Vinteum - Apr. 26th, 2024</div>
  </div>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/jaonoctus" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
  <a href="https://www.kernel.org/doc/html/next/process/maintainer-pgp-guide.html" target="_blank" alt="Kernel Maintainer PGP guide"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-notebook-reference />
  </a>
  <a href="https://github.com/lfit/itpol/blob/master/protecting-code-integrity.md" target="_blank" alt="Protecting code integrity with PGP"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-notebook-reference />
  </a>
  <a href="https://asecuritysite.com/bouncy/bc_rsa2" target="_blank" alt="RSA"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-notebook-reference />
  </a>
</div>

---
transition: fade
---

# A luta do governo para tornar criptografia ilegal

<Youtube id="DViojRQPcwM" />

---
layout: quote
transition: fade
---

# Manifesto Cypherpunk

HUGHES, Eric. 1993

- Privacy is necessary for an open society in the electronic age.
- Privacy is the power to selectively reveal oneself to the world.
- If I say something, I want it heard only by those for whom I intend it.
- Furthermore, to reveal one's identity with assurance when the default is anonymity requires the cryptographic signature.

---
transition: fade
---

# Criptografia

- Cipher
- Criptografia simétrica
- Criptografia assimétrica

<a href="https://storopoli.io/2024-02-05-crypto-basics/" target="_blank">Cryptography Basics</a>

---
transition: fade
layout: image-right
image: https://images.unsplash.com/photo-1683918891762-ed43ae8d0da4?q=80&w=1935&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

# Cipher

- Caesar's cipher

Julius Caesar encrypted by shifting the letters of the alphabet 3 places forward.

````md magic-move
```txt
a b c d e f g h i j k l m n o p q r s t u v w x y z
```

```txt
a b c d e f g h i j k l m n o p q r s t u v w x y z
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
```

```txt
a b c d e f g h i j k l m n o p q r s t u v w x y z
Z A B C D E F G H I J K L M N O P Q R S T U V W X Y
```

```txt
a b c d e f g h i j k l m n o p q r s t u v w x y z
Y Z A B C D E F G H I J K L M N O P Q R S T U V W X
```

```txt
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
```

```txt {4|2|1}
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

G L X L
```

```txt {5|2|1}
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

G L X L
j
```

```txt {5|2|1}
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

G L X L
j o
```

```txt {5|2|1}
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

G L X L
j o a
```

```txt {5}
a b c d e f g h i j k l m n o p q r s t u v w x y z
X Y Z A B C D E F G H I J K L M N O P Q R S T U V W

G L X L
j o a o
```
````

---
transition: fade
layout: image
image: https://i.imgur.com/dwvXih5.png
backgroundSize: contain
---

# Criptografia simétrica

---
transition: fade
layout: image
image: https://i.imgur.com/X2R2Vm1.png
backgroundSize: contain
---

# Criptografia simétrica

---
transition: fade
layout: image
image: https://i.imgur.com/leakjLj.png
backgroundSize: contain
---

# Criptografia assimétrica

---
transition: fade
layout: fact
---

# PGP
## Operações

---
transition: fade
---

# Visão geral extremamente básica

Não é necessário conhecer os detalhes exatos do funcionamento do PGP; basta compreender os conceitos básicos para poder usá-lo com êxito para nossos propósitos. O PGP se baseia na criptografia de chave pública para converter texto simples em texto criptografado. Esse processo requer duas chaves distintas:

- Uma <span v-mark.underline.red="1">chave privada</span>, que só é <span v-mark.circle.red="2">conhecida pelo dono</span>.
- Uma <span v-mark.underline.green="3">chave pública</span>, que é <span v-mark.circle.green="4">conhecida por todos</span>.


---
transition: fade
---

# Encryption (RSA)

o PGP usa a <span v-mark.underline.green="1">chave pública</span> para criar uma <span v-mark.underline.gray="2">mensagem criptografada</span> que só pode ser <span v-mark.underline.gray="3">descriptografada</span> usando a <span v-mark.underline.red="4">chave privada</span>.

- o remetente gera uma <span v-mark.underline.orange="5">chave de criptografia aleatória</span> (`nonce, simétrica`).
- o remetente <span v-mark.underline.gray="6">criptografa</span> o <span v-mark.underline.blue="7">conteúdo</span> usando essa <span v-mark.underline.orange="8">chave de sessão</span>.
- o remetente <span v-mark.underline.gray="9">criptografa</span> a <span v-mark.underline.orange="10">chave de sessão</span> usando a <span v-mark.underline.green="11">chave pública PGP do destinatário</span> (`assimétrica`).
- o remetente envia o <span v-mark.circle.orange="12">conteúdo criptografado</span> e a <span v-mark.circle.green="12">chave de sessão criptografada</span> para o destinatário.

<v-click at="+13">
<br>

# Decryption (RSA)

- o destinatário <span v-mark.underline.gray="14">descriptografa</span> a <span v-mark.circle.green="15">chave de sessão</span> usando sua <span v-mark.underline.red="16">chave PGP privada</span>.
- o destinatário <span v-mark.underline.gray="17">descriptografa</span> o <span v-mark.circle.orange="18">conteúdo</span> usando a <span v-mark.underline.orange="19">chave de sessão</span>.
- o destinatário acessa o <span v-mark.underline.blue="20">conteúdo</span>.

</v-click>

---
transition: fade
layout: center
---

<img src="https://i.imgur.com/u3PCsvB.png"/>

---
transition: fade
layout: center
---

<img src="https://i.imgur.com/zAA4Ugp.png"/>

---
transition: fade
---

# Signatures (RSA)

Para criar assinaturas, as chaves PGP privadas/públicas são usadas de maneira oposta:

- o assinante gera o <span v-mark.underline.purple="1">checksum</span> do <span v-mark.underline.blue="2">conteúdo</span>.
- o assinante usa sua própria <span v-mark.underline.red="3">chave PGP privada</span> para <span v-mark.underline.gray="4">criptografar</span> esse <span v-mark.circle.gray="5">hash</span>.
- o assinante fornece o <span v-mark.circle.gray="6">hash criptografado</span> juntamente com o <span v-mark.underline.blue="7">conteúdo</span>.

<v-click at="+8">
<br>

# Verificar a assinatura (RSA)

- o verificador gera seu próprio <span v-mark.underline.pink="9">checksum</span> do <span v-mark.underline.blue="10">conteúdo</span>.
- o verificador usa a <span v-mark.underline.green="11">chave pública PGP do assinante</span> para <span v-mark.underline.gray="12">descriptografar</span> o <span v-mark.circle.gray="13">hash</span>.
- se o <span v-mark.underline.purple="14">hash do assinante</span> e <span v-mark.underline.pink="15">hash do verificador</span> forem iguais, a assinatura é válida.
</v-click>

---
transition: fade
layout: center
---

<img src="https://i.imgur.com/zEho3aH.png"/>

---
transition: fade
layout: center
---

<img src="https://i.imgur.com/FsSwgd1.png"/>

---
transition: fade
layout: fact
---

# PGP
## Identidades


---
transition: fade
---

# Identidades

Cada chave PGP deve ter uma ou várias identidades associadas a ela. Normalmente, uma "Identidade" é o nome completo e o endereço de e-mail da pessoa no seguinte formato:


- `Satoshi Nakamoto <satoshin@gmx.com>`
- `Satoshi Nakamoto (confia) <craigwright@gmx.com>`

---
transition: fade
layout: fact
---

# PGP
## Validade

---
transition: fade
---

# Validade

Para poder usar a chave pública de outra pessoa para criptografia ou verificação, você precisa ter certeza de que ela realmente pertence à pessoa certa (Satoshi) e não a um impostor (Faketoshi). No PGP, essa certeza é chamada de "key validity".


- `full` significa que temos certeza de que essa chave pertence ao Satoshi.
- `marginal` significa que temos indícios de que essa chave pertence ao Satoshi.
- `unknown` significa que não podemos afirmar que a chave percente ao Satoshi.

---
transition: fade
layout: fact
---

# PGP
## Capacidades da chave

---
transition: fade
---

# Capacidades da chave

Cada chave PGP pode ter 4 "propósitos":

- `[C]` chave usada para certificar outras chaves (`Certifying`)
- `[S]` chave usada para assinar (`Signing`)
- `[E]` chave usada para criptografar (`Encryption`)
- `[A]` chave usada para autenticar (`Authentication`)

<v-click>
<br>

### Chave de certificação

A chave de certificação costuma ser chamada de "chave mestra", mas é uma analogia ruim, pois ela não age de forma alguma como uma chave mestra física (no sentido de que ela não pode descriptografar o conteúdo criptografado para nenhuma das subchaves, por exemplo).

- Não há diferenças técnicas entre a chave de certificação e nenhuma das subchaves.
- Uma única chave pode ter vários propósitos.
</v-click>

---
transition: fade
layout: fact
---

# PGP
## Na unha!

---
transition: fade
---

# Criando nossa primeira chave

````md magic-move
```text
$ gpg --version
```

```text
$ gpg --version

gpg (GnuPG) 2.2.27
libgcrypt 1.9.4
Copyright (C) 2021 Free Software Foundation, Inc.
License GNU GPL-3.0-or-later <https://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Home: /home/jaonoctus/.gnupg
Supported algorithms:
Pubkey: RSA, ELG, DSA, ECDH, ECDSA, EDDSA
Cipher: IDEA, 3DES, CAST5, BLOWFISH, AES, AES192, AES256, TWOFISH,
        CAMELLIA128, CAMELLIA192, CAMELLIA256
Hash: SHA1, RIPEMD160, SHA256, SHA384, SHA512, SHA224
Compression: Uncompressed, ZIP, ZLIB, BZIP2
```

```text
$ gpg --generate-key
```

```text{7}
$ gpg --generate-key

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name:
```

```text{7}
$ gpg --generate-key

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Satoshi Nakamoto
```

```text{8}
$ gpg --generate-key

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Satoshi Nakamoto
Email address:
```

```text{8}
$ gpg --generate-key

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Satoshi Nakamoto
Email address: satoshin@gmx.com
```


```text{10,11|13}
$ gpg --generate-key

Note: Use "gpg --full-generate-key" for a full featured key generation dialog.

GnuPG needs to construct a user ID to identify your key.

Real name: Satoshi Nakamoto
Email address: satoshin@gmx.com

You selected this USER-ID:
    "Satoshi Nakamoto <satoshin@gmx.com>"

Change (N)ame, (E)mail, or (O)kay/(Q)uit?
```


```text
// DIGITA A SENHA
```

```text
// CONFIRMA A SENHA DIGITANDO NOVAMENTE
```

```text{*|1|2|5|6|8|7}
gpg: key 77DBA9E0B2892782 marked as ultimately trusted
gpg: revocation certificate stored as '/home/jaonoctus/.gnupg/openpgp-revocs.d/77DBA9E0B2892782.rev'
public and secret key created and signed.

pub   rsa3072 2024-04-26 [SC] [expires: 2026-04-26]
      04058591575A0545D924F7D977DBA9E0B2892782
uid                      Satoshi Nakamoto <satoshin@gmx.com>
sub   rsa3072 2024-04-26 [E] [expires: 2026-04-26]
```
````

---
transition: fade
---

# Fazendo backup da chave privada

````md magic-move
```text
$ gpg --list-secret-keys --keyid-format long
```

```text{*|5}
$ gpg --list-secret-keys --keyid-format long

/home/jaonoctus/.gnupg/pubring.kbx

sec   rsa3072/77DBA9E0B2892782 2024-04-26 [SC] [expires: 2026-04-26]
      04058591575A0545D924F7D977DBA9E0B2892782
uid                 [ultimate] Satoshi Nakamoto <satoshin@gmx.com>
ssb   rsa3072/92DFC784842D8C93 2024-04-26 [E] [expires: 2026-04-26]
```

```text
$ gpg --armor --export-secret-keys
```

```text
$ gpg --armor --export-secret-keys 77DBA9E0B2892782
```

```text
$ gpg --armor --export-secret-keys 77DBA9E0B2892782 > private_key.asc
```
````


---
transition: fade
---

# Fazendo backup da chave pública

````md magic-move
```text
$ gpg --armor --export
```

```text
$ gpg --armor --export 77DBA9E0B2892782
```

```text
$ gpg --armor --export 77DBA9E0B2892782 > public_key.asc
```
````

---
transition: fade
---

# Criando nossa chave do "jeito certo"

````md magic-move
```text
$ gpg --expert --full-generate-key
```

```text{3-15|12|15}
$ gpg --expert --full-generate-key

Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
   (9) ECC and ECC
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (13) Existing key
  (14) Existing key from card
Your selection?
```

```text{15}
$ gpg --expert --full-generate-key

Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
   (9) ECC and ECC
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (13) Existing key
  (14) Existing key from card
Your selection? 11
```

```text{*|2|4|8}
Possible actions for a ECDSA/EdDSA key: Sign Certify Authenticate
Current allowed actions: Sign Certify

   (S) Toggle the sign capability
   (A) Toggle the authenticate capability
   (Q) Finished

Your selection?
```

```text{8}
Possible actions for a ECDSA/EdDSA key: Sign Certify Authenticate
Current allowed actions: Sign Certify

   (S) Toggle the sign capability
   (A) Toggle the authenticate capability
   (Q) Finished

Your selection? s
```

```text{2}
Possible actions for a ECDSA/EdDSA key: Sign Certify Authenticate
Current allowed actions: Certify

   (S) Toggle the sign capability
   (A) Toggle the authenticate capability
   (Q) Finished

Your selection?
```

```text{8}
Possible actions for a ECDSA/EdDSA key: Sign Certify Authenticate
Current allowed actions: Certify

   (S) Toggle the sign capability
   (A) Toggle the authenticate capability
   (Q) Finished

Your selection? q
```

```text{*|2|10}
Please select which elliptic curve you want:
   (1) Curve 25519
   (3) NIST P-256
   (4) NIST P-384
   (5) NIST P-521
   (6) Brainpool P-256
   (7) Brainpool P-384
   (8) Brainpool P-512
   (9) secp256k1
Your selection?
```

```text{10}
Please select which elliptic curve you want:
   (1) Curve 25519
   (3) NIST P-256
   (4) NIST P-384
   (5) NIST P-521
   (6) Brainpool P-256
   (7) Brainpool P-384
   (8) Brainpool P-512
   (9) secp256k1
Your selection? 1
```


```text{*|7}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)
```

```text{9,10}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)

Key does not expire at all
Is this correct? (y/N)
```

```text{10}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)

Key does not expire at all
Is this correct? (y/N) y
```

```text{*|5}
gpg: key FB9810E9ED801B71 marked as ultimately trusted
gpg: revocation certificate stored as '/home/jaonoctus/.gnupg/openpgp-revocs.d/FB9810E9ED801B71.rev'
public and secret key created and signed.

pub   ed25519 2024-04-26 [C]
      2A284766F3558D90C880DEC4FB9810E9ED801B71
uid                      Satoshi Nakamoto <satoshin@gmx.com>
```

````


---
transition: fade
---

# Adicionando subchaves

````md magic-move
```text
$ gpg --expert --edit-key FB9810E9ED801B71
```

```text{3-10|10}
$ gpg --expert --edit-key FB9810E9ED801B71

Secret key is available.

sec  ed25519/FB9810E9ED801B71
     created: 2024-04-26  expires: never       usage: C
     trust: ultimate      validity: ultimate
[ultimate] (1). Satoshi Nakamoto <satoshin@gmx.com>

gpg>
```

```text{10}
$ gpg --expert --edit-key FB9810E9ED801B71

Secret key is available.

sec  ed25519/FB9810E9ED801B71
     created: 2024-04-26  expires: never       usage: C
     trust: ultimate      validity: ultimate
[ultimate] (1). Satoshi Nakamoto <satoshin@gmx.com>

gpg> addkey
```

```text{2-14|9}
gpg> addkey
Please select what kind of key you want:
   (3) DSA (sign only)
   (4) RSA (sign only)
   (5) Elgamal (encrypt only)
   (6) RSA (encrypt only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (12) ECC (encrypt only)
  (13) Existing key
  (14) Existing key from card
Your selection?
```

```text{14}
gpg> addkey
Please select what kind of key you want:
   (3) DSA (sign only)
   (4) RSA (sign only)
   (5) Elgamal (encrypt only)
   (6) RSA (encrypt only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (12) ECC (encrypt only)
  (13) Existing key
  (14) Existing key from card
Your selection? 10
```

```text{*|2}
Please select which elliptic curve you want:
   (1) Curve 25519
   (3) NIST P-256
   (4) NIST P-384
   (5) NIST P-521
   (6) Brainpool P-256
   (7) Brainpool P-384
   (8) Brainpool P-512
   (9) secp256k1
Your selection?
```

```text{10}
Please select which elliptic curve you want:
   (1) Curve 25519
   (3) NIST P-256
   (4) NIST P-384
   (5) NIST P-521
   (6) Brainpool P-256
   (7) Brainpool P-384
   (8) Brainpool P-512
   (9) secp256k1
Your selection? 1
```

```text
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0)
```

```text{7}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y
```

```text{9-10}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y

Key expires at Sat Apr 26 15:43:24 2025 -03
Is this correct? (y/N)
```

```text{10}
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y

Key expires at Sat Apr 26 15:43:24 2025 -03
Is this correct? (y/N) y
```

```text{*|4-5}
sec  ed25519/FB9810E9ED801B71
     created: 2024-04-26  expires: never       usage: C
     trust: ultimate      validity: ultimate
ssb  ed25519/7D3F19426CBACE9E
     created: 2024-04-26  expires: 2025-04-26  usage: S
[ultimate] (1). Satoshi Nakamoto <satoshin@gmx.com>

gpg>
```

```text{2-14|11}
gpg> addkey
Please select what kind of key you want:
   (3) DSA (sign only)
   (4) RSA (sign only)
   (5) Elgamal (encrypt only)
   (6) RSA (encrypt only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (12) ECC (encrypt only)
  (13) Existing key
  (14) Existing key from card
Your selection?
```

```text{14}
gpg> addkey
Please select what kind of key you want:
   (3) DSA (sign only)
   (4) RSA (sign only)
   (5) Elgamal (encrypt only)
   (6) RSA (encrypt only)
   (7) DSA (set your own capabilities)
   (8) RSA (set your own capabilities)
  (10) ECC (sign only)
  (11) ECC (set your own capabilities)
  (12) ECC (encrypt only)
  (13) Existing key
  (14) Existing key from card
Your selection? 12
```

```text{*|6-7}
sec  ed25519/FB9810E9ED801B71
     created: 2024-04-26  expires: never       usage: C
     trust: ultimate      validity: ultimate
ssb  ed25519/7D3F19426CBACE9E
     created: 2024-04-26  expires: 2025-04-26  usage: S
ssb  cv25519/765F1659AC5ACCA5
     created: 2024-04-26  expires: 2025-04-26  usage: E
[ultimate] (1). Satoshi Nakamoto <satoshin@gmx.com>

gpg>
```

```text{10}
sec  ed25519/FB9810E9ED801B71
     created: 2024-04-26  expires: never       usage: C
     trust: ultimate      validity: ultimate
ssb  ed25519/7D3F19426CBACE9E
     created: 2024-04-26  expires: 2025-04-26  usage: S
ssb  cv25519/765F1659AC5ACCA5
     created: 2024-04-26  expires: 2025-04-26  usage: E
[ultimate] (1). Satoshi Nakamoto <satoshin@gmx.com>

gpg> save
```
````

---
transition: fade
---

# Exportando uma subchave privada

````md magic-move
```text
$ gpg --list-secret-keys --keyid-format long
```

```text{3-7|6}
$ gpg --list-secret-keys --keyid-format long

sec   ed25519/FB9810E9ED801B71 2024-04-26 [C]
      2A284766F3558D90C880DEC4FB9810E9ED801B71
uid                 [ultimate] Satoshi Nakamoto <satoshin@gmx.com>
ssb   ed25519/7D3F19426CBACE9E 2024-04-26 [S] [expires: 2025-04-26]
ssb   cv25519/765F1659AC5ACCA5 2024-04-26 [E] [expires: 2025-04-26]
```

```text
$ gpg --armor --export-secret-subkeys 7D3F19426CBACE9E! > sign_only.asc
```

```text
$ gpg --import sign_only.asc
```


```text{*|4|1|5}
sec#  ed25519/FB9810E9ED801B71 2024-04-26 [C]
      2A284766F3558D90C880DEC4FB9810E9ED801B71
uid                 [ultimate] Satoshi Nakamoto <satoshin@gmx.com>
ssb   ed25519/7D3F19426CBACE9E 2024-04-26 [S] [expires: 2025-04-26]
ssb>  cv25519/765F1659AC5ACCA5 2024-04-26 [E] [expires: 2025-04-26]
```
````


---
transition: fade
---

# Encriptando uma mensagem

````md magic-move
```text
$ echo "mensagem secreta" > /tmp/msg1
```

```text
$ gpg --armor --encrypt --recipient FB9810E9ED801B71 /tmp/msg1
```

```text
$ cat /tmp/msg1.asc

-BEGIN PGP MESSAGE-

hF4Ddl8WWaxazKUSAQdAET0mPfX/A6vl+f4kmZyHmt1WUKKjgyr/mSYp6ePKFWQw
qKpnMBqMfaktpLdmFuMSWkTPBYfCWetgPmyNfc/B56JYzHRi7rQbn6oFjwdGPnIg
0k8BBaFcStkLqPZH/JbUkad4aeZQ9xfxyXTDzuDfcYDn4OoIe6D2YXmvu2VvVPhV
1kAV4zvvoxx4R2iNEzBt8nKBKAE89jmsZGjKzXUFRiHg
=waxA
-END PGP MESSAGE-
```
````


---
transition: fade
---

# Decriptando uma mensagem

````md magic-move
```text
$ gpg --decrypt /tmp/msg1.asc
```

```text{3-5}
$ gpg --decrypt /tmp/msg1.asc

gpg: encrypted with 255-bit ECDH key, ID 765F1659AC5ACCA5, created 2024-04-26
      "Satoshi Nakamoto <satoshin@gmx.com>"
mensagem secreta
```

```text{4-6}
$ gpg --decrypt /tmp/msg1.asc
// eu não tenha essa chave privada no meu keyring

gpg: encrypted with 2048-bit ELG key, ID CF1857E6D6AAA69F, created 2008-10-30
      "Satoshi Nakamoto <satoshin@gmx.com>"
gpg: decryption failed: No secret key
```
````

---
transition: fade
---

# Assinando uma mensagem

````md magic-move
```text
$ echo "mensagem do satoshi" > /tmp/msg2
```

```text{1}
$ gpg --armor --local-user 7D3F19426CBACE9E! --detach-sign /tmp/msg2
// gera um arquivo msg2.asc apenas com a assinatura
```

```text{4-10}
$ gpg --armor --local-user 7D3F19426CBACE9E! --detach-sign /tmp/msg2
// gera um arquivo msg2.asc apenas com a assinatura

-BEGIN PGP SIGNATURE-

iHUEARYIAB0WIQQeb0HEGMwrfdut4ux9PxlCbLrOngUCZiwC9gAKCRB9PxlCbLrO
nol+AQCZWQiAA/znWykG70en4tx1qQaNSjcOgcThbx7Iysx5LgD9FOFcrbxWImtC
0IFdwTKSu1cGvz/QIyI+8wVkUPw5zQw=
=oaK7
-END PGP SIGNATURE-
```

```text{1}
$ gpg --armor --local-user 7D3F19426CBACE9E! --clear-sign /tmp/msg2
// gera um arquivo msg2.asc com a mensagem + assinatura
```

```text{3-13}
$ gpg --armor --local-user 7D3F19426CBACE9E! --clear-sign /tmp/msg2

-BEGIN PGP SIGNED MESSAGE-
Hash: SHA256

mensagem do satoshi
-BEGIN PGP SIGNATURE-

iHUEARYIAB0WIQQeb0HEGMwrfdut4ux9PxlCbLrOngUCZiwC9gAKCRB9PxlCbLrO
nol+AQCZWQiAA/znWykG70en4tx1qQaNSjcOgcThbx7Iysx5LgD9FOFcrbxWImtC
0IFdwTKSu1cGvz/QIyI+8wVkUPw5zQw=
=oaK7
-END PGP SIGNATURE-
```
````

---
transition: fade
---

# Verificando uma mensagem

````md magic-move
```text
$ gpg --verify /tmp/msg2.asc
```

```text{3-5}
$ gpg --verify /tmp/msg2.asc

gpg: Signature made Fri Apr 26 16:46:10 2024 -03
gpg:                using EDDSA key 1E6F41C418CC2B7DDBADE2EC7D3F19426CBACE9E
gpg: Good signature from "Satoshi Nakamoto <satoshin@gmx.com>" [ultimate]
```


```text{4-6}
$ gpg --verify /tmp/msg2.asc
// a mensagem não foi assinada por satoshi

gpg: Signature made Fri Apr 26 16:46:10 2024 -03
gpg:                using EDDSA key 1E6F41C418CC2B7DDBADE2EC7D3F19426CBACE9E
gpg: BAD signature from "Satoshi Nakamoto <satoshin@gmx.com>" [ultimate]
```
````

---
transition: fade
layout: fact
---

# Obrigado

#### @jaonoctus
