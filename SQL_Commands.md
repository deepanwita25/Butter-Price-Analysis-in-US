```SQL
  CREATE TABLE `nass`.`butter`(
	`id` INT auto_increment PRIMARY KEY,
    `date` date NOT NULL,
    `month_name` VARCHAR(10) NOT NULL,
    `month_no` bigint NOT NULL,
    `year` int NOT NULL,
    `product` VARCHAR(50) NOT NULL,
    `product_desc` VARCHAR(150) NOT NULL,
    `country` VARCHAR(150) NOT NULL,
    `state_name` VARCHAR(150) NOT NULL,
    `measure` VARCHAR(150) NOT NULL,
    `unit` VARCHAR(150) NOT NULL,
    `value` float NOT NULL,
    `sector` VARCHAR(150) NOT NULL,
    `source` VARCHAR(150) NOT NULL,
    `updated_at` timestamp default current_timestamp
		ON UPDATE current_timestamp,
    CONSTRAINT `unique_key` unique(`date`, `product`, `country`, `measure`, `unit`)
    )
ENGINE = InnoDB
DEFAULT char set = utf8mb4
collate = utf8mb4_0900_ai_ci;
```
```SQL
	CREATE TABLE `clal`.`wholesale_price`(
	`id` int auto_increment primary key,
    `year` int NOT NULL,
    `month` VARCHAR(50) NOT NULL,
    `product_desc` varchar(200) NOT NULL,
    `unit` varchar(50) NOT NULL,
    `month_no` INT NOT NULL,
    `product` varchar(150) NOT NULL,
    `country` varchar(150) NOT NULL,
    `state_name` varchar(150) NOT NULL,
    `measure` varchar(150) NOT NULL,
    `source` varchar(150) NOT NULL,
    `date` DATE NOT NULL,
    `value` double NOT NULL,
    `updated_at` timestamp default current_timestamp
		ON UPDATE current_timestamp,
	constraint `unique_key` UNIQUE(`date`, `year`, `month_no`, `product`, `country`, `source`)
    )
ENGINE = InnoDB
DEFAULT char set = utf8mb4
collate = utf8mb4_0900_ai_ci;

```

```SQL
	SHOW INDEX FROM `clal`.wholesale_price
```
```SQL
	ALTER TABLE clal.wholesale_price
	DROP INDEX unique_key;

	ALTER TABLE clal.wholesale_price
	ADD UNIQUE KEY unique_key (`date`, `year`, `month_no`, `product`, `country`, `source`, `unit`);
```
```SQL
	CREATE TABLE `clal`.`milk`(
	`id` INT auto_increment primary key,
    `year` INT NOT NULL,
    `month` VARCHAR(50) NOT NULL,
    `product_desc` VARCHAR(100) NOT NULL,
    `unit` VARCHAR(50) NOT NULL,
    `product` VARCHAR(100) NOT NULL,
    `country` VARCHAR(100) NOT NULL,
    `state_name` VARCHAR(100) NOT NULL,
    `measure` VARCHAR(100) NOT NULL,
    `source` VARCHAR(100) NOT NULL,
    `value` DOUBLE NOT NULL,
    `date` DATE NOT NULL,
    `month_no` INT NOT NULL,
    `updated_at` timestamp default current_timestamp
		ON update current_timestamp,
	CONSTRAINT `unique_key` UNIQUE(`year`, `month_no`, `date`, `unit`, `product`, `country`, `measure`)
    )
ENGINE = InnoDB
DEFAULT char set = utf8mb4
collate = utf8mb4_0900_ai_ci;
```

