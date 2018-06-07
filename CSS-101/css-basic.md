* css
** css selectors
*** 什么是css selectors
**** 官方定义： CSS selectors define the elements to which a set of CSS rules apply.
**** 通俗讲法 ： 选出你想要修改的元素，进行css的修改. 
*** selectors type(css specification level3)
**** type selector https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors
**** id selector https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors
**** class selector https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors
**** attribute selector https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors
**** universal selector (课后阅读https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)
*** Combinators(https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors -- Combinators)
*** selector combination
**** css 选择器可以进行组合来选出我们的元素
**** 选择器权重表 a,b,c,d
     - 行内样式 a=1
     - b=ID选择器数量
     - c=类/伪类/属性选择器数量
     - d=类型选择器和伪元素选择器数量
**** 
    | 选择器     | 特殊性  | 以10为基数的特殊性 |
    |------------+---------+--------------------|
    | Style=""   | 1,0,0,0 |               1000 |
    | #foo #bar  | 0,2,0,0 |                200 |
    | #foo .bar  | 0,1,1,0 |                110 |
    | div#foo    | 0,1,0,1 |                101 |
    | #foo       | 0,1,0,0 |                100 |
    | p.foo .foo | 0,0,2,1 |                 21 |
    | p.foo      | 0,0,1,1 |                 11 |
    | div p      | 0,0,0,2 |                  2 |
    | p          | 0,0,0,1 |                  1 |
**** 同级权重下，后定义的会覆盖先定义的.
*** https://flukeout.github.io/ (1-8)
*** BEM (block element modifier)
**** What is BEM --- Naming Convention
**** 基本概念http://getbem.com/introduction/
***** block footersummary
***** Element footersummary__primary-button
***** modifier footersummary__primary-button--ghost
**** Example FooterSummary [[http://dotrez-dev.uat.jetstar.com/docs/uitoolkit/storybook/?knob-selectedItem=0&selectedKind=ui%2FFooterSummary&selectedStory=page%20type&full=0&down=1&left=1&panelRight=1&downPanel=storybooks%2Fstorybook-addon-knobs][FooterSmuuary]]

** 伪元素 伪类
*** 伪元素 ::before ::after https://codepen.io/hateonion/pen/qoZyyb
*** 伪类 :active :hover 
