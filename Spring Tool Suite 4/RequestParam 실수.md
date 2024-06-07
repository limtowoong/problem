# 오류 코드

```java
@GetMapping("hello-mvc")
public String helloMvc(@RequestParam("name") String name, Model model) {
	model.addAttribute("name", name);
	return "mvc";
}
```

<br>

# 오류 문장

Required request parameter 'name' for method parameter type String is not present

<br>

# 발생 원인

name 값을 안 줬기 떄문에 발생하였다.

<br>

# 해결 방법

http://localhost:8080/hello-mvc?name=Spring
이렇게 주소 뒤에 Query String을 사용하여 name에 "Spring" 값을 줘서 해결했다.
