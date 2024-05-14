# what-is-service
Service: Service ek background task ko represent karta hai jo UI ke bina run hota hai. Kotlin mein aap Services ka use kar sakte hain for long-running operations jaise ki downloading files, playing music, etc.
1.Foreground Services:
Yeh services user ke actively aware hone par run hoti hain aur ek ongoing notification dikhati hain. Example include music player, file download, etc.
Foreground services ko notification ke through user ko notify karna padta hai.
2.Background Services:
Yeh services directly user ke interaction ke bina background mein run hoti hain. Example include syncing data, processing data in the background, etc.
3.Bound Services:
Yeh services client-server interface provide karti hain jahan ek application component (client) ek service ke saath bind hota hai aur interact karta hai.
Bound services ko tab tak run kiya jata hai jab tak clients bound rahte hain.
Detailed Breakdown of Each Type
Foreground Services:
Example: Music player app jo background mein music play karta hai.
Usage: startForeground()
Notification Requirement: Yes, ongoing notification display karna zaroori hai.
Background Services:

Example: Data sync karna ya file download karna jo user ke direct interaction ke bina hota hai.
Usage: startService()
Restrictions: Android 8.0 se kuch restrictions lagayi gayi hain. JobIntentService ya WorkManager ka use suggest kiya jata hai.
Bound Services:

Example: Service jo multiple activities ko data provide karti hai. Example is accessing a remote server.
Usage: bindService()
Lifecycle: Service bind hone par shuru hoti hai aur unbind hone par destroy hoti hai.
Implementation Example in Kotlin
