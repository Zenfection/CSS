# Selectors

| Selector                                                                                 | Example                    | Description                                                         | Test |
| ---------------------------------------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------- | ---- |
| [.class](https://www.w3schools.com/cssref/sel_class.asp)                                 | .`intro`                   | chọn phần tử lớp là `intro`                                         |      |
| .class1.class2                                                                           | .`name1`.`name2`           | chọn phần tử có lớp là `name1` và `name2`                           |      |
| .class1 .class2                                                                          | .`name1` .`name2`          | chọn phần tử có lớp `name2` là con của `name1`                      |      |
| [#id](https://www.w3schools.com/cssref/sel_id.asp)                                       | #`firstname`               | chọn phần tử có ID là `firstname`                                   |      |
| [\*](https://www.w3schools.com/cssref/sel_all.asp)                                       | *                          | chọn tất cả phần tử                                                 |      |
| [element](https://www.w3schools.com/cssref/sel_element.asp)                              | `p`                        | chọn tất thẻ `p`                                                    |      |
| [element.class](https://www.w3schools.com/cssref/sel_element_class.asp)                  | `p`.`intro`                | chọn tất cả thẻ `p` có lớp là `intro`                               |      |
| [element,element](https://www.w3schools.com/cssref/sel_element_comma.asp)                | `div`,`p`                  | chọn tất cả thẻ `p` và phần tử trong lớp `intro`                    |      |
| [element element](https://www.w3schools.com/cssref/sel_element_element.asp)              | `div` `p`                  | chọn tất cả thẻ  `p` nằm trong thẻ `div`                            |      |
| [element>element](https://www.w3schools.com/cssref/sel_element_gt.asp)                   | `div` > `p`                | chọn tất cả thẻ `p` mà mà có `div` là cha                           |      |
| [element+element](https://www.w3schools.com/cssref/sel_element_pluss.asp)                | `div` + `p`                | chọn thẻ `p` đầu tiên được đặt ngay sau thẻ `div`                   |      |
| [element1\~element2](https://www.w3schools.com/cssref/sel_gen_sibling.asp)               | `p` ~ `ul`                 | chọn tất cả thẻ `ul` đứng sau thẻ `p`                               |      |
| [[attribute]](https://www.w3schools.com/cssref/sel_attribute.asp)                        | [`target`]                 | chọn tất cả các phần tử có thuộc tích `target`                      |      |
| [[attribute=value]](https://www.w3schools.com/cssref/sel_attribute_value.asp)            | [`target`=`_blank`]        | chọn tất cả các phần tử có thuộc tính `target`, giá trị là `_blank` |      |
| [[attribute\~=value]](https://www.w3schools.com/cssref/sel_attribute_value_contains.asp) | [`title`~=`flower`]        |                                                                     |      |
| [[attribute\|=value]](https://www.w3schools.com/cssref/sel_attribute_value_lang.asp)     | [`lang`\|=`en`]            |                                                                     |      |
| [[attribute^=value]](https://www.w3schools.com/cssref/sel_attr_begin.asp)                | `a`[`href`^=`"https"`]     |                                                                     |      |
| [[attribute\$=value]](https://www.w3schools.com/cssref/sel_attr_end.asp)                 | `a`[`href`\$="`.pdf`"]     |                                                                     |      |
| [[attribute\*=value]](https://www.w3schools.com/cssref/sel_attr_contain.asp)             | `a`[`href`\*="`w3school`"] |                                                                     |      |
| [:active](https://www.w3schools.com/cssref/sel_active.asp)                               | `a:active`                 |                                                                     |      |
| [::after](https://www.w3schools.com/cssref/sel_after.asp)                                | `p::after`                 |                                                                     |      |
| [::before](https://www.w3schools.com/cssref/sel_before.asp)                              | `p::before`                |                                                                     |      |
| [:checked](https://www.w3schools.com/cssref/sel_checked.asp)                             | `input:checked`            |                                                                     |      |
| [:default](https://www.w3schools.com/cssref/sel_default.asp)                             | `input:default`            |                                                                     |      |
| [:disabled](https://www.w3schools.com/cssref/sel_disabled.asp)                           | `p:empty`                  |                                                                     |      |
| [:enabled](https://www.w3schools.com/cssref/sel_empty.asp)                               | `input:enabled`            |                                                                     |      |
| [:first-child](https://www.w3schools.com/cssref/sel_firstchild.asp)                      | `p:first-child`            |                                                                     |      |
| [::first-letter](https://www.w3schools.com/cssref/sel_firstletter.asp)                   | `p::first-letter`          |                                                                     |      |
| ::first-line                                                                             |                            |                                                                     |      |
| :first-of-type                                                                           |                            |                                                                     |      |
| :focus                                                                                   |                            |                                                                     |      |
| :fullscreen                                                                              |                            |                                                                     |      |
| :hover                                                                                   |                            |                                                                     |      |
| :in-range                                                                                |                            |                                                                     |      |
| :indeterminate                                                                           |                            |                                                                     |      |
| :invalid                                                                                 |                            |                                                                     |      |
| :lang(*language*)                                                                        |                            |                                                                     |      |
| :last-of-type                                                                            |                            |                                                                     |      |
| :link                                                                                    |                            |                                                                     |      |
| ::marker                                                                                 |                            |                                                                     |      |
| :not(*selector*)                                                                         |                            |                                                                     |      |
| :nth-child(*n*)                                                                          |                            |                                                                     |      |
| :nth-last-of-type(*n*)                                                                   |                            |                                                                     |      |
| :nth-of-type(*n*)                                                                        |                            |                                                                     |      |
| :only-of-type                                                                            |                            |                                                                     |      |
| :only-child                                                                              |                            |                                                                     |      |
| :optional                                                                                |                            |                                                                     |      |
| :out-of-range                                                                            |                            |                                                                     |      |
| ::placeholder                                                                            |                            |                                                                     |      |
| :readonly                                                                                |                            |                                                                     |      |
| :read-only                                                                               |                            |                                                                     |      |
| :read-write                                                                              |                            |                                                                     |      |
| :required                                                                                |                            |                                                                     |      |
| :root                                                                                    |                            |                                                                     |      |
| ::selection                                                                              |                            |                                                                     |      |
| :target                                                                                  |                            |                                                                     |      |
| :valid                                                                                   |                            |                                                                     |      |
| :visited                                                                                 |                            |                                                                     |      |
