# TestFlightDoc
Translation of Apple TestFlight Doc

##[TestFlight Beta 测试](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/BetaTestingTheApp.html#//apple_ref/doc/uid/TP40011225-CH35-SW2)

有了TestFlight beta 测试，你可以将你的app的预发布版本分发给测试者来收集反馈、并且可以为你的app在App Store发布做准备。TestFlight beta 测试是可选的；不用TestFlight beta你可以提交你的app去审核。然而；在App Store 发布你的app之前，它是一种很容易、免费、值得做的方式来改善你的app。在iTunes Connect中TestFlight beta仅适用于iOS apps.在你的开发者账号中，你最多使10个app使用TestFlight beta测试。 

#####你应该在iTunes Connect中按照下面的步骤设置app的prerelease
* 如果app是新的，创建一条iTunes Connect记录。
* 生成一个新的包含beta entitlement的App Store Distribution profile来通过TestFlight分发你的版本
* 上传一个app build
* 给版本添加app的描述和要测试的内容。这一步对内部测试者是可选的，但当为了外部测试而发布你的app给Beta App 审核时，这一步是要求的。
* 分发你的app给内部测试者
* 提交你的app Beta App审核，并且分发给外部测试者
* 从测试者得到用户反馈
* 上传更新的app build
* 当你完成了让用户测试app的预发布版本，就可以提交你的app审核或者关闭TestFlight测试

##给TestFlight Beta创建一条iTunes Connect记录
#### 内部测试者
你不需要提供所有的metadata来邀请内部测试者测试app的预发布版本

#### 外部测试者
想要外部测试者测试app的预发布版本，你必须提供下面的metadata

* What to test
* App description
* Feedback email
* Marketing URL
* Support URL
* Privacy policy URL (可选)
* Beta App Review contact information
* Beta App Review notes (可选)

##上传build
就像在Uploading a Build for an App中解释的那样，在iTunes Connect记录中，你通过Xcode或Application Loader上传app。
`为了使用iTunes Connect进行TestFlight beta 测试，你必须最新的包含beta entitlement的 App Store Distribution profiles。`
当你成功上传了版本后，你可以在Prerelease看到它
####查看build详情
1. iTunes Connect中打开App详情页
2. 点击Prerelease查看你已经上传的build列表
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/AppDetails-menu-2_2x.png)
		
3. 你可以点击build号查看版本更多信息
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/1BuildNumber_2x.png)
4. 内部测试者和外部测试者区域让你管理哪些用户会成为你的测试者，就像下面**设置和邀请测试者**解释的那样

##为你的app的预发布版添加Metadata
一旦你已经创建了iTunes Connect记录并且上传了版本，你就可以填写该版本的详情信息来和测试者分享。这一步对内部测试者是可选的，但是推荐的，因为这些在TestFlight的内容可以帮助测试者。
####添加build描述
1. iTunes Connect中打开App详情页
2. 点击Prerelease	
3. 点击你想测试的build号
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/1BuildNumber_2x.png)
	
4. 点击TestFlight

5. 填写TestFlight beta信息 
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/TestInformationTab_2x.png)

##设置和邀请测试者
每个app，你可以从你的iTunes Connect team中最多邀请**25**个用户成为你的内部测试者、最多邀请1000个用户成为你的外部测试者。
`外部测试者不一定是你开发者账号组织中的，你可以通过邮箱邀请任何人成为你的外部测试者。`

###邀请内部测试者
首先验证iTunes Connect用户是否符合成为内部测试者的条件，然后再使改用户成为内部测试者并且邀请他（她）测试

####内部测试者的条件
iTunes Connect用户必须是iTunes Connect team中Admin, Legal, or Technical角色的一部分

![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/U-RUsers_2x.png)

####添加内部测试者和邀请他们测试
1. 在Prerelease中的内部测试者窗格，选择不超过25个的用户作为内部测试者
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/3AddInternalTester_2x.png)
	
2. 点击保存
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/4AddInternalTester2_2x.png)


####打开TestFlight Beta开关
1. 在Prerelease区域，点击Builds tap
2. 打开TestFlight Beta Testing开关
	* 你选中的用户会收到一封邀请邮件；他们可以通过iOS设置中的TestFlight app接受邀请来测试你的最新的可用的版本
	* ![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/5TurnOnTesting_2x.png)

