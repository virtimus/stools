
cd /src && git clone https://github.com/plantuml/plantuml-server
cd plantuml-server
docker image build -f Dockerfile.jetty -t plantuml-server:local .
#docker image build -f Dockerfile.tomcat -t plantuml-server:local .
docker run -d -p 8080:8080 plantuml-server:local