2024年10月 linode centos最低版本7.9 不能正常安装使用，以下是安装bt 5.9.1免费版本的记录过程！<br>
1.更新linode centos7.9 yum数据源 wget都不能使用<br>
下载:<code>https://mirrors.aliyun.com/repo/Centos-7.repo</code> 重命名CentOS-Base.repo <br>
覆盖到/etc/yum.repos.d/CentOS-Base.repo<br>
2.安装wget<br>
yum install wget<br>
3.下载安装文件<br>
wget --no-check-certificate https://raw.githubusercontent.com/ysmtw2024/linode-centos7.9/master/install-5.9.1.sh<br>
chmod +x install-5.9.1.sh<br>
sh install-5.9.1.sh<br>
4.更新ssl可用文件<br>
wget --no-check-certificate /root/.acme.sh/acme.sh https://raw.githubusercontent.com/ysmtw2024/linode-centos7.9/master/acme.sh<br>
chmod 755 /root/.acme.sh/acme.sh<br>
（默认ssl使用zerossl.com，需要修改默认acme.sh的ssl文件生成路径把路径中<br>
/www/server/panel/vhost/cert 域名的_ecc 去掉即可使用，后续或许需要升级备注待用）
<br>
内容资源来源：<br>
bt历史版本：https://github.com/lolkda/LinuxPanel/<br>
安装脚本借鉴:https://github.com/leitbogioro/Crack_BT_Panel<br>
