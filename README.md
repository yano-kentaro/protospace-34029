# 〜Users Table〜  
## ・columns  
|column_name|column_type|remarks|
|-----------|-----------|-------|
|email|string|NOT NULL|
|password|string|NOT NULL|
|name|string|NOT NULL|
|profile|text|NOT NULL|
|occupation|text|NOT NULL|
|position|text|NOT NULL|
<br>

## ・association  
|tables_name|association_type|
|-----------|----------------|
|prototypes table|has_many|
|comments table|has_many|
<br>
<br>

# 〜Prototypes Table〜  
## ・columns  
|column_name|column_type|remarks|
|-----------|-----------|-------|
|title|string|NOT NULL|
|catch_copy|text|NOT NULL|
|concept|text|NOT NULL|
|image||Active Strageで実装|
|user|references||  
<br>

## ・association  
|tables_name|association_type|
|-----------|----------------|
|users table|belongs_to|
|comments table|has_many|
<br>
<br>

# 〜Comments Table〜  
## ・columns  
|column_name|column_type|remarks|
|-----------|-----------|-------|
|text|text|NOT NULL|
|user|references||
|prototype|references||  
<br>

## ・association  
|tables_name|association_type|
|-----------|----------------|
|users table|belongs_to|
|prototypes table|belongs_to|