#Автотест для входа в аккаунт
---------------------------------------------------------------------
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://prostayaeda.ru")
elem = driver.find_element(By.CLASS_NAME, "b-h__iconsItem_user")
elem.click()
elem = driver.find_element(By.XPATH, "//*[@id='USER_LOGIN")
elem.clear()
elem.send_keys("89959147261")
elem = driver.find_element(By.XPATh, "//*[@id='USER_PASSWORD']")
elem.clear()
elem.send_keys("123")
elem.send_keys(Keys.ENTER)
#
time.sleep(7)
---------------------------------------------------------------------
#Автотест для проверки добавления продукта в корзину
---------------------------------------------------------------------
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

driver = webdriver.Chrome()
driver.maximize_window()
driver.get("https://prostayaeda.ru")
elem = driver.find_element(By.CLASS_NAME, "b-menu__link ")
elem.click()
elem = driver.find_element(By.ID, "bx_10163737_9751_4f877ed29f8ae72b74be00bb9098a65a")
elem.click()
elem = driver.find_element(By.CLASS_NAME, "b-basketBtn_detail")
elem.click()
elem = driver.find_element(By.CLASS_NAME, "vs__dropdown-menu")
elem.click()
elem = driver.find_element(By.CLASS_NAME, "b-basketBtn__link_inBasket")
elem.click()
#
time.sleep(7)
