##安裝pip, virtualenv, vtool
###1.
	先載python3的tgz檔
	tar -zxvf Python.tgz

###2.
	進入剛剛解壓縮出來的資料夾
	cd Python-3.2.1
	然後輸入下面的指令來設定一些安裝參數並且檢查安裝環境
	./configure –prefix=/usr

###3.
	make,給他編譯

###4.
	make install,再讓他開始安裝

###5.
	如果失敗去zypper se python-setuptool
	安裝package，若找不到去yast-software-repositories
	把光碟的sdk跟sles掛上去，通常在/home/pkg裡面

###6.
	完成安裝pip
	pip install virtualenv	安裝環境
	python -m pip install requests
	pip install --upgrade pip	更新

	virtualenv --python=python3 project名稱	創造虛擬環境
	在file裡面打source bin/activate	開始py環境
	或是VIRTUAL_ENV_DISABLE_PROMPT=1 source bin/activate	 解除

###7.
	Pybuilder 
	在virtualenv裡面安裝
	pip install pybuilder 
	在裝vtool或vtool3,
	pyb_ clean install
