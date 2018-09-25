# C++ vs java vs python


## 主函数

C++

	// 自由函数
	int main( int argc, char* argv[])
	{
		printf( "Hello, world" );
	}

 
java

	// 每个函数必须是类成员；当java类运行时类中的主函数就会被调用
	//（所以你可以为每个类写一个主函数－－这样用于给类写单元测试时会很方便）
	class HelloWorld {
		public static void main(String args[]) {
		    System.out.println( "Hello, World" );
		}
	}

python

	# 条件语句
	if __name__ == '__main__':
		print "Hello, World"

--------------------------------------------------------------------------------
## 编译

C++

    // 编译
    g++ foo.cc -o outfile
    // 运行
    ./outfile
    
java

    // 编译在foo.java里的类成为<类名>.class
    javac foo.java 
    // 调用<类名>中的静态main函数
    java <classname>

python

	解释型语言, 不需要编译, 直接运行
	python foo.py

--------------------------------------------------------------------------------
## 注释

C++

	单行注释 //
	多行注释 /* */

java

	单行注释 //
	多行注释 /* */

python

	注释 # (与shell相同)
  
--------------------------------------------------------------------------------
## 引用vs.指针

C++

    // 引用是不可改的，使用指针能得到更大的弹性
    int bar = 7, qux = 6;
    int& foo = bar;
    

java

    // 引用是可改的，它仅存放对象的地址。没有原生指针。
    myClass x;
    x.foo(); // 错误，x是空“指针”

    // 注意java里总是使用 . 存取域
     
--------------------------------------------------------------------------------
## 内存管理

大致相同--new 分配, 不过因为java著名的垃圾回收机制所以没有delete 。
NULL vs. null
C++

    // 初始化指针为NULL
    int *x = NULL;
    

java

    // 使用未初始化的引用会被计算机捕获，不过可以赋值为null指明引用为无效。
    myClass x = null;
    
--------------------------------------------------------------------------------
## 布尔值

java要长一点，你得写boolean来代替简短的bool。
C++

bool foo;

java

boolean foo;

--------------------------------------------------------------------------------
## 常量

C++

    const int x = 7;
    

java

    final int x = 7;
    
--------------------------------------------------------------------------------
## Throw说明

首先, java在编译时强制要求有throw说明－如果一个方法要抛出一个异常你必须先说明它
C++

int foo() throw (IOException)

java

int foo() throws IOException

--------------------------------------------------------------------------------
## 数组

C++

    int x[10];
    // 或者 
    int *x = new x[10];
    // 使用x然后收回内存
    delete[] x;
    

java

    int[] x = new int[10];
    // 使用x，内存由垃圾回收机制回收
    
--------------------------------------------------------------------------------
## 集合和迭代

C++

迭代器是类成员，一个范围起始于<container>.begin(), 终止于<container>.end(). 使用++操作前进，使用*存取。

    vector myVec;
    for ( vector<int>::iterator itr = myVec.begin();
          itr != myVec.end();
          ++itr )
    {
        cout << *itr;
    }
    

java

迭代器仅仅是一个接口。一个范围起始于<collection>.iterator, 接着使用itr.hasNext()检查确认是否已到末尾。使用itr.next()取得下一个数据。

    ArrayList myArrayList = new ArrayList();
    Iterator itr = myArrayList.iterator();
    while ( itr.hasNext() )
    {
        System.out.println( itr.next() );
    }

    // 在java 5中：
    ArrayList myArrayList = new ArrayList();
    for( Object o : myArrayList ) {
        System.out.println( o );
    }
    










