# AwCamera
Instagram-like photo browser
## Screen
![alt text](http://www.lucabarbara.com/awcamera/screen1.png)
## Features

## Docs
### Methods:
```java
AwCamera.setGalleryEnabled(true); // enables/disables gallery tab. (default: true)
AwCamera.setPhotoEnabled(true);   // enables/disables photo tab. (default: true)
AwCamera.setVideoEnabled(true);   // enables/disables video tab. (default: true)
```
### Example:
```java
    //[...]
    private final int RESULT_IMAGE = 0;
    //[...]

    Intent i = new Intent(MainActivity.this,AwCamera.class);
    startActivityForResult(i, RESULT_IMAGE);

    //[...]

    @Override
    public void onActivityResult(int requestCode, int resultCode, Intent data) {
        super.onActivityResult(requestCode, resultCode, data);

        switch (requestCode) {
            case RESULT_IMAGE :
                if (data != null) {
                    Picasso.with(this).load(data.getData()).fit().centerCrop().into(mImageView);
                }
                break;
            default:
                break;
        }
    }
```
## License
AwCamera is released under the MIT license.