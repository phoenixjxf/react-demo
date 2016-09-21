# react-demo
a new begin
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Hello React!</title>
	<!--1.引入React库-->
	<script src="http://www.hubwiz.com/course/552762019964049d1872fc88/lib/react.min.js"></script>
	<style>
		p{font:italic bold 50px verdana;}
	</style>
</head>
<body>
	<!--2.在真实DOM上定义容器-->
	<div id="content"></div>
  	<div id="content2"></div>
	<script>
	
		//3.在虚拟DOM上创建p元素
		var el = React.createElement("p",null,"Hello React!");
        var el2 = React.createElement(
          "ul",
          null,
          React.createElement("li",null,"China"),
          React.createElement("li",null,"Japan"),
          React.createElement("li",null,"Korea")
        );

		//4.将虚拟DOM上的p元素渲染到真实DOM上的#content容器
		
      	React.render(el2,document.querySelector("#content2"));
      	React.render(el,document.querySelector("#content"));
	</script>
</body>
</html>
