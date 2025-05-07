# allofbugs

*cc: yuzadef@gmail.com*

*bugcrowd: https://bugcrowd.com/yuza101*

### bugs
- [cross-site scripting (xss)](https://github.com/yuzadef/allofbugs/blob/main/xss.md)
- [information disclosure](https://github.com/yuzadef/allofbugs/blob/main/information-disclosure.md)

### resources
- [6-digits otp bruteforce wordlist](https://raw.githubusercontent.com/indahud/otp-wordlist/master/6_digit_mix.txt)
- [custom http headers](https://gist.githubusercontent.com/kaimi-/6b3c99538dce9e3d29ad647b325007c1/raw/921b0dd64e01c31106ece6087a3582e2d6fc6bc2/gistfile1.txt)
- [rate limit bypass techniques](https://medium.com/@raxomara/bypassing-rate-limits-all-known-techniques-25891bb5ca59)
- [sqli advanced concept](https://johnermac.github.io/notes/ewptx/sqli/)
- [cyber swiss army knife](https://gchq.github.io/CyberChef/)

### tips
<details>
  <summary>using authorize</summary>
  
1. configuration tab, add lower privilege users cookie in the temporary header section.
  
2. interceptions filters, add in-scope items only.
  
3. browse the app using higher privilege user.

4. check for bypassed!
  
5. verify manually.
</details>

<details>
  <summary>wildcard target & xss</summary>

1. subfinder -dL domain.txt -o sub1.txt

2. cat domain.txt | assetfinder --subs-only | tee -a sub2.txt

3. cat sub1.txt sub2.txt > subdomains.txt

4. cat subdomains.txt | anew >> final_subs.txt

5. cat final_subs.txt | httpx -o alive_subs.txt

6. cat alive_subs.txt | waybackurls >> urls1.txt

7. cat alive_subs.txt | gau >> urls2.txt

8. katana -list alive_subs.txt -o urls3.txt

9. cat urls1.txt urls2.txt urls3.txt >> all_urls.txt

10. cat all_urls.txt | uro >> final_urls.txt

11. cat final_urls.txt | gf xss >> xss.txt

12. cat xss.txt | kxss
</details>
