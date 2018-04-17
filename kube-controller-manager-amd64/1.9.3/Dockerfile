FROM gcr.io/google_containers/kube-controller-manager-amd64:v1.9.3
ENV CEPH_VERSION "luminous"
RUN rpm -i https://download.ceph.com/rpm-$CEPH_VERSION/el7/noarch/ceph-release-1-1.el7.noarch.rpm && \
  yum install -y epel-release && \
  yum install -y --nogpgcheck ceph-common && \
  yum clean all

COPY rbd-provisioner /usr/local/bin/rbd-provisioner
ENTRYPOINT ["/usr/local/bin/rbd-provisioner"]
MAINTAINER zw12078 <zn-5566@163.com>
