# 记录一下自己去面试遇到的一些问题，回来整理了一下答案，如果您发现有错误记得告诉我哦
## 深圳白骑士大数据有限公司（2018.6.28 上午）
笔试：
>>
#### 1.LinkedList和Vector___谁是线程安全的？____插入的效率更高？
    Vector由于使用了synchronized方法-线程安全,LinkedList使用双向链表实现存储，按序号索引数据需要进行向前或向后遍历，
    但是插入数据时只需要记录本项前后项即可，插入数据较快。
#### 2.类中的一个方法被synchronized修饰，该类中的其他
    
#### 3.char是否可以储存一个中文汉字？为什么？
    char型变量是用来储存Unicode编码的字符的，Unicode编码字符集中包含了汉字，所以char型变量可以存储汉字
#### 4.说说List、Set、Map各自的特点
    Set：检索元素效率低下，删除和插入效率高，插入和删除不会引起元素位置改变；
    List：和数组类似，List可以动态增长，查找元素效率高，插入删除元素效率低，因为会引起其他元素位置改变；
    Map：适合储存键值对的
#### 5.简述什么是Singleton模式？写代码实现（手写单例模式）
     单例模式确保一个类只有一个实例，自行提供这个实例并向整个系统提供这个实例。
     ①懒汉式(比较懒，需要时才创建)
     public class Singleton{
        private static Singleton instance = null;
        public static synchroized Singleton getInstance() {
            if(instance == null){
                instance = new Singleton();
                return instance;
            }
        }
     }
     ②饿汉式(比较饥饿，一上来就创建)
     public class Singleton{
        private Singleton(){};
        private static Singleton instance = new Singleton();
        public static Singleton getInstance{
            return instance;
        }
     }
#### 6.写一个你知道的排序？（手写排序）
    public static void bubbleSort(int[] arr) {
        if(arr.length == 0 && arr == null){
            system.out.prilentln("array is null");
        }
        for(i = 0;i < arr.length - 1;i++){
            for(j = 0;j < arr.length;j++){
                if(arr[i] > arr[j]){
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
    }
#### 7.js代码实现，ID为table的表格，alert显示第二行第三列的值，写代码实现
    用table的属性获取吧
    var _tab = document.getElementById('table'); // 获取table对象
    var _row = _tab.rows; //获取table的行
    var _cell = _row[1].cells; //获取第二行的列
    alert(_cell[2].innerHTML); //获取第三列的值
#### 8.写五个Linux命令，并写出他们的作用
    ①mkdir:建立新目录；②cd：变换目录；③cp：复制档案或目录；④rm：删除档案或目录；⑤mv：移动档案或目录，或更名；
    ⑥ls：档案与目录的显示>>更过命令链接：https://zhidao.baidu.com/question/1609431995174944987.html
#### 9.page、request、session、application，作用域从小到大排序
    page<request<session<application  详情链接：https://blog.csdn.net/weixin_40836179/article/details/79414854
#### 10.Linux查看8080端口被占用的命令？
    netstat –apn | grep 8080
#### 11.编程实现：输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字。
例如，如果输入如下矩阵：
1  2  3  4 
5  6  7  8 
9  10 11 12 
13 14 15 16 
则依次打印出数字1,2,3,4,8,12,16,15,14,13,9,5,6,7,11,10.
    答案链接：https://blog.csdn.net/u013686654/article/details/74456113
#### 12.简述tomcat、jvm或其他你熟悉的开源框架的原理
--
面试：
>>
#### 1.自我介绍一下
#### 2.上一个项目采用了哪些技术？
#### 3.用了spring框架带来了哪些好处？
#### 4.Hibernate和Mybatis比较
#### 5.对当前流行的技术有没有关注过，如SpringBoot，SpringCloud
#### 6.谈一谈你比较熟悉的开源框架
#### 7.SpringBoot主要的特点是什么？当前技术已经很不错了，为什么还要用它？
#### 8.了解爬虫吗？爬虫用来干什么？有什么反爬虫的机制？
