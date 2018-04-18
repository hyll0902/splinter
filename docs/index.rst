from splinter import Browser

with Browser() as browser:
    # Visit URL
    url = "https://ticket.urbtix.hk/internet/login/transaction?saveRequestUrl=/secure/event/35323/performanceDetail/337944"
    browser.visit(url)
    browser.fill('q', 'splinter - python acceptance testing for web applications')
    # Find and click the '登入' button
    button = browser.find_by_name('登入')
    # Interact with elements
    button.click()
    if browser.is_text_present('splinter.readthedocs.io'):
        print("Yes, the official website was found!")
    else:
        print("No, it wasn't found... We need to improve our SEO techniques")

