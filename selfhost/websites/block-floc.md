# How to block FLoC on your website

vv01f made me aware of the issue and told me to set the permission-policy header to block FLoC.

The easiest way I found is to edit your .htaccess file and add this line:

```
Header set Permission-Policy: interest-cohort=()
```

<br>

stuebinm pointed out that you can do that in nginx with:

```
add_header Permissions-Policy "interest-cohort=()";
```

<br>

if you know of different circumstances that need different solutions, feel free to add them :)

<br>

## Sources

- https://www.eff.org/deeplinks/2021/03/googles-floc-terrible-idea
- https://amifloced.org/
- https://developer.chrome.com/blog/floc/#how-can-websites-opt-out-of-the-floc-computation
