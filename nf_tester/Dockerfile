FROM golang:1.14.4-stretch

WORKDIR /workspace

RUN git clone --branch validations_v1.0.0 https://github.com/my5G/my5G-RANTester.git \
    && cd my5G-RANTester  \
    && go mod download 
    
# Move to the binary path
WORKDIR /workspace/my5G-RANTester/cmd

RUN go build -o app

# Config files volume
VOLUME [ "/workspace/my5G-RANTester/config" ]
