# pack-b2g-ubuntu

This is a example files to build ami for b2g(boot2gecko).


## requirements

- [Packer](http://www.packer.io/)
- [Ansible](http://www.ansible.com/home)


## build

```
$ packer build -var-file=aws_credentials.json ami.json
```

You need `aws_credentials.json` to build.

like this:

```
{
  "aws_access_key": "YOUR_AWS_ACCESS_KEY",
  "aws_secret_key": "YOUR_AWS_SECRET_KEY"
},
```

also you can give the values with `-var` option.

```
$ packer build\
  -var 'aws_access_key=YOUR_AWS_ACCESS_KEY'\
  -var 'aws_secret_key=YOUR_AWS_SECRET_KEY'\
  ami.json
```


## resources

- [Firefox OS build prerequisites - Mozilla | MDN](https://developer.mozilla.org/en-US/Firefox_OS/Firefox_OS_build_prerequisites)
- [Ubuntu Cloud Images](http://cloud-images.ubuntu.com/)
