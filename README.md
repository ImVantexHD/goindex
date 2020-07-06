![GoIndex](https://raw.githubusercontent.com/imvantexhd/goindex/master/themes/logo.png)  

GoIndex  
====  

This is a modified version of [goindex](https://github.com/yanzai/goindex) which adds multi-disk support, search, and incremental loading to the [original goindex](https://github.com/donwa/goindex)

`index.js` contains the code needed for Workers.

## Preview

Demo: https://yanzai-goindex.java.workers.dev



Multi-disk：  
![Multi-disk](imgs/1.png)



Search：  
![Search](imgs/2.png)



Incremental loading：  
![Incremental loading](imgs/3.png)



## Changelog

### 2020-4-28

- Added Basic Auth Authentication with individually configurable username and password for each disk to protect all subfiles and subfolders on that disk.

- Support for custom theme colors, dark_mode added ; can be configured in `uiConfig`.

- The .password authentication method of the original goindex remains as a back-up authentication method, but isn't enabled by default.

  See the comments on the config in `index.js`.

### 2020-4-23

- Added support for opening nPlayer / MXPlayer Free / MXPlayer Pro / PotPlayer / VLC for playback and copying of direct links.
- Simple PDF Preview Support
- You can configure whether or not to allow other web frontends to fetch files with CORS.

### 2020-3-9

- flac file play support

### 2020-3-7

- Added search function, incremental loading in search results, and support for opening the corresponding path
- Search function supports personal and team search.
- Search page loading is configurable, see `index.js`
- Tried to solve the incremental loading issue when scrolling to the bottom on mobile
- UI optimization, disk selection changed to drop-down box display

### 2020-3-5

- Added incremental loading in file list, supports custom page size, multi-page content can be cached, see `index.js`
- Photo Gallery Previous/Next Navigation
- Optimized listing speed

### 2020-3-4

Modified from the original:

- Added multi-disk support, you can set mulitple disks to be displayed and the respective passwords.
- Only material is modified at the front end, so classic theme is not supported.
- See `index.js` comments for configuration
  



## Deployment  
1.Install `rclone` software locally  
2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  
3.Execute the command`rclone config file` to find the file `rclone.conf` path  
4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  
5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  
6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## Quick Deployment  
1.Open https://installen.gd.workers.dev/  
2.Auth and get the code  
3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  



## About  
Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  
