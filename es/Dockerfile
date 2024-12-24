ARG ELASTIC_VER=7.17.8
ARG SUDACHI_PLUGIN_VER=3.3.0


######################################################################
# Sudachiプラグインを入れたElasticsearchのイメージをビルドする
######################################################################
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTIC_VER}

ARG ELASTIC_VER
ARG SUDACHI_PLUGIN_VER


RUN wget http://sudachi.s3-website-ap-northeast-1.amazonaws.com/sudachidict/sudachi-dictionary-latest-core.zip && \
    wget http://sudachi.s3-website-ap-northeast-1.amazonaws.com/sudachidict/sudachi-dictionary-latest-full.zip &&  \
    unzip -o -d config/sudachi -j  'sudachi-dictionary*.zip'  && \
    rm -f sudachi-dictionary*.zip && \
    bin/elasticsearch-plugin install https://github.com/WorksApplications/elasticsearch-sudachi/releases/download/v${ELASTIC_VER}-${SUDACHI_PLUGIN_VER}/analysis-sudachi-elasticsearch${ELASTIC_VER}-${SUDACHI_PLUGIN_VER}.zip
