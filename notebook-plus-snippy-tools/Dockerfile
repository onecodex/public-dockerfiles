FROM quay.io/refgenomics/docker-onecodex-notebook:v0.7.2

LABEL software.version="v0.1.0"

# COPY --from=quay.io/refgenomics/samtools:1.9 /usr/local/bin/* /usr/local/bin/
# COPY --from=quay.io/refgenomics/samtools:1.9 /usr/local/lib/libhts* /usr/local/lib/

COPY --from=staphb/snippy:4.6.0 /snippy-4.6.0/binaries/linux/minimap2 /usr/local/bin/
COPY --from=staphb/snippy:4.6.0 /snippy-4.6.0/binaries/linux/samtools /usr/local/bin/
COPY --from=staphb/snippy:4.6.0 /snippy-4.6.0/binaries/linux/bcftools /usr/local/bin/
COPY --from=staphb/snippy:4.6.0 /snippy-4.6.0/binaries/linux/freebayes /usr/local/bin/
COPY --from=staphb/snippy:4.6.0 /snippy-4.6.0/binaries/linux/vt /usr/local/bin/

ENV LD_LIBRARY_PATH=/usr/local/lib

ADD snippy.sh /usr/local/bin/snippy