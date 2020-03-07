server.port=9090
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp


spring.datasource.url=jdbc:mysql://localhost/enbilet?useUnicode=true&characterEncoding=utf-8&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect
spring.jpa.hibernate.ddl-auto=update

spring.jpa.open-in-view=false


---

<dependency>
    <groupId>org.owasp.antisamy</groupId>
    <artifactId>antisamy</artifactId>
    <version>1.5.8</version>
</dependency>
