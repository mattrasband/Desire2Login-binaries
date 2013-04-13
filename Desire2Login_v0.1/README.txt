-- DESCRIPTION --

This is a simple program to login to D2L at Regis University, poll for updates
of unread discussion messages, new emails, and dropbox feedback.  It is based
on Tkinter and Python and is compiled for Windows using py2exe, as a result
(in windows) it should not require a Python install nor configuration.

-- AUTHOR --

Matt Rasband, (c)2013 - All Rights Reserved.

-- REQUIREMENTS --

You need to edit the 'config.json' file to include your username, number of classes,
and encoded password (use encodePw.exe in the encodePassword folder to determine the
encoded password).  You also need to change the number of classes to how many you're taking,
otherwise the program will log errors in Desire2Login.exe.log

config.json Example:

{
	"Username" : "jdoe",
	"Password" : "cGFzc3dvcmQ=",
	"NumClasses" : "1"
}

-- NOTICES --

The password is stored in an encoded manner, but it is not a very strong
encoding (the idea for now is portability).  But I also don't want my (or your)
passwords stored in plain text.  So do note, if you choose to not store this
in a protected folder (i.e. One without administrator access protections), then
there is a chance someone else could discover your password.

I have nothing sent to me, so everything in the program happens between the
user's computer and D2L (@ Regis University).

-- RELEASE NOTES v0.1 (beta) --

Version Updates v0.1:
	- Initial Release
	- Establish protocol to login to D2L through Python
	- Parse pages for desired content
	- Functioning pieces:
		- Email count
		- Discussion count
	
Plans for future:
	- Dropbox support (I haven't had 'new' feedback to test with yet)
	- Polling intervals
	- Option to email you when updates happen (based on polling intervals)
	- Perhaps optional pop-up notifications (Rather than building my own, I'll probably use windows APIs)

Hopeful, but unlikely plans:
	- Forward emails from D2L to alternate email (Tough due to the way D2L is setup in frames and weird use of Javascript)
	- Send emails (locally) through D2L (Again, difficult but probably possible.)