Android Retrofit的json请求如果作为一个paramas的值进行传输，
在tomcat8.3以上会报header解析错误，因此在android端的设置为：
```
@Headers({"Content-Type: application/json","Accept: application/json"})//需要添加头
@POST("AddUser")
Observable<OutputBean<User>> addUser(@Body RequestBody route);
```
```
 RequestBody body= RequestBody.create(okhttp3.MediaType.parse("application/json; charset=utf-8"),json);
 ```

 在服务端：
```
protected void doPost(HttpServletRequest request,
			HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
	
		BufferedReader bw=request.getReader();
		String data=bw.readLine();
		
		bw.close();
		}
```