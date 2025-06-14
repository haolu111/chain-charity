# chain-charity
chain-charity是一个基于Spring Boot和Fisco区块链的公益项目系统，旨在通过区块链技术提高公益活动的透明度和信任度。系统允许用户注册、登录、参与公益项目捐款，同时通过区块链技术追踪捐款的使用情况。
## 安装环境要求
操作系统：支持Linux和Windows操作系统。\
JDK：JDK 1.8 或更高版本。\
数据库：MySQL 5.7 或更高版本。\
区块链环境：Fisco BCOS节点已部署且运行正常。\
内存和存储：最低要求4GB RAM，20GB硬盘空间。
## 安装过程
(1) 环境准备
确保已安装Java环境和MySQL数据库，并且Fisco BCOS节点运行正常。
(2) 下载项目
(3) 配置项目
- 修改`src/main/resources/application.properties`文件，配置数据库连接和区块链节点信息。\
properties\
spring.datasource.url=jdbc:mysql://localhost:3306/yourdb?useSSL=false&serverTimezone=UTC\
spring.datasource.username=yourusername\
spring.datasource.password=yourpassword\
### 区块链节点配置
blockchain.nodeAddress=节点地址\
blockchain.privateKey=你的私钥\
(4) 构建项目
使用Maven构建项目：\
mvn clean package\
(5) 运行项目
java -jar target/yourproject-0.0.1-SNAPSHOT.jar\
项目启动后，访问`http://localhost:8081`查看项目首页。\
## 主要流程
(1)默认安装流程\
按照上述安装过程进行，即可完成项目的默认安装。确保所有环境依赖满足，并正确配置项目文件。\
(2)典型使用流程\
捐助者\
①用户注册和登录：用户首次访问系统需进行注册，注册成功后进行登录。\
②浏览公益项目：登录后，用户可以浏览当前的公益项目列表。\
③捐款：用户选择一个公益项目进行捐款，输入捐款金额并提交。\
④捐款追踪：系统通过FiscoBCOS区块链技术记录捐款流向，用户可以实时查看自己捐款的使用情况。\
受益者\
①注册和登录：受益者首次访问系统需要进行注册，注册成功后进行登录。\
②查看捐款情况：登录后，受益者可以查看自己受益的公益项目列表，以及每个项目收到的捐款情况。\
③申请资助：受益者可以选择一个公益项目，并向该项目发起资助申请，说明申请资助的原因和资金需求。\
④资助追踪：系统通过FiscoBCOS区块链技术记录资助流向，受益者可以实时查看自己所申请到的资助使用情况。\
管理员\
①登录管理后台：管理员登录系统后台，获得管理权限。\
②管理公益项目：管理员可以对公益项目进行管理，包括创建新的公益项目、编辑项目信息、审核受益者的资助申请等。\
③监督资金流向：管理员可以通过系统记录的资金流向数据，监督捐款和资助的使用情况，确保资金使用合法合规。\
④处理异常情况：管理员负责处理系统中出现的异常情况，如资助申请审核问题、捐款记录错误等，确保平台的正常运行和公平公正。
