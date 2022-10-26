# <center>Choose Products You Want</center>

### Background

---

Product hunt is a website dedicated to discovering product brilliance, where individuals and officials can upload their products (products including hardware and software, across various platforms, and various use cases) to the platform for public voting.

<img src="./images/1.jpg" width="60%" height = "50%" />

<center> Fig1. Portal of Product hunt</center>

[^此处我为AI Persona投了票]: Here I voted for AI Persona

Andrew Thompson and collaborators created a dataset of 76,000+  products in ***Product hunt*** . The dataset includes the name, description, launch date, upvote count, and other details for every product from 2014 to 2021 in the platform’s sitemap. **The prototype of the visualization we found was created based on this dataset.**  [The datasets are available here](https://components.one/datasets/product-hunt-products)



### Why is this story so appealing?

---

Our lives are full of all kinds of products, and sometimes we have a headache about which product is more suitable for us. For example, when we want to install a gaming platform, it seems difficult to choose between using Steam or Origin; When we were looking for a simple but reliable text editor, we were often jumbled by a dizzying array of products on the market. At this time, the existence of  Product hunt seems to be significant, because users can easily learn about the recognized (and often excellent) product and experience it for themselves. However, querying the website always requires a lot of effort (you need to register, and many times the query information is not intuitive...), at this time, a good visualization is particularly important, it can help people quickly get **Product hunt information on this website, our selected visualization to be improved is one of them.



### How products are displayed and what can we gain from the plot?

---

The image below is our selection of *** visualizations to be improved***

 [Link to the original visualization](https://twitter.com/npechl/status/1578845494477889536@Polaris)

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\Rplot.png" width="80%" height = "80%" />

<center> Fig2. Original Visualization</center>

This visualization shows the number of likes on products in the dataset from 2014 to 2022, with variables such as time, number of likes, and rank. Each dot represents a different product. The horizontal axis is the time of product release, which is measured in years and ranges from 2014-2022. The vertical axis is the number of likes, and the coordinate axis is <u>uneven</u>, showing the vertical axis coordinates of 100, 1000, and 10000, respectively. At the same time, rank represents the ranking of the number of likes in the time period, that is, rank1 represents the product with the first number of likes in the same period, and rank2 represents the product with the second number of likes in the same period. The author categorized the visualizations by rank to create several subgraphs.

For example, the editor I used to edit the Markdown document, Typora, can also be found on the website:

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\2.jpg" width="60%" height = "80%" />

<center> Fig3. Typora</center>

[^这个软件总共获得了649个投票，rank为2，发布于2019-01]: This software received a total of 649 votes, with a rank of 2, and was released in 2019-01

For example, the representative point of the Typora product will probably appear in this position in the figure:

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\3.jpg" width="30%" height ="30%"/>

<center> Fig4. Typora point on the plot</center>

Let's first reproduce the old one, and the reproduction diagram is as follows:

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\test1.svg" width="80%" height ="80%"/>

<center> Fig5. Visualization Replication</center>



###  Awesome troubles in the graph

---

But in observation, we found problems:

* First of all, users need comparisons that are not different types of products over the same period, which may make sense for data developers but are meaningless to users.

* Secondly, the graph shows too many data points and stacks between data points, numerous labels, which does not meet the principle of simplicity, according to the principle of proximity, without reading carefully, the reader may mistake the complex stacked data points for some products of the same category, in fact, they are not related.

* Finally, the use of curves in the figure is not labeled, which leads to ambiguity, and users may wonder about the true meaning of the curve, which violates cognitive theory.





### See what can we do to improve it!

---
We also improved some small details to **make the picture look more beautiful**.

 1. We have a lot of dots stacked together in our diagram. **How do we make the chart look less cluttered?**

* **Add borders** to the dots; the borders should be darker than the fill color so that each dot can be seen clearly.

* **Set transparency** (0.9) for the non-Top dots. This will give a more layered stack of dots.

* **Use an unsaturated color as the fill color for the dots**, as often, a large area of saturated colors can look unattractive.



 2. How will we **highlight the difference** between Top and non-Top dots?

- **Use contrasting colors**, which should be of the same color family.

- Contrasting colors should satisfy **the progressive relationship**, from light to dark should be: Fill color of non-Top dot < Fill color of Top dot < Color of non-Top dot border < Color of Top dot border

- Contrast color selection. For **how the four colors should be selected**, I refer to a [color matching website](![img](file:///C:\Users\86156\AppData\Roaming\Tencent\QQ\Temp\%W@GJ$ACOF(TYDYECOKVDYB.png)http://colormind.io/), which proposes the theme colors that appear in a certain photography collection, a documentary, through a deep learning approach.
       

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\4.jpg" width="50%" height ="50%"/>

<center> Fig6. The dots we use</center>



<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\5.jpg" width="60%" height ="60%"/>

<center> Fig7. The color scheme derived from deep learning</center>



### Let's see the amazing achievements! 

---

<img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\test3.svg" width="100%" height ="100%"/>

<center> Fig8. Visualization Replication</center>

**Description of new plot**

This visualisation shows the number of likes for products in the dataset for the years 2014-2022, with the variables time, number of likes and product category. The horizontal axis is time, which is measured in years and ranges from 2014-2022. the vertical axis is the number of likes, and the axes are represented linearly, showing the vertical axis coordinates from 0 to 5000 respectively. The product categories represent the position of the product and the systems it can be used on, namely design tools, developer tools, iPhone, mac, windows, and others. we have grouped the visualizations by category labels to create several sub-graphs.

**Access to content**
For example, when we are new to design, we feel overwhelmed by the number and iterations of design products on the market. So we look online for relevant and good design software. At this point, we found two diagrams, the original and an improved one.

<center><figure class="half">     <img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\Rplot.png" width="80%"/>     <img src="D:\OneDrive - childishcherry\桌面\信息可视化assignments\project2\images\test3.svg" width="80%"/> </figure>
</center>

<center> Fig9. Comparison of the old plot and new plot</center>

When we saw the original diagram, we were overwhelmed by the comparison of different products in the same period and the extremely dense and indistinguishable dots, making it impossible to compare the merits of the design software and whether we needed it or not.

When we looked at the improvement chart, we first extracted our needs by simply looking at the 'design tools' column. Then, as the top software is prominently identified and named, we can easily target the software we need, e.g. 'remove.bg'.

It is clear that the improved graph is more user-friendly and easier to extract valid information.



### Conclusion

----

In the course of a detailed restoration of the original image. By analyzing the shortcomings of the original diagram, the group has optimized its classification methods, color labeling, highlighting, and aesthetics of the interface. The user-friendly interface makes it easier and more convenient to extract valid information and improves the efficiency of the search.



