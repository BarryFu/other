## windows virtualenv

### 1.create virtualenv

	pip3 install virtualenv 
	virtualenv py3	#py3=job name
	在py3\script下 activate開始執行虛擬環境

### 2.vtool安裝
	
	安裝pybuilder: pip install pybuilder
	在vtool下 pyb_ clean install
###	Error
	
	Windows下pybuilder會有編譯的問題,V跟F開頭的scripts名稱會錯誤
	目前先改為cv2g,cvfreq,cvscan

![Error](https://github.com/BarryFu/picture/blob/master/14599745_1233657679988641_1987580550_o.png)

### 3.pycharm load virtualenv
	
	在settings,project interpreter 
	addlocal: py3\scripts\python.exe 

### 4.windows pycharm

	在windows-virtualenv下，vfreq要把路徑打出來，且\要2次
	python C:\\Users\\Casey\\AppData\\Local\\Programs\\Python\\Python35\\py3\\Scripts\\cvfreq

	cat改成type

	