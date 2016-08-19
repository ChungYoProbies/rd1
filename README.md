#研發一處#



##作業(一) 簡報技巧

- 1.上網搜尋「**簡報技巧**」
- 2.把制做簡報時應該要注意那些原則事項列出來
- 3.如何制做一個好的簡報與心得

寫成一個work檔或ppt檔，不限字數，檔名: 簡報技巧-username.doc
在今天下班前繳交上傳至個人的gitlab上

##作業(二)
網址更新 : http://www.freebsd.org/doc/zh_TW/books/handbook/basics-processes.html


##學習
IOC 控制反轉 & DI 依賴注入  
http://blog.developer.idv.tw/2014/05/ioc-di.html  
深入理解IoC(控制反转)和DI(依赖注入)  
http://www.importnew.com/13619.html 

##實作一
    $url = "http://tt181.me/test0975313025.php"; 
    $ch = curl_init(); 
    curl_setopt($ch, CURLOPT_URL, $url); 
    curl_setopt($ch, CURLOPT_POST, true); 
 
    $postfiled = http_build_query(array("id"=>"10","name"=>"test")); 
    //or  
    $postfiled = array("id"=>"10","name"=>"test"); 
 
    curl_setopt($ch, CURLOPT_POSTFIELDS, $postfiled);  
    curl_setopt($ch, CURLOPT_HTTPHEADER , array( 
	    "token:rd1" 
    )); 

    $result = curl_exec($ch);  
    curl_close($ch); 
  
    echo $result; 

    output  
    {"md5":"688caa7036f89ae493d50b30d0069433","id":"10","name":"test","time":"01:23:44"}
    
##實作二
    php xxxx.php & 

    因為PHP是弱型別語言，所以更需要強壯的寫法，而JAVA是強型別語言 
    (其它詳說明) 
