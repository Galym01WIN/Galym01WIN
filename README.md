create database University;
use University;

-- -------------------------------------- --
CREATE TABLE Department(
  ID INT NOT NULL AUTO_INCREMENT,
    Name VARCHAR(255) NOT NULL,
    PRIMARY KEY(ID)
);
INSERT INTO Department(Name) VALUES ('SDU');
SELECT * FROM Department;

CREATE TABLE Faculty(
  ID INT NOT NULL AUTO_INCREMENT,
    Name VARCHAR(255) NOT NULL,
    Department_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (Department_ID) REFERENCES Department(ID)
); 

INSERT INTO Faculty VALUES
(1, 'Business School', 1),
(2, 'Engineering and Natural Sciences', 1),
(3, 'Social Sciences', 1),
(4, 'Education and Humanities', 1);

CREATE TABLE Specialty(
  ID INT NOT NULL AUTO_INCREMENT,
    Name VARCHAR(255) NOT NULL,
    Faculty_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (Faculty_ID) REFERENCES Faculty(ID)
);

INSERT INTO Specialty VALUES
(1,'Materials Science',2),
(2,'Electrical',2),
(3,'Computers',2),
(4,'Mechanical',2),
(5,'Nuclear Technology',2),
(6,'Civil Engineering',2),
(7,'Industrial',2),
(8,'Aerospace',2),
(9,'Operations Research',2),
(10,'Metals-Metallurgy',2),
(11,'Miscellaaneous',2),
(12,'Information Systems',2),
(13,'Math Science',2),
(14,'Phisic Science',2),
(15,'Math teacher',2),
(16,'Physics teacher',2),
(17,'Computer Science',2),
(18,'Accounting',1),
(19,'Business Analytics',1),
(20,'Entrepneourship',1),
(21,'Finance',1),
(22,'Information Systems',1),
(23,'Management',1),
(24,'Marketing',1),
(25,'Nonprofit',1),
(26,'Production',1),
(27,'ProjectManagment',1),
(28,'Accounting',3),
(29,'Antropology',3),
(30,'Archelogy and History',3),
(31,'Architecture', 3),
(32,'Economics', 3),
(33,'Emerging issues', 3),
(34,'Geograhpy', 3),
(35,'Law', 3),
(36,'ManagementStudios', 3),
(37,'Media', 3),
(38,'Other social science', 3),
(39,'Political Science', 3),
(40,'Social Science', 4),
(41,'Population Studios', 4),
(42,'Physylogy', 4),
(43,'Sociology', 4),
(44,'Technology Management', 4),
(45,'Tourism', 4),
(46,'Transportation', 4),
(47,'Arts and Culture', 4),
(48,'Dances', 4),
(49,'Historical', 4),
(50,'Music', 4),
(51,'Other humanities', 4);


CREATE TABLE City(
  ID INT NOT NULL,
    Name VARCHAR(255) NOT NULL,
    PRIMARY KEY(ID)
);
create index nout on City(Name)
INSERT INTO City VALUES
(1, 'Atyrau'),
(2, 'Aqtau'),
(3, 'Aqtobe'),
(4, 'Qostanai'),
(5, 'Pavlodar'),
(6, 'Astana'),
(7, 'Qyzylorda'),
(8, 'Shymkent'),
(9, 'Taraz'),
(10, 'Almaty'),
(11, 'Oskemen'),
(12, 'Semey'),
(13, 'Qaragandy'),
(14, 'Taldyqorgan'),
(15, 'Aral'),
(16, 'Qazaly'),
(17, 'Baiqonyr'),
(18, 'Ankara'),
(19, 'Istanbul'),
(20, 'Paris'),
(21, 'Moskva'),
(22, 'Mexico'),
(23, 'Manilla'),
(24, 'Afina'),
(25, 'London'),
(26, 'Seul'),
(27, 'Singapur'),
(28, 'Izmir'),
(29, 'Bursa'),
(30, 'Adana'),
(31, 'Konya'),
(32, 'Antalya'),
(33, 'Samsun'),
(34, 'Mersin'),
(35, 'Kayseri'),
(36, 'Denizli'),
(37, 'Baku'),
(38, 'Quba'),
(39, 'Tartar'),
(40, 'Masally'),
(41,'Bangor'),
(42,'Bath'),
(43,'Bradford'),
(44,'Bristol'),
(45,'Cambridge'),
(46,'Carlisle'),
(47,'Cardiff'),
(48,'Chester'),
(49,'Chelmsford'),
(50,'Coventry'),
(51,'Derby'),
(52,'Doncaster'),
(53,'Dundee'),
(54,'Dunfermline'),
(55,'Exeter'),
(56,'Glasgow'),
(57,'Hereford'),
(58,'Lancaster'),
(59,'Leicester'),
(60,'Lincoln'),
(61,'Manchestor'),
(62,'Norwich'),
(63,'Preston'),
(64,'Ripon'),
(65,'Albans'),
(66,'Davids'),
(67,'Sunderland'),
(68,'Truro'),
(69,'Wells'),
(70,'Agryz'),
(71,'Alagir'),
(72,'Anadyr'),
(73,'Apatity'),
(74,'Belaya'),
(75,'Bely'),
(76,'Bor'),
(77,'Bolokhova'),
(78,'Chadan'),
(79,'Chekhov'),
(80,'Chita'),
(81,'Elista'),
(82,'Fokino'),
(83,'Bristol'),
(84,'Cambridge'),
(85,'Glazov'),
(86,'Vahdat'),
(87,'Farkhor'),
(88,'Isfara'),
(89,'Hulbuk'),
(90,'Buston'),
(91,'Norak'),
(92,'Hisor'),
(93,'Sharora'),
(94,'Panj'),
(95,'Sovet'),
(96,'Sfax'),
(97,'Gafsa'),
(98,'Bizerte'),
(99,'Kairouan'),
(100,'Gabes'),
(101, 'New York');

CREATE TABLE Country(
  ID INT NOT NULL,
    Name VARCHAR(255) NOT NULL,
    PRIMARY KEY(ID)
);
create index rout on Country(Name);

INSERT INTO Country VALUES
(1, 'Kazakhstan'),
(2, 'Russia'),
(3, 'Azerbaijan'),
(4, 'Turkey'),
(5, 'France'),
(6, 'Germany'),
(7, 'Italia'),
(8, 'Spain'),
(9, 'Argentina'),
(10, 'Morocco'),
(11, 'Portugal'),
(12, 'Brazil'),
(13, 'Armenia'),
(14, 'Tadjikistan'),
(15, 'Belarus'),
(16, 'Belgium'),
(17, 'Canada'),
(18, 'China'),
(19, 'Columbia'),
(20, 'Costa Rica'),
(21, 'USA'),
(22, 'Estonia'),
(23, 'Ghana'),
(24, 'India'),
(25, 'Indonesia'),
(26, 'Iran'),
(27, 'Iraq'),
(28, 'Jamaica'),
(29, 'Jordan'),
(30, 'Japan'),
(31, 'Qyrqystan'),
(32, 'Latvia'),
(33, 'Mali'),
(34, 'New Zealand'),
(35, 'Netherlands'),
(36, 'Nigeria'),
(37, 'North Korea'),
(38, 'Norway'),
(39, 'Pakistan'),
(40, 'Paraguay'),
(41, 'Peru'),
(42, 'Poland'),
(43, 'Qatar'),
(44, 'Romania'),
(45, 'Senegal'),
(46, 'Serbia'),
(47, 'Slovenia'),
(48, 'South Korea'),
(49, 'Sri Lanka'),
(50, 'Sweden');



