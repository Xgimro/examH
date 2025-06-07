CREATE TABLE material_types ( material_type_id SERIAL PRIMARY KEY UNIQUE, material_type VARCHAR(100) UNIQUE NOT NULL, percent_of_loss NUMERIC(4,2));

CREATE TABLE product_types ( product_type_id SERIAL PRIMARY KEY UNIQUE, product_type VARCHAR(100) UNIQUE NOT NULL, coef_type_product NUMERIC(4,2));

CREATE TABLE products ( product_id SERIAL PRIMARY KEY UNIQUE, product_type_id INT REFERENCES product_types(product_type_id), product_name VARCHAR(100) UNIQUE NOT NULL, articul INTEGER UNIQUE NOT NULL, min_cost_for_partner NUMERIC(9,2), material_type_id INT REFERENCES material_types(material_type_id) );

CREATE TABLE workshops ( workshop_id SERIAL PRIMARY KEY UNIQUE, workshop_name VARCHAR(100) UNIQUE NOT NULL, workshop_type VARCHAR(100) NOT NULL, workshop_members INTEGER );

CREATE TABLE product_workshops( product_id INT REFERENCES products(product_id), workshop_id INT REFERENCES workshops(workshop_id), time_todo NUMERIC(2,2) NOT NULL );

ТЕМЧИК, НУЖНА ПОМОЩЬ С ЗАВИСИМОСТЯМИ: import/export data -> куда идти, в general, oprions или columns?

в генерал выбираешь файл, в  втором ставишь точку с зпт и двойные ковычки


я выбрала файл Прил_В4_КОД и тд, в конце поставили точку с зпт и двойные ковычки, мне выдало ошибку 

а почему ты его вырала, надо файл цсв котоыре появятсья когда ты эксель файлы переделаешь 

ебать я дура 
смотри, у меня у одной папки product_types, стоит 1, типо public - product_types - product_type character vacying(100) и вот перед этим стот 1, это норм или нет 

не понял нчиего

как сюда фотку добавить ?


add file на глайной странице
 добавила
