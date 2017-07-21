# MediaPicker
视频,图片选择库(lib for select video and picture)

## Video
```
Intent i = new Intent(this, PhotoMediaActivity.class);
i.putExtra("loadType", PhotoVideoDir.Type.VEDIO.toString());
startActivityForResult(i, 555);
```

```
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    super.onActivityResult(requestCode, resultCode, data);
    if (resultCode == RESULT_OK) {
        ArrayList<String> selectedVedioPaths = data.getStringArrayListExtra("videopath");
        }
    }
}
```

## Picture
```
Intent i = new Intent(this, PhotoMediaActivity.class);
i.putExtra("loadType", PhotoVideoDir.Type.IMAGE.toString());
startActivityForResult(i, 666);
```


```
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    super.onActivityResult(requestCode, resultCode, data);
    if (resultCode == RESULT_OK) {
         ArrayList<File> selectedImgPaths = (ArrayList<File>) data.getSerializableExtra("files");
        }
    }
}
```