CREATE TABLE PersonalData(
  ID INT NOT NULL AUTO_INCREMENT,
    Position ENUM('Student', 'Teacher', 'Advisor') NOT NULL,
    FirstName VARCHAR(255) NOT NULL,
    LastName VARCHAR(255) NOT NULL,
    IsForeign BOOLEAN,
    Email VARCHAR(255),
    Phone VARCHAR(20),
    Gender ENUM('male', 'female') NOT NULL,
    City_ID INT NOT NULL,
    Country_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (City_ID) REFERENCES City(ID),
    FOREIGN KEY (Country_ID) REFERENCES Country(ID)
);


INSERT INTO Country VALUES
(1, 'Kazakhstan'),
(2, 'Russia'),
(3, 'Azerbaijan'),
(4, 'Turkey'),
(5, 'France'),
(6, 'Germany'),
(7, 'Italia'),
(8, 'Spain'),
(9, 'Argentina'),
(10, 'Morocco'),
(11, 'Portugal'),
(12, 'Brazil'),
(13, 'Armenia'),
(14, 'Tadjikistan'),
(15, 'Belarus'),
(16, 'Belgium'),
(17, 'Canada'),
(18, 'China'),
(19, 'Columbia'),
(20, 'Costa Rica'),
(21, 'USA'),
(22, 'Estonia'),
(23, 'Ghana'),
(24, 'India'),
(25, 'Indonesia'),
(26, 'Iran'),
(27, 'Iraq'),
(28, 'Jamaica'),
(29, 'Jordan'),
(30, 'Japan'),
(31, 'Qyrqystan'),
(32, 'Latvia'),
(33, 'Mali'),
(34, 'New Zealand'),
(35, 'Netherlands'),
(36, 'Nigeria'),
(37, 'North Korea'),
(38, 'Norway'),
(39, 'Pakistan'),
(40, 'Paraguay'),
(41, 'Peru'),
(42, 'Poland'),
(43, 'Qatar'),
(44, 'Romania'),
(45, 'Senegal'),
(46, 'Serbia'),
(47, 'Slovenia'),
(48, 'South Korea'),
(49, 'Sri Lanka'),
(50, 'Sweden');


CREATE TABLE PersonalData(
  ID INT NOT NULL AUTO_INCREMENT,
    Position ENUM('Student', 'Teacher', 'Advisor') NOT NULL,
    FirstName VARCHAR(255) NOT NULL,
    LastName VARCHAR(255) NOT NULL,
    IsForeign BOOLEAN,
    Email VARCHAR(255),
    Phone VARCHAR(20),
    Gender ENUM('male', 'female') NOT NULL,
    City_ID INT NOT NULL,
    Country_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (City_ID) REFERENCES City(ID),
    FOREIGN KEY (Country_ID) REFERENCES Country(ID)
);
create index qazaq on personaldata(firstname,lastname);
select  PA.ID , PA.Position, PA.FirstName, PA.LastName, PA.Email, PA.phone_number, PA.Gender,PA.City_ID,PA.Country_ID from personaldata as PA;



select P.ID , P.Position , P.FirstName, P.LastName, P.Email 
from personaldata  as P
ORDER BY P.FirstName asc;

select P.gender , count(*) 
from personaldata as P
group by P.gender ;
 
