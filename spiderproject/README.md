##������ȡ������Ʒ�����ݣ��ܹ�100ҳ����ǧ���ͬ����Ʒ

#####ʹ��˵��
�����Ҫ��װ�Ŀ�Ϊ��pip install selenium

1������url������https://www.jd.com/

2�������������롮�ֻ���url����������
https://search.jd.com/Search?keyword=%E6%89%8B%E6%9C%BA&enc=utf-8&wq=%E6%89%8B%E6%9C%BA&pvid=0a71461cbe564bfd899a363b05caed27
    ��ʼ����ҳ�������
    ![Image text](http://p9.pstatp.com/large/pgc-image/a5f12d4f007e4807ae4a02976bfbbfba)
    
    �ȿ��Բ鿴��`<li>Ԫ����<div id='J_goodsList'>`��
    <li class='gl-item'>���Բ鿴�����е��ֻ���Ϣ
 ![Image_text](http://p3.pstatp.com/large/pgc-image/dc7122d64e4e48aea74f2c7b3c1c7214)
 
 ʹ��xpath�����г���Ҫ�����ݣ�
 `find_elements_by_xpath("//div[@id='J_goodsList']//li[@class='gl-item']")`
 �۸����������price = li.find_element_by_xpath(".//div[@class='p-price']//i").text
 ͼƬ������src1 = li.find_element_by_xpath(".//div[@class='p-img']//a//img").get_attribute('src')

�ڽ��ֻ��ͺź�����չʾ������
    ![Image_text](http://p1.pstatp.com/large/pgc-image/9dda62edea2c4fd1a8ed85b521477944)

