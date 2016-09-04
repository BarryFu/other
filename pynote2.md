## array and list(python on list)

    list : 像是link，可動態增加
    array : 先宣告記憶體空間再把東西放入

##set序列

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

##反轉
    
    反轉a.reverse，要先做完才能print(a)
    注意python是code by reference
    若用 a =c, 反轉c會使得來源被反轉，因此a也會反轉
    所以a.任何事情都會影響到a原本的值

    c= copy.deepcopy(a)

	運用deepcopy複製reference才不會影響原本的

##hashmap
	
	定義key 和 value
	要注意Enum是value不能相同
	hash是key不能相同
	如同之前sun對sunday是key對value
  
###hw 
	
	看差別 
	
	if x == [ ] :
  	print()
	if x is [ ] :
	print()
