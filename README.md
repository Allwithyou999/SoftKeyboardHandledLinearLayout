# SoftKeyboardHandledLinearLayout
=================================
A hack to catch soft keyboard show/hide event on Android

- XML file
```
	 <com.vanguard.basestation.utils.SoftKeyboardHandledLinearLayout
		android:id="@+id/main_dialog"
		android:layout_width="match_parent"
		android:layout_height="match_parent"
		android:gravity="center">
	 </com.vanguard.basestation.utils.SoftKeyboardHandledLinearLayout>
```
- Java file
```
	SoftKeyboardHandledLinearLayout mainView = (SoftKeyboardHandledLinearLayout) findViewById(R.id.main_dialog);
	mainView.setOnSoftKeyboardVisibilityChangeListener(new SoftKeyboardHandledLinearLayout.SoftKeyboardVisibilityChangeListener() {
	    @Override
	    public void onSoftKeyboardShow() {
		// TODO: do something here
	    }

	    @Override
	    public void onSoftKeyboardHide() {
		// TODO: do something here
	    }
	});
```