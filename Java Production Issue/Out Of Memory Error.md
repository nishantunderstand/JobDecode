

||Heap|Metaspace|
|---|---|---|
|Stores|Objects / arrays|Class metadata|
|Example|`new Employee()`|Metadata of `Employee` class|
|Memory area|Heap|Native memory|
|Main limit|`-Xmx`|`-XX:MaxMetaspaceSize`|
|GC involved?|Yes|Class unloading can reclaim metadata|
|Typical OOM|`Java heap space`|`Metaspace`|




### Question:

> Is Metaspace part of Heap?

**No.**

Metaspace is **outside the Java heap** and uses native memory.