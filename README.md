# DexExtractor
Android dex file extractor, anti-bangbang (Bangcle)

## Usage
Put libdvm.so on the emulator `/system/lib` or download the pre-setup system image
Update! fix memory leak
https://drive.google.com/file/d/0B4IvHmkRqgS4Nlh5WmVhRU9aNlE/view?usp=sharing

Boot the emulator with an sdcard and install protected application.
Open logcat and monitor for the Application tag for the dalvikvm like this ![logcat](art/image.png), you will see created file name output here.
Then use adb to pull the file, `adb  pull /sdcard/pkg_classes_xxx.dex`<br>
Then run `java -jar Decoder.jar pkg_dexs_dir` to get all odex used from the unprotected file.
