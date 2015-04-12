# MonitorNewsFeeds
一个监听搜集互联网上的新闻推送信息流（RSS）的小爬虫 using Python

该程序基于 MOOC课程  MITx: 6.00.1x 计算机科学和Python编程导论  PS 7
个人觉得是个不错的既学习Python又学习爬虫的好项目，弄下来学习并尝试自己修改之。
除了该PS作业要求部分为个人完成，其他部分均为课程提供。




*项目文件说明：*


  * ps7.py, a skeleton of the solution

  * ps7_test.py, a test suite that will help you check your answers

  * triggers.txt, a sample trigger configuration file. You may modify this file to try other trigger configurations

  * feedparser.py, a module that will retrieve and parse feeds for you

  * project_util.py, a module that includes a function to convert simple HTML fragments to plain text
  
  
*RSS Overview：*

Many websites have content that is updated on an unpredictable schedule. News sites, such as Google News, are a good example of this. One tedious way to keep track of this changing content is to load the website up in your browser, and periodically hit the refresh button. Fortunately, this process can be streamlined and automated by connecting to the website's RSS feed, using an RSS feed reader instead of a web browser (e.g. Sage). An RSS reader will periodically collect and draw your attention to updated content.

RSS stands for "Really Simple Syndication". An RSS feed consists of (periodically changing) data stored in an XML-format file residing on a web-server. For this project the details are unimportant. You don't need to know what XML is, nor do you need to know how to access these files over the network.


*About triggers.txt*

we read your trigger configuration from a triggers.txt file every time your application starts, and use the triggers specified there.

Each line in this file does one of the following:

  *  is blank

  *  is a comment (begins with a #)

  *  defines a named trigger

  *  adds triggers to the trigger list.


Each type of line is described below.

  *  Blank: blank lines are ignored. A line that consists only of whitespace is a blank line.

  *  Comments: Any line that begins with a # character is ignored.

  *  Trigger definitions: Lines that do not begin with the keyword ADD define named triggers. The first element in a trigger definition is the name of the trigger. The name can be any combination of letters without spaces, except for "ADD". The second element of a trigger definition is a keyword (e.g., TITLE, PHRASE, etc.) that specifies the kind of trigger being defined. The remaining elements of the definition are the trigger arguments. What arguments are required depends on the trigger type:

  **      TITLE : a single word.

  **      SUBJECT : a single word.

  **      SUMMARY : a single word.

  **      NOT : the name of the trigger that will be NOT'd.

  **      AND : the names of the two other triggers that will be AND'd.

  **      OR : the names of the two other triggers that will be OR'd.

  **      PHRASE : a phrase.

  *  Trigger addition: A trigger definition should create a trigger and associate it with a name but should not automatically add that trigger to the running trigger list. One or more ADD lines in the .txt file will specify which triggers should be in the trigger list. An addition line begins with the ADD keyword. Following ADD are the names of one or more previously defined triggers. These triggers will be added to the the trigger list.

