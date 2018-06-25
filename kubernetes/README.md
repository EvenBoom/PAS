# Kubernetes
## 安装与集群
网上有一篇集群的[文章](https://blog.csdn.net/real_myth/article/details/78719244)还不错，还有一篇简单部署nginx的[文章](http://www.ppzedu.com/archives/1127.html),
用centos7部署应用时遇到
```
Error syncing pod, skipping: failed to "StartContainer" for "POD" with ErrImagePull: 
"image pull failed for registry.access.redhat.com/rhel7/pod-infrastructure:latest, 
this may be because there are no credentials on this request.  
details: (open /etc/docker/certs.d/registry.access.redhat.com/redhat-ca.crt: no such file or directory)"
```
找了两天，终于在网上找到[解决方案](https://www.codetd.com/article/1013558)</br>
注意:registry.access.redhat.com/rhel7/pod-infrastructure:latest是一个kubernetes的基础镜像来的，下载不了，是缺少文件，CA认证不了
