# images/ipfix-collector

This Docker image is based on Ubuntu 18.04 which includes an IPFIX collector based on [libipfix](http://libipfix.sourceforge.net/), a C library.
In this image, IPFIX collector listening on tcp:4739 port.

libipfix package is downloaded from https://svwh.dl.sourceforge.net/project/libipfix/libipfix/libipfix-impd4e_110224.tgz

New version of the image can be built and pushed to Dockerhub using following instructions:

```bash
cd build/images/ipfix-collector
docker build -t antrea/ipfix-collector:$TAG .
docker push antrea/ipfix-collector:$TAG
```

The `docker push` command will fail if you do not have permission to push to the
`antrea` Dockerhub repository.