INSERT INTO PersonalData VALUES
(1, 'Advisor', 'Zhanar', 'Zhoha', false, 'zhanarZh@mail.ru', '+77476155417', 'female', 1, 1),
(2, 'Advisor', 'Erbol', 'Erkha', false, 'erbolEr@mail.ru', '+77476145414', 'male', 3, 1),
(3, 'Advisor', 'Maqsat', 'Maga', false, 'maqsatMg@mail.ru', '+77076538497', 'male', 5, 1),
(4, 'Advisor', 'Duman', 'Telman', false, 'dumanDuka@mail.ru', '+77476184537', 'male', 1, 1),
(5, 'Advisor', 'Aiman', 'Aiau', false, 'aimanAr@mail.ru', '+77478332137', 'female', 8, 1),
(6, 'Advisor', 'Ulpan', 'Ulbul', false, 'ulpanchik01@mail.ru', '+77476123456', 'female', 10, 1),
(7, 'Advisor', 'Galym', 'Gala', false, 'galaDuka@mail.ru', '+77777777777', 'male', 7, 1),
(8, 'Advisor', 'Perizat', 'Yessenova', false, 'perizatyessenova@mail.ru', '+77004567134', 'female', 8, 1),
(9, 'Advisor', 'Aizada', 'Kuanyshkyzy', false, 'aizaka@mail.ru', '+77476165537', 'female', 1, 1),
(10, 'Advisor', 'Sayat', 'Ayazbai', false, 'ayazbaiS@mail.ru', '+77476145325', 'male', 13, 1),
(11, 'Student', 'Dauren', 'Baibai', false, 'baybai@mail.ru', '+77476145695', 'male', 13, 1),
(12, 'Student', 'Eldos', 'Zharkyn', false, 'zharkyniS@mail.ru', '+774761444525', 'male', 17, 1),
(13, 'Student', 'Dias', 'Erbaev', false, 'erbabaeviS@mail.ru', '+774781444525', 'male', 14, 1),
(14, 'Student', 'Doshan', 'Aikyn', false, 'doshan@mail.ru', '+7747614544578', 'male', 7, 1),
(15, 'Student', 'Sazhen', 'Zharkyn', false, 'sazhenS@mail.ru', '+774745644525', 'male', 3, 1),
(16, 'Student', 'Zhandos', 'Onaibaev', false, 'zhandos@mail.ru', '+77474654525', 'male', 9, 1),
(17, 'Student', 'Rakhym', 'Basbaev', false, 'rakhym@mail.ru', '+774745444625', 'male', 15, 1),
(18, 'Student', 'Tasbol', 'Raikyn', false, 'tasblo@mail.ru', '+774761444465', 'male', 14, 1),
(19, 'Student', 'Aiym', 'Qazbay', false, 'qazbay@mail.ru', '+774745444525', 'female', 11, 1),
(20, 'Student', 'Ernar', 'Kabdolov', false, 'ernark@mail.ru', '+774761347524', 'male', 17, 1),
(21, 'Student', 'Madina', 'Erbolava', false, 'madinak@mail.ru', '+774745647523', 'female', 15, 1),
(22, 'Student', 'Amina', 'Abdolov', false, 'aminek@mail.ru', '+774761347789', 'female', 13, 1),
(23, 'Student', 'Qaisar', 'Dosdolov', false, 'dosdolovk@mail.ru', '+774761344633', 'male', 17, 1),
(24, 'Student', 'Dosbol', 'Sasbaev', false, 'ernark@mail.ru', '+774761347524', 'male', 7, 1),
(25, 'Student', 'Nurislam', 'Sakitzhan', false, 'nurik@mail.ru', '+774748947533', 'male', 2, 1),
(26, 'Student', 'Rasul', 'Daldolov', false, 'rasulk@mail.ru', '+774755547104', 'male', 6, 1),
(27, 'Student', 'Tasbay', 'Qazbolov', false, 'tasbay@mail.ru', '+774761345594', 'male', 4, 1),
(28, 'Student', 'Yerbol', 'Kabdolov', false, 'yerbol@mail.ru', '+774778944529', 'male', 7, 1),
(29, 'Student', 'Ernar', 'Kabdolov', false, 'ernark@mail.ru', '+774761347524', 'male', 17, 1),
(30, 'Student', 'Sagdat', 'Besbay', false, 'saga@mail.ru', '+774745347434', 'male', 11, 1),
(31, 'Student', 'Anuar', 'Ospanov', false, 'anuark@mail.ru', '+774761346894', 'male', 9, 1),
(32, 'Student', 'Darhan', 'Erhanov', false, 'darhan@mail.ru', '+774765547544', 'male', 8, 1),
(33, 'Student', 'Uali', 'Lesbay', false, 'ualil@mail.ru', '+774767847528', 'male', 12, 1),
(34, 'Student', 'Olzhas', 'Abdolov', false, 'abdolov@mail.ru', '+774764544534', 'male', 15, 1),
(35, 'Student', 'Erbol', 'Bakytzhanov', false, 'bakytzhan@mail.ru', '+774761447515', 'male', 14, 1),
(36, 'Student', 'Damir', 'Zhanybekov', false, 'zhanybekov@mail.ru', '+774761345641', 'male', 1, 1),
(37, 'Student', 'Madiyar', 'Kalzhanov', false, 'kalzhanov@mail.ru', '+774767895243', 'male', 5, 1),
(38, 'Student', 'Damir', 'Olzhan', false, 'olzhan@mail.ru', '+774761344567', 'male', 9, 1),
(39, 'Student', 'Raibek', 'Erkegali', false, 'yerkesh@mail.ru', '+774725847534', 'male', 3, 1),
(40, 'Student', 'Zangar', 'Daldolov', false, 'zangar@mail.ru', '+774761347523', 'male', 6, 1),
(41, 'Student', 'Sayat', 'Erbolov', false, 'sayat@mail.ru', '+774771546522', 'male', 4, 1),
(42, 'Student', 'Toktar', 'Gabit', false, 'toha@mail.ru', '+774764337524', 'male', 6, 1),
(43, 'Student', 'Nazar', 'Gava', false, 'nazar@mail.ru', '+774765337548', 'male', 9, 1),
(44, 'Student', 'Nazgul', 'Kabdolova', false, 'nazgul@mail.ru', '+774761344463', 'female', 15, 1),
(45, 'Student', 'Nazerke', 'Galym', false, 'nazek@mail.ru', '+774761345655', 'female', 3, 1),
(46, 'Student', 'Aiganym', 'Yernar', false, 'aigan@mail.ru', '+774771546645', 'female', 7, 1),
(47, 'Student', 'Nurai', 'Galym', false, 'nurai@mail.ru', '+770764345751', 'female', 7, 1),
(48, 'Student', 'Nazerke', 'Galym', false, 'nazek@mail.ru', '+774761345655', 'female', 3, 1),
(49, 'Student', 'Zhanar', 'Bakytzhanova', false, 'zhan@mail.ru', '+774761342004', 'female', 7, 1),
(50, 'Student', 'Dana', 'Erkekyzy', false, 'dana@mail.ru', '+774741647845', 'female', 11, 1),
(51, 'Student', 'Erke', 'Dosbolkyzy', false, 'erke@mail.ru', '+774778344551', 'female', 9, 1),
(52, 'Student', 'Naz', 'Alymova', false, 'alymova@mail.ru', '+770745345249', 'female', 8, 1),
(53, 'Student', 'Aizhan', 'Toty', false, 'aizhan@mail.ru', '+774700010289', 'female', 13, 1),
(54, 'Student', 'Raigul', 'Dosanbaeva', false, 'raigul@mail.ru', '+770278345663', 'female', 18, 1),
(55, 'Student', 'Madina', 'Tostan', false, 'madina12@mail.ru', '+774711345604', 'female', 2, 1),
(56, 'Student', 'Zhandos', 'Elymov', false, 'zhandos@mail.ru', '+770727642578', 'male', 5, 1),
(57, 'Student', 'Nalina', 'Taspay', false, 'nalinak@mail.ru', '+770271645751', 'female', 3, 1),
(58, 'Student', 'Amina', 'Durken', false, 'aminad@mail.ru', '+774701045058', 'female', 9, 1),
(59, 'Student', 'Aizere', 'Tulegenova', false, 'tulegen@mail.ru', '+777700345115', 'female', 7, 1),
(60, 'Student', 'Nazerke', 'Tolepbergen', false, 'naz@mail.ru', '+77001341289', 'female', 5, 1),
(61, 'Student', 'Abdullah', 'Arslan', true, 'abdullah@mail.ru', '+902582132965', 'male', 36, 4),
(62, 'Student', 'Emine', 'Çakir', true, 'eminecakir@mail.ru', '+90258432865', 'female', 36, 4),
(63, 'Student', 'Hasan', 'Erdoğan', true, 'hasan@mail.ru', '+902165683987', 'male', 19, 4),
(64, 'Student', 'Hanife', 'Kara', true, 'karah@mail.ru', '+902161239736', 'female', 19, 4),
(65, 'Student', 'Kadir', 'Koç', true, 'kadir@mail.ru', '+902164358765', 'male', 19, 4),
(66, 'Student', 'Yusuf', 'Yilmaz', true, 'yusufyilmaz@mail.ru', '+902429876543', 'male', 32, 4),
(67, 'Student', 'Kemal', 'Korkmaz', true, 'korkmazkemal@mail.ru', '+902425464765', 'male', 32, 4),
(68, 'Student', 'Merve', 'Kurt', true, 'merve@mail.ru', '+902424937635', 'female', 32, 4),
(69, 'Student', 'Özlem', 'Özkan', true, 'özkan@mail.ru', '+903624358765', 'female', 33, 4),
(70, 'Student', 'Meryem', 'Özdemir', true, 'özdemir@mail.ru', '+903623587651', 'female', 33, 4),
(71, 'Student', 'Tural', 'Frank', true, 'frank@mail.ru', '+994123587651', 'male', 37, 3),
(72, 'Student', 'Kamran', 'Tahir', true, 'tahirkam@mail.ru', '+994122358765', 'male', 37, 3),
(73, 'Student', 'Resad', 'Metro', true, 'metrores@mail.ru', '+994122587651', 'male', 37, 3),
(74, 'Student', 'Elshad', 'Amil', true, 'amil004@mail.ru', '+994121357651', 'male', 37, 3),
(75, 'Student', 'Azer', 'Kerem', true, 'azerkerem@mail.ru', '+994122387651', 'male', 37, 3),
(76, 'Student', 'Fidan', 'Togrul', true, 'fidantogrul@mail.ru', '+994122358151', 'female', 37, 3),
(77, 'Student', 'Humay', 'Elshan', true, 'humayishpe@mail.ru', '+9941223587633', 'female', 37, 3),
(78, 'Student', 'Ruxana', 'Michel', true, 'ruxana92@mail.ru', '+9941223757651', 'female', 37, 3),
(79, 'Student', 'Fatimah', 'Shahin', true, 'fat1mah@mail.ru', '+9941243587541', 'female', 37, 3),
(80, 'Student', 'Nazrienne', 'Muhammed', true, 'nazrienne@mail.ru', '+994122384365', 'female', 37, 3),
(81, 'Student', 'Aleksandr', 'Ivanov', true, 'ivanovaleks@mail.ru', '+754353535', 'male', 21, 2),
(82, 'Student', 'Alexsei', 'Petrov', true, 'alex@mail.ru', '+754195435', 'male', 21, 2),
(83, 'Student', 'Dmitri', 'Smirnoff', true, 'demia@mail.ru', '+754398765', 'male', 21, 2),
(84, 'Student', 'Dominik', 'Volkov', true, 'volkdom@mail.ru', '+754435234', 'male', 21, 2),
(85, 'Student', 'Igor', 'Fedorov', true, 'fedorov@mail.ru', '+754353537', 'male', 21, 2),
(86, 'Student', 'Alina', 'Semenova', true, 'semenova@mail.ru', '+754353538', 'female', 21, 2),
(87, 'Student', 'Katya', 'Mikhailova', true, 'katya@mail.ru', '+754353539', 'female', 21, 2),
(88, 'Student', 'Karina', 'Egorova', true, 'egorova00@mail.ru', '+754353540', 'female', 21, 2),
(89, 'Student', 'Sasha', 'Alexeevna', true, 'alex1@mail.ru', '+754353541', 'female', 21, 2),
(90, 'Student', 'Natalya', 'Vasilieva', true, 'natalya_vas@mail.ru', '+754353542', 'female', 21, 2),
(91, 'Student', 'Liam', 'Smith', true, 'smith@mail.ru', '+15555551234', 'male', 101, 21),
(92, 'Student', 'Noah', 'Johnson', true, 'johnsnow@mail.ru', '+15554444321', 'male', 101, 21),
(93, 'Student', 'Oliver', 'Williams', true, 'olivie@mail.ru', '+15553339845', 'male', 101, 21),
(94, 'Student', 'Elijah', 'Brown', true, 'browneyes@mail.ru', '+15552220983', 'male', 101, 21),
(95, 'Student', 'James', 'Martinez', true, 'martinez@mail.ru', '+15559997593', 'male', 101, 21),
(96, 'Student', 'William', 'Rodriguez', true, 'will@mail.ru', '+15558884569', 'male', 101, 21),
(97, 'Student', 'Benjamin', 'Hernandez', true, 'hernandez@mail.ru', '+15557770398', 'male', 101, 21),
(98, 'Student', 'Lucas', 'Lopez', true, 'lucasmodric@mail.ru', '+15555553243', 'male', 101, 21),
(99, 'Student', 'Henry', 'Anderson', true, 'andersonspider@mail.ru', '+15552229876', 'male', 101, 21),
(100, 'Student', 'Theodore', 'Taylor', true, 'rusvelt@mail.ru', '+15553333241', 'male', 101, 21),
(101, 'Student', 'Sade', 'Taiwo', true, 'sade@mail.ru', '+234 1 2279038', 'female', 40, 36),
(102, 'Student', 'Ayofemi', 'Oba', true, 'obaoba@mail.ru', '+234 1 2357651', 'female', 40, 36),
(103, 'Student', 'Obi', 'Olutosin', true, 'olutosin@mail.ru', '+234 1 3587651', 'female', 40, 36),
(104, 'Student', 'Dola', 'Oluwatobi', true, 'dola@mail.ru', '+234 1 3857651', 'female', 40, 36),
(105, 'Student', 'Adanna', 'Adesina', true, 'adanna@mail.ru', '+234 1 2353651', 'female', 40, 36),
(106, 'Student', 'Jaja', 'Chinelo', true, 'jaja@mail.ru', '+234 1 2358761', 'male', 41, 36),
(107, 'Student', 'Chinara', 'Chinua', true, 'chihua03@mail.ru', '+234 1 5872651', 'male', 41, 36),
(108, 'Student', 'Abiodun', 'Ovie', true, 'oviewesd@mail.ru', '+234 1 2347651', 'male', 41, 36),
(109, 'Student', 'Okechukwu', 'Ngozi', true, 'nqash@mail.ru', '+234 1 1238651', 'male', 41, 36),
(110, 'Student', 'Uchechi', 'Adeola', true, 'gkfj@mail.ru', '+234 1 9878651', 'male', 41, 36),
(111, 'Teacher', 'Aisholpan', 'Tanysbergenova', false, 'aisholpan@mail.ru', '+77074541389', 'female', 5, 1),
(112, 'Teacher', 'Zhuldyz', 'Raibekova', false, 'raibekova@mail.ru', '+77774551889', 'female', 8, 1),
(113, 'Teacher', 'Yerbol', 'Yereke', false, 'yereke@mail.ru', '+77074541385', 'male', 7, 1),
(114, 'Teacher', 'Maksat', 'Galiev', false, 'maksatbest@mail.ru', '+77074789301', 'male', 11, 1),
(115, 'Teacher', 'Sholpan', 'Aimanova', false, 'aimanova@mail.ru', '+77774545639', 'female', 17, 1),
(116, 'Teacher', 'Gulnur', 'Erkesh', false, 'guleke@mail.ru', '+77274040380', 'female', 2, 1),
(117, 'Teacher', 'Dauren', 'Erbaev', false, 'dauren@mail.ru', '+77000500089', 'male', 5, 1),
(118, 'Teacher', 'Sayat', 'Berdenov', false, 'berdenov@mail.ru', '+77706667755', 'male', 13, 1),
(119, 'Teacher', 'Azamat', 'Tanyrbergen', false, 'azamat01@mail.ru', '+77774523359', 'male', 15, 1),
(120, 'Teacher', 'Rasul', 'Bakbaev', false, 'bakbaev@mail.ru', '+77024041356', 'female', 8, 1),
(121, 'Teacher', 'Adem', 'Ozkan', true, 'adema@mail.ru', '+31024042565', 'male', 19, 4),
(122, 'Teacher', 'Ridvan', 'Chiltov', true, 'ridanchiltov@mail.ru', '+32024041356', 'female', 19, 4),
(123, 'Teacher', 'Mehmet', 'Ozdur', true, 'meh007@mail.ru', '+387024041356', 'male', 18, 4),
(124, 'Teacher', 'Gemel', 'Guzel', true, 'gemel@mail.ru', '+35704041356', 'male', 19, 4),
(125, 'Teacher', 'Sulfan', 'Gulten', true, 'sulfan87@mail.ru', '+37024041356', 'female', 18, 4),
(126, 'Teacher', 'John', 'Alex', true, 'jaks@mail.ru', '+18524051348', 'male', 101, 21),
(127, 'Teacher', 'Leo', 'Step', true, 'leo789@mail.ru', '+17024041356', 'male', 86, 21),
(128, 'Teacher', 'Steve', 'Dorman', true, 'dor1man@mail.ru', '+1201404115', 'male', 101, 21),
(129, 'Teacher', 'Alexandr', 'Jobs', true, 'alexan@mail.ru', '+1452404145', 'male', 101, 21),
(130, 'Teacher', 'Elon', 'Bale', true, 'elonc01@mail.ru', '+15124241336', 'male', 101, 21);

