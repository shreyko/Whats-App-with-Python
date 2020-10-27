# Whats-App-with-Python
# very very basic code at the moment
# only sending message function
# will add automatic messaging at certain times to certain contacts (like linking this to a database containing the birthdays of people along with phone number so that it automatically wishes them)
# I find getting through the QR scanner particularly hard so am trying to figure out a way to get around it using cached data(HELP)





























from selenium import webdriver
from selenium.webdriver.support.select import Select
import time
from keyboard import press


options = webdriver.ChromeOptions()
phone = int(input("enter the phone number to message"))
browser = webdriver.Chrome("chromedriver")
browser.get("https://web.whatsapp.com/")
print("please scan QR_Code")
time.sleep(6)
browser.get("https://web.whatsapp.com/send?phone="+ str(phone))


time.sleep(7)



time.sleep(5)
def send_message():
    type_message = browser.find_element_by_xpath("/html/body/div[1]/div/div/div[4]/div/footer/div[1]/div[2]/div/div[2]")
    type_message.send_keys("hello \
    [This is actually an automated machine message]")
    press("enter")
    time.sleep(3)




send_message()
