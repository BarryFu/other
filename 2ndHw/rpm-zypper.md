## 1. rpmbuild pdsh

PDSH(Parallel Distributed SHell)

可並行的執行對目標主機的操作，對於批量執行命令和分發任務有很大的幫助，在使用前需要配置的ssh無密碼登錄

a.下載完後進入/usr/src/packages，會看到rpmbuild的格式{BUILD, RPMS, SOURCE, SPECS, SRPMS}

b.將壓縮檔解壓至BUILD，pdsh.spec檔放入SPECS後，rpmbuild -bb(或ba) pdsh.spec 即可做成rpm檔(或+srpm)

![](https://github.com/BarryFu/other/blob/master/2ndHw/rpmbuild1.PNG)

c.過程中有缺少的再用zypper安裝即可

## 2. openjdk, oraclejdk install and switch 

a.oraclejdk : 在http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html 下載壓縮檔在/opt解壓縮

b.openjdk : 則是在sles12中可直接zypper in或是在sles11中先安裝glibc2.14以上版本也可以開啟

此作業在centOS上執行可直接yum install java-1.7.0-openjdk　

c.在安裝完openjdk後先執行update-alternatives --config java 準備進行java版本轉換

若只有一種java會顯示only 1 kind java

d.新增oraclejdk: update-alternatives --install /usr/bin/java java /{PATH}/bin/java 700  

700為執行序，在有多種java時會優先以數字大的先執行

也可用update-alternatives --config java 轉換如圖

![](https://github.com/BarryFu/other/blob/master/2ndHw/java1.PNG)

## 3. zypper 安裝oracle

a. 首先先安裝2.7版python及pip，這邊是先上python網wget到2.7.10版python在自行編譯安裝

b. 之後pip 安裝或更新pip install or pip install --upgrate python-setuptools 以及wheels

c. pip install ansible後不確定是否成功安裝完...

![](https://github.com/BarryFu/other/blob/master/2ndHw/ansible1.PNG)

