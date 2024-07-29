# Live Preview URLs

- [node labmda](https://asrffimpobrcu3qvpnucowjmae0pdwyc.lambda-url.us-east-1.on.aws/)
- [python labmda](https://g7i5xag6l5etp2q2gtfbjtjifm0utgst.lambda-url.us-east-1.on.aws/)


# Dev notes
## node
- no tests included, could add
- had some issues with package-lock file location but fixed with "cache-dependency-path" flag

## python
 - needed to update "runtime settings" in "Code" tab to reflect project setup by setting the handler to "main.handler". nb: important to "deploy" code to test these changes in situe
 - need improved testing hanlding + response
 - maybe slack integration on test or deploy failure

# TODO

- setup staging for both functions
- potential hooks for something like slack integration
- store artifacts from builds and testing so they are available for inspection if required or resuse
- investigate lambda versioning and rollbacks, could this be automated with a post deploy test? [Aliases could be usefull potentially](https://docs.aws.amazon.com/lambda/latest/dg/configuration-aliases.html)
- investigate what happens when code is updated frequently causing multiple calls to github actions, push vs merge request etc... 
- investigate security best practice such as CODEOWNERS, code scanning, ensure aws policies are minimal, check (and pin if possible all third party actions if possible) etc...