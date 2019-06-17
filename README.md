# Puppeteer Test
Puppeteer test docker image

[Nodejs](https://nodejs.org/en/)
[Puppeteer](https://github.com/GoogleChrome/puppeteer)

### Jenkins file uses
```groovy  
agent {  
  docker {      
      image 'puppeteer:latest'      
      args '--privileged'  
   }  
 }  
```   
### Puppetter launch config
```javascript   
const browser = await puppeteer.launch(
      {
          headless: true,
          args: [
            `--no-sandbox`,
            '--start-maximized',
            '--disable-setuid-sandbox',
            `--disable-infobars`,
            `--disable-dev-shm-usage`,
          ],
          ignoreHTTPSErrors: true,
          dumpio: false,
       }
   );
```
