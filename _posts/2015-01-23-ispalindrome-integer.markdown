---
layout: post
title:  "Palindrome Integer!"
date:   2015-01-23 23:55:31
categories: algorithms
---

Code for checking if an integer is a palindrome number.

{% highlight java %}
public static boolean isPalindrome(int x) {
	if (x < 0) 
		return false;
	int div = 1;
	while (x / div >= 10) {
		div *= 10;
	}        
	while (x != 0) {
		int l = x / div;
		int r = x % 10;
		if (l != r) 
			return false;
		x = (x % div) / 10;
		div /= 100;
	}
	return true;
}
{% endhighlight %}
