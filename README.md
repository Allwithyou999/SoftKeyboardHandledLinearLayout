# SoftKeyboardHandledLinearLayout
=================================
A hack to catch soft keyboard show/hide event on Android

- XML file
```
	 <ScrollView
		android:id="@+id/activity_dialog"
		android:layout_width="match_parent"
		android:layout_height="match_parent">
		 <com.vanguard.basestation.utils.SoftKeyboardHandledLinearLayout
			android:id="@+id/main_dialog"
			android:layout_width="match_parent"
			android:layout_height="match_parent"
			android:gravity="center">
		 </com.vanguard.basestation.utils.SoftKeyboardHandledLinearLayout>
	</ScrollView>
```
- Java file
```
	@BindView(R.id.activity_dialog)
	ScrollView activity_scrollView;
	.....



	SoftKeyboardHandledLinearLayout mainView = (SoftKeyboardHandledLinearLayout) findViewById(R.id.main_dialog);
	mainView.setOnSoftKeyboardVisibilityChangeListener(new SoftKeyboardHandledLinearLayout.SoftKeyboardVisibilityChangeListener() {
	    @Override
	    public void onSoftKeyboardShow() {
		// TODO: do something here
		// for example:
	    }

	    @Override
	    public void onSoftKeyboardHide() {
		// TODO: do something here
		// for example:
		DisplayMetrics displayMetrics = new DisplayMetrics();
                getWindowManager().getDefaultDisplay().getMetrics(displayMetrics);
                int height = displayMetrics.heightPixels;
                activity_scrollView.getLayoutParams().height = height;
	    }
	});
```