# allofbugs

this repo is a collection of notes, payloads, and resources around web app security — stuff like sqli, xss, idor, ssrf, and all the fun ways things break online.

no fluff, no theory dumps. just real, useful info that comes in handy when testing apps or digging for bugs.

whether you’re:
- exploring a new target
- chasing weird behavior
- writing up a report
- or just collecting cool tricks

this is the kind of reference you'd want nearby.

## what you’ll find here:
- notes on common and not-so-common vulns
- payloads that have worked in the wild
- bypass tricks and edge cases
- links to tools, writeups, and other solid resources
- occasional tips that don’t make it into the docs

🤝 use it however you want:
clone it, copy bits, share it, suggest improvements — whatever.
if you’ve got a cool tip or resource to add, feel free to open a pr.

### bugs
- [cross-site scripting (xss)](https://github.com/yuzadef/allofbugs/blob/main/xss.md)
- [information disclosure](https://github.com/yuzadef/allofbugs/blob/main/information-disclosure.md)

### general testing checklist
- [web application testing checklist](https://github.com/yuzadef/allofbugs/blob/main/checklist.md)

### resources
- [6-digits otp bruteforce wordlist](https://raw.githubusercontent.com/indahud/otp-wordlist/master/6_digit_mix.txt)
- [custom http headers](https://gist.githubusercontent.com/kaimi-/6b3c99538dce9e3d29ad647b325007c1/raw/921b0dd64e01c31106ece6087a3582e2d6fc6bc2/gistfile1.txt)
- [rate limit bypass techniques](https://medium.com/@raxomara/bypassing-rate-limits-all-known-techniques-25891bb5ca59)
- [sqli advanced concept](https://johnermac.github.io/notes/ewptx/sqli/)

**using authorize**
1. configuration tab, add lower privilege users cookie in the temporary header section.
2. interceptions filters, add in-scope items only.
3. browse the app using higher privilege user.
4. check for bypassed!
5. verify manually.
