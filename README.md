# CSMTP

example code:

````go

	csmtp.Host = Settings.SMTP.Host
	csmtp.Port = Settings.SMTP.Port
	csmtp.Name = Settings.SMTP.SenderName
	csmtp.From = Settings.SMTP.SenderEmail
	csmtp.Auth(Settings.SMTP.SenderPassword)

	subject := "测试主题"
	body := "我是一封电子邮件!golang发出."

	err := csmtp.SendMail(subject, body, toEmail)
	if err != nil {
		log.Fatal(err)
	} else {
		log.Print("send OK")
	}
````
