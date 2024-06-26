# SpringAccountTest-Docker



## 安裝方式:
*  <h3> 將此專題 clone  </h3> 
<img width="822" alt="image" src="https://github.com/ShaoweiTeng-lab/SpringAccountTest-Docker/assets/50354880/9b920fa1-ce3d-49dc-8d4e-8c14fe19637f">

*  <h3> 打開 cmd 進入 該資料夾 </h3> 
<img width="822" alt="image" src="https://github.com/ShaoweiTeng-lab/SpringAccountTest-Docker/assets/50354880/f2225633-5217-408b-835e-dab96fc861e1">


*  <h3> 使用docker-compose build --no-cache 製作Docker Image </h3> 
```
docker-compose build --no-cache
```
<img width="822" alt="image" src="https://github.com/ShaoweiTeng-lab/SpringAccountTest-Docker/assets/50354880/536f7ef5-6ab3-49d3-9057-d9df08057674">

*  <h3> 使用docker-compose up -d 運行  </h3> 
```
docker-compose up -d
```
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest-Docker/assets/50354880/62a6820a-1a87-4d55-bc9e-e85ab0578f6e)





## MySql Table:
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/984446bc-7888-4008-acb3-ceb2ea724618)
## 使用技術:
### * Spring boot 2.7.13
### * Spring boot Starter Security 2.7.13
### * mysql 8.0.33
### * Redis
### * Swagger (knife4j)



### 測試方式:
 * Local測試網址: http://localhost:8080/doc.html#/home
 
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/132072cf-956a-4996-bf05-265aa990af3e)

### <h2> 資料庫預設資料 (帳號密碼相同，使用 bcryptPasswordEncoder 加密) </h2>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/84e86841-940a-4584-a3e6-9f1c2e28b17f)


## 功能展示(會員):

* <h2> 註冊會員 (新增功能) : </h2>
  
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/0ebed0d9-03c3-4a1f-b9f8-f47d56cd4582)

* <h2> 登入會員 拿到token :</h2>

![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/eb29d7cc-fb67-49f7-bc13-e07210050728)


* <h2> 查詢此帳戶資訊 (單筆查詢):</h2>

  1. <h3> 在 header 中帶入 token </h3> 
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/1d4313b2-9721-4542-8368-e892a27574ca)
  2. <h3> 取得此帳戶資訊</h3>
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/0df8a664-3139-4411-948d-387c196bfe48)
* <h2>會員修改密碼 (修改功能):</h2>

  1. <h3> 在 header 中帶入 token </h3> 
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/4d70d448-17d6-4432-bb4b-3c03fb88688f)
  2. <h3> 在RequestBody 設定密碼 </h3>
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/c9743916-3605-4cc6-a13b-3b38277f95d0)
  3. <h3> 再次登入 即可以新密碼登入</h3>
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/08424978-368b-4b29-a4b6-00486c0738c7)




## 功能展示(管理員):
* <h2>登入管理員 拿到token : </h2>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/6c29616e-e7b8-4682-9d2c-53baafb14458)

* <h2>管理員查詢會員(關鍵字查詢、分頁查詢) : </h2> 

   1. <h3> 在 header 中帶入 token</h3>
      
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/84ef5806-db3e-4997-9776-37e8f507c5b3)
  
   2. <h3> 取得會員資訊</h3>
      * 可帶參數 : search (帳戶名稱，使用模糊查詢) 、page(頁數)、 order(排序類別) 、 size(回傳筆數) 、sort (降冪、 升冪 )

     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/78a0dd1e-19e8-4822-9d2b-310aaefb56e1)
 
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/a711a636-b91e-4ea9-a516-6c3626333908)


*  <h2> 管理員修改帳戶狀態(修改功能): </h2>  
  1. <h3> 在 header 中帶入 token</h3>
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/95334ba2-3927-4a37-9db8-5e4bdf6d4e3a)
     
  2. <h3> 設定帳戶狀態為 : 開啟/停權</h3>
  
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/8cda36b3-076a-4d5f-a639-974446a3f438)
     
* <h3> 管理員刪除帳戶(刪除功能):</h3>

    1. <h3> 在 header 中帶入 token</h3>
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/ababb7b9-568a-474f-8342-8b381dad3c7c)
  
    2. <h3> 刪除會員資訊</h3>
     ![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/30f7a493-95c0-4322-bd5d-eb7691a8b478)

     
## 異常處理
* <h3>密碼錯誤</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/4eaa81d4-5d50-4951-bff2-53122a205284)

*  <h3>無此帳戶</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/d0d8ffe1-ee50-4c1a-a286-759da64eaefe)
*  <h3>帳戶停權後 登入</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/548f77ab-18db-4855-b48e-25c364e5b72c)
*  <h3>會員使用token 呼叫管理員專用 api</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/f70b37cd-7306-4f6e-a47d-9b6573191000)
*  <h3>管理員刪除管理員</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/d497a7aa-3d35-42a8-bc5d-eac2173a5e33)
*  <h3>更改管理員帳號狀態</h3>
![image](https://github.com/ShaoweiTeng-lab/SpringAccountTest/assets/50354880/807e39d6-8c83-451e-ac82-75ba6d8a074f)



<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki

<h1>My Skills</h1>

[![My Skills](https://skillicons.dev/icons?i=java,spring,css,html,redis,mysql,maven,hibernate,js&theme=light)](https://skillicons.dev)
