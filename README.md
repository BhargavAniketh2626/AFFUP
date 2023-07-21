# AFFUP
AUTO FORM FILLING USING PYTHON

step 1:
open cmd: pip install selenium

step 2:
create a new python idle file

step 3:
select any simple website and select the fields which are need to be auto filled.

step 4:(Windows)
right on one of the field and click on inspect and your html code will be highlighted do select that and right click again to get an option copy and you can find the term XPATH and click on that.

step 5:
from selenium import webdriver
import time
from selenium.webdriver.common.by import By 

web = webdriver.Firefox()
web.get('https://www.starbucks.in/registration')

time.sleep(2)

email = "bhargavan19@gmail.com"
last = web.find_element(By.XPATH,'//*[@id="mat-input-0"]')
last.send_keys(email)

Mobile_Number = "9618029818"
first = web.find_element(By.XPATH,'//*[@id="mat-input-3"]')
first.send_keys(Mobile_Number)

Password = "SSBBA@1234"
first1 = web.find_element(By.XPATH,'//*[@id="mat-input-2"]')
first1.send_keys(Password)

Repassword = "SSBBA@1234"
first2 = web.find_element(By.XPATH,'//*[@id="mat-input-5"]')
first2.send_keys(Repassword)

Submit = web.find_element(By.XPATH,'/html/body/app-root/div/app-registration/div/section/form/div[2]/button')
Submit.click()