###添加和邀请外部测试者
每个app最多邀请1000个用户作为外部测试者。首页你添加外部测试者，然后邀请他们测试你的app。你需要每个测试的邮箱地址。在邀请你的外部测试者测试app之前，你的app必须通过Beta App审核。版本对测试者的有效期为30天。

####添加外部测试者
1. 在Prerelease区域的外部测试者窗格，点击添加（+）选择添加新的测试者
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/6AddExternalTesters_2x.png)

2. 输入每个测试者的email, first name（可选）, and last name（可选）
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/8AddExternalTesters2b_2x.png)

3. 想导入邮件地址的列表，点击导入文件
	* 选择一个下面格式的CSV文件
		* `first name, last name, email address`
	* 更多信息，下载testing import template
4. 可选的，在“Add to Groups” 区域，勾选组或添加一个组
5. 点击添加

####Builds tab中邀请外部测试者
1. 点击Builds tab
2. 在外部测试列中，点击发送邀请
	![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/9SendInvites_2x.png)
	* 版本状态变为Active状态并且显示版本还有多少天可用。
	* 30天过期后，为了继续测试，需要上传新版本。新版本可用时，内部测试者会自动收到更新通知；为了分发新版本给外部测试者，你需要重新提交Beta App审核；一通过审核，就可以像上面那样重新发送邀请邮件。
	
##提交Beta App审核
在邀请外部测试者之前，你的app必须通过Beta App审核。点击Submit For Beta App Review来开始Beta App审核。
![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/10SubmitForBetaAppReview_2x.png)
版本的外部测试状态变为Waiting for Review。第一个版本提交到Beta App Review需要全面的审核（大概一天）；以后相同版本号的也许不需要全面审核。

你提交	Beta App审核后，Apple审核build和相关的metadata

* 如果Apple批准你的版本TestFlight beta，iTunes Connect中Admin或Technical角色的用户回收到版本被批准的邮件；然后你可以给外部测试者发邀请。
* 如果Apple拒绝了你的build或metadata，iTunes Connect中Admin和Technical角色的用户回收的版本拒绝的邮件。
* 如果你更新提交相同版本号的build，你会被问到你的app是否和上次提交的发生了Significant changes；Significant changes是指你添加或移除了主要的特性或功能

##查看测试者和build的状态

###测试者的状态
在内部测试者和外部测试者区域中，你可以查看每个测试者的状态。

* 当测试者被加入到TestFlight beta testers后，他们的状态变为**Added**
* 当邀请被发送后，他们的状态变为**Invited**
* 当测试者接受邀请后，他们的状态变为**Accepted**
* 当他们下载app后，他们的状态变为**Testing**

###build的状态
* build处于**Active**状态时，会显示该版本剩余可用天数
* 30天的测试时间过后，版本状态变为**Expired**
* 版本不可测时，状态为**Inactive**
* 当版本的测试者下载后，版本状态为**Installed**

`如果你的app使用了Game Center，在测试你的app时为了使用Game Center的特性，测试者需要在他们的设备中打开Game Center sandbox开关。`


##从测试者获取反馈信息
在测试阶段的任何时候，测试者都可以通过TestFlight app来给你发送用户反馈；用户反馈会发送到你在Test Information中指定的邮箱。
![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/BuildsFeedbackEmail_2x.png)

##上传新的版本
预发布的TestFlight beta测试的版本，同一时间只能有一个可以使用TestFlight beta测试。例如，你上传了1.0和2.0的版本，只能有一个可以使用TestfLlight beta测试。
![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/9TestOneVersion-TestFlight_2x.png)
上传一个新的build后，老的build状态会变为Inactive；你可以手动决定哪个版本使用TestFlight beta测试

##完成测试app

![alt text](https://developer.apple.com/library/prerelease/ios/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Art/12TestingOff_2x.png)

想停止一个TestFlight beta测试中Active状态的app，关闭Testing switch就可以了


##提交到App Store
当你通过TestFlight beta测试完成了版本，你可以提交app最终审核。在你提交之前，确认你不需要测试并且改版本是最新版本。当app变成**Ready for Sale in the App Store**状态，之前的builds会自动不可用，你也不可以再测试它们了。






