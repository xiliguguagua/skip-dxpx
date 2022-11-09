# skip-dxpx
chrome浏览器插件  
跳过dxpx.nuaa.edu.cn中培训视频，一秒播放完毕
## 使用方法
解压后在扩展程序-加载已解压的扩展程序  
进入dxpx.nuaa.edu.cn按常规流程播放学习视频，一秒后进度自动到视频结束，提示学习完成  
  
    
    
    
    
`非nuaa的没试过，可以把manifest.json中的url匹配改了去试试`  
## 原理  
强制将player对象currentTime属性赋值为duration属性值，即将当前进度修改为视频长度  
player对象通过逆向html中js代码可知为video播放控制对象  
