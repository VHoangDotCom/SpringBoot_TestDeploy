# SpringBoot_TestDeploy
## 1. Dependencies
- Spring Web
- Jpa
- Lombok
- mssql - microsoft

## 2. Create folder + class
- Controller
- Repository
- Model

## 3. Create Source Group + Database on Azure
link : https://www.youtube.com/watch?v=puVMCRvdE9A

## 4. Config DB
- resources -> create new file -> application.yml
- config 
  
    spring:
      datasource:
        url: jdbc:sqlserver://springboot-server.database.windows.net:1433;database=CRUD_Basic;encrypt=true;trustServerCertificate=false;hostNameInCertificate=*.database.windows.net;loginTimeout=30;
        username: springboot-server
        password: your_password
      jpa:
        show-sql: true
        hibernate:
          ddl-auto: update
          dialect : org.hibernate.dialect.SQLServer2012Dialect
    
    server:
      port: 9191

## 5. Create Git Repository (App Service)
- Follow previous link
- Terminal Step:
- git init
- git status 
- git add pom.xml
- git add src/
- git commit -m "code"
- git branch -M main
- git remote add origin https://github.com/VHoangDotCom/SpringBoot_TestDeploy.git
- git push -u origin main
- Add README.md file

## 6. Create App Service ( follow https://www.youtube.com/watch?v=puVMCRvdE9A)
- 18:27

## 7. Check Build + Deploy status in Git
- Actions -> build - deploy (check)

## 8. Run Link in AppService
- If still cannot run -> restart AppService or check code





