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
