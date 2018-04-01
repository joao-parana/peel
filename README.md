# peel


```bash
export BUNDLE_SRC=$PWD/filter-benchmark
cd "$BUNDLE_SRC"
mvn archetype:generate -B                         \
    -Dpackage="org.peelframework.wordcount"       \
    -DgroupId="org.peelframework"                 \
    -DartifactId="peel-wordcount"                 \
    -DarchetypeGroupId=org.peelframework          \
    -DarchetypeArtifactId=peel-flinkspark-bundle  \
    -DarchetypeVersion=1.1.8
cd "peel-wordcount"
mvn clean deploy
mkdir -p bin
mv peel-wordcount-bundle/target/peel-wordcount/* bin/
export BUNDLE_BIN=$PWD/bin
cd "$BUNDLE_BIN"
# getting HELP on PEEL usage
./peel.sh -h 
```

> For details see this site: http://peel-framework.org/manual/motivation.html


