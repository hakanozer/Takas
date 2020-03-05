server.port=9090
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp


spring.datasource.url=jdbc:mysql://localhost/enbilet?useUnicode=true&characterEncoding=utf-8&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect
spring.jpa.hibernate.ddl-auto=update

spring.jpa.open-in-view=false


###


package com.takasbank.twodays.restcontroller;

import java.util.ArrayList;
import java.util.Date;
import java.util.HashMap;
import java.util.LinkedHashMap;
import java.util.List;
import java.util.Map;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

import com.takasbank.twodays.models.User;

@RestController
public class UserRestController {

	@GetMapping("/allUser")
	public Map<String, Object> allUser() {
		Map<String, Object> hm = new LinkedHashMap<>();
		hm.put("name", "Ali");
		hm.put("age", 39);
		hm.put("statu", true);
		hm.put("users", allUserResult());
		return hm;
	}
	
	
	public List<User> allUserResult() {
		List<User> ls = new ArrayList<>();
		for (int i = 0; i < 10; i++) {
			User us = new User();
			us.setMail("mail " + i);
			us.setPass("12"+i);
			us.setuDate(new Date());
			us.setUid(i);
			ls.add(us);
		}
		return ls;
	}
	
	
	
}
