WebServer:
Ir para a pasta webserver/Projeto_CNV/src
Em primeiro lugar � necess�rio fazer: export _JAVA_OPTIONS="-XX:-UseSplitVerifier"
Depois � preciso fazer o export do classpath para a biblioteca da Amazon

Para ser mais r�pido testar n�s criamos um script que compila e corre a tool e o server.
Claro que tamb�m poder� ser testado colocando em /etc/rc.local e fizemos testes assim mas por enquanto, 
como h� altera��es constantes no c�digo, achamos mais conveniente utilizar este script.
Para correr basta fazer "bash compile.sh" que faz as seguintes opera��es por ordem:
- Compila a nossa tool de instrumenta��o (InstTool.java)
- Compila o IntFactorization.java
- Compila o WebServer.java
- Corre a nossa tool de instrumenta��o no IntFactorization
- Corre o WebServer

LoadBalancer:
export do classpath para a biblioteca da Amazon
Ir para a pasta loadbalancer\src
javac *.java para compilar
java LoadBalancer para correr o LoadBalancer

Para fazer pedidos de fatoriza��o:
http://IPPublicoLoadBalancer:8000/f.html/n?=NumeroPretendido