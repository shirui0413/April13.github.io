# MYSQL

### 创建DATABASE

#### 创建DATABASE

```
CREATE DATABASE `sql_tutorial`;     // ``是为了防止db名与关键字冲突
```

#### 显示DATABASE

```
SHOW DATABASES;
```

#### 删除DATABASE

```
DROP DATABASE `sql_turorial`;
```

### 创建表格

#### 数据类型

```
INT               --整数
DECIMAL(3,2)      --有小数点的数,  例，总共3位数，小数点后2位，2.33
VARCHAR(n)        --字串， 例，最多可存放n位字串
BLOB              --(Binary Large Object)图片，影片，档案
DATE              --'YYYY-MM-DD'
TIMESTAMP         --'YYYY-MM-DD HH:MM:SS'纪录时间
```

#### 创建表格

```
CREATE TABLE `student`(
    `student_id` INT PRIMARY KEY,
    `name` VARCHAR(20),
    `major` VARCHAR(20)
);


或主键的另一种写法
CREATE TABLE `student`(
    `student_id` INT,
    `name` VARCHAR(20),
    `major` VARCHAR(20),
    PRIMARY KEY(`student_id`)
);
```

#### 显示表格

```
DESCRIBE `student`；
```

#### 删除表格

```
DROP TABLE `student`;
```

#### 追加属性

```
ALTER TABLE `student` ADD `gpa` DECIMAL(3,2);
```

#### 删除属性

```
ALTER TABLE `student` DROP COLUMN `gpa`;
```

