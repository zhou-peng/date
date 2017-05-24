# date


表格中firefox的格式是符合国际标准ISO 8601的，最后紧跟大写字母“Z”表示UTC时间。

此格式“yyyy-MM-dd”字符串都是以UTC时间来进行解析的，再转变为中国标准时间（CST），加上时区（+8:00）。

后台返回的日期数据都是“-”格式的，前端js把“-”替换为“/”在进行处理，这样就可以放心使用。

“2017/09/10 10:30:50.60”带了毫秒的格式也不要用，Chrome和Opera浏览器支持。

Date对象的方法中有带“UTC”和不带的两种方法（如：getDate()，getUTCDate()；
getHours()，getUTCHours()），二者之间相差时区（+8:00）个小时。不过，我们基本只用不带“UTC”的方法。
