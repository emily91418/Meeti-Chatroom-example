Meeti-Chatroom-example
======================

Chat Room Example - The Usage of MeetiFramework

# About Meeti-iOS
https://github.com/MOBAGEL/MeetiFramework

# Web to Apply for Testing Account for Meeti
http://meeti.mobagel.com

# Notice of Development    
1.Please enter APP ID and APP SecretKey when using this framework in AppDelegate.m  
2.The default group id is provided in AppDelegate.h   

# Introduction of Main Objects  

### groupVC  
Segue for showing the groups that you've joined and creating another group. The group is private by default.  

      
### chatRoomViewController 
Segue where chat is actually be held at.  

1.You MUST join the group before sending the message to that group  
> {
  [[MeetiServer sharedInstance] joinToGroup:EXAMPLE_GROUP_ID shandle:^(NSString *responseString) {
        NSLog(@"Join to group success %@",responseString);
    } fhandle:^(NSString *responseString, NSError *error) {
        NSLog(@"Join to group Fail %@ , error = %@",responseString,error);
    }];
  }

### profileViewController  
Segue where the user can change their information  