select * from personalData;
 

CREATE TABLE Advisor(
  ID INT NOT NULL AUTO_INCREMENT,
    Personal_ID INT NOT NULL,
    Faculty_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (Faculty_ID) REFERENCES Faculty(ID),
    FOREIGN KEY (Personal_ID) REFERENCES PersonalData(ID)
);


CREATE TABLE Student(
  ID INT NOT NULL,
    Personal_ID INT NOT NULL,
    Specialty_ID INT NOT NULL,
    Course INT NOT NULL,
    Advisor_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (Specialty_ID) REFERENCES Specialty(ID),
    FOREIGN KEY (Advisor_ID) REFERENCES Advisor(ID),
    FOREIGN KEY (Personal_ID) REFERENCES PersonalData(ID)
);

select first_name 
from personaldata
intersect


INSERT INTO Student VALUES
(1, 11, 1, 1, 3),
(2, 12, 2, 1, 4),
(3, 13, 3, 1, 5),
(4, 14, 4, 1, 6),
(5, 15, 5, 1, 3),
(6, 16, 6, 1, 4),
(7, 17, 7, 1, 5),
(8, 18, 8, 1, 6),
(9, 19, 9, 1, 3),
(10, 20, 10, 1, 3),
(11, 21, 11, 1, 4),
(12, 22, 12, 1, 5),
(13, 23, 13, 1, 6),
(14, 24, 14, 1, 3),
(15, 25, 15, 1, 4),
(16, 26, 16, 1, 5),
(17, 27, 17, 1, 6),
(18, 28, 18, 1, 1),
(19, 29, 19, 1, 2),
(20, 30, 20, 1, 1),
(21, 31, 21, 1, 2),
(22, 32, 22, 1, 1),
(23, 33, 23, 1, 2),
(24, 34, 24, 1, 1),
(25, 35, 25, 1, 2),
(26, 36, 26, 1, 1),
(27, 37, 27, 1, 2),
(28, 38, 28, 1, 7),
(29, 39, 29, 1, 8),
(30, 40, 30, 1, 7),
(31, 41, 31, 1, 8),
(32, 42, 32, 1, 7),
(33, 43, 33, 1, 8),
(34, 44, 34, 1, 7),
(35, 45, 35, 1, 8),
(36, 46, 36, 1, 7),
(37, 47, 37, 1, 8),
(38, 48, 38, 1, 7),
(39, 49, 39, 1, 8),
(40, 50, 40, 1, 9),
(41, 51, 41, 1, 10),
(42, 52, 42, 1, 9),
(43, 53, 43, 1, 10),
(44, 54, 44, 1, 9),
(45, 55, 45, 1, 10),
(46, 56, 46, 1, 9),
(47, 57, 47, 1, 10),
(48, 58, 48, 1, 9),
(49, 59, 49, 1, 10),
(50, 60, 50, 1, 9),
(51, 61, 51, 1, 10),
(52, 62, 1, 2, 3),
(53, 63, 2, 2, 3),
(54, 64, 3, 2, 4),
(55, 65, 4, 2, 5),
(56, 66, 5, 2, 6),
(57, 67, 6, 2, 6),
(58, 68, 7, 2, 4),
(59, 69, 8, 2, 4),
(60, 70, 9, 2, 5),
(61, 71, 10, 2, 6),
(62, 72, 11, 2, 5),
(63, 73, 12, 2, 6),
(64, 74, 13, 2, 3),
(65, 75, 14, 2, 4),
(66, 76, 15, 2, 6),
(67, 77, 16, 2, 3),
(68, 78, 17, 2, 4),
(69, 79, 18, 2, 1),
(70, 80, 18, 2, 2),
(71, 81, 19, 2, 1),
(72, 82, 20, 2, 2),
(73, 83, 21, 3, 1),
(74, 84, 22, 3, 2),
(75, 85, 23, 3, 1),
(76, 86, 24, 2, 2),
(77, 87, 25, 3, 1),
(78, 88, 27, 4, 1),
(79, 89, 28, 3, 7),
(80, 90, 28, 1, 7),
(81, 91, 29, 4, 7),
(82, 92, 30, 1, 8),
(83, 93, 31, 2, 8),
(84, 94, 32, 3, 7),
(85, 95, 33, 3, 8),
(86, 96, 34, 2, 7),
(87, 97, 35, 1, 7),
(88, 98, 36, 2, 7),
(89, 99, 37, 3, 8),
(90, 100, 38, 2, 8),
(91, 101, 39, 3, 7),
(92, 102, 40, 3, 9),
(93, 103, 41, 2, 10),
(94, 104, 42, 1, 10),
(95, 105, 43, 4, 9),
(96, 106, 44, 4, 10),
(97, 107, 45, 4, 10),
(98, 108, 46, 4, 10),
(99, 109, 47, 4, 9),
(100, 110, 48, 4, 9);


