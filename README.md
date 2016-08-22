# You don't know CSS

Talk about drafts no one usually cares. 

1.  Hi, I am Anton, frontender at VAIMO. And I actually think that most of you don't know CSS.
2.  When was last time you read drafts?
3.  A month ago?
4.  Half a year ago, maybe?
5.  A year ago?
6.  If question «what drafts» has crossed your mind …
7.  You don't know css.
8.  So what drafts and where to find them?
9.  CSS Working Group Editor Drafts. You may find them here.
10. From this page snapshots of drafts from time to time are moved to …
11. CSS Working Group, which may be find here.
12. This marks — specification stages.
13. They are parts of specification life cicle. From draft to recommendation. There are more stages, than you see here, and you may read about them in the corresponding document.
14. Any vendor has feature roadmap.
15. webkit
16. Can be found here
17. blink
18. here
19. Even EDGE has its cool feature roadmap site
20. here
21. And only Firefox has simple document 
22. that may be found here
23. Until this year, when they also created cool new site … with uncomplete data
24. that may be found here. I hope they will improve it any time soon.
25. Let's just get to the point!
26. Did you know there is such thing as motion path module?
27. It allows you to assign motion path to element. Theoretically it may be url, shape functions or path, but in fact at the moment only path is working properly. For exmaple this one, with four points. It looks like that:
28. Let this red square be our element.
29. We may set its position with 'motion-offset' property. 
30. Like that.
31. And the nicest thing that we may animate it.
32. Moreover — element turns according to the path.
33. It can be done with motion-rotation: auto; but if we set ninety degrees angle it will look 
34. like that
35. And if we set reverse as a value 
36. it will move back to front.
37. And, naturally, this properties have shortcard: motion. With path, start point and rotation mode.
38. This can be used in landings, advertisements, you name it.
39. At the moment draft supported only by blink engine. 
40. You may read more about in the specification.
41. Ok, now what do you know about images?
42. Do you know about object-fit and object-position?
43. For example we have this image with paddington bear. I mean 'img' element.
44. When we define size for img element without object-fit and with aspect ratio different from image ratio it will be distorted. But you may fix this little problem if you set object-fit to cover and set appropriate object-position. This properties work a lot like backround-size keywords.
45. It's supported everywhere but IE. Let's hope they'll catch up soon.
46. Until that moment you may use polyfill
47. You may read more about this properties here:
48. Also did you know that you can use one element as background of another? With 'element' function.
49. Let's me show how it works. I have set element, that contains this article, as background to this element and now I may show what part of article is currently in the view.
50. Element function is supported only by gecko engine. 
51. You may read about this here. 
52. Let's move on. We are living at the world of wearables now. And some of them have round displays. Did you know that now there is draft to handle them?
53. I have chatted with Hyojin Song — one of two draft editors. Both of them work in LG. First of all, this spec is more for applications then for browsers. This is css specification, so we are talking about application on the html/css/js basis. 
54. So we are talking about web-based OS. Major platforms are Tizen by Samsung, webOS by LG and Firefox OS by Mozilla.
55. Firefox OS. I have smartphone with this one. 
56. But in twenty fifteen Mozilla anounced epic failure of smartphone experiment and switched to internet of things. It sound like a obituary of commercial version of OS to me, so now we have
57. Boot to gecko os, which may be used by anyone. Anyone may create wearables on the basis of this OS.
58. I have spoken with guys from community and it looks like no one wants to. 
60. About Tizen — they already have two watch models
61. And one of them — WITH ROUND DISPLAY!
62. And, finally, Web OS from LG, the maintainer of specification,
63. They have great watches with LTE internet connectivity which was highly rated at last CES.
64. At the moment Tizen has some market share and I believe WebOS also will get one in the future. 
65. Ok, but how do we know if display is round?
66. With media query. In html.
67. Or CSS.
68. But I can't find it in media queries level 4.
69. And how to handle content in the round display? If you have tried to put content in the container with border-radius one hundred percents you know that content will be cropped.
70. With shape-inside: display 
71. We may make content flow around display borders like that
72. shape-inside is defined in css shapes module, but it is not supprted by any browser. I have used shape-outside to emulate it. And there is no such value as display at spec.
73. But what about borders? Are they cropped?
74. Not if we are using border-boundary: display;
75. Border will wrap like that.
76. And, yep, no mentioning in the borders module specification.
77. What about origin? Does it exist?
78. Guys from LG propose to use polar coordinates instead of decard system.
79. in this system point is described as radius and rotation angle around origin. 
80. You are setting position: polar; angle, radius, origin coordinates in decard system and anchor at the element.
81. Nope, positioned layout module does not contain any information about polar value yet.
82. But currently there are discussion at blink community about implementation of this spec.
83. Until then you may play with polyfill in chrome.
84. Create weather app which support both round and square display.
85. Imagine how facebook app may look. And even play with content presentation in display of different shape.
86. You may read about it there.
87. Let's talk about scroll snap — new cool feature.
88. It allows us to snap scroll to elements. In current version of specification for container element we should set scroll-snap-type to mandatory if we want always snap scroll to element and to proximity if we want snap scroll to element only if we scroll aproximately to the snap point. scroll-snap-stop define may we scroll more then one scroll snap point at time. For elements in the container we should set scroll-snap-margin if we set scroll-snap-type to proximity. That property defines proximity area. And scroll-snap-align to defined wich part of element should stick to the container.
89. But in the real world old specification is implemented. We may snap to grid there. We should only set snap-points-* property to specific value or set repeat function to the container. And we may set scroll-snap-coordinate to child element.
90. It works like this. In the left column we may scroll only whole lines, we can't scroll half of line. And in right — only whole news, we can't scroll half of block. And I think it nicer that way.
91. Support is quite good — only blink is not supported. But they are working on the implementation of new specification.
92. For those who want to use it — we have polyfill.
93. You may read more at the specification.
94. This dog — real mechanic.
95. And CSS is real programming language, you know.
96. It has variables.
97. You may set them as two dashes and variable name. They are strings only. Nothing fancy, but may be useful.
98. You may use var function to add value. And yes, you may use variables for values only.
99. It is already working and colors for this text were set this way
100. And IE spoils all fun. But when it starts supporting variables — well, we will have instruments to create nice themes and dry our code without preprocessors.
101. You may read more about them in the spec.
102. In the future we will be able to create custom selectors. 
103. like this. But for now it nothing but draft. No implementations yet.
104. You may read about custom selectors at CSS Extensions specification.
105. Also we may check css-feature support with native @support query, instead of modernizer.
106. It will look like this.
107. For example blink supports motion path, and doesn't support stack-sizing. But Firefox — vice versa.
108. @support is supported everywhere but old IEs. So you may just use it in most cases;
109. You may read about it here.
110. And let's talk about some typography features.
111. Did you know that with regions you may take content from one or more source-elements with flow-into and then set multiple elements where this flow should be displayed?
112. Let's see how it works. See this text? Yey! Now it under the image. Can you do it other way? 
113. Moreover if we inspect blocks we may see container flow-order. If you have worked with adobe indesign you now what is it and how it works. Imposible to design a book without such feature.
114. It is supported only in webkit and IE. IE actually supports it … well like IE usually does. Not long ago we also had blink support … but it was removed. Bruce Lawson from opera sad that they should maintaine huge amount of slow code for this feature and they will support it but later, after specification is updated.
115. You may read about regions here.
116. Do you know about wrap-flow? 
117. We may achive interesting effect with this and new GRID specification or multicolumn, like in this case. We add call-out just above multicolumn and text wraps around it. 
118. Sadly it is only supported by IE at the moment.
119. You may read more about this feature here.
120. And here you may find my presentation. This is only examples of drafts, merely an iceberg peak. If you read drafts you may predict trends, know how things will be going in the future. This is your chance to stop caching up the professional train, and start driving it. Take care. And read the drafts.
