Android Retrofit��json���������Ϊһ��paramas��ֵ���д��䣬
��tomcat8.3���ϻᱨheader�������������android�˵�����Ϊ��
```
@Headers({"Content-Type: application/json","Accept: application/json"})//��Ҫ���ͷ
@POST("AddUser")
Observable<OutputBean<User>> addUser(@Body RequestBody route);
```
```
 RequestBody body= RequestBody.create(okhttp3.MediaType.parse("application/json; charset=utf-8"),json);
 ```

 �ڷ���ˣ�
```
protected void doPost(HttpServletRequest request,
			HttpServletResponse response) throws ServletException, IOException {
		// TODO Auto-generated method stub
	
		BufferedReader bw=request.getReader();
		String data=bw.readLine();
		
		bw.close();
		}
```