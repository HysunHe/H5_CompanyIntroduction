组件化开发web项目

首先组件化在于页面大幅度差不多，就可以抽取一个base界面出来

- loader 对象初始化
- addPage  增加一个新页
- addComponent新增一个组件


###添加页面：

         使用jq append(dom元素) 





##### 1.在body元素添加子元素H5也就是整个组件化模板元素

	this.el=$('<div class="h5" id="'+this.id+'">')
	$('body').append(this.el);

##### 2.模板元素添加Page(子页面)元素

    var page=$('<div class="h5_page section">');
    this.el.append(page);



##### 3.子页面添加Component(子组件)元素

    var component=$('<div class="h5_component '+cla+' h5_component_name_'+name+'" id="'+id+'">');
    page.append(component);




知识点：

链式调用，和组件的封装(基础组件,散点图，柱状图，折线图，雷达图，饼状图)