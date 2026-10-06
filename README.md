# Task_06-10-26
## WEB_FORM
### Program
```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import Select

driver = webdriver.Chrome()
driver.get("https://www.selenium.dev/selenium/web/web-form.html")

text_box = driver.find_element(By.NAME, "my-text")
text_box.send_keys("Python Selenium")

driver.find_element(By.NAME, "my-text").send_keys("John")
driver.find_element(By.NAME, "my-password").send_keys("Password123")
driver.find_element(By.NAME, "my-textarea").send_keys("Learning Selenium")

radio_buttons = driver.find_elements(
    By.CSS_SELECTOR, "input[type='radio']"
)

if not radio_buttons[0].is_selected():
    radio_buttons[0].click()

checkboxes = driver.find_elements(
    By.CSS_SELECTOR, "input[type='checkbox']"
)

for checkbox in checkboxes:
    if not checkbox.is_selected():
        checkbox.click()

country = Select(driver.find_element(By.NAME, "my-select"))

country.select_by_index(1)

for option in country.options:
    print(option.text)


input("Press ENTER in the terminal when you want to close the browser...")

driver.quit()

```
### Output

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c33019ea-39f8-4033-ae41-196a71506be5" />


## REGISTRATION_FORM
### Program
```
from selenium import webdriver
from selenium.webdriver.common.by import By
import time

driver = webdriver.Chrome()

driver.get("https://vinothqaacademy.com/demo-site/")

driver.maximize_window()

time.sleep(3)

driver.find_element(By.ID, "vfb-5").send_keys("Dappili")

driver.find_element(By.ID, "vfb-7").send_keys("Vasavi")

driver.find_element(
    By.XPATH, "//label[contains(.,'Female')]"
).click()

driver.find_element(
    By.XPATH, "//label[contains(.,'Selenium WebDriver')]"
).click()

driver.find_element(
    By.XPATH, "//label[contains(.,'Java')]"
).click()

driver.find_element(
    By.XPATH, "//label[contains(.,'TestNG')]"
).click()

driver.find_element(
    By.XPATH, "//label[contains(.,'Street Address')]/preceding::input[1]"
).send_keys("123 Anna Nagar")


driver.find_element(
    By.XPATH, "//label[contains(.,'Apt, Suite, Bldg.')]/preceding::input[1]"
).send_keys("Flat 101")

driver.find_element(
    By.XPATH, "//label[contains(.,'City')]/preceding::input[1]"
).send_keys("Chennai")

driver.find_element(
    By.XPATH, "//label[contains(.,'Postal / Zip Code')]/preceding::input[1]"
).send_keys("600040")

driver.find_element(By.ID, "vfb-14").send_keys("vasavi@gmail.com")


print("All details filled successfully!")

input("Press Enter to close the browser...")

driver.quit()
```
### Output
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fe16f611-ada2-479f-8a12-41533d23298a" />


