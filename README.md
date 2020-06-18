- **将com.tencent.qq.widget.jar放置项目下libs内**
- **将anim.zip解压后复制到项目/res/anim/下**
- **导入qqwidget组件**

```java
import com.tencent.qq.widget.*;
import com.tencent.qq.widget.QQMenuDialog.*;```
- **调用方法**

一个按钮的对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.ORANGE );//设置对话框顶部线条的颜色
dialogs.setTitle("标题",QQDialog.setTextColor.RED);//设置对话框的标题
dialogs.setMessage("这是一个按钮的对话框",QQDialog.setTextColor.BROWN);//设置对话框的内容
dialogs.setCanceledOnTouchOutside(true);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setPositiveButton("确定",QQDialog.setTextColor.BLUE,new OnClickListener()
			  {
				  @Override
				  public void onClick(View p1)
				  {   //点击事件
					  dialog.dismiss();//关闭对话框
				  }
			  } );
dialogs.show();//显示对话框```
简化方法
```java
newQQDialog(MainActivity.this).setLineColor(QQDialog.Colors.BLUE).setTitle("标题").setMessage("这是两个按钮的对话框").setPositiveButton("确定",null).show();```
------------
两个按钮的对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.BLUE);//设置对话框顶部线条的颜色
dialogs.setTitle("标题",QQDialog.setTextColor.RED);//设置对话框的标题
dialogs.setMessage("这是两个按钮的对话框",QQDialog.setTextColor.ORANGE);//设置对话框的内容
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNeutralButton("取消",QQDialog.setTextColor.BROWN,null);
dialogs.setPositiveButton("确定",QQDialog.setTextColor.GREEN,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {   //点击事件
				     b.dismiss();//关闭对话框
			     }
		     } );
dialogs.show();//显示对话框```
简化方法
```java
newQQDialog(MainActivity.this).setLineColor(QQDialog.Colors.BLUE).setTitle("标题").setMessage("这是两个按钮的对话框").setPositiveButton("确定",null).setNegativeButton("取消",null).show();```
------------
三个按钮的对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.GREEN);//设置对话框顶部线条的颜色
dialogs.setMessage("这是三个按钮的对话框",QQDialog.setTextColor.BLUE);//设置对话框的内容
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNeutralButton("按钮一",QQDialog.setTextColor.ORANGE,new OnClickListener()
		    {
			    @Override
			    public void onClick(View p1)
			    {   //点击事件
				    d.dismiss();//关闭对话框
			    }
		    } );
dialogs.setNegativeButton("按钮二",QQDialog.setTextColor.BLUE,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {
                     //点击事件
				     d.dismiss(); //关闭对话框
			     }
		     } );
dialogs.setPositiveButton("按钮三",QQDialog.setTextColor.GREEN,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {
                     //点击事件
				     d.dismiss();//关闭对话框
			     }
		     } );
dialogs.show();//显示对话框```
简化方法
```java
newQQDialog(MainActivity.this).setLineColor(QQDialog.Colors.BLUE).setTitle("标题").setMessage("这是三个按钮的回话框").setPositiveButton("忽略",null).setNegativeButton("确定",null).setNeutralButton("取消",null).show();```
------------
自定义布局的两个按钮对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.RED);//设置对话框顶部线条的颜色
dialogs.setTitle("标题");//设置对话框的标题
dialogs.setView(R.layout.test);//设置布局文件
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNeutralButton("取消",QQDialog.setTextColor.DEFAULT,null);
dialogs.setNegativeButton("确定",QQDialog.setTextColor.DEFAULT,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {   //点击事件
				     e.dismiss();//关闭对话框
			     }
		     } );
dialogs.show();//显示对话框```
------------
自定义布局的三个按钮对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.GREEN);//设置对话框顶部线条的颜色
dialogs.setTitle("标题",QQDialog.setTextColor.ORANGE);//设置对话框的标题
dialogs.setView(R.layout.test);//设置布局文件
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNeutralButton("按钮一",QQDialog.setTextColor.ORANGE,new OnClickListener()
		    {
			    @Override
			    public void onClick(View p1)
			    {   //点击事件
				    d.dismiss();//关闭对话框
			    }
		    } );
dialogs.setNegativeButton("按钮二",QQDialog.setTextColor.BLUE,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {
                     //点击事件
				     d.dismiss(); //关闭对话框
			     }
		     } );
dialogs.setPositiveButton("按钮三",QQDialog.setTextColor.GREEN,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {
                     //点击事件
				     d.dismiss();//关闭对话框
			     }
		     } );
dialogs.show();//显示对话框```
------------
自定义图片布局的对话框
```java
ImageView image=new ImageView(MainActivity.this);
image.setImageResource(R.drawable.ic_launcher);
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.RED);//设置对话框顶部线条的颜色
dialogs.setTitle("标题");//设置对话框的标题
dialogs.setView(image);//设置图片
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNeutralButton("取消",QQDialog.setTextColor.DEFAULT,null);
dialogs.setNegativeButton("确定",QQDialog.setTextColor.DEFAULT,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {   //点击事件
				     e.dismiss();//关闭对话框
			     }
		     } );
dialogs.show();//显示对话框```
------------
带输入框的对话框
```java
finalQQDialog dialogs=newQQDialog(MainActivity.this,R.style.dialog_qq_animation);//定义一个对话框及弹出动画
dialogs.setLineColor(QQDialog.Colors.BROWN);//设置对话框顶部线条的颜色
dialogs.setTitle("标题");//设置对话框的标题
dialogs.setMessage("这是带输入框的对话框");//设置对话框的内容
dialogs.setEditText("","这是提示信息");//设置输入框的默认文本和提示信息
dialogs.setCanceledOnTouchOutside(false);//设置对话框是否可以触摸关闭
dialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
dialogs.setNegativeButton("取消",QQDialog.setTextColor.DEFAULT,null);
dialogs.setPositiveButton("确定",QQDialog.setTextColor.DEFAULT,new OnClickListener()
		     {
			     @Override
			     public void onClick(View p1)
			     {   //点击事件
				     f.dismiss();//关闭对话框
				     Toast.makeText(MainActivity.this,f.getEditText(),0).show();//展示所输入的内容
			     }
		     } );
dialogs.show();//显示对话框```
------------
选择菜单对话框
```java
final QQMenuDialog MenuDialogs=new QQMenuDialog(MainActivity.this,R.style.actionsheet_qq_animation);//定义一个对话框及弹出动画
MenuDialogs.setCancelable(true);//设置对话框是否可以点击返回键关闭
MenuDialogs.setCanceledOnTouchOutside(true);//设置对话框是否可以触摸关闭
MenuDialogs.setTitle("标题",QQMenuDialog.setTextColor.BLUE);//设置对话框的标题
MenuDialogs.setButton("取消",QQMenuDialog.setTextColor.RED);//设置对话框取消按钮的文字
MenuDialogs.addItem("按钮一",QQMenuDialog.setTextColor.ORANGE,new OnSheetItemClickListener()
	   {
		   @Override
		   public void onClick(int which)
		   {
		          //点击事件
		   }
	   } );
MenuDialogs.addItem("按钮二",QQMenuDialog.setTextColor.BLUE,new OnSheetItemClickListener()
	   {
		   @Override
		   public void onClick(int which)
		   {
                   //点击事件
		   }
	   } );
MenuDialogs.addItem("按钮三",QQMenuDialog.setTextColor.DEFAULT,new OnSheetItemClickListener()
	   {
		   @Override
		   public void onClick(int which)
		   {
                   //点击事件
		   }
	   } );
MenuDialogs.addItem("按钮四",QQMenuDialog.setTextColor.BLACK,new OnSheetItemClickListener()
	   {
		   @Override
		   public void onClick(int which)
		   {
                  //点击事件
		   }
	   } );
MenuDialogs.addItem("按钮五",QQMenuDialog.setTextColor.BLACK,new OnSheetItemClickListener()
	   {
		   @Override
		   public void onClick(int which)
		   {
                 //点击事件
		   }
	   } );
MenuDialogs.show();//显示对话框```
提示信息弹窗
```java
QQToast Toasts=new QQToast();//定义一个弹窗
Toasts.makeText(MainActivity.this,"这是一个提示",QQToast.setTheme.RED);//设置弹窗的信息
Toasts.setImage(MainActivity.this,R.drawable.ic_launcher);//设置弹窗的图标
Toasts.setTextColor(QQToast.Colors.RED);//设置弹窗的文字颜色
Toasts.setBackgroundColor(QQToast.Colors.ORANGE);//设置弹窗的背景颜色
Toasts.show();//显示弹窗```
简化方法
```java
QQToast.makeText(MainActivity.this,"这是一个提示",QQToast.setTheme.DEFAULT).show();```
------------
提示信息弹窗
```java
QQProgress Progresss=new QQProgress();//定义一个弹窗
Progresss.showPorgressBar(MainActivity.this,"这是一个进度条",QQProgress.setTheme.MATERIAL);//设置弹窗的文字及主题
Progresss.setProgressColor(QQProgress.Colors.BLUE);//设置进度条的颜色
Progresss.setTextColor(QQProgress.Colors.RED);//设置弹窗的文字颜色
Progresss.setBackgroundColor(MainActivity.this,QQProgress.Colors.WHITE);//设置弹窗的背景颜色
Progresss.show();//显示弹窗```
简化方法
```java
QQProgress.showPorgressBar(MainActivity.this,"这是一个进度条",QQProgress.setTheme.DEFAULT).show();```
