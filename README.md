# ExpendMenu

用FloatingActionButton实现展开菜单

<img src="https://www.ice97.cn/download/unfoldmenu.png" width="200" alt="效果图">



# 使用方法：

在XML文件中，这个父类是FloatingActionButton：

```
    <com.ice.view.UnfoldButton
        android:id="@+id/unfoldButton"
        android:layout_alignParentBottom="true"
        android:layout_alignParentRight="true"
        android:layout_marginRight="20dp"
        android:layout_marginBottom="18dp"
        app:elevation="5dp"
        app:borderWidth="0dp"
        android:layout_gravity="right"
        android:src="@drawable/add"
        android:background="@color/colorAccent"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentEnd="true" />
```

在Activity中：

```
        UnfoldButton f = (UnfoldButton) findViewById(R.id.unfoldButton);
        f.addElement(R.drawable.bestjay, new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                //这里写菜单的点击事件
            }
        });
        f.addElement(R.drawable.bestjay,null);//同上
        f.addElement(R.drawable.bestjay,null);//同上
        f.setmScale(1);//设置弹出缩放的比例  1为不缩放 范围是0—1
        f.setLength(250);//设置弹出的距离
```

弹出菜单后，背景颜色由你自己定，你需要在colors.xml里面声明一个color:
`<color name="background">#9b414141</color>`
name必须是background

好了，这样就可以啦！
如果你的弹出菜单个数不是三个，那么请修改expendMenu方法
