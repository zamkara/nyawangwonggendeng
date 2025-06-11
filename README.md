# nyawangwonggendeng

`nya` is a lightweight yet powerful Bash script to upload and download files via the [Ranoz.gg](https://ranoz.gg) API. Designed for simplicity and portability, it enables local uploads, downloads by ID/URL, and re-uploads from direct links with optional desktop notifications and QR code previews.

---

## 🔧 Features

* ✅ Upload files to Ranoz.gg
* ✅ Display QR code (if `qrrs` is installed)
* ✅ Desktop notification (via `notify-send` if available)
* ✅ Pure Bash CLI, no bloated dependencies

---

## 📦 Dependencies

### Required:

* `bash`
* `curl`
* `jq`

### Optional:

* `notify-send` — desktop notification
* `qrrs` — display QR code in terminal
* `wget` / `aria2c` / `axel` — used for `-r` redirect uploads

---

## 🚀 Installation

```bash
git clone https://github.com/zamkara/nya.git
cd nya
chmod +x nya
sudo mv nya /usr/local/bin/nya
```

---

## 📚 Usage

### Show Help

```bash
nya --help
nya -v
```

### Upload a File

```bash
nya up file.txt
nya --up image.png
```

### Download a File

```bash
nya get RZ123abc
nya --get https://ranoz.gg/f/RZ123abc
```

### Redirect Upload from Direct Link

```bash
nya -r https://example.com/file.zip
```

The script will ask you to enter a filename to save the downloaded file. If left blank, it defaults to the filename parsed from the URL or `downloaded_file`.

---

## 💡 Example Outputs

```
Uploading file.zip...
Upload successful!
File ID    : RZxxyyzz
File Name  : file.zip
URL        : https://ranoz.gg/f/RZxxyyzz
```

### 🔁 Redirect Upload

```
➡️  Using downloader: wget
Enter file name to save as (or press Enter to use default):
✔️  Download finished. Now uploading...
```

---

## ⚖️ Licence

**Proprietary Licence — Personal Use Only**
Parts of this software are subject to a closed-source license.

---

## 🙏 Credits

* Platform/API: [Ranoz.gg](https://ranoz[.]gg)
* Script Author: [zamkara](https://github.com/zamkara)

---

## 🤝 Contributing

Currently closed-source. However, feedback and suggestions are always welcome.

Reach out via [GitHub Issues](https://github.com/zamkara/nya/issues)
