<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>JSP 예제 request2.jsp</title>
</head>
<body>
	<% 
	request.setCharacterEncoding("euc-kr");
	%>
	
	<%
	String name = request. getParameter ("studentNum");
	String majors = request. getParameter ("major");
	%>
	
	<h2>학생 정보 입력 결과</h2>
	
	학번 : <%= studentNum%><p>
	전공 : <%
	
			if (majors == null)
			{
				out.println("전공 없음");
			}else{
				for (int i=0; i < majors.legth; i++)
					out.println(majors[i]+" ");
				
				
			}
		  %>
		  
<h2> 요청 정보</h2>
요청 방식: <%=request. getParameter()%><p>
요청 URL: <%=request. getParameter()%><p>
요청 URI: <%=request. getParameter()%><p>
클라이언트 주소 : <%=request. getParameter()%><p>
클라이언트 호스트 : <%=request. getParameter()%><p>
프로토콜 방식 : <%=request. getParameter()%><p>
서버 이름:<%=request. getParameter()%><p>
서버 포트 번호:<%=request. getParameter()%><p>



</body>
</html>
