- A simple namespace is nothing more than identifying the class that we are going to use

- Namespaces allow you to use the same names for variables, functions, and others without overwriting them

- Makes life easier

- A lot of program APIs started using those same methods so when you call a namespace called std you can import that library into your code

- Page 28 

- Declares the program will be accessing entities

- Namespaces allow you to use the same names for variables, functions, and others without overwriting them

	NameSpace A {
		void func()
		 { std::cout << "Hello!"; }
		}

	NameSpace B {
		void func()
		 { std::cout << "World!"; }
		}

- In the example, you have two void functions that are named the exact same but will not overwrite or break one another. 