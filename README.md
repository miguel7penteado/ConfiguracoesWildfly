# ConfiguracoesWildfly
Configurações diversas do RedHat Wildfly 8.x

# 1 - Ativando o jconsole:

## declare o endereço de escuta na interface ativa da sua máquina:
vim /opt/wildfly/8.1.0/bin/standalone.conf
JAVA_OPTS="$JAVA_OPTS -Djboss.bind.address.management=ip_servidor  "


##Linha de comando:
$JAVA_HOME/bin/jconsole -J-Djava.class.path=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/jconsole.jar:/opt/wildfly/8.1.0/bin/client/jboss-cli-client.jar

entre com o endereço: service:jmx:http-remoting-jmx://ip_servidor:9990

usuário e senha de gerenciamento.