CREATE TABLE AcademicPosition(
  ID INT NOT NULL,
    Name varchar(255),
    PRIMARY KEY(ID)
);

INSERT INTO AcademicPosition VALUES
(1, 'Instructor'),
(2, 'Assistant Professor'),
(3, 'Associate Professor'),
(4, 'Professor'),
(5, 'Lecturer'),
(6, 'Senior Lecturer'),
(7, 'Master Lecturer');


CREATE TABLE ScienceDegree(
  ID INT NOT NULL,
    Name varchar(255),
    PRIMARY KEY(ID)
);

INSERT INTO ScienceDegree VALUES
(1, 'Computer Science'),
(2, 'Business Administration'),
(3, 'Finance'),
(4, 'Information Technology'),
(5, 'Biology'),
(6, 'Psychology'),
(7, 'Chemistry'),
(8, 'Mathematics'),
(9, 'Mechanical Engineering'),
(10, 'Electrical Engineering');

CREATE TABLE Teacher(
  ID INT NOT NULL,
    Personal_ID INT NOT NULL,
    Faculty_ID INT NOT NULL,
  AcadPosition_ID INT NOT NULL,
  ScienceDeg_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY(Faculty_ID) REFERENCES Faculty(ID),
    FOREIGN KEY(AcadPosition_ID) REFERENCES AcademicPosition(ID),
    FOREIGN KEY(ScienceDeg_ID) REFERENCES ScienceDegree(ID),
    FOREIGN KEY (Personal_ID) REFERENCES PersonalData(ID)
);


INSERT INTO Teacher VALUES 
(1, 111, 1, 1, 2),
(2, 112, 2, 5, 1),
(3, 113, 2, 6, 4),
(4, 114, 2, 1, 7),
(5, 115, 3, 6, 4),
(6, 116, 3, 3, 5),
(7, 117, 1, 6, 3),
(8, 118, 4, 4, 5),
(9, 119, 1, 1, 2),
(10, 120, 1, 3, 2),
(11, 121, 2, 6, 1),
(12, 122, 2, 5, 4),
(13, 123, 2, 3, 7),
(14, 124, 3, 3, 4),
(15, 125, 1, 3, 3),
(16, 126, 1, 4, 2),
(17, 127, 2, 7, 1),
(18, 128, 3, 4, 4),
(19, 129, 3, 7, 4),
(20, 130, 4, 7, 5);


select * from teacher;

select T.ID ,A.Name , S.name , P.FirstName FROM (Teacher AS T Inner join academicposition as A on T.AcadPosition_ID = A.ID) inner join sciencedegree AS S on  S.id = T.ScienceDeg_id  inner join  personaldata as P on P.id = T.personal_id;

select count(*)
from teacher
group by teacher.AcadPosition_ID = '7';


CREATE TABLE Subject(
  ID INT NOT NULL,
    Name VARCHAR(255) NOT NULL,
    Faculty_ID INT NOT NULL,
    Teacher_ID INT NOT NULL,
    LectureHours INT,
    PracticeHours INT,
    PRIMARY KEY(ID),
    FOREIGN KEY(Faculty_ID) REFERENCES Faculty(ID),
    FOREIGN KEY(Teacher_ID) REFERENCES Teacher(ID)
);

select  sub.id , sub.name, sub.Faculty_ID,sub.Teacher_ID,sub.LectureHours,sub.PracticeHours from subject as sub;
  update subject
  set name = 'JAVA 2', PracticeHours = 20
  where subject.id = 1



select Sub.ID , Sub.Name , Sub.Faculty_ID,Sub.LectureHours,Sub.PracticeHours from Subject as Sub where Faculty_Id IN (select Faculty.ID from faculty where Faculty.name = 'Business School');

