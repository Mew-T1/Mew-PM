<template>
    <div>
        <p>
            本文档记录了 MySQL 的配置、数据迁移、维护。
        </p>

        <h2 tag-bar fs-md mt-xl mb-sm>MySQL 的配置</h2>
        <p>
            MySQL 通过配置文件对功能进行修改，<kbd>盘符:\安装路径\mysql-8.0.22-winx64</kbd> 目录下的 <kbd>my.ini</kbd> 文件，该配置文件是在安装时创建的，若修改需先停止 MySQL 服务。
        </p>
        <imager fill mx-auto :src="imgs[0]" width="80%"></imager>
        <small flex justify-center mt-xs mb-xl fs-xs>my.ini 的位置</small>
        <pre mx-auto quote py-md px-xl col-20>
<blockquote class="fs-xs">[mysqld]
# 设置 mysql 服务所占用的系统端口，默认是 3306
port=3306
# 设置 mysql 的安装目录
basedir=C:\ISD\mysql-8.0.22-winx64
# 设置 mysql 数据库的数据的存放目录
datadir=D:\Desktop\Git\Database\MySQL
# 允许最大连接数
max_connections=200
# 允许连接失败的次数。
max_connect_errors=10
# 服务端使用的字符集默认为 utf8mb4
character-set-server=utf8mb4
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
# 默认使用“mysql_native_password”插件认证
#mysql_native_password
default_authentication_plugin=mysql_native_password
[mysql]
# 设置 mysql 客户端默认字符集
default-character-set=utf8mb4
[client]
# 设置 mysql 客户端连接服务端时默认使用的端口
port=3306</blockquote>
        </pre>
        <small flex justify-center mt-xs mb-xl fs-xs>my.ini 的内容</small>
        <divider/>
    </div>
</template>

<script>
    import myini from './my_ini.png'
    export default {
        name: "MySQL",
        mounted(){
        },
        data(){
            return {
                imgs:[
                    myini
                ]
            }
        },
    }
</script>

<style scoped lang="scss">
div.testA{
    background-color: #00a1ff;
    width: 500px;height: 500px;
    div{
        height: 20px;
        background-color: grey;
    }
    div.testB{
        word-wrap: break-word;
        width: 200px;height: 200px;
        box-sizing: border-box;border: 1px solid black;
    }
}
</style>