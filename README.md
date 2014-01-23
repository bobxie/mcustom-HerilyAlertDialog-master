mcustom-HerilyAlertDialog-master
================================

完全custom的Android Dialog[HerilyAlertDialog]

HerilyAlertDialog is an Open Source Android library that allows developers to easily create applications 
with HerilyAlertDialog like use AlertDialog. Feel free to use it all you want in your Android apps provided that you cite this project and include the license in your app.

-----
1.HerilyAlertDialog 是由Herily[虚拟名]研究android对话框源码后的结晶，继承自AlertDialog并根据需要重写了部分代码，使其能满足自己所需要的风格的对话框。你可以像使用AlertDialog一样的使用HerilyAlertDialog。你也可以直接使用HerilyAlertDialog来直接替换已有项目中的AlertDialog而不需要做任何修改。
2.如果你想更换对话框风格，你可以替换掉drawable-hidp中对应的.png图片资源即可。
3.建议配置成双选择形式来使用(通过配置文件或者某一个定向变来空控制到底使用哪一种对话框)


Setup
-----
* In Eclipse, just import the library as an Android library project. Project > Clean to generate the binaries 
you need, like R.java, etc.
* Then, just add HerilyAlertDialog as a dependency to your existing project and you're good to go!

Simple Example
-----
```java
	/**
	 * 根据IS_CUSTOM_DIALOG创建progressLoadingDialog对象
	 * @return AlertDialog progressLoadingDialog
	 */
	protected AlertDialog createProgressDialog() {
		AlertDialog progressLoadingDialog = null;
		if (isCustomDialog) {
			progressLoadingDialog = new GoldtelProgressDialog(context);
		} else {
			progressLoadingDialog = new ProgressDialog(context);
		}
		return progressLoadingDialog;
	}
	
	
	/**
	 * 根据IS_CUSTOM_DIALOG创建AlertDialog的Builder对象
	 * @return AlertDialog.Builder adb
	 */
	protected AlertDialog.Builder createDialogBuilder() {
		AlertDialog.Builder abd = null;
		if (isCustomDialog) {
			abd = new GoldtelAlertDialog.Builder(this);
		} else {
			abd = new AlertDialog.Builder(context);
		}
		return abd;
	}

        //boolean type isCusomtDialog is config in your Constants.java 
```

Developed By
------------
* Herily

License
-------

    Copyright 2012 Herily
    
