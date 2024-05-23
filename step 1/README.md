# try_pybind11

第一步，下载pybind11的源代码到step 1目录的extern下面，可以用下面的命令
```
# 假设你在 path/try_pybind11/step 1/ 这个文件夹下面
git clone https://github.com/pybind/pybind11.git extern/pybind11
```

第二步，运行cmake和make
```
mkdir build
cd build
cmake ..
cmake --build . --config Release
```
测试：
在Try_pybind\build\Release中建立一个test_example.py
import example

# 测试 add 函数
result = example.add(3, 4)
print("The result of adding 3 and 4 is:", result)


取消在test_example.py中import example中的黄色警告：
1.在 VS Code 的顶部菜单栏中，选择 文件（File）菜单，然后选择 首选项（Preferences）> 设置（Settings）。
2.在设置页面的搜索框中输入“python analysis”，这将筛选出与 Python 代码分析相关的设置。
找到 Python › Analysis: Extra Paths 选项，这里可以添加额外的路径，帮助 Python 语言服务找到你的 .pyd 文件所在的目录。
点击添加按钮（通常是一个加号），然后输入或粘贴路径 E:/Microsoft VS Code__workspace/Try_pybind/build/Release。


第三步，在python中测试使用，进入build文件夹
```
python
import example
example.add(1,1)
```