INSERT INTO Subject VALUES 
(1, 'JAVA 1', 2, 5, 15, 15), 
(2, 'JAVA 2', 2, 3, 15, 20),
(3, 'Business Technics', 1, 1, 10, 5),
(4, 'Algorithm', 2, 2, 15, 15),
(5, 'Database Management Systems', 2, 19, 15, 15),
(6, 'Anatomy', 3, 20, 20, 15),
(7, 'Operations Management', 1, 9, 10, 15),
(8, 'Business Statistics', 1, 7, 12, 20),
(9, 'Information Management', 1, 15, 10, 15),
(10, 'Marketing Management', 1, 16, 20, 15);

select *  from subject;

update subject
set name = 'JAVA 2', PracticeHours = 20
where subject.id = 1;


CREATE TABLE Library(
  ID INT NOT NULL,
    Name VARCHAR(255) NOT NULL,
    Faculty_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY(Faculty_ID) REFERENCES Faculty(ID)
);

INSERT INTO Library VALUES 
(1,'Library Business School',1),
(2,'Library Engineering and Natural sciences',2),
(3,'Library Social Sciences',3),
(4, 'Library Education and Humanities',4);

select * from library;
select L.id , L.name  , F.name from library as L inner join Faculty as F on  F.id = L.Faculty_ID where F.name

CREATE TABLE Book(
  ID INT NOT NULL,
    Name VARCHAR(255) NOT NULL,
    Author VARCHAR(255) NOT NULL,
    Category VARCHAR(255),
    Library_ID INT NOT NULL,
    PRIMARY KEY(ID),
    FOREIGN KEY (Library_ID) REFERENCES Library(ID)
);
select B.Id , B.Name , B.Author , B.Category  from book as B;
alter table book drop category;

select B.id , B.name , B.Author,B.Library_Id from  Book as B where B.Library_Id LIKE '4' or B.ID < 5;

select count(*)
from book
where library_ID LIKE '3' OR library_ID LIKE '2';


CREATE TABLE book_view AS
   SELECT ID,Author,Category
   FROM book
   where ID < 50;
   select * from book_view;
create index westwood on Book(Name);


