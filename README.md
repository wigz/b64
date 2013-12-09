ALL YOUR PNG ARE BASE64 ENCODE
====

Setup
---

1. Download / checkout this repository.
2. Copy b64 into your bin (usr/bin)
3. `which b64` from any dir should return `usr/bin/b64`

Use
---
b64 will base64 encode all of the png files in the current directory, write them to a valid JSON array and create a file with the passed name to save them in. Simply cd to the directory you want to encode and run `b64 myfile.json`. The result will be a file named myfile.json with the following format:

```
[
    "data:image/png;base64, ...",
    "data:image/png;base64, ...",
    "data:image/png;base64, ..."
]
```

Known Issues
---
1. Works on Mac only and requires openssl (http://www.openssl.org/).
2. Does not support spaces in file names.
3. Encoding large images / lots of images might take a while. Depending on what time it is or how you roll, grab some coffee or a beer.
4. To keep your images in sequential order, name them with leading zeros (i.e. for hundreds of images: `001.png, 002.png ... 100.png` instead of `1.png, 2.png ... 100.png`).
