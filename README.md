jets3t
======

hadoop s3 filesystem custom fix.                                                                                                          

Modify hadoop s3 filesystem endpoint 
======

```
$ cat >/tmp/jets3t.properties << EOF
s3service.s3-endpoint=s3.nctu.edu.tw
s3service.https-only=false
s3service.s3-endpoint-http-port=80
s3service.disable-dns-buckets=true
storage-service.disable-live-md5=true                                                                                                    
EOF
$ cd /tmp
$ sudo zip -r /usr/lib/hadoop/hadoop-core-*.jar . -i jets3t.properties
```

Source Code Link
======
 - [jets3t.0.6.1] 

[jets3t.0.6.1]: http://grepcode.com/snapshot/repo1.maven.org/maven2/net.java.dev.jets3t/jets3t/0.6.1