INSERT INTO Book VALUES
(1, '1984', 'George Orwell', 'Fiction', 4),
(2, "A Doll's House", 'Henrik Ibsen', 'Fiction', 4),
(3, 'Absalom, Absalom!', 'William Faulkner', 'Fiction', 4),
(4, 'The Adventures of Huckleberry Finn', 'Mark Twain', 'Fiction', 4),
(5, 'The Aeneid', 'Virgil', 'Fiction', 4),
(6, 'Anna Karenina', 'Lev Tolstoy', 'Fiction', 4),
(7, 'Beloved', 'Toni Morrison', 'Fiction', 4),
(8, 'Berlin Alexanderplatz', 'Alfred Doblin', 'Fiction', 4),
(9, 'Blindness', 'Jose Saramago', 'Fiction', 4),
(10, 'The Book of Disquiet', ' Fernando Pessoa', 'Fiction', 4),
(11, 'The Book of Job', 'Undefined', 'Fiction', 4),
(12, 'The Brothers Karamazov', 'Fyodor M Dostoyevsky', 'Fiction', 4),
(13, 'Buddenbrooks', 'Thomas Mann', 'Fiction', 4),
(14, 'Canterbury Tales', 'Geoffrey Chaucer', 'Fiction', 4),
(15, 'The Castle', 'Franz Kafka', 'Fiction', 4),
(16, 'Children of Gebelawi', 'Naguib Mahfouz', 'Fiction', 4),
(17, 'Collected Fictions', 'Jorge Luis Borges', 'Fiction', 4),
(18, 'Complete Poems', 'Giacomo Leopardi', 'Fiction', 4),
(19, 'The Complete Stories', 'Franz Kafka', 'Fiction', 4),
(20, 'The Complete Tales', 'Edgar Allan Poe', 'Fiction', 4),
(21, 'Confessions of Zeno', 'Italo Svevo', 'Fiction', 4),
(22, 'Crime and Punishment', 'Fyodor M Dostoyevsky', 'Fiction', 4),
(23, 'Dead Souls', 'Nikolai Gogol', 'Fiction', 4),
(24, 'The Death of Ivan Ilyich and Other Stories', 'Leo Tolstoy', 'Fiction', 4),
(25, 'Decameron', 'Giovanni Boccaccio', 'Fiction', 4),
(26, 'The Devil to Pay in the Backlands', 'Joao Guimaraes Rosa', 'Fiction', 4),
(27, 'Diary of a Madman and Other Stories', 'Lu Xun', 'Fiction', 4),
(28, 'The Divine Comedy', 'Dante Alighieri', 'Fiction', 4),
(29, 'Don Quixote', 'Miguel de Cervantes Saavedra', 'Fiction', 4),
(30, 'Essays', 'Michel de Montaigne', 'Fiction', 4),
(31, 'Fairy Tales and Stories', 'Hans Christian Andersen', 'Fiction', 4),
(32, 'Faust', 'Johann Wolfgang', 'Fiction', 4),
(33, 'Gargantua and Pantagruel', 'Francois Rabelais', 'Fiction', 4),
(34, 'Gilgamesh', 'Undefined', 'Fiction', 4),
(35, 'The Golden Notebook', 'Doris Lessing', 'Fiction', 4),
(36, 'Great Expectations', 'Charles Dickens', 'Fiction', 4),
(37, "Gulliver's Travels", ' Jonathan Swift', 'Fiction', 4),
(38, 'Gypsy Ballads', 'Federico Garcia Lorca', 'Fiction', 4),
(39, 'Hamlet', 'William Shakespeare', 'Fiction', 4),
(40, 'History', 'Elsa Morante', 'Fiction', 4),
(41, 'Hunger', 'Knut Hamsun', 'Fiction', 4),
(42, 'The Idiot', 'Fyodor M Dostoyevsky', 'Fiction', 4),
(43, 'The Iliad', 'Homer', 'Fiction', 4),
(44, 'Independent People', 'Halldor K Laxness', 'Fiction', 4),
(45, 'Invisible Man', 'Ralph Ellison', 'Fiction', 4),
(46, 'Jacques the Fatalist and His Master', 'Denis Diderot', 'Fiction', 4),
(47, 'Journey to the End of the Night', 'Louis-Ferdinand Celine', 'Fiction', 4),
(48, 'King Lear', 'William Shakespeare', 'Fiction', 4),
(49, 'Leaves of Grass', 'Walt Whitman', 'Fiction', 4),
(50, 'The Life and Opinions of Tristram Shandy', 'Laurence Sterne', 'Fiction', 4),
(51, 'Antifragile', 'Nassim Nicholas', 'Non-Fiction', 2),
(52, 'The Toyota Way', 'Jeffrey K. Liker', 'Non-Fiction', 2),
(53, 'The Science of Structures', 'E. Gordon', 'Non-Fiction', 2),
(54, 'Fasteners and Plumbing', 'Carroll Smith', 'Non-Fiction', 2),
(55, 'The Way Things Work Now', 'David Macaulay', 'Non-Fiction', 2),
(56, 'Exploring the Marvelous', 'Mark Miodownik', 'Non-Fiction', 2),
(57, 'The Hidden Stories Behind our Structures ', 'Roma Agrawal', 'Non-Fiction', 2),
(58, 'Dune', 'Frank Herbert', 'Non-Fiction', 2),
(59, 'Flowers for Algernon', 'Daniel Keyes', 'Non-Fiction', 2),
(60, 'How to Win Friends', 'Dale Carnegie', 'Non-Fiction', 2),
(61, 'Essays on Software Engineering ', 'Frederick Brooks Jr', 'Non-Fiction', 2),
(62, 'The Alchemy of Air', 'Thomas Hager', 'Non-Fiction', 2),
(63, 'Slide Rule', ' Nevil Shute', 'Non-Fiction', 2),
(64, 'Learning to Learn', 'Richard W. Hamming', 'Non-Fiction', 2),
(65, 'a Fantastic Future', 'Ashlee Vance', 'Non-Fiction', 2),
(66, 'Airframe ', 'Michael Crichton', 'Non-Fiction', 2),
(67, 'Existential Pleasures of Engineering ', 'Samuel C. Florman', 'Non-Fiction', 2),
(68, 'How to Get Things Right', 'Atul Gawande', 'Non-Fiction', 2),
(69, 'Ignition!', 'John D. Clark', 'Non-Fiction', 2),
(70, 'Flying the World’s Fastest Jet', 'Brian Shul', 'Non-Fiction', 2),
(71, 'Engineering Design', 'Ann Johnson', 'Non-Fiction', 2),
(72, 'World’s Greatest Formula 1 Designer', 'Adrian Newey', 'Non-Fiction', 2),
(73, 'The Soul of A New Machine', 'Tracy Kidder', 'Non-Fiction', 2),
(74, 'Engineer to Win ', 'Carroll Smith', 'Non-Fiction', 2),
(75, 'The Perfectionists', 'Simon Winchester', 'Non-Fiction', 2),
(76, 'The Design of Everyday Things', 'Don Norman', 'Non-Fiction', 2),
(77, 'Machinery’s Handbook', 'Andrey Alex', 'Non-Fiction', 2),
(78, 'A Process of Ongoing Improvement', 'Eliyahu M. Goldratt', 'Non-Fiction', 2),
(79, 'An Unorthodox Guide to Making Things', 'Eliya Alose', 'Non-Fiction', 2),
(80, 'Serious Scientific', 'Randall Munroe', 'Non-Fiction', 2),
(81, 'Surely You’re Joking, Mr. Feynman!', 'Richard P. Feynman', 'Non-Fiction', 2),
(82, 'The New Science of Strong Materials', 'J. E. Gordon', 'Non-Fiction', 2),
(83, 'The Martian ', 'Andy Weir', 'Non-Fiction', 2),
(84, 'To Engineer Is Human', 'Henry Petroski', 'Non-Fiction', 2),
(85, 'Skunk Works', ' Ben R. Rich', 'Non-Fiction', 2),
(86, 'Structures', 'J. E. Gordon', 'Non-Fiction', 2),
(87, 'Clean Code', 'Robert C. Martin', 'Non-Fiction', 2),
(88, 'Design Patterns', 'Erich Gamma', 'Non-Fiction', 2),
(89, 'Patterns of Enterprise Application Architecture', 'Martin Fowler', 'Non-Fiction', 2),
(90, 'Enterprise Integration Patterns', 'Gregor Hohpe', 'Non-Fiction', 2),
(91, 'Code Complete', 'Steve Mcconnell', 'Non-Fiction', 2),
(92, 'Head First Java ', 'Kathy Sierra & Bert Bates', 'Non-Fiction', 2),
(93, 'Java: A Beginner’s Guide', 'Herbert Schildt', 'Non-Fiction', 2),
(94, 'Effective Java ', ' Joshua Bloch', 'Non-Fiction', 2),
(95, 'Head First Design Patterns ', 'Eric Freeman', 'Non-Fiction', 2),
(96, 'Spring in Action ', 'Craig Walls and Ryan Breidenbach', 'Non-Fiction', 2),
(97, 'Test Driven: TDD and Acceptance TDD for Java Developers ', 'Lasse Koskela', 'Non-Fiction', 2),
(98, 'Test-Driven Java Development', 'Alex Garcia and Viktor Farcic', 'Non-Fiction', 2),
(99, 'Thinking in Java ', 'Bruce Eckel', 'Non-Fiction', 2),
(100, 'Python Crash Course', 'Eric Matthes', 'Non-Fiction', 2),
(101, 'Rich Dad Poor Dad', 'Robert T. Kiyosaki', 'Non-Fiction', 1),
(102, 'Atomic Habits: An Easy & Proven Way to Build Good Habits', 'James Clear', 'Non-Fiction', 1),
(103, 'The Intelligent Investor: The Definitive Book on Value Investing', 'Benjamin Graham', 'Non-Fiction', 1),
(104, 'The Innovator’s Dilemma', 'Clayton M. Christensen', 'Non-Fiction', 1),
(105, 'Blue Ocean Strategy', 'W. Chan Kim; Renée Mauborgne', 'Non-Fiction', 1),
(106, 'Start with Why: How Great Leaders Inspire Everyone to Take Action', 'Simon Sinek', 'Non-Fiction', 1),
(107, 'Lean In: Women, Work, and the Will to Lead', 'Sheryl Sandberg', 'Non-Fiction', 1),
(108, 'The Lean Startup', 'Eric Ries', 'Non-Fiction', 1),
(109, 'The 4-Hour Workweek', 'Timothy Ferriss', 'Non-Fiction', 1),
(110, 'Good to Great', 'Jimm Collins', 'Non-Fiction', 1),
(111, 'Think and Grow Rich', 'Napoleon Hill', 'Non-Fiction', 1),
(112, 'Zero to One', 'Peter Thiel', 'Non-Fiction', 1),
(113, 'The E-Myth Revisited', 'Michael E. Gerber', 'Non-Fiction', 1),
(114, 'The Hard Thing About Hard Things', 'Ben Horowitz', 'Non-Fiction', 1),
(115, 'The Personal MBA: Master the Art of Business ', 'Josh Kaufman', 'Non-Fiction', 1),
(116, 'Deep Work', 'Cal Newport', 'Non-Fiction', 1),
(117, 'Traction: How any Start-up Can Achieve Explosive Customer Growth', 'Gabriel Weinberg; Justin Mares', 'Non-Fiction', 1),
(118, 'The Answer', 'John Assaraf; Murray Smith', 'Non-Fiction', 1),
(119, 'Master Content Marketing', 'Pamela Wilson', 'Non-Fiction', 1),
(120, 'Getting Past No: Negotiating in Difficult Situations', 'William Ury', 'Non-Fiction', 1),
(121, 'Never Split the Difference', 'Chris Voss; Tahl Raz', 'Non-Fiction', 1),
(122, 'Decisive: How to Make Better Choices', 'Chip Heath; Dan Heath', 'Non-Fiction', 1),
(123, 'The 10X Rule', 'Grant Cardone', 'Non-Fiction', 1),
(124, 'Crushing It', 'Gary Vaynerchuk', 'Non-Fiction', 1),
(125, 'Virtual freedom', 'Chris Ducker', 'Non-Fiction', 1),
(126, 'Idea to Execution', 'Ari Meisel; Nick Sonnenberg', 'Non-Fiction', 1),
(127, 'Work the System', 'Sam Carpenter', 'Non-Fiction', 1),
(128, 'Dotcom Secrets', 'Russell Brunson', 'Non-Fiction', 1),
(129, 'The 80/20 Principle', 'Richard Koch', 'Non-Fiction', 1),
(130, 'The Secret of Selling Anything', 'Harry Browne', 'Non-Fiction', 1),
(131, 'How to Get Rich', 'Felix Dennis', 'Non-Fiction', 1),
(132, 'Million Dollar Consulting', 'Alan Weiss', 'Non-Fiction', 1),
(133, 'Simple Numbers, Straight Talk, Big Profits!', 'Greg Crabtree', 'Non-Fiction', 1),
(134, 'Managing Oneself', 'Peter F. Drucker', 'Non-Fiction', 1),
(135, 'The Effective Executive', 'Peter F. Drucker', 'Non-Fiction', 1),
(136, 'SWIM WITH THE SHARKS WITHOUT BEING EATEN ALIVE', 'Harvey B. Mackay', 'Non-Fiction', 1),
(137, 'Purple Cow', 'Seth Godin', 'Non-Fiction', 1),
(138, 'The First 90 Days', 'Michael Watkins', 'Non-Fiction', 1),
(139, 'Leadership and Self-Deception', 'Arbinger Institute', 'Non-Fiction', 1),
(140, 'StrengthsFinder 2.0 ', 'Tom Rath', 'Non-Fiction', 1),
(141, 'Built to Last', 'Jim Collins', 'Non-Fiction', 1),
(142, 'Competitive Advantage', 'Michael E.Porter', 'Non-Fiction', 1),
(143, 'The Great Game of Business', 'Jack Stack', 'Non-Fiction', 1),
(144, 'How to Win Friends and Influence People', 'Dale Carnegie', 'Non-Fiction', 1),
(145, 'Great by Choice', 'Jim Collins', 'Non-Fiction', 1),
(146, 'The 4 Disciplines of Execution', 'Chris McChesney', 'Non-Fiction', 1),
(147, 'Profit First', 'Mike Michalowicz', 'Non-Fiction', 1),
(148, 'Getting Things Done', 'David Allen', 'Non-Fiction', 1),
(149, ' Influence: Science and Practice', 'Robert B. Cialdini', 'Non-Fiction', 1),
(150, 'First, Break All the Rules', 'Jim Harter', 'Non-Fiction', 1),
(151, 'The Mismeasure of Man', 'Stephen Jay Gould', 'Fiction', 3),
(152, 'The Portable Jung', 'Carl Jung', 'Fiction', 3),
(153, 'The Upside of Irrationality', 'Dan Ariely', 'Fiction', 3),
(154, 'Man’s Search for Meaning', 'Victor Frankl', 'Fiction', 3),
(155, 'David and Goliath', 'Malcolm Gladwell', 'Fiction', 3),
(156, 'Proven Techniques to Detect Deception', 'Pamela Meyer', 'Fiction', 3),
(157, 'How We Lie to Everyone', 'Dan Ariely', 'Fiction', 3),
(158, 'Outliers', 'Malcolm Gladwell', 'Fiction', 3),
(159, 'Prozac Nation', 'Elizabeth Wurtzel', 'Fiction', 3),
(160, 'Public Discourse in the Age of Show Business', 'Neil Postman', 'Fiction', 3),
(161, 'Thoughts on the Nature of Mass Movements', 'Eric Hoffer', 'Fiction', 3),
(162, 'When Breath Becomes Air', 'Paul Kalanithi', 'Fiction', 3),
(163, 'The Tipping Point:', 'Malcolm Gladwell', 'Fiction', 3),
(164, 'Stiff: The Curious Lives of Human Cadavers', 'Mary Roach', 'Fiction', 3),
(165, 'The Confidence Game', 'Maria Konnikova', 'Fiction', 3),
(166, '$2.00 a Day', 'Kathryn J. Edin', 'Fiction', 3),
(167, 'Gang Leader for a Day', 'Sudhir Venkatesh', 'Fiction', 3),
(168, 'Sociopathic Society', 'Charles Derber', 'Fiction', 3),
(169, 'Freakonomics', 'Steven D. Levitt', 'Fiction', 3),
(170, 'The Sociopath Next Door', 'Martha Stout', 'Fiction', 3);


