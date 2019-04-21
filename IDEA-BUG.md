# IDEA 遇到的bug及解决 

##  非法字符:'\ufeff'  
*  问题:  
![with-bom]{https://raw.githubusercontent.com/baldass/gitstudy/master/idea/idea-withBOM-bug.png}  
> 解决: 这个err是由于File Encodings的BOM for new UTF-8 files设置为with BOM的关系,把文件转成无BOM的UTF-8就OK了。  
> 1. File=>settings=>Editor=>File Encodings=>将BOM for new UTF-8 files设置为with NO BOM  
> 2. 右键项目选择Remove BOM,重启项目一般就可以了           
> 3. 要是仍然不行则可以用Notepad++ 将文件修改编码为UTF-8 with no BOM  
