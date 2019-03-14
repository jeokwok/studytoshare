# README
Hello Git! Git Bash 命令

##函数注释参数信息 
Android Studio ->File -> Setting -> Keymap ->发现框输入comment -> 选择Other的Fix doc comment 
选择 Add keyboard shortcut 添加你自己喜欢的快捷方式（快捷键） 将鼠标光标放置到你想要添加方法注释的
方法前,按下你自己设置的快捷方式. 就自动生成了方法注释了. 

##JSON 获取部分中数组的数据
public static void jsonToBean(String data) {
try {

JSONArray array = new JSONArray(data);//将json字符串转成json数组

for (int i = 0; i < array.length(); i++) {//循环json数组
JSONObject ob = (JSONObject) array.get(i);//得到json对象
String name= ob.getString("name");//name这里是列名称，获取json对象中列名为name的值
System.out.print(name);//输出name
} catch (JSONException e) {
}
} 
