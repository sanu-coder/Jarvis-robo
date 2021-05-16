# Jarvis-robo

<img height="500px" width="500px" src="https://user-images.githubusercontent.com/72346984/118402867-7125a780-b689-11eb-94ec-ceb6e44fdfc1.jpg" alt="">
It is a virtual assistant like iron man Jarvis in Python. 

It takes the command as input and follows the given instruction and generates the output accordingly. This project is only for beginners who has just recently started AI. In my code, it takes the following instructions : 

1. Opens wikipedia. 
2. Opens youtube, google.
3. Opens websites like geeksforgeeks, stackoverflow, etc.
4. Sends email to many peoples at  time.


Algorithm : -

1. For wikipedia : 

      To open wikipedia, wikipedia module has been imported. "summary" function helps to open wikipedia.<br>
      Function syntax :<br> 
     
         import wikipedia
         results=wikipedia.summary(query,sentences=10)
2. For websites : 

      To open websites like youtube, google, geeksforgeeks, stackoverflow "webbrowser" module has been imported.<br>
      Function syntax :<br> 
     
         import webbrowser
         results=webbrowser.open('website_url') 
        
3. For time : 

      For time, 'datetime' module is imported. 'datetime.now()' function helps to know the current time where as 'strftime("%H:%M:%S")' function converts the time into hours-min-second format.<br>
      Function syntax :<br> 
      
        import datetime
        time=datetime.datetime.now().strftime("%H:%M:%S")
        
 4. For Code Editors :
 
    For opening Code Editors, 'os' module is imported and 'startfile()' function helps to open the code editor.<br>
    Function syntax:<br>
    
        code_path: str= "Path_seperated_by_double_slash"
        os.startfile(code_path)
  
  5. Send Email :
      For sending Emails you have to import 'smtplib' module. Then following procedure is followed : <br>
      
      a. First of all, “smtplib” library needs to be imported.
      
      b. After that, to create a session, we will be using its instance SMTP to encapsulate an SMTP connection.
      
          server=smtplib.SMTP('smtp.gmail.com',587)
        
        In this, you need to pass the first parameter of the server location and the second parameter of the port to use. For Gmail, we use port number 587.
      
      c. For security reasons, now put the SMTP connection in the TLS mode. TLS (Transport Layer Security) encrypts all the SMTP commands. 
      
          server.starttls()
          
      d.  After that, for security and authentication, you need to pass your Gmail account credentials in the login instance.The compiler will show an authentication error if you enter invalid email id or password.
      
          server.login('your-email','your-email-password')
         
      e. Store the message you need to send in a variable say, message. Using the sendmail() instance, send your message. sendmail() uses three parameters: sender_email_id, receiver_email_id and message_to_be_sent. The parameters need to be in the same sequence.
      
          server.sendmail('your-email',to,content)
          
      f. Close the session.
      
          server.close()
      
