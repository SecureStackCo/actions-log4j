# SecureStack Log4j Vulnerability Analysis GitHub Action

A GitHub Action that analyses your java source code for all versions of the log4j vulnerability that affect both log4j 1.x and 2.x.  You can read more about all versions of Log4j that are affected here:  https://logging.apache.org/log4j/2.x/security.html

```
name: Example Workflow Using the SecureStack log4j scanning Action
on: push
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
      - name: log4j Scanning Step
        id: log4j
        uses: SecureStackCo/actions-log4j@v0.1.2
        with:
          securestack_api_key: ${{ secrets.SECURESTACK_API_KEY }}
          securestack_app_id: ${{ secrets.SECURESTACK_APP_ID }}
          severity: critical
```
## Create your SecureStack API Key and save as GitHub Secret

1. Log in to [SecureStack](https://app.securestack.com) and go to the Profile -> GENERATE KEY screen.
2. Generate an API key and copy the value.
3. Go to Settings for your GitHub repository and click on Secrets -> Actions at the bottom left.
4. Create a new secret named SECURESTACK_API_KEY_SECRET and paste the value from step 2 into the field.

## Retreiving your SecureStack Application ID

1. Log in to [SecureStack](https://app.securestack.com).
2. Open the application you wish to analyse.
3. Copy the value of the application id on the View Application screen.
4. Go to Settings for your GitHub repository and click on Secrets -> Actions at the bottom left.
5. Create a new secret named SECURESTACK_APP_ID and paste the value from step 3 into the field.


Made with 💜  by [SecureStack](https://securestack.com)
