# shortcode拓展(四)

<!--more-->
---
# shortcode拓展(四)

### mapbox

#### `mapbox` 示例

```markdown
{{</* mapbox 121.589 38.910 12 */>}}
或者
{{</* mapbox lng=121.589 lat=38.910 zoom=12 */>}}
```

代码效果

{{< mapbox lng=121.589 lat=38.910 zoom=12 >}}

#### 自定义样式 `mapbox` 示例

```markdown
{{</* mapbox 126.979 37.564 8 false "mapbox://styles/mapbox/streets-zh-v1" */>}}
或者
{{</* mapbox lng=126.979 lat=37.564 zoom=8 marked=false light-style="mapbox://styles/mapbox/streets-zh-v1" */>}}
```

代码效果

{{< mapbox 126.979 37.564 8 false "mapbox://styles/mapbox/streets-zh-v1?optimize=true" >}}


### music

```markdown
{{</* music auto="https://music.163.com/#/playlist?id=2524387" */>}}
或者
{{</* music "https://music.163.com/#/playlist?id=2524387" */>}}
```

代码效果

{{< music "https://music.163.com/#/playlist?id=2524387" >}}

### B站视频

```markdown
{{</* bilibili BV1764y1D7fD */>}}
或者
{{</* bilibili id=BV1764y1D7fD */>}}
```

代码效果

{{< bilibili id=BV1764y1D7fD >}}

### typeit

#### 文本

```markdown
{{</* typeit */>}}
This is [CCJEE](https://dillonzq.com/)  **Journal**
{{</* /typeit */>}}
```

代码效果

{{< typeit >}}
This is [CCJEE](https://dillonzq.com/)  **Journal**
{{< /typeit >}}

#### 自定义 HTML 标签

```markdown
{{</* typeit tag=h4 */>}}
This is [CCJEE](https://dillonzq.com/)  **Journal**
{{</* /typeit */>}}
```

代码效果

{{< typeit tag=h4 >}}
This is [CCJEE](https://dillonzq.com/)  **Journal**
{{< /typeit >}}

#### 代码

```markdown
{{</* typeit code=java */>}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{</* /typeit */>}}
```

代码效果

{{< typeit code=java >}}
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World");
    }
}
{{< /typeit >}}

#### 分组

```markdown
{{</* typeit group=paragraph */>}}
**首先**, 这个段落开始
{{</* /typeit */>}}

{{</* typeit group=paragraph */>}}
**然后**, 这个段落开始
{{</* /typeit */>}}
```

代码效果

{{< typeit group=paragraph >}}
**首先**, 这个段落开始
{{< /typeit >}}

{{< typeit group=paragraph >}}
**然后**, 这个段落开始
{{< /typeit >}}
