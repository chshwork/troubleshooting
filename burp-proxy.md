### Burp can't connect to localhost app
- Description: Can't proxy localhost app, error page "Failed to connect to `localhost:<port>`"
- Try: Without burp, app can be accessed using localhost **but not 127.0.0.1**
- Cause of error: Routing weirdness, burp always resolves localhost to 127.0.0.1
- Solution: restart the application to run on 127.0.0.1
  - Angular: `ng serve --host 127.0.0.1`
