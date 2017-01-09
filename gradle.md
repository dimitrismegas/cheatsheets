* Create sources .jar in android project
```groovy
    task sourcesJar(type: Jar){
        from android.sourceSets.main.java.srcDirs
        classifier = 'sources'
    }

    artifacts {
        archives sourcesJar
    }
```    
