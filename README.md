# JDBC-MySql

A] how to connect mysql databse to java program.
B] so here i use maven => create maven project * file> new > maven> give Artufact id > place Enter.
 inside this maven project we able see some bydefault file 1.src main 2.src test 3.JRE 4,MAVEN dependency 5.pom.xml .
 so use pom.xml file and inside this add dependency for jdbc . 
 =====> <!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
  <dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>8.0.22</version>
		</dependency>
      *this is a jdbc driver , if we are not use this driver then our program is anable to communicate with databse 
      *driver act like a traslater whose translate a java application call into database specific call
      *4 type of driver are thaire A] JDBC-ODBC bridge driver B] java native API driver c] Netwirk protocall driver D] Thin driver => this thin driver is most commanlu used driver .
      
C] create project in src main file i use Samosa.java file oe we can use  App.java file .

D] for the proper connection we need to right some magical lines .
      String url = "jdbc:mysql://localhost:3306/customer_db";
		String user ="root";
		String password = "#####";
then ==		we need to open a protal whitch communicate between java application and databse 
  Connection con = DriverManager.getConnection(url,user,password);
  
after open a protal we need to add another magical lines that help use to create , insert or update a sql query so fo that we can use Statment or Prepared Statment object
for Example if i want to insert a new customer in a databse so we can follow below format .
String sq = "insert into Customers values(name,city
    
