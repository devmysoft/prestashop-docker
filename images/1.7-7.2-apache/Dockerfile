FROM devmysoft/prestashop-base:7.2-apache
LABEL maintainer="DEVMYSOFT <contact@devmysoft.fr>"

ENV PS_VERSION 1.7.6.3

# Get PrestaShop
ADD https://www.prestashop.com/download/old/prestashop_1.7.6.3.zip /tmp/prestashop.zip

# Extract
RUN mkdir -p /tmp/data-ps \
	&& unzip -q /tmp/prestashop.zip -d /tmp/data-ps/ \
	&& bash /tmp/ps-extractor.sh /tmp/data-ps \
	&& rm /tmp/prestashop.zip


#docker image build -t prestashop:1.7-7.2-apache .
#docker image tag prestashop:1.7-7.2-apache devmysoft/prestashop:1.7-7.2-apache
#docker image push devmysoft/prestashop:1.7-7.2-apache