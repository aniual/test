##测试爬取京东商品的数据，总共100页，六千多个同类商品

#####使用说明
大家需要安装的库为：pip install selenium

1、进行url分析，https://www.jd.com/

2、搜索框中输入‘手机’url进行搜索：
https://search.jd.com/Search?keyword=%E6%89%8B%E6%9C%BA&enc=utf-8&wq=%E6%89%8B%E6%9C%BA&pvid=0a71461cbe564bfd899a363b05caed27
    开始进行页面分析：
    ![Image text](http://p9.pstatp.com/large/pgc-image/a5f12d4f007e4807ae4a02976bfbbfba)
    
    既可以查看到`<li>元素在<div id='J_goodsList'>`中
    <li class='gl-item'>可以查看到所有的手机信息
 ![Image_text](http://p3.pstatp.com/large/pgc-image/dc7122d64e4e48aea74f2c7b3c1c7214)
 
 使用xpath方法列出需要的数据：
 `find_elements_by_xpath("//div[@id='J_goodsList']//li[@class='gl-item']")`
 价格分析出来：price = li.find_element_by_xpath(".//div[@class='p-price']//i").text
 图片分析：src1 = li.find_element_by_xpath(".//div[@class='p-img']//a//img").get_attribute('src')

在将手机型号和描述展示出来：
    ![Image_text](http://p1.pstatp.com/large/pgc-image/9dda62edea2c4fd1a8ed85b521477944)

