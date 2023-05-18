# vimrc
#### 1. 在用户自己路径下创建 .vim文件 mkdir ~/ .vim 
#### 2. 在 .vim 下创建 vimrc文件 Vim vimrc 
#### 3. 在 .vimrc文件中配置如下 

      //noremap 键盘映射 noremap修改键位
      noremap k i    
      
      //map 修改指令
      map S :W<CR>//在普通模式下 S 保存
      map s <nop>//小写s无用
      map Q ：q<CR>
      map R :source $MYVIMRC<CR>
      
      syntax on //代码高亮
      
      //set 设置功能
      set number //显示行号
      set relativenumber //让当前所在行 行号为1
      set cursorline //在每行下面显示一条线 （直观显示编辑所在位置）
      set wrap //编辑的内容不会超过显示框
      set showcmd //显示所打的命令 让自己知道
      set wildmenu //按Tab键后 可以进行选择功能（非常实用）
#### 4. vim在普通模式下的一些编辑操作
     <operation> <motion>
      在vim中的所有删除都是剪切，可按p黏贴
      u撤销上一个动作
      x删除所在光标的字符
      w光标移动到下一个单词
      d（可加数字）→ //向右删除几个字符
      d（可加数字）← //向左删除几个字符
      y(可加数字) →//向右复制几个字符
      y(可加数字) ←//向左复制几个字符
      c（change 改变）
      c w 更改下个单词 **非常有用**
