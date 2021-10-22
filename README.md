# SQL_Demo-inserir-dados
```txt
API:
* PreparedStatement
* executeUpdate
* Statement.RETURN_GENERATED_KEYS
* getGeneratedKeys
Checklist:
* Inserção simples com preparedStatement
* Inserção com recuperação de Id
```
### Inserir
```java
			st = conn.prepareStatement("INSERT INTO seller " + "(Name, Email, BirthDate, BaseSalary, DepartmentId)"
					+ "VALUES " + "(?, ?, ?, ?, ?)", Statement.RETURN_GENERATED_KEYS);

			st.setString(1, "Carl Purple");
			st.setString(2, "carl@gmail.com");
			st.setDate(3, new java.sql.Date(sdf.parse("22/04/1985").getTime()));
			st.setDouble(4, 3000.0);
			st.setInt(5, 4);
```
