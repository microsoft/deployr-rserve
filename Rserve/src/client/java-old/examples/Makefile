JAVA_PREFIX=java
JAVAR=$(JAVA_PREFIX)
JAVAC=$(JAVA_PREFIX)c $(JFLAGS)
JRC_JAR=../JRclient.jar

all: jt.class t.class PlotDemo.class

jt.class: jt.java $(JRC_JAR)
	$(JAVAC) -classpath $(JRC_JAR) $<

t.class: t.java $(JRC_JAR)
	$(JAVAC) -classpath $(JRC_JAR) $<

PlotDemo.class: PlotDemo.java $(JRC_JAR)
	$(JAVAC) -classpath $(JRC_JAR) $<

run: jt.class $(JRC_JAR)
	$(JAVAR) -cp $(JRC_JAR):. jt

test: t.class $(JRC_JAR)
	$(JAVAR) -cp $(JRC_JAR):. t

clean:
	rm -rf *.class *~
