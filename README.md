# ms
Zipped code for the programming challenge
Instructions
------------------
1. Please refer to the attached zip file. I have used IntelliJ IDEA for development, I did exported project as eclipse hence it should be able to run in Eclipse as well.
2. For sake of simplicity and code readability I preferred to use double over BigDecimal for calculation considering it as exercise (non-prod code).
3. I have just divided the classes in client and quantrisk considering few no of classes.
4. H2 Default DB Test is used for this exercise (non-server mode).
5. Please fire following command on H2 console for the initial table setup on Test DB. Same script is available in resources/h2dbsetup.sql
 DROP TABLE IF EXISTS EQUITIES;
    CREATE TABLE EQUITIES(TICKER VARCHAR(255) PRIMARY KEY, SECTYPE VARCHAR(3), STOCKPRICE DECIMAL(20,4),DAYSTOEXPIRE INT, STRIKEPRICE DECIMAL(20,4),  RIGHTTYPE VARCHAR(4),EXPECTEDRETURN DECIMAL(5,4),STANDARDDEVIATION DECIMAL(5,4));
    INSERT INTO EQUITIES VALUES ('AAPL', 'STK',139.91,0,0.0,'',0.87,0.82);
    INSERT INTO EQUITIES VALUES ('AAPLJG', 'OPT',139.91,80,136.39,'CALL',0.87,0.82);
    INSERT INTO EQUITIES VALUES ('AAPLTQ', 'OPT',139.91,70,141.43,'PUT',0.87,0.82);
    INSERT INTO EQUITIES VALUES ('NFLX', 'STK',145.11,0,0.0,'',0.67,0.52);
    INSERT INTO EQUITIES VALUES ('MS', 'STK',45.02,0,0.0,'',0.23,0.12);
    INSERT INTO EQUITIES VALUES ('MSEB', 'OPT',45.02,40,44.74,'CALL',0.23,0.12);
    INSERT INTO EQUITIES VALUES ('MSQN', 'OPT',45.02,40,46.54,'PUT',0.23,0.12);
    SELECT * FROM EQUITIES ORDER BY TICKER;
6. ConsoleApiClient - Prints the NAV of the trade file supplied in continuous manner on console.
7. TextPrinterApiClient - Creates an .rpt file in the resources folder, yet prints the output on console as well for reviewer's ease.
8. Code is written using jdk6 to avoid any environment conflicts. 
9. Tests are skipped since this project is not to be maintained.
