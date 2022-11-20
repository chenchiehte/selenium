# selenium
#載入selenium相關模組
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from time import sleep
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys


#設定ChromeDriver的執行路徑檔
options=Options()
options.add_argument("--disable-notifications")
options.chrome_executable_path="C:\\Users\\88693\\AppData\\Local\\Programs\\Python\\Python39\\pythonselenium\\chromedriver.exe"
#建立Driver物件實體,用程式操作瀏覽器運作
driver = webdriver.Chrome(options=options)

driver.get("https://www.youtube.com/")
sleep(5)
button=driver.find_element(By.ID, "search")
sleep(5)
button.send_keys("123")
button.send_keys(Keys.RETURN)

sleep(10)
