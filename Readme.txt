网站后端

1.HTTPserver + WebFrame

HttpServer第三版：
	功能：
		HTTPserver
			获取http请求
			解析HTTP请求
			将请求发送给WebFrame
			从WebFrame接收反馈数据
			将数据组织为Response格式发送给客户端
		WebFrame
			从HttpServer接收具体请求
			根据请求进行逻辑处理和数据处理
				* 静态页面 
				* 逻辑数据
			将需要的数据反馈给httpserver

	升级点：
			1.采用httpserver和应用处理分离的模式
			2.降低了偶合度
			3.原则上httpserver可以搭配任意的WebFrame
============================================================================================================================================================

2.Httpserver 项目结构：

		  |---HTTPserver --HTTPServer.py(主程序)
		  |				 --settings(HttpServer配置)
		  |		
project --|		
		  |		
		  |---WebFrame	--static(存放静态网页)
						--views.py (应用数据处理程序)
						--urls.py(存放路由)
						--settings(框架配置)
						--WebFrame.py(主程序代码) 