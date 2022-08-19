# 云扩自定义类型
</br>

**Encoo.DataType.FilePath** 云扩自定义的类型，代表了一个文件,和string用法一样，在UI界面上该类型可以使用图形化方式选取文件。
</br>

**Encoo.DataType.FolderPath** 云扩自定义的类型，代表了一个文件目录，和string用法一样，在UI界面上该类型可以使用图形化方式选取目录。
</br>

**Encoo.DataType.Password** 云扩自定义的类型，代表了一个密码,和string用法一样，在UI界面上该类型会显示成暗文。
</br>

**Encoo.DataType.Selector** 云扩自定义的类型，供选择器定位元素，一般不需要自己去定义变量，选择器通常是通过UI元素录制或者是通过选择器编辑器进行修改。
</br>

**IBotTimeWebDriver** 云扩自定义的类型，绑定浏览器组件/打开浏览器组件的输出，可以将这个输出传递给其他组件，如绑定浏览器组件，关闭浏览器组件，这样这些组件就不需要再次指定元素，来到达变量的重用。 该类型本身没有其他作用，不提供额外的接口，不需要使用里面的方法和属性
</br>

**Encoo.DataType.MobileSelector** 云扩自定义的类型， 供手机选择器定位元素，一般不需要自己去定义变量，选择器通常是通过UI元素录制或者是通过选择器编辑器进行修改。
</br>

**IUiObject** 云扩自定义的类型，获取元素/等待元素出现/判断元素是否存在的输出，可以将输出传递给其他自动化组件的控件元素属性， 该类型本身没有其他作用，不提供额外的接口，不需要使用里面的方法和属性。
</br>