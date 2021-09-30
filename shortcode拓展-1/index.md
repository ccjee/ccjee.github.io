# shortcode拓展(一)

<!--more-->
---
# shortcode拓展(一)

### admonition

#### 注意示例

```markdown
{{</* admonition */>}}
一个 **注意** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition >}}
一个 **注意** 横幅
{{< /admonition >}}

#### 摘要示例

```markdown
{{</* admonition abstract */>}}
一个 **摘要** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition abstract >}}
一个 **摘要** 横幅
{{< /admonition >}}

#### 信息示例

```markdown
{{</* admonition info */>}}
一个 **信息** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition info >}}
一个 **信息** 横幅
{{< /admonition >}}

#### 技巧示例

```markdown
{{</* admonition tip */>}}
一个 **技巧** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition tip >}}
一个 **技巧** 横幅
{{< /admonition >}}

#### 成功示例

```markdown
{{</* admonition success */>}}
一个 **成功** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition success >}}
一个 **成功** 横幅
{{< /admonition >}}

#### 问题示例

```markdown
{{</* admonition question */>}}
一个 **问题** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition question >}}
一个 **问题** 横幅
{{< /admonition >}}

#### 警告示例

```markdown
{{</* admonition warning */>}}
一个 **警告** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition warning >}}
一个 **警告** 横幅
{{< /admonition >}}

#### 失败示例

```markdown
{{</* admonition failure */>}}
一个 **失败** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition failure >}}
一个 **失败** 横幅
{{< /admonition >}}

#### 危险示例

```markdown
{{</* admonition danger */>}}
一个 **危险** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition danger >}}
一个 **危险** 横幅
{{< /admonition >}}

#### Bug示例

```markdown
{{</* admonition bug */>}}
一个 **Bug** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition bug >}}
一个 **Bug** 横幅
{{< /admonition >}}

#### 示例

```markdown
{{</* admonition example */>}}
一个 **示例** 横幅
{{</* /admonition */>}}
```
代码效果

{{< admonition example >}}
一个 **示例** 横幅
{{< /admonition >}}

#### 引用示例

```markdown
{{</* admonition quote */>}}
一个 **引用** 横幅
{{</* /admonition */>}}
```

代码效果

{{< admonition quote >}}
一个 **引用** 横幅
{{< /admonition >}}


### link

```markdown
{{</* link "https://ccjee.github.io" */>}}
{{</* link "mailto:ccjee@mail.com" */>}}
{{</* link "https://ccjee.github.io" CCJEE-Journal */>}}
{{</* link "https://github.com/upstage/" CCJEE-Journal "点击浏览" */>}}
```

代码效果

- {{< link "https://ccjee.github.io" >}}
- {{< link "mailto:ccjee@mail.com" >}}
- {{< link "https://ccjee.github.io" CCJEE-Journal >}}
- {{< link "https://ccjee.github.io" CCJEE-Journal "点击浏览" >}}
