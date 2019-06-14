
# <font color=#4285f4>动</font><font color=#ea4335>态</font><font color=#fbbc05>图</font><font color=#4285f4>表</font><font color=#34a853>绘</font><font color=#ea4335>制</font>

✅**环境配置：**

    获取pyecharts：

    1️⃣pip install pyecharts

    2️⃣git clone https://github.com/pyecharts/pyecharts.git
      cd pyecharts
      pip install -r requirements.txt
      python setup.py install

✅**基础内容**
    
    pyecharts以基于python和echarts生成html的形式运作；
    配置项分为系列设置项（具体系列）和全局设置项（图中区域）
    更多教程：
    ✅pyecharts：https://pyecharts.org/#/zh-cn/
    ✅echarts：https://echarts.baidu.com/option.html
![image.png](attachment:image.png)
    


✅**已封装应用charts_input.py**    

    基于已经探索的图表绘制案例，封装了以下几类的图表模板：  

1️⃣<font color=#376956>Line : 折线图</font>

      数据格式：date,num||分别为日期，数量

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/1.png)


2️⃣<font color=#376956>Bar : 柱状图</font>

      数据格式：date,num||分别为日期，数量

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/2.png)


3️⃣<font color=#376956>bar_and_line : 柱状图与折线图组合</font>

      数据格式：date,bar_num,line_num||分别为日期，柱状图数量，折线图数量

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/3.png)

4️⃣<font color=#376956>Area_and_line: 面积图和折线图组合</font>
      
      数据格式：date,area_num,line_num||分别为日期，面积图数量，折线图数量

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/4.png)


5️⃣<font color=#376956>trans-map: 基于地图包的迁徙图</font>

      数据格式：From,To||起点，终点

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/5.png)


6️⃣<font color=#376956>trans-Bmap: 基于百度地图的迁徙图</font>

      数据格式：coorlist||经纬度（若i+1=i则自动省略）

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/6.png)


7️⃣<font color=#376956>Bmap_Point: 基于百度地图的散点图（带日期系列的轮播）</font>

      数据格式：idate,ihour,coordinate_source,coordinate||分别为日期，小时，经纬度类型，经纬度

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/7.png)


8️⃣<font color=#376956>customize: 自定义-用于修改源码测试</font>

      数据格式自定义
      基于已有的形式，配置更多设置，并完成渲染

✅**基础用法**

    在shell进去根目录，找到charts_input.py
    
    1️⃣shell运行，通过输入图表编号和数据目录完成图表建立

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/run.png)


    2️⃣直接打开python文件,赋值

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/python_run.png)
    

✅**其他说明**
    
⚠️**base文件夹存放两个方法：**
        ----chart_class.py  存放封装的图表类
        ----wgs2bd.py       存放经纬度转换方法
    
⚠️**demo_data文件夹存放了每个图表的demo，序号对应**

⚠️**目前定制8个类，输入编号超出8会提示check type！**

⚠️**数据文件支持xlsx、txt、csv，暂时请按要求格式导入（因为采用的是列的index进行读取）**

⚠️**生成html文件存放于render_html文件中**

⚠️**图表7-百度地图散点图中，源码不支持自定义的经纬度，故需要修改源码：**

    找到python包路径site-pacakge下pyecharts/charts/basic_charts/bmap.py打开
    
    ⚠️找到_feed_data()中if判断，加入
        elif type_ == 'scatter':
            result = data_pair

![avatar](https://raw.githubusercontent.com/kiverc/visual/master/picture/bmap_point_code.png)


                                             ▶️未完待续...


```python

```
