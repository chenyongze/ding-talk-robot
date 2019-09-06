###### 钉钉机器人 ---- 如何使用


> composer require chenyongze/ding-talk-robot:2.0.1

1.引入命名空间
use Yongze\DingtalkRobot;

2.实例化类
$a = new DingtalkRobot($webhook);

3.调用方法进行发送机器人消息
$a->setText(text)->send();

同理还支持其他格式的消息类型，使用方法类似，如下：
- $a->setText(text,[$atMobiles,$isAtAll])->send();
- $a->setLink(text,$title,$messageUrl,$picUrl)->send();
- $a->setMarkdown(text,$title)->send();
- $a->setActionCard(text,$title,$btns,$btnOrientation,$hideAvatar)->send();
- $a->setFeedcard($data)->send(); **必须包含title，messageURL，picURL的数组**
