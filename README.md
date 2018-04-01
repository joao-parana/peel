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
cd "$BUNDLE_BIN/peel-wordcount"
```
