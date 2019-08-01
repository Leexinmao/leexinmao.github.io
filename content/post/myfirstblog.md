---
title: "Myfirstblog"
date: 2019-08-01T20:12:00+08:00
draft: true

---



## 数据库框架查询

```

Connection conn = new GetSqlPool().getMydqlpool();

​		QueryRunner queryRunner = new QueryRunner();

​		String sql = "select * from customer";

​		List<Object[]> list = new  QueryRunner().query(conn,sql,new ArrayListHandler());

​		

​		System.out.println("用户ID\t\t姓名卡号\t\t手机号\t\t\t邮编\t\t邮箱\t\t\t银行号\t\t密码\t\t卡号\t\t余额\t");

​				for(Objec

t[] object:list) {

​					for(Object e:object) {

​						System.out.print(e +"\t\t");

​					}System.out.println();

​				}

```











​	





#### 查询

```


​	public static void setSalary(double money) throws Exception {

​		Scanner scanner = new Scanner(System.in);

​		Connection conn =new GetSqlPool().getMydqlpool();

​		String sql = "update admin set money = money +?";

​		new QueryRunner().update(conn, sql,money);

​		conn.close();

}
```

​	