# cross-site scripting cheatsheets

### testing flow
1. collect as much urls as possible -- ***waybackurls, hakrawler, paramspider, etc...***
2. filter the urls that have parameters potentially vulnerable to xss -- ***gf***
3. identify urls that reflects their values in the response page -- ***Gxss***
4. determine the context of the reflections -- ***html, attributes, script, etc...***
5. verify if special characters are escaped gracefully -- ***' " < > - / \ # { } [ ] ( ) = ; , * & % :***
6. craft the payload structure -- ***escaping the context***
7. trigger xss -- ***alert, prompt, confirm, etc...***
8. escalate xss exploitation to higher impact -- ***ato, csrf, etc...***

### top 25 xss parameters
```
?q=
?s=
?search=
?id=
?lang=
?keyword=
?query=
?page=
?keywords=
?year=
?view=
?email=
?type=
?name=
?p=
?month=
?immagine=
?list_type=
?url=
?terms=
?categoryid=
?key=
?!=
?begindate=
?enddate=
```

### resources
- [how to find origin ip of any website behind a waf](https://freedium.cfd/https://infosecwriteups.com/how-to-find-origin-ip-of-any-website-behind-a-waf-c85095156ef7)
- [csp bypass search](https://cspbypass.com/)
