**Disclaimer:**

All content in this repository is for learning and reference only and is prohibited for commercial use. No individual or organization may use the content of this repository for illegal purposes or infringe upon the legitimate rights and interests of others. The web crawling technology involved in this repository is only for learning and research purposes and may not be used for large-scale web crawling or other illegal activities on other platforms. This repository shall not be held liable for any legal liability arising from the use of its content. The use of the content in this repository implies that you agree to all the terms and conditions of this disclaimer.

# Repository Description

**Xiaohongshu Crawler**, **Douyin Crawler**, **Kuaishou Crawler**, **Bilibili Crawler**, **Weibo Crawler**...  
Currently capable of fetching videos, images, comments, likes, and reposts from Xiaohongshu, Douyin, Kuaishou, Bilibili, and Weibo.

Principle: Using [playwright](https://playwright.dev/) to build a bridge, retaining the context browser environment after successful login, and obtaining some encrypted parameters by executing JS expressions. This approach eliminates the need to reproduce core encrypted JS code, greatly reducing the difficulty of reverse engineering.

Crawler technology exchange group: [949715256](http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=NFz-oY7Pek3gpG5zbLJFHARlB8lKL94f&authKey=FlxIQK99Uu90wddNV5W%2FBga6T6lXU5BRqyTTc26f2P2ZK5OW%2BDhHp7MwviX%2BbrPa&noverify=0&group_code=949715256), welcome everyone to contribute code and submit PRs.

Video configuration tutorial: [MediaCrawler Video Tutorial](https://space.bilibili.com/434377496/channel/series)

## Thanks to the following sponsors for sponsoring this repository
<a href="https://dashboard.ipcola.com/register?referral_code=vkybwyucyuidpne">Global IP Proxy Supernova</a>
<a href="https://dashboard.ipcola.com/register?referral_code=vkybwyucyuidpne" target="_blank"><img src="https://s2.loli.net/2024/03/18/LKJaWcIHQl92ip5.jpg" alt="IPCola, Global IP Proxy Supernova - Official Website"></a>


Become a sponsor and showcase your product here. Contact the author: relakkes@gmail.com

## Feature List
| Platform | Cookie Login | QR Code Login | Specify Creator Homepage | Keyword Search | Specify Video/Post ID Crawling | Login State Cache | Data Saving | IP Proxy Pool | Slider Captcha |
|:--------:|:------------:|:-------------:|:------------------------:|:--------------:|:----------------------------:|:------------------:|:-----------:|:-------------:|:--------------:|
| Xiaohongshu |      ✅      |       ✅       |            ✅            |       ✅        |              ✅              |         ✅         |      ✅      |       ✅       |       ❌       |
| Douyin   |      ✅      |       ✅       |            ❌            |       ✅        |              ✅              |         ✅         |      ✅      |       ✅       |       ✅       |
| Kuaishou |      ✅      |       ✅       |            ❌            |       ✅        |              ✅              |         ✅         |      ✅      |       ✅       |       ❌       |
| Bilibili |      ✅      |       ✅       |            ❌            |       ✅        |              ✅              |         ✅         |      ✅      |       ✅       |       ❌       |
| Weibo    |      ✅       |       ✅        |            ❌            |       ✅         |              ✅               |          ✅          |       ✅      |        ✅        |        ❌        |


## Usage

### Create and activate a Python virtual environment
   ```shell   
   # Go to the project root directory
   cd MediaCrawler
   
   # Create a virtual environment
   python -m venv venv
   
   # Activate the virtual environment on macOS & Linux
   source venv/bin/activate

   # Activate the virtual environment on Windows
   venv\Scripts\activate

   ```

### Install dependencies

   ```shell
   pip3 install -r requirements.txt
   ```

### Install playwright browser driver

   ```shell
   playwright install
   ```

### Run the crawler program

   ```shell
   # Comment crawling mode is not enabled by default. If needed, please specify in the configuration file.
   # Fetch post information and comments based on keyword searches from the configuration file
   python main.py --platform xhs --lt qrcode --type search
   
   # Fetch information and comments of specified posts based on post IDs from the configuration file
   python main.py --platform xhs --lt qrcode --type detail
  
   # Open the corresponding app to scan the QR code for login
     
   # Example of using crawlers for other platforms, run the following command to check
   python main.py --help    
   ```


### Data saving
- Supports saving to relational databases (MySQL, PostgreSQL, etc.)
- Supports saving to CSV (in the data/ directory)
- Supports saving to JSON (in the data/ directory)

## Donation

If you find the project helpful, feel free to donate. Your support is my greatest motivation!

When donating, you can include your name as a note, and I will add you to the donation list.
<p>
  <img alt="WeChat Pay" src="static/images/wechat_pay.jpeg" style="width: 200px;margin-right: 140px;" />
  <img alt="Alipay" src="static/images/zfb_pay.jpeg" style="width: 200px" />
</p>

## Donation Information

PS: If you make a donation, please include your name as a note. If there are omissions, please contact me to add them (sometimes messages may be overlooked due to a large number of them, I apologize).

| Donor         | Amount  | Date       |
|-------------|-------|------------|
| Tsen Ming   | 100 CNY | 2024-03-18 |
| *Hao          | 50 CNY  | 2024-03-18 |
| *Gang          | 50 CNY  | 2024-03-18 |
| *Le          | 20 CNY  | 2024-03-17 |
| *Mu          | 20 CNY  | 2024-03-17 |
| *Cheng          | 20 CNY  | 2024-03-17 |
| Strem Gamer | 20 CNY  | 2024-03-16 |
| *Xin          | 20 CNY  | 2024-03
