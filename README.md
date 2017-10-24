public class MyTest {

    private WebDriver driver;
    private WebDriver wait;

    /*
     * Navigate to "gmail.com"
     * Maximize the window
     * Enter the "selenium" into the search bar
     * Click the ‘Google Search’ button.
     * Click the 'Back' button
     * Refresh the page
     * Close the web page
     */

    @Test
    public void MyFirst() {
    driver = new ChromeDriver();
    driver.get("https://www.google.com/");
    driver.manage().window().maximize();
    driver.findElement(By.id("lst-ib")).sendKeys("selenium");
    driver.findElement(By.xpath("//input[@name='btnK']"));
    driver.navigate().back();
    driver.quit();
    }
}