FROM registry.fedoraproject.org/fedora-minimal:35

RUN microdnf -y install kubernetes-client && \
    microdnf clean all

RUN curl -qSsL https://github.com/kubernetes-sigs/aws-iam-authenticator/releases/download/v0.5.3/aws-iam-authenticator_0.5.3_linux_amd64 | \
    install /dev/stdin /usr/local/bin/aws-iam-authenticator

ENTRYPOINT ["kubectl"]
