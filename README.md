# Chulchek
#무신사 출첵하기


import selenium
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions

ID = '아이디' # Change ID if you need to use your ID
PW = '비밀번호'

URL = 'https://www.musinsa.com/'

driver = webdriver.Chrome(executable_path='chromedriver')
driver.get(url=URL)

search_box = driver.find_element_by_xpath('//*[@id="wrapper"]/div[1]/div/div[2]/ul/li[1]/a')
search_box.click()

id_box = driver.find_element_by_xpath('/html/body/div[1]/div/div[2]/form/span[1]/input')
id_box.send_keys(ID)
pw_box = driver.find_element_by_xpath('/html/body/div[1]/div/div[2]/form/span[2]/input')
pw_box.send_keys(PW)

login_box = driver.find_element_by_xpath('/html/body/div[1]/div/div[2]/form/span[3]/input')
login_box.click()

