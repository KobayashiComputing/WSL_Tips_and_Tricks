# A New Kali Linux Archive Signing Key

[Kali Linux Archive Signing Key]([https://www.kali.org/blog/new-kali-archive-signing-key/) Blog Article

## TL;DR

Bad news for Kali Linux users! In the coming day(s), `apt update` is going to fail for pretty much everyone out there:

```
Missing key 827C8569F2518CC677FECA1AED65462EC8D5E4C5, which is needed to verify signature.
```

Reason is, we had to roll a new signing key for the Kali repository. **You need to download and install the new key manually**, here’s the one-liner:

```
┌──(kali㉿kali)-[~]
└─$ sudo wget https://archive.kali.org/archive-keyring.gpg -O /usr/share/keyrings/kali-archive-keyring.gpg
```

Now your Kali is ready to keep rolling! Sorry for the inconvenience.