### JDBC的入门学习案例

包含了
1.加载驱动
  1.DriverManager.registerDriver(new Driver());
  2.Class.forName("com.mysql.jdbc.Driver"); 通常使用第二种
2.获得链接
Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/jdbctest?characterEncoding=utf8", "root", "123456");
3.创建并编写SQL语句
  1.String sql = "select * from user";
  2.Statement stmt = conn.createStatement();
  3.ResultSet rs = stmt.executeQuery(sql);
4.根据执行的SQL语句，是使用executeQuery()，还是executeUpdate()
5.释放资源