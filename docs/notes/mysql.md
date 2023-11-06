[toc]
# MySQL

## 简介
MySQL是一个关系型数据库管理系统，由瑞典MySQL AB 公司开发，属于 Oracle旗下产品。MySQL是最流行的关系型数据库管理系统之一，在 WEB 应用方面，MySQL是最好的RDBMS (Relational Database Management System，关系数据库管理系统)应用软件之一。

MySQL是一种关系型数据库管理系统，关系数据库将数据保存在不同的表中，而不是将所有数据放在一个大仓库内，这样就增加了速度并提高了灵活性。

MySQL所使用的 SQL 语言是用于访问数据库的最常用标准化语言。MySQL 软件采用了双授权政策，分为社区版和商业版，由于其体积小、速度快、总体拥有成本低，尤其是开放源码这一特点，一般中小型和大型网站的开发都选择 MySQL作为网站数据库。

## 系统特性
1 MySQL使用 C和 C++编写，并使用了多种编译器进行测试，保证了源代码的可移植性。
2 支持 AIX、FreeBSD、HP-UX、Linux、Mac OS、NovellNetware、OpenBSD、OS/2 Wrap、Solaris、Windows等多种操作系统。
3 为多种编程语言提供了 API。这些编程语言包括 C、C++、Python、Java、Perl、PHP、Eiffel、Ruby,.NET和 Tcl 等。
4 支持多线程，充分利用 CPU 资源。
5 优化的 SQL查询算法，有效地提高查询速度。
6 既能够作为一个单独的应用程序应用在客户端服务器网络环境中，也能够作为一个库而嵌入到其他的软件中。
7 提供多语言支持，常见的编码如中文的 GB 2312、BIG5，日文的 Shift_JIS等都可以用作数据表名和数据列名。
8 提供 TCP/IP、ODBC 和 JDBC等多种数据库连接途径。
9 提供用于管理、检查、优化数据库操作的管理工具。
10 支持大型的数据库。可以处理拥有上千万条记录的大型数据库。
11 支持多种存储引擎。
12 MySQL 是开源的，所以你不需要支付额外的费用。
13 MySQL 使用标准的 SQL数据语言形式。
14 MySQL 对 PHP 有很好的支持，PHP是比较流行的 Web 开发语言。
15 MySQL是可以定制的，采用了 GPL协议，你可以修改源码来开发自己的 MySQL 系统。
16 在线 DDL/更改功能，数据架构支持动态应用程序和开发人员灵活性（5.6新增）
17 复制全局事务标识，可支持自我修复式集群（5.6新增）
18 复制无崩溃从机，可提高可用性（5.6新增）
19 复制多线程从机，可提高性能（5.6新增）
20 3倍更快的性能（5.7新增）
21 新的优化器（5.7新增）
22 原生JSON支持（5.7新增）
23 多源复制（5.7新增）
24 GIS的空间扩展 （5.7新增）

## 数据字典
```
SELECT
    t.TABLE_SCHEMA AS 库名,
    t.TABLE_NAME AS 表名,
    t.COLUMN_NAME AS 字段名,
    t.COLUMN_TYPE AS 数据类型,
    CASE IFNULL(t.COLUMN_DEFAULT,'Null')
        WHEN '' THEN '空字符串'
        WHEN 'Null' THEN 'NULL'
        ELSE t.COLUMN_DEFAULT END  AS 默认值,
    CASE t.IS_NULLABLE WHEN 'YES' THEN '是' ELSE '否' END AS 是否允许为空,
    t.COLUMN_COMMENT AS 字段说明
FROM information_schema.COLUMNS t
WHERE t.TABLE_SCHEMA='库名'  AND t.TABLE_NAME='表名'
```