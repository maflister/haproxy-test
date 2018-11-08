# haproxy-test

```
docker build -t eg_sshd .
docker run -d -P --name test_sshd1 eg_sshd
docker run -d -P --name test_sshd2 eg_sshd
docker build -t my-haproxy .
docker run -it --rm --name haproxy-syntax-check my-haproxy haproxy -c -f /usr/local/etc/haproxy/haproxy.cfg
docker run -d --name my-running-haproxy my-haproxy
```
