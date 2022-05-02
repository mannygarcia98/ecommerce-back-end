-- MySQL Workbench Forward Engineering

SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0;
SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0;
SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';

---

-- Schema mydb

---

---

-- Schema ecommerce

---

---

-- Schema ecommerce

---

CREATE SCHEMA IF NOT EXISTS `ecommerce` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci ;
USE `ecommerce` ;

---

-- Table `ecommerce`.`tag`

---

CREATE TABLE IF NOT EXISTS `ecommerce`.`tag` (
`id` INT NOT NULL AUTO_INCREMENT,
`tag_name` VARCHAR(30) NOT NULL,
PRIMARY KEY (`id`))
ENGINE = InnoDB
AUTO_INCREMENT = 6
DEFAULT CHARACTER SET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;

---

-- Table `ecommerce`.`category`

---

CREATE TABLE IF NOT EXISTS `ecommerce`.`category` (
`id` INT NOT NULL AUTO_INCREMENT,
`category_name` VARCHAR(30) NOT NULL,
PRIMARY KEY (`id`))
ENGINE = InnoDB
AUTO_INCREMENT = 10
DEFAULT CHARACTER SET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;

---

-- Table `ecommerce`.`product`

---

CREATE TABLE IF NOT EXISTS `ecommerce`.`product` (
`id` INT NOT NULL AUTO_INCREMENT,
`product_name` VARCHAR(30) NOT NULL,
`price` DECIMAL(10,2) NOT NULL,
`stock` INT NOT NULL DEFAULT 10,
`category_id` INT NULL,
PRIMARY KEY (`id`),
INDEX `category_id_idx` (`category_id` ASC) VISIBLE,
CONSTRAINT `category_id`
FOREIGN KEY (`category_id`)
REFERENCES `ecommerce`.`category` (`id`)
ON DELETE NO ACTION
ON UPDATE NO ACTION)
ENGINE = InnoDB
AUTO_INCREMENT = 10
DEFAULT CHARACTER SET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;

---

-- Table `ecommerce`.`product_tag`

---

CREATE TABLE IF NOT EXISTS `ecommerce`.`product_tag` (
`id` INT NOT NULL AUTO_INCREMENT,
`product_id` INT NOT NULL,
`tag_id` INT NULL,
PRIMARY KEY (`id`),
INDEX `product_id_idx` (`product_id` ASC) VISIBLE,
INDEX `tag_id_idx` (`tag_id` ASC) VISIBLE,
CONSTRAINT `product_id`
FOREIGN KEY (`product_id`)
REFERENCES `ecommerce`.`product` (`id`)
ON DELETE NO ACTION
ON UPDATE NO ACTION,
CONSTRAINT `tag_id`
FOREIGN KEY (`tag_id`)
REFERENCES `ecommerce`.`tag` (`id`)
ON DELETE NO ACTION
ON UPDATE NO ACTION)
ENGINE = InnoDB
AUTO_INCREMENT = 6
DEFAULT CHARACTER SET = utf8mb4
COLLATE = utf8mb4_0900_ai_ci;

SET SQL_MODE=@OLD_SQL_MODE;
SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS;
SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS;
