# mariadb

- https://mariadb.org/

## mariadb install on CentOS

- https://mariadb.com/ko/resources/blog/installing-mariadb-10-on-centos-7-rhel-7/

- https://mariadb.com/
    - Home > Download
    - apt/yum tab

```bash
curl -LsS https://downloads.mariadb.com/MariaDB/mariadb_repo_setup | sudo bash
yum install mariadb-server
systemctl start mariadb.service
# 비밀번호 변경
mysqladmin -uroot password <비밀번호 지정>
```

- 방화벽 추가

```bash
firewall-cmd --permanent --zone=public --add-port=3306/tcp

# OR

firewall-cmd --permanent --zone=public --add-service=mysql
```

- 자동 실행 설정

```bash
systemctl enable mariadb
systemctl is-enabled mariadb
```

