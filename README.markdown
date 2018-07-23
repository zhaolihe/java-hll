java-hll
========

detail using method please see https://github.com/aggregateknowledge/java-hll

this project which fork https://github.com/aggregateknowledge/java-hll implement the method of `exists` in hll class that to check whether having the rawValue already.

## Usage
```java
final int seed = 123456;
final Murmur3_128HashFunction hash = new Murmur3_128HashFunction(seed);
final Hasher hasher = hash.newHasher();
hasher.putLong(1L/*value to hash*/);

final long rawValue = hasher.hash().asLong();
Hll hll = new Hll(12,8);
boolean hasValue = hll.exists(rawValue);

```