# es---docker
关于docker如何建立es搜索                                
1、先获取es和es-head                                
docker pull elasticsearch:6.8.4    
docker pull mobz/elasticsearch-head:5    
2、创建es容器和es-head容器
docker run -d --name es -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:6.8.4
docker create --name elasticsearch-head -p 9100:9100 elasticsearch-head:5
