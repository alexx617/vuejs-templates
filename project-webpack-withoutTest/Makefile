CI_BUILD_REF_NAME = $(branch)
REF_NAME=`tr '[A-Z]' '[a-z]' <<<"$(CI_BUILD_REF_NAME)"`

build:
	npm run build && cd dist/static/css && mkdir static && cd .. && mv img css/static/ && cp -rf fonts css/static/

d2t: build
	$ mv ./dist ./$(REF_NAME) && tar czf MIDTrade.tar ./$(REF_NAME) && scp MIDTrade.tar test@1.16.19.1:~/ && ssh test@1.16.1.1 "tar xvzf MIDTrade.tar -C /opt/weixin/zhongpan/public"

buildProd:
	TARGET=prod npm run build && cd dist/static/css && mkdir static && cd .. && mv img css/static/ && cp -rf fonts css/static/ && cd ../.. && tar czf MIDTrade_prod.tar.gz ./dist && scp MIDTrade_prod.tar.gz test@12.16.1.11:/opt/weixin/zhongpan/public

.PHONY: build
