---
layout: post
author: Kenar716
title: "Syntax Highlighting Jekyll"
date: 2020-03-19 12:00:00 +0545
cover: assets/images/posts/2019-07-08-measuretwicecutoncepart3/architecture-design.jpg
categories: blog
summary:
custom_css: syntax_highlighting/manni
---
**Syntax Highlighting Jekyll**

{% highlight csharp linenos %}
// reverse byte order (16-bit)
public static UInt16 ReverseBytes(UInt16 value)
{
  return (UInt16)((value & 0xFFU) << 8 | (value & 0xFF00U) >> 8);
}
{% endhighlight %}

{% highlight ruby linenos %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}
