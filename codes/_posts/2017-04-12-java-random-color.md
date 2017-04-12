---
layout: code
title:  "Random color"
date:   2017-04-12 11:43:51 +0000
categories: java
tags: [java, random]
author: aNNiMON
---

```java
import java.util.Random;
 
public class Rand {
 
    private static final Random rnd = new Random();

    /* Random RGB Color */
    public static int randomColor() {
        return rnd.nextInt(0xffffff);
    }
 
    /* Random RGB Color from min to max */
    public static int random2Color(int min, int max) {
        final int tmp = max - min;
        final int r = min + rnd.nextInt(tmp);
        final int g = min + rnd.nextInt(tmp);
        final int b = min + rnd.nextInt(tmp);
        return (r << 16) | (g << 8) | b;
    }
}
```

Usage:

```java
g.setColor(Rand.randomColor(0, 100));
```