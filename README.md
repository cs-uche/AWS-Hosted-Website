![](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiMFhGRW81SkhhTldxU3VJMTFOTlVDVFRVaVBnK1liUEJDYkFPSm1aalp6ODBHYWpleTVGK2FYOGV1SUxvekI5ZHBseGZodDhvTGtuL3hiR01XUTI3cmFjPSIsIml2UGFyYW1ldGVyU3BlYyI6IjVVSkhjU3liL04zQmFCN1IiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=main)

       _____ ____      __    __  _____ __    __ _____
      /  __ | __ |    |  |  |  |/  __ |  |__|  |  ___|
                                                  ___
     |  |   \____ \   |  |  |  |  |   |   __   |  ___|
     |  |__  ____) |  |  \__/  |  |__ |  |  |  |  ___
      \_____|_____/    \ ____ / \_____|__|  |__|_____|
 ----------------------------------------------------------------- 
<i>Little art inspired by AWS Cloud9 above</i>

## Creating a Continuous Delivery Pipeline for an AWS hosted Website

1. create a new local website
```bash
hugo new site new-website
```
2. Create a post
```bash
hugo new posts/welcome-post.md
```
3. Upload public folder to website hosting enabled s3 bucket
4. Bind ip to port for testing(8080)
```bash
curl ipinfo.io
hugo serve --bind=0.0.0.0 --port=8080 --baseURL=http://0.0.0.0/ 
```
5. Create a reuseable pipeline(AWS codebuild)
