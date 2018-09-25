# C++ vs java vs python


## 类声明

C++

	// 注意结尾的';'
    class Bar {};
    
java
	// 结尾无需';'
    class Bar {}

python

	class Bar(Object):
		pass
    
--------------------------------------------------------------------------------
## 方法声明

基本相同，除了java中必须是类成员并且可能有public/private/protected前缀之外。

C++



java



python

--------------------------------------------------------------------------------
## 构造函数

C++



java



python

--------------------------------------------------------------------------------
## 析构函数

C++



java



python



--------------------------------------------------------------------------------
## 类的静态变量

C++


java

	// 提供了static initialization blocks来初始化静态变量
	class Foo {

		static private int x;
		// static initialization block
		{ 
			x = 5; 
		}
	}

python




--------------------------------------------------------------------------------
## 对象声明

C++
    // 栈对象
    myClass x;
    // 堆对象
	// 构造函数无参数可以省略括号
    myClass *x = new myClass;
    

java
    // 对象总是分配在堆上
	// 构造总是要写括号
    myClass x = new myClass();

python
    
--------------------------------------------------------------------------------
## 继承

C++

    class Foo : public Bar
    { ... };
    

java

    class Foo extends Bar
    { ... }
    
--------------------------------------------------------------------------------
## 保护级别

C++

    public:
        void foo();
        void bar();
    

java

    public void foo();
    public void bar();
    
--------------------------------------------------------------------------------
## 虚函数

C++

    virtual int foo(); 
    

java

    // 函数默认就是虚函数；使用final防止被重载
    int foo();
    
--------------------------------------------------------------------------------
## 抽象类

C++

    // 只要包含一个纯虚函数
    class Bar { public: virtual void foo() = 0; };
    

java

    // 可以用语法直接定义
    abstract class Bar { public abstract void foo(); }

    // 或者指定为接口
    interface Bar { public void foo(); }

    // 然后，用一个类实现implement
它:
    class Chocolate implements Bar
    {
        public void foo() { /* do something */ }
    }
    



