## def

	def f(x) 先定義函數
	return 2* x + x宣告回傳函數
	print(f(1)) 噴出變數函數值

	def g(x)
	retuen 5*x + f(x) + 5 定義完後前面的變數也可以使用
	print(g(1)) 一起噴出變數函數

	###直接定義雙變數

	def g(x, y)
	return 5 * y * y + f(x) + 5
	print(g(1, 1))

	結果會同上但是可以有x、y變數

	def say_hello(words = None): 用none比較奇怪變成Hi None
    print('Hi ' + str(words))

    def say_hello(words=''):
    print('Hi ' + words)	給它空白

    或是一次多個人

    def say_hello(w1='', w2=''):
    print('Hi ' + w1 + w2)

    def say_hello(*words):

    sentence = ''
    for w in words:
        sentence += w + ' '
    print('Hi ' + sentence)	利用迴圈增加	

    print('Hi ' + ', '.join(words))	使用join加在後面
    say_hello("tino")
	say_hello("tino2", "tino1")
	say_hello("tino2", "tino1", 't3')	再放上使用的字
	依序得到(Hi tino), (Hi tino2, tino1),((Hi tino2, tino1, t3)

	def show_element(e, x=0, y=0, z=0):	給名稱及相對應數值，像應用在座標上
    print(e)
    print(x)
    print(y)
    print(z)
	show_element("H", 1, 1)	這個會得到x=1, y=1 的值
	show_element("H", y=1, z=1) 所以若想讓第一項或第二項為0只好定義每一項

	def show_element2(e, *coordinate):	給名稱及對應的函數
    print(e)
    print(coordinate)

	show_element2("H", 1, 1, 1)	除了給名稱外還順便把函數給寫進來

	最後得到(H, 1, 1, 1)

	a = 123	先給個global值

	def f1():		定義
    	print(a)	因為此層沒有a，所以會往上層找，得到123
	f1()			叫f1函數出來，因為def裡面是空的

	def f2():		
    	a = 22		定義此層的a值
    	print(a)	所以這層會得到22
	f2()

	def f3(a):		把變數a key入函數f3
    	print(a)	所以直接把a填入也是往上層找得到123

	def f4(l):		變數為l 
    	l = 345		定義此層l值
    	print(l)	得到345 相似於f3

	f4(a)			放一個新的變數a
	print(a)		最後得到123，因為此層沒有a, 但要注意因為又用了f4(a) 導致l= a 
					l就變成a了，所以print出來才是123


	def f5(l):		陣列也有相同效果
    	l = [345]
    	print(l)	得到[345]

	b = [1,2,3]

	f5(b)
	print(b)		得到[1,2,3]	且l變b


	def f6(l):		先定義函數f6
    	l.append(7)	新增7在後面
    	print(l)	

	c = [1,2,3]		再給訂c

		f6(c)		把C帶入，l= c, 第一次回得到[1,2,3,7]
		print(c)
		f6(c)		再一次因為新的c是[1,2,3,7]所以會得到[1,2,3,7,7]

		