### 简介
收集网络中在cobaltstrike中使用的bof工具集。项目基于CS-Situational-Awareness-BOF推荐的创建方式和流程。代码均来之网络。

### 直接使用
```
git clone https://github.com/AttackTeamFamily/cobaltstrike-bof-toolset.git
使用CobaltStrike加载cobaltstrike-bof-toolset/bof.cna脚本
```

### 自己编译
```
编译环境：kali linux
命令：
sudo apt install mingw-x64
git clone https://github.com/AttackTeamFamily/cobaltstrike-bof-toolset.git
cd cobaltstrike-bof-toolset
cd src/bof
for i in `ls`;do cd $i && make && cd ..;done
```

### 功能
|命令|使用|说明|
|-------|-----|-----|
|domaininfo|domaininfo|获取当前域和域控信息|
|clipboard|clipboard|获取粘贴板中的文本|
|wifienum|wifienum|枚举wifi接口|
|wifiedump|wifiedump [Wifi_Profile_Name]|dump wifi明文凭据|
|etw|etw [stop\|start]|ETW Patching|
|read_function|read_function [module] [function1,function2]|read_function ntdll.dll NtCreateProcess,NtCreateFile|
|check_function|check_function [module] [function]|check_function ntdll.dll EtwEventWrite|
|patch_function|patch_function [dll_path] [function_name]|patch_function ntdll.dll EtwEventWrite|
|curl|curl host [port] [method] [--show] [useragent] [headers] [body] [--noproxy]|curl http://example.com 80 GET --show|

### 来源
- https://github.com/ajpc500/BOFs
- https://github.com/rvrsh3ll/BOF_Collection
- https://github.com/trustedsec/CS-Situational-Awareness-BOF

### 免责声明
本项目代码仅能在取得足够合法授权的企业安全建设中使用，在使用本项目过程中，您应确保自己所有行为符合当地的法律法规。 如您在使用本项目的过程中存在任何非法行为，您将自行承担所有后果，本项目所有开发者和所有贡献者不承担任何法律及连带责任。 除非您已充分阅读、完全理解并接受本协议所有条款，否则，请您不要安装并使用本项目。 您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。
