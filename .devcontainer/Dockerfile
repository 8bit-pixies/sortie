# x86_64 base
FROM quay.io/pypa/manylinux2014_x86_64 as base-amd64

RUN curl --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
RUN yum install -y libffi-devel openssh-clients
RUN yum install -y openssl openssl-devel
RUN python3.8 -m pip install cffi maturin \
    && python3.9 -m pip install cffi maturin \
    && python3.10 -m pip install cffi maturin \
    && python3.11 -m pip install cffi maturin \
    && python3.12 -m pip install cffi maturin \
    && mkdir /io
