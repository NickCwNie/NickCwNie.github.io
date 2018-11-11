---
title: Note keepass - trigger sync
key: 20181021
tags: note
---

keepass-trigger-sync
http://code.xiaole.pro/KeepassSync.html
```xml
<?xml version="1.0" encoding="utf-8"?>
<TriggerCollection xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<Triggers>
		<Trigger>
			<Guid>L2euC7Mr/EKh7nPjueuZvQ==</Guid>
			<Name>SaveSync</Name>
			<Events>
				<Event>
					<TypeGuid>s6j9/ngTSmqcXdW6hDqbjg==</TypeGuid>
					<Parameters>
						<Parameter>1</Parameter>
						<Parameter>kdbx</Parameter>
					</Parameters>
				</Event>
			</Events>
			<Conditions />
			<Actions>
				<Action>
					<TypeGuid>tkamn96US7mbrjykfswQ6g==</TypeGuid>
					<Parameters>
						<Parameter>SaveSync</Parameter>
						<Parameter>0</Parameter>
					</Parameters>
				</Action>
				<Action>
					<TypeGuid>Iq135Bd4Tu2ZtFcdArOtTQ==</TypeGuid>
					<Parameters>
						<Parameter>https://dav.jianguoyun.com/dav/keePass/passwordSync.kdbx</Parameter>
						<Parameter>123456</Parameter>
						<Parameter>123456</Parameter>
					</Parameters>
				</Action>
				<Action>
					<TypeGuid>tkamn96US7mbrjykfswQ6g==</TypeGuid>
					<Parameters>
						<Parameter>SaveSync</Parameter>
						<Parameter>1</Parameter>
					</Parameters>
				</Action>
			</Actions>
		</Trigger>
	</Triggers>
</TriggerCollection>
```

**Warnning:**   
在主界面上点击工具>选项，切到最后一个高
级页面，在文件输入输出里  
不勾选**将写入数据库时使用文件交换**
