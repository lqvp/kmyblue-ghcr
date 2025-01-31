FROM docker.elastic.co/elasticsearch/elasticsearch:7.17.27

RUN elasticsearch-plugin install https://github.com/WorksApplications/elasticsearch-sudachi/releases/download/v3.3.0/elasticsearch-7.17.8-analysis-sudachi-3.3.0.zip
RUN curl -Lo sudachi-dictionary-20241021-core.zip http://sudachi.s3-website-ap-northeast-1.amazonaws.com/sudachidict/sudachi-dictionary-20241021-core.zip && \
    unzip sudachi-dictionary-20241021-core.zip && \
    mkdir -p /usr/share/elasticsearch/config/sudachi/ && \
    mv sudachi-dictionary-20241021/system_core.dic /usr/share/elasticsearch/config/sudachi/ && \
    rm -rf sudachi-dictionary-20241021-core.zip sudachi-dictionary-20241021/

RUN echo '{"systemDict": "system_core.dic"}' > /usr/share/elasticsearch/config/sudachi/config.json
