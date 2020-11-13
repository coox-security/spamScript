# spamScript
Reads a text file, line by line, enters into text field, and sends


# need pyautogui for this to work, time module to set a delay
import pyautogui, time

# you will need a text file to spam with as a file in the same project
# reads txt file to spam with, in this case it is the Bee Movie script
spamText = open("beeMovieScript.txt", 'r')

# start the script, then open the website...time delay to get set
time.sleep(5)

# for loop to cycle through the lines, print, and hit enter line by line
for word in spamText:
	pyautogui.typewrite(word)
	
	# built in time delay in case something goes wrong
	time.sleep(5)
	pyautogui.press("enter")
