# PlateNumberKeyBoard
Android 自定义车牌键盘

![](https://github.com/yechaoa/PlateNumberKeyBoard/raw/master/pic/1.jpg)
![](https://github.com/yechaoa/PlateNumberKeyBoard/raw/master/pic/2.jpg)

> 最近在做物流的项目，需要输入车牌号，传统的输入体验并不好，来回切换还要手打，便有了自定义键盘的想法。
> 其实这个车牌需求并不多见，物流、租车、停车相关的会常见一些，好在有前辈已经铺好路了
> 这个比较详细：[https://blog.csdn.net/dgs960825/article/details/50344743](https://blog.csdn.net/dgs960825/article/details/50344743)

#### 1.在res文件夹下新建xml文件夹，新建两个文件：number_or_letters.xml（数字和大写字母）、province_abbreviation.xml（省会、直辖市、特别行政区简称）。

> number_or_letters.xml

```
<?xml version="1.0" encoding="UTF-8"?>
<Keyboard android:keyWidth="10%p" android:keyHeight="8%"
          android:horizontalGap="0.0px" android:verticalGap="0.0px"
          xmlns:android="http://schemas.android.com/apk/res/android">
    <Row android:verticalGap="1%p">
        <Key android:codes="49" android:keyLabel="1"
             android:horizontalGap="1%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left"  />
        <Key android:codes="50" android:keyLabel="2"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="51" android:keyLabel="3"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="52" android:keyLabel="4"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="53" android:keyLabel="5"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="54" android:keyLabel="6"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="55" android:keyLabel="7"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="56" android:keyLabel="8"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="57" android:keyLabel="9"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="48" android:keyLabel="0"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right"/>
    </Row>

    <Row android:verticalGap="1%p">
        <Key android:codes="81" android:keyLabel="Q"
             android:horizontalGap="1%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left" />
        <Key android:codes="87" android:keyLabel="W"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="69" android:keyLabel="E"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="82" android:keyLabel="R"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="84" android:keyLabel="T"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="89" android:keyLabel="Y"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="85" android:keyLabel="U"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="73" android:keyLabel="I"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="79" android:keyLabel="O"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="80" android:keyLabel="P"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right" />
    </Row>

    <Row android:verticalGap="1%p">
        <Key android:codes="65" android:keyLabel="A"
             android:horizontalGap="6%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left"/>
        <Key android:codes="83" android:keyLabel="S"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="68" android:keyLabel="D"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="70"  android:keyLabel="F"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="71" android:keyLabel="G"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="72"  android:keyLabel="H"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="74" android:keyLabel="J"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="75" android:keyLabel="K"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="76"  android:keyLabel="L"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right" />
    </Row>

    <Row >
        <Key android:codes="-1"
             android:keyEdgeFlags="left" android:keyLabel="省份"
             android:horizontalGap="1%p" android:keyWidth="13%p"
             android:isModifier="true" android:isSticky="true"  />
        <Key android:codes="90" android:keyLabel="Z"
             android:horizontalGap="2%p" android:keyWidth="8%p"/>
        <Key android:codes="88" android:keyLabel="X"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="67" android:keyLabel="C"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="86" android:keyLabel="V"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="66" android:keyLabel="B"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="78" android:keyLabel="N"
             android:horizontalGap="2%p" android:keyWidth="8%p"/>
        <Key android:codes="77" android:keyLabel="M"
             android:horizontalGap="2%p" android:keyWidth="8%p"/>
        <Key  android:codes="-3"
              android:keyEdgeFlags="right" android:keyLabel="删除"
              android:horizontalGap="2%p" android:keyWidth="13%p"
              android:isRepeatable="false" />
    </Row>

</Keyboard>
```

> province_abbreviation.xml

```
<?xml version="1.0" encoding="UTF-8"?>
<Keyboard
    android:keyWidth="10%p" android:keyHeight="8%p"
    android:horizontalGap="0.0px" android:verticalGap="0.0px"
    xmlns:android="http://schemas.android.com/apk/res/android">

    <Row android:verticalGap="1%p">
        <Key android:codes="20140" android:keyLabel="京"
             android:horizontalGap="1%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left"  />
        <Key android:codes="27941" android:keyLabel="津"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="20864" android:keyLabel="冀"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="40065" android:keyLabel="鲁"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="26187" android:keyLabel="晋"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="33945" android:keyLabel="蒙"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="36797" android:keyLabel="辽"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="21513" android:keyLabel="吉"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="40657" android:keyLabel="黑"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="27818" android:keyLabel="沪"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right"/>
    </Row>

    <Row android:verticalGap="1%p">
        <Key android:codes="33487" android:keyLabel="苏"
             android:horizontalGap="1%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left" />
        <Key android:codes="27993" android:keyLabel="浙"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="30358" android:keyLabel="皖"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="38397" android:keyLabel="闽"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="36195" android:keyLabel="赣"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="35947" android:keyLabel="豫"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="37122" android:keyLabel="鄂"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="28248" android:keyLabel="湘"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="31908" android:keyLabel="粤"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="26690" android:keyLabel="桂"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right" />
    </Row>

    <Row android:verticalGap="1%p">
        <Key android:codes="28189" android:keyLabel="渝"
             android:horizontalGap="11%p" android:keyWidth="8%p"
             android:keyEdgeFlags="left"/>
        <Key android:codes="24029" android:keyLabel="川"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="36149" android:keyLabel="贵"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="20113"  android:keyLabel="云"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="34255" android:keyLabel="藏"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="38485"  android:keyLabel="陕"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="29976" android:keyLabel="甘"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="38738"  android:keyLabel="青"
             android:horizontalGap="2%p" android:keyWidth="8%p"
             android:keyEdgeFlags="right" />
    </Row>

    <Row >
        <Key android:codes="-1"
             android:keyEdgeFlags="left" android:keyLabel="ABC"
             android:horizontalGap="4%p" android:keyWidth="15%p"
             android:isModifier="true" android:isSticky="true"  />
        <Key android:codes="29756" android:keyLabel="琼"
             android:horizontalGap="2%p" android:keyWidth="8%p"/>
        <Key android:codes="26032" android:keyLabel="新"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="23425" android:keyLabel="宁"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="28207" android:keyLabel="港"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="28595" android:keyLabel="澳"
             android:horizontalGap="2%p" android:keyWidth="8%p" />
        <Key android:codes="21488" android:keyLabel="台"
             android:horizontalGap="2%p" android:keyWidth="8%p"/>
        <Key  android:codes="-3"
              android:keyEdgeFlags="right" android:keyLabel="删除"
              android:horizontalGap="2%p" android:keyWidth="15%p"
              android:isRepeatable="false" />
    </Row>

</Keyboard>
```

#### 2.新建键盘工具类KeyboardUtil（初始化、交互、显示和隐藏）

```
package yechaoa.com.platenumberkeyboard;

import android.app.Activity;
import android.content.Context;
import android.inputmethodservice.Keyboard;
import android.inputmethodservice.KeyboardView;
import android.text.Editable;
import android.text.InputType;
import android.view.View;
import android.view.WindowManager;
import android.widget.EditText;

import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

/**
 * Created by yechao on 2018/5/15/015.
 * Describe :
 */
public class KeyboardUtil {

    private Activity mActivity;
    private KeyboardView mKeyboardView;
    private EditText mEdit;
    /**
     * 省份简称键盘
     */
    private Keyboard provinceKeyboard;
    /**
     * 数字与大写字母键盘
     */
    private Keyboard numberKeyboard;

    KeyboardUtil(Activity activity, EditText edit) {
        mActivity = activity;
        mEdit = edit;
        provinceKeyboard = new Keyboard(activity, R.xml.province_abbreviation);
        numberKeyboard = new Keyboard(activity, R.xml.number_or_letters);
        mKeyboardView = (KeyboardView) activity.findViewById(R.id.keyboard_view);
        mKeyboardView.setKeyboard(provinceKeyboard);
        mKeyboardView.setEnabled(true);
        mKeyboardView.setPreviewEnabled(false);
        mKeyboardView.setOnKeyboardActionListener(listener);
    }

    private KeyboardView.OnKeyboardActionListener listener = new KeyboardView.OnKeyboardActionListener() {
        @Override
        public void swipeUp() {
        }

        @Override
        public void swipeRight() {
        }

        @Override
        public void swipeLeft() {
        }

        @Override
        public void swipeDown() {
        }

        @Override
        public void onText(CharSequence text) {

        }

        @Override
        public void onRelease(int primaryCode) {
        }

        @Override
        public void onPress(int primaryCode) {
        }

        @Override
        public void onKey(int primaryCode, int[] keyCodes) {
            Editable editable = mEdit.getText();
            int start = mEdit.getSelectionStart();
            //判定是否是中文的正则表达式 [\\u4e00-\\u9fa5]判断一个中文 [\\u4e00-\\u9fa5]+多个中文
            String reg = "[\\u4e00-\\u9fa5]";
            if (primaryCode == -1) {// 省份简称与数字键盘切换
                if (mEdit.getText().toString().matches(reg)) {
                    changeKeyboard(true);
                }
            } else if (primaryCode == -3) {
                if (editable != null && editable.length() > 0) {
                    //没有输入内容时软键盘重置为省份简称软键盘
                    if (editable.length() == 1) {
                        changeKeyboard(false);
                    }
                    if (start > 0) {
                        editable.delete(start - 1, start);
                    }
                }
            } else {
                editable.insert(start, Character.toString((char) primaryCode));
                // 判断第一个字符是否是中文,是，则自动切换到数字软键盘
                if (mEdit.getText().toString().matches(reg)) {
                    changeKeyboard(true);
                }
            }
        }
    };

    /**
     * 指定切换软键盘 isNumber false表示要切换为省份简称软键盘 true表示要切换为数字软键盘
     */
    private void changeKeyboard(boolean isNumber) {
        if (isNumber) {
            mKeyboardView.setKeyboard(numberKeyboard);
        } else {
            mKeyboardView.setKeyboard(provinceKeyboard);
        }
    }

    /**
     * 软键盘展示状态
     */
    public boolean isShow() {
        return mKeyboardView.getVisibility() == View.VISIBLE;
    }

    /**
     * 软键盘展示
     */
    public void showKeyboard() {
        int visibility = mKeyboardView.getVisibility();
        if (visibility == View.GONE || visibility == View.INVISIBLE) {
            mKeyboardView.setVisibility(View.VISIBLE);
        }
    }

    /**
     * 软键盘隐藏
     */
    public void hideKeyboard() {
        int visibility = mKeyboardView.getVisibility();
        if (visibility == View.VISIBLE) {
            mKeyboardView.setVisibility(View.INVISIBLE);
        }
    }

    /**
     * 禁掉系统软键盘
     */
    public void hideSoftInputMethod() {
        mActivity.getWindow().setSoftInputMode(WindowManager.LayoutParams.SOFT_INPUT_STATE_ALWAYS_HIDDEN);
        int currentVersion = android.os.Build.VERSION.SDK_INT;
        String methodName = null;
        if (currentVersion >= 16) {
            // 4.2
            methodName = "setShowSoftInputOnFocus";
        } else if (currentVersion >= 14) {
            // 4.0
            methodName = "setSoftInputShownOnFocus";
        }
        if (methodName == null) {
            mEdit.setInputType(InputType.TYPE_NULL);
        } else {
            Class<EditText> cls = EditText.class;
            Method setShowSoftInputOnFocus;
            try {
                setShowSoftInputOnFocus = cls.getMethod(methodName, boolean.class);
                setShowSoftInputOnFocus.setAccessible(true);
                setShowSoftInputOnFocus.invoke(mEdit, false);
            } catch (NoSuchMethodException e) {
                mEdit.setInputType(InputType.TYPE_NULL);
                e.printStackTrace();
            } catch (IllegalAccessException e) {
                e.printStackTrace();
            } catch (IllegalArgumentException e) {
                e.printStackTrace();
            } catch (InvocationTargetException e) {
                e.printStackTrace();
            }
        }
    }

}

```

#### 3.Activity引用

```
package yechaoa.com.platenumberkeyboard;

import android.annotation.SuppressLint;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.text.Editable;
import android.text.TextWatcher;
import android.util.Log;
import android.view.KeyEvent;
import android.view.MotionEvent;
import android.view.View;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    private KeyboardUtil keyboardUtil;
    private EditText mEditText;

    @SuppressLint("ClickableViewAccessibility")
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mEditText = findViewById(R.id.edit_text);
        mEditText.setOnTouchListener(new View.OnTouchListener() {
            @Override
            public boolean onTouch(View view, MotionEvent event) {
                if (keyboardUtil == null) {
                    keyboardUtil = new KeyboardUtil(MainActivity.this, mEditText);
                    keyboardUtil.hideSoftInputMethod();
                    keyboardUtil.showKeyboard();
                } else {
                    keyboardUtil.showKeyboard();
                }
                return false;
            }
        });

        mEditText.addTextChangedListener(new TextWatcher() {

            @Override
            public void afterTextChanged(Editable s) {
                Log.i("字符变换后", "afterTextChanged");
            }

            @Override
            public void beforeTextChanged(CharSequence s, int start, int count, int after) {
                Log.i("字符变换前", s + "-" + start + "-" + count + "-" + after);
            }

            @Override
            public void onTextChanged(CharSequence s, int start, int before, int count) {
                Log.i("字符变换中", s + "-" + "-" + start + "-" + before + "-" + count);
            }
        });
    }

    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if (keyCode == KeyEvent.KEYCODE_BACK) {
            if (keyboardUtil.isShow()) {
                keyboardUtil.hideKeyboard();
            } else {
                finish();
            }
        }
        return false;
    }

}

```
#### 4.相关属性

android:keyBackground="@drawable/selector_key" 
* 按键的背景颜色

android:shadowColor="#FFFFFF"
android:shadowRadius="0.0" 
* 不加这两个属性  文字会出现模糊

android:keyTextColor="#000"
* 字体颜色

android:keyTextSize="18sp"
* 字体大小

android:keyIcon="@drawable/ic_delete"
* 按键上的图标

android:codes="20140"
* 输出的内容 对照ASCII表

android:keyLabel="京"
* 按键上显示的内容

android:horizontalGap="0px"
* 水平方向的间隙

android:verticalGap="0px"
* 垂直反向的间隙

android:keyEdgeFlags="right"
* 按键的对齐方式
