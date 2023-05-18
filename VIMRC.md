# vimrc
#### 1. 在用户自己路径下创建 .vim文件 mkdir ~/ .vim 
#### 2. 在 .vim 下创建 vimrc文件 Vim vimrc 
#### 3. 在 .vimrc文件中配置如下 

      //noremap 键盘映射 noremap修改键位
      noremap k 5k
      noremap j 5j
      noremap h 7h
      noremap l 7l
      noremap N :vsplip<CR> //左右分屏
      //map 修改指令
      map S :W<CR>//在普通模式下 S 保存
      map s <nop>//小写s无用
      map Q ：q<CR>
      map R :source $MYVIMRC<CR>
      
      syntax on //代码高亮
      
      //set 设置功能
      set mapleader = " "//leader键
      set number //显示行号
      set relativenumber //让当前所在行 行号为1
      set cursorline //在每行下面显示一条线 （直观显示编辑所在位置）
      set wrap //编辑的内容不会超过显示框
      set showcmd //显示所打的命令 让自己知道
      set wildmenu //按Tab键后 可以进行选择功能（非常实用）
      //exec 打开vim时运行的指令
      set hlsearch //高亮搜索的 单词 方法：在普通模式下 /单词
      exec "nohlsearch"
      set incsearch //遍搜索遍高亮
      set ignorecase //搜索时忽略大小写
      set smartcase //智能搜索
      
#### 4. vim在普通模式下的一些编辑操作（可在linux 终端敲 vimtutor 有部分教程）
     <operation> <motion>
      在vim中的所有删除都是剪切，可按p黏贴
      zz将光标前移到串口中间
      u撤销上一个动作
      x删除所在光标的字符
      w光标移动到下一个单词
      d（可加数字）→ //向右删除几个字符
      d（可加数字）← //向左删除几个字符
      y(可加数字) →//向右复制几个字符
      y(可加数字) ←//向左复制几个字符
      c（change 改变）
      c w 更改下个单词 （非常有用）
      c i w （change in word在单词中修改）
      c i "  (change in ""在双引号中修改)
      y i "  (在双引号中复制)
      f（find 寻找）
      f ：//找到：
      d f： //删除直到找到：
      c f： //修改到：
      y f： //复制到：
      在普通模式下 ：color 可以搜到很多配色（使用上wildmenu功能）
                     color defult //回到默认配色
#### 5.vim配件使用
##### 1. 在gitup中 搜索 vim-plug 这是一个配件管理器
         复制下面的命令在Linux终端中输入（要下载curl，sudo apt-get install curl 或者在root下安装 apt-get install curl）
         curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
         https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
##### 2. 然后在vimrc以以下模式配置：
          call plug#begin('~/.vim/plugged')    
            Plug 'junegunn/vim-easy-align'
          call plug#end()
       
       
       
       
       
       
       
       
       
      
      
      
