# How to use

- **maven**

```
<dependency>
  <groupId>com.chan.circleprogress</groupId>
  <artifactId>circleprogress</artifactId>
  <version>0.1</version>
  <type>pom</type>
</dependency>
```

- **gradle**

```
 compile 'com.chan.circleprogress:circleprogress:0.1'

 //可能jcenter还在审核 如果发现不能使用的话 还需要添加：
 repositories {
    maven {
        url "https://dl.bintray.com/chanjlee/maven"
    }
 }
```
-------------------

##Example

```
	    final CircleProgress circleProgress = (CircleProgress) findViewById(R.id.id_progress);

        findViewById(R.id.id_button).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                final ValueAnimator valueAnimator = ValueAnimator.ofInt(0, 100);
                valueAnimator.setDuration(3000);
                valueAnimator.addUpdateListener(new ValueAnimator.AnimatorUpdateListener() {
                    @Override
                    public void onAnimationUpdate(ValueAnimator animation) {
                        circleProgress.setCurrentProgress(
		                        (Integer) valueAnimator.getAnimatedValue()
	                        );
                    }
                });
                valueAnimator.start();
            }
        });
```

## Screenshot

![这里写图片描述](http://img.blog.csdn.net/20160324115354443)

##github
[这里写链接内容](https://github.com/ChanJLee/CircleProgress)