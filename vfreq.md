## robotframework

	分成4部分來寫, Settings, Variables, Keywords, Test Cases

### vfreq
	
	Settings:除了OperatingSystem外，還可以放入其他變數資料庫
	Library OperatingSystem
	Libaray diff
	Resorce ...

	Variables:則是把會用到的檔案給寫入變數中，才引用的到
	${files_dir}= vfreq_test_temple
	${outcar}= ${files_dir}/OUTCAR 
	${vlog}= ${files_dir}/OUTCAR ...

	Keywords:將動作給寫出來但還不是執行
	Generate vlog From OUTCAR
		Run vfreq ${outcar} ${vlog} ...

	Test Cases:
	Convert OUTCAR To vlog說明
    	Test Setup OUTCAR To vlog 執行Keywords內的動作
    	Generate vlog From OUTCAR
    	Check vlog ...

### 問題

	vtool3,vfreq會有浮點數的error，出現在vasp.py553行
!(https://github.com/BarryFu/other/blob/master/vfreq-error.PNG)
	在541行處修改
!(https://github.com/BarryFu/other/blob/master/vfreq2.PNG)	


	pybot執行後，vtool3的格式有些不同，且原子編號不對
!(https://github.com/BarryFu/other/blob/master/vfreq3.PNG)	