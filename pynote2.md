## array and list(python on list)

    list : 像是link，可動態增加
    array : 先宣告記憶體空間再把東西放入

## set序列

    集合概念，重復的會省略

    [A, B, C] = [A, B, C]
    [A, A, A] = [A]
    [A, A, B, B] = [A, B]

    a= []
    a.append('123')

    把123放入a中，會得到[123]
    若是寫2次
    
    a= []
    b= [1, 2, 3]
    a.append('123')
    a.append('456')
    print(a)
    
    會得到[123[456]]    
    也可以a+b

    print(a+b)

    [ , 1, 2, 3]

## 反轉
    
    反轉a.reverse，要先做完才能print(a)
    注意python是code by reference
    若用 a =c, 反轉c會使得來源被反轉，因此a也會反轉
    所以a.任何事情都會影響到a原本的值
   
    import copy
    c= copy.deepcopy(a)

	運用deepcopy複製reference才不會影響原本的
  
### hw 
	
	看差別 if x == [ ] :
  	print()
	if x is [ ] :
	print()
	
### sol 

	a = [1,2,3]
	b = a

	print ( a == b )	# true
	print ( a is b )	# true

	c = [1,2,3]

	print ( c == a )	# true
	print (c is a)		# false



## tuple 

    不可改的序列，和串列很像，但不可改語法

    list，dictionary用{}，array用[]
    a=[], b=[1, 2, 3]
    for - in b, print(var) 會得到
    1
    2
    3

## dict 
## hashmap
	
	定義key 和 value
	要注意Enum是value不能相同
	hash是key不能相同
	如同之前sun對sunday是key對value
  
  dict = {'a': 3, 'b': 2, 'c': 1}
    無排序性，所以print順序會散
    取出用print(dict['a'])，會噴出3

    for var in dict.key()
    print(var)
    print(dict[var])

    a b c
    3 2 1

    ** for k,v in dict.items(): 
    print(k, v)
    這個較清楚

    範例
![2](https://github.com/BarryFu/other/blob/master/picture/2.JPG)
![1](https://github.com/BarryFu/other/blob/master/picture/1.PNG)

## Enum 

    可先看java範例，在python的使用方式不一樣，要注意value不能相同
    hash則是key不能相同

