FROM alpine:latest

RUN apk add --no-cache \
texinfo \
texlive \
texlive-xetex \
texmf-dist \
texmf-dist-formatsextra

WORKDIR /data
VOLUME ["/data"]

# docker build . -t latex:latest
# docker run --rm -v $(pwd):/data latex:latest pdflatex cposc2023.tex
# OR
# docker run --rm -v $(pwd):/data latex:latest make pdf