CREATE TABLE Arrangement(
  ID INT AUTO_INCREMENT,
    Book_ID INT NOT NULL,
    User_ID INT NOT NULL,
    Start_Date DATE NOT NUll,
    PRIMARY KEY(ID), 
    FOREIGN KEY (Book_ID) REFERENCES Book(ID),
  FOREIGN KEY (User_ID) REFERENCES PersonalData(ID)
);
START TRANSACTION;
DELETE FROM Transaction.arrangement WHERE User_ID = 31;
SELECT * FROM Transaction.arrangement;
ROLLBACK;

select * from arrangement;

CREATE TABLE arrangement_view AS
SELECT ID, User_ID,Start_Date
FROM arrangement
where User_ID is not null;

select * from arrangement_view;

select  A.ID , A.Book_ID, A.User_ID, A.Start_Date from arrangement AS A;
INSERT INTO Arrangement VALUES
(1,5,31,'10.09.2022'),
(2,8,38,'10.09.2022'),
(3,11,33,'10.09.2022'),
(4,55,41,'11.09.2022'),
(5,78,37,'11.09.2022'),
(6,89,33,'11.09.2022'),
(7,25,49,'12.09.2022'),
(8,36,46,'12.09.2022'),
(9,69,43,'13.09.2022'),
(10,85,36,'13.09.2022');
truncate table arrangement;
select  * from arrangement;




delete
from arrangement
where id = 10;
CREATE TABLE Dorm(
  ID INT,
    Category ENUM('Girls', 'Boys', 'Teachers') NOT NULL,
    PRIMARY KEY(ID)
);

INSERT INTO Dorm VALUES
(1,'Girls'),
(2,'Boys'),
(3,'Teachers');


CREATE TABLE InDorm(
  ID INT AUTO_INCREMENT,
    User_ID INT NOT NULL,
    Dorm_ID INT NOT NULL,
    Room VARCHAR(255),
    PRIMARY KEY(ID),
    FOREIGN KEY (User_ID) REFERENCES PersonalData(ID),
    FOREIGN KEY (Dorm_ID) REFERENCES Dorm(ID)
);

drop table InDorm;
select user_id,dorm_id,room
from InDorm
where room LIKE 'C115'
union
select user_id,dorm_id,room
from InDorm
where room LIKE 'C228';

INSERT INTO InDorm VALUES
(1,27,2,'C115'),
(2,28,2,'C228'),
(3,29,2,'C115'),
(4,30,2,'C165'),
(5,31,2,'C175'),
(6,32,2,'C225'),
(7,101,1,'B175'),
(8,102,1,'B145'),
(9,103,1,'D215'),
(10,104,1,'B195'),
(11,105,1,'B228'),
(12,111,3,'A175'),
(13,112,3,'A143'),
(14,113,3,'A165'),
(15,114,3,'A275'),
(16,115,3,'A225'),
(17,116,3,'A211'),
(18,117,3,'A228'),
(19,118,3,'A245'),
(20,119,3,'A258');

use transaction;	

START TRANSACTION;
SELECT USER_ID,DORM_ID,ROOM
FROM TRANSACTION.InDorm
WHERE ROOM = 'C115';
ROLLBACK;

CREATE TRIGGER End_DATE
BEFORE INSERT ON Arrangement FOR EACH ROW
SET NEW.end_date = DATE_ADD(NEW.start_date, INTERVAL 21 DAY);

select Sub.ID , Sub.Name , Sub.Faculty_ID,Sub.LectureHours,Sub.PracticeHours 
  from Subject as Sub 
  where Faculty_Id IN (select Faculty.ID 
                       from faculty 
                       where Faculty.name = 'Business School')
                       
                       
