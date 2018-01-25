# discernnetwork on Objective C<br>

Import class to project<br>

Reachability *rech = [Reachability reachabilityWithHostName:@"www.apple.com"];<br>
NetworkStatus netStatus = [rech currentReachabilityStatus];<br>
if (netStatus == NotReachable) {<br>
	return @"No network";<br>
	}<br>
else if (netStatus == ReachableViaWiFi){<br>
	//Wifi<br>
	return @"Wifi";<br>
	}<br>
else if (netStatus == kReachableVia2G){<br>
	//2G<br>
	return @"2G";<br>
	}<br>
	else if (netStatus == kReachableVia3G){<br>
	//3G<br>
	return @"3G";<br>
	}<br>
	else if (netStatus == kReachableVia4G){<br>
	//4G<br>
	return @"4G";<br>
	}<br>
	else{<br>
	return @"Error";<br>
	//error<br>
}
