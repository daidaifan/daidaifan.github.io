---
layout: post
title:  "Welcome to Jekyll!"
date:   2018-10-23 17:24:20 +0800
categories: jekyll update
---

Description

Implementation:
{% highlight ruby %}
class Solution:
    def minEatingSpeed(self, piles, H):
        left, right = 1, max(piles)
        while left < right:
            mid = left + (right - left) // 2
            hours = 0
            for pile in piles:
                hours += (pile // mid) + int(pile % mid != 0)
            print(left, mid, right, hours, H)
            if hours > H:
                left = mid + 1
            else:
                right = mid
        return left
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
