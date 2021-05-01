# CakePHP 4 Timezone Aware Application

Sample CakePHP install that I used to get a better rudimentary understanding of timezone aware application.

* Uses locale middleware
* UTC for DB and Application
* Convert to local timezone for frontend
* TimeHelper configuration and settings
* TIME type to StringType so TIME is viewed as a string


From my blog post at [https://toggen.com.au/it-tips/cakephp-4-time-zones/](https://toggen.com.au/it-tips/cakephp-4-time-zones/)

This is the DB table


```sql


CREATE TABLE `users` (
  `id` bigint unsigned NOT NULL AUTO_INCREMENT,
  `email` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL,
  `created` timestamp NULL DEFAULT NULL,
  `modified` timestamp NULL DEFAULT NULL,
  `tzdate` datetime DEFAULT NULL,
  `tztime` time DEFAULT NULL,
  `timezone` varchar(100) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=10 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;


```

