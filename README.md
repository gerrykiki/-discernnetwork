# discernnetwork on Objective C<br>

### Function Code to Network State<br>

```objective-c
- (NSString *)CheckNetwork{
    Reachability *rech = [Reachability reachabilityWithHostName:@"www.apple.com"];
    NetworkStatus netStatus = [rech currentReachabilityStatus];
    if (netStatus == NotReachable) {
        return @"No network";
    }
    else if (netStatus == ReachableViaWiFi){
        //Wifi
        return @"Wifi";
    }
    else if (netStatus == kReachableVia2G){
        //2G
        return @"2G";
    }
    else if (netStatus == kReachableVia3G){
        //3G
        return @"3G";
    }
    else if (netStatus == kReachableVia4G){
        //4G
        return @"4G";
    }
    else{
        return @"Error";
        //error
    }
}
```

