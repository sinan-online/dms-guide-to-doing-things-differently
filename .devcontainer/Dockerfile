FROM pandoc/latex:3.7.0.2-ubuntu

# Install tools for better DX (optional)
RUN apt update
RUN apt install -y git
RUN apt install -y vim
RUN apt install -y zsh
RUN apt install -y texlive-full
RUN rm -rf /var/lib/apt/lists/*


RUN tlmgr init-usertree
RUN tlmgr install \
    enumitem \
    gensymb \
    hang \
    numprint \
    tcolorbox \
    pdfcol \
    ragged2e \
    tocloft \
    titlesec \
    multitoc \
    lettrine \
    cfr-initials \
    initials \
    contour \
    tikzfill \
    gillius \
    xkeyval \
    bookman \
    fontaxes \
    kpfonts \
    keycommand \
    xstring \
    xkcdcolors \
    mdframed \
    zref \
    needspace \
    titling

RUN tlmgr install \
    courier


RUN tlmgr update --self --all

# Set working directory
WORKDIR /workspace
