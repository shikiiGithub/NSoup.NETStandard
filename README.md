# NSoup.NETStandard
## NSoup for .NET Standard(NSoup .net standard 版本)
### 支持Xamarin.Android,Xamarin.IOS,Xamarin.Forms 和 Windows/linux/macOS下的开发。
在项目中碰到要处理HTML，如果是.NET程序员的话，强烈推荐使用NSoup，不然的话截取字符串是在是太痛苦了。
NSoup是一个开源框架，是JSoup的.NET移植版本，使用方法基本一致！
#### 使用：
```c#
                   String url_template = "http://dict.youdao.com/w/eng/{0}";
                    String url = String.Format(url_template, GetCombineString(word));
                    //解析html
                    Document doc = NSoup.NSoupClient.Parse(url, 3000);
                    Elements WordBig = doc.Select("#phrsListTab > h2 > span");
                    Elements newsHeadlines = doc.Select("#phrsListTab > div.trans-container > ul");
                    Element el = newsHeadlines[0]; 
                    //获取Html标签文本
                    newsHeadlines[0].Text().Trim();
                    
```
