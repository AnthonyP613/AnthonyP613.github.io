---
layout: post
title: "[Swift_UIKit] Setting Content Inset to Custom"
subtitle: "If you have space between border and content, unknowingly"
categories: Swift
tags: [Swift, Storyboard, UIKit, ContentInset]
---

## Content Insets
> From [Apple doc][apple-dev-doc] 
> The custom distance that the content view is inset from the safe area or scroll view edges.

[apple-dev-doc]: https://developer.apple.com/documentation/uikit/uiscrollview/1619406-contentinset

When following [100 Days of Swift][100-of-swift], You could find something different between your result and the tutorial's 

[100-of-swift]: https://www.hackingwithswift.com/100

In my case, It was a space between content view and button edges. 

![image](/assets/images/in_posts/220614_Flags.png "problematic example image")

Thinking It would be caused by version difference, and updates from versions. 
Anyway, the key point for making a fittable border, with pictures is setting Content Inset to Custom. (but without changing any values)

![image](/assets/images/in_posts/220614_ContentInsets.png "solution image")

### UIEdgeInsetsZero
According to the [document][apple-dev-doc-for-default]  
> An edge insets struct whose top, left, bottom, and right fields are all set to 0.

[apple-dev-doc-for-default]: https://developer.apple.com/documentation/uikit/uiedgeinsetszero

Still not understandable, but setting Custom (with same value of Default) from Default makes the border without any white spaces.

If you watching old version of Video, implementing something comparatively in a new env, hope Content Insets setting could be helpful to resolve your issue.


#### References 

- Apple Dev Docs: Content Insets
https://developer.apple.com/documentation/uikit/uiscrollview/1619406-contentinset
- Apple Dev Docs: UIEdgeInsetsZero
https://developer.apple.com/documentation/uikit/uiedgeinsetszero
- Positioning Content Relative to Safe Area
https://developer.apple.com/documentation/uikit/uiview/positioning_content_relative_to_the_safe_area

