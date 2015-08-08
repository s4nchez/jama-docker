from tomcat:7.0.63-jre7

env JAMA_FILE jama-spring2015.tgz
env JAMA_DIST_URL http://www.jamasoftware.com/media/download/$JAMA_FILE
env JAMA_SHA b108a292c084b659048697d0a0b660ddb35303dc0d9b3133a11703f75144649e

RUN set -x \
	&& echo "$JAMA_SHA  jama.tgz" > jama.sha \
	&& curl -fSL "$JAMA_DIST_URL" -o jama.tgz \
	&& sha256sum jama.tgz \
	&& sha256sum -c jama.sha \
	&& tar -xzf jama.tgz -C /usr/local/tomcat/webapps \
	&& rm jama.tgz
	
