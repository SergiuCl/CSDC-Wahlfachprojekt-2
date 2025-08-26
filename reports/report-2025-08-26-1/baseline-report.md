# ZAP Scanning Report

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 5 |
| Informational | 5 |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| Content Security Policy (CSP) Header Not Set | Medium | 12 |
| Cross-Domain Misconfiguration | Medium | 12 |
| Cross-Domain JavaScript Source File Inclusion | Low | 10 |
| Dangerous JS Functions | Low | 2 |
| Deprecated Feature Policy Header Set | Low | 12 |
| Insufficient Site Isolation Against Spectre Vulnerability | Low | 10 |
| Timestamp Disclosure - Unix | Low | 16 |
| Information Disclosure - Suspicious Comments | Informational | 2 |
| Modern Web Application | Informational | 11 |
| Non-Storable Content | Informational | 1 |
| Storable and Cacheable Content | Informational | 1 |
| Storable but Non-Cacheable Content | Informational | 9 |




## Alert Detail



### [ Content Security Policy (CSP) Header Not Set ](https://www.zaproxy.org/docs/alerts/10038/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/coupons_2013.md.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/eastere.gg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/encrypt.pyc
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/package-lock.json.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/package.json.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/suspicious_errors.yml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:421:3
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 12

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy ](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy)
* [ https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
* [ https://www.w3.org/TR/CSP/ ](https://www.w3.org/TR/CSP/)
* [ https://w3c.github.io/webappsec-csp/ ](https://w3c.github.io/webappsec-csp/)
* [ https://web.dev/articles/csp ](https://web.dev/articles/csp)
* [ https://caniuse.com/#feat=contentsecuritypolicy ](https://caniuse.com/#feat=contentsecuritypolicy)
* [ https://content-security-policy.com/ ](https://content-security-policy.com/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Cross-Domain Misconfiguration ](https://www.zaproxy.org/docs/alerts/10098/)



##### Medium (Medium)

### Description

Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/ftp/acquisitions.md
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/ftp/encrypt.pyc
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/ftp/incident-support.kdbx
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: http://juice-shop:3000/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`

Instances: 12

### Solution

Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).
Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.

### Reference


* [ https://vulncat.fortify.com/en/detail?id=desc.config.dotnet.html5_overly_permissive_cors_policy ](https://vulncat.fortify.com/en/detail?id=desc.config.dotnet.html5_overly_permissive_cors_policy)


#### CWE Id: [ 264 ](https://cwe.mitre.org/data/definitions/264.html)


#### WASC Id: 14

#### Source ID: 3

### [ Cross-Domain JavaScript Source File Inclusion ](https://www.zaproxy.org/docs/alerts/10017/)



##### Low (Medium)

### Description

The page includes one or more script files from a third-party domain.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:421:3
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:421:3
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: `//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js`
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.2.4/jquery.min.js"></script>`
  * Other Info: ``

Instances: 10

### Solution

Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.

### Reference



#### CWE Id: [ 829 ](https://cwe.mitre.org/data/definitions/829.html)


#### WASC Id: 15

#### Source ID: 3

### [ Dangerous JS Functions ](https://www.zaproxy.org/docs/alerts/10110/)



##### Low (Low)

### Description

A dangerous JS function seems to be in use that would leave the site vulnerable.

* URL: http://juice-shop:3000/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `bypassSecurityTrustHtml(`
  * Other Info: ``
* URL: http://juice-shop:3000/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `bypassSecurityTrustHtml(`
  * Other Info: ``

Instances: 2

### Solution

See the references for security advice on the use of these functions.

### Reference


* [ https://angular.io/guide/security ](https://angular.io/guide/security)


#### CWE Id: [ 749 ](https://cwe.mitre.org/data/definitions/749.html)


#### Source ID: 3

### [ Deprecated Feature Policy Header Set ](https://www.zaproxy.org/docs/alerts/10063/)



##### Low (Medium)

### Description

The header has now been renamed to Permissions-Policy.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/coupons_2013.md.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/eastere.gg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/encrypt.pyc
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/package-lock.json.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/package.json.bak
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``
* URL: http://juice-shop:3000/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Feature-Policy`
  * Other Info: ``

Instances: 12

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header instead of the Feature-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Permissions-Policy)
* [ https://scotthelme.co.uk/goodbye-feature-policy-and-hello-permissions-policy/ ](https://scotthelme.co.uk/goodbye-feature-policy-and-hello-permissions-policy/)


#### CWE Id: [ 16 ](https://cwe.mitre.org/data/definitions/16.html)


#### WASC Id: 15

#### Source ID: 3

### [ Insufficient Site Isolation Against Spectre Vulnerability ](https://www.zaproxy.org/docs/alerts/90004/)



##### Low (Medium)

### Description

Cross-Origin-Embedder-Policy header is a response header that prevents a document from loading any cross-origin resources that don't explicitly grant the document permission (using CORP or CORS).

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: `Cross-Origin-Embedder-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/ftp
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: `Cross-Origin-Opener-Policy`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``

Instances: 10

### Solution

Ensure that the application/web server sets the Cross-Origin-Embedder-Policy header appropriately, and that it sets the Cross-Origin-Embedder-Policy header to 'require-corp' for documents.
If possible, ensure that the end user uses a standards-compliant and modern web browser that supports the Cross-Origin-Embedder-Policy header (https://caniuse.com/mdn-http_headers_cross-origin-embedder-policy).

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 14

#### Source ID: 3

### [ Timestamp Disclosure - Unix ](https://www.zaproxy.org/docs/alerts/10096/)



##### Low (Low)

### Description

A timestamp was disclosed by the application/web server. - Unix

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1650485437`
  * Other Info: `1650485437, which evaluates to: 2022-04-20 20:10:37.`
* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1981395349`
  * Other Info: `1981395349, which evaluates to: 2032-10-14 19:35:49.`
* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `2038834951`
  * Other Info: `2038834951, which evaluates to: 2034-08-10 15:02:31.`
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1650485437`
  * Other Info: `1650485437, which evaluates to: 2022-04-20 20:10:37.`
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1981395349`
  * Other Info: `1981395349, which evaluates to: 2032-10-14 19:35:49.`
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `2038834951`
  * Other Info: `2038834951, which evaluates to: 2034-08-10 15:02:31.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1650485437`
  * Other Info: `1650485437, which evaluates to: 2022-04-20 20:10:37.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1680327869`
  * Other Info: `1680327869, which evaluates to: 2023-04-01 05:44:29.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1701244813`
  * Other Info: `1701244813, which evaluates to: 2023-11-29 08:00:13.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1818181818`
  * Other Info: `1818181818, which evaluates to: 2027-08-13 18:30:18.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1839622642`
  * Other Info: `1839622642, which evaluates to: 2028-04-17 22:17:22.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1863874346`
  * Other Info: `1863874346, which evaluates to: 2029-01-23 14:52:26.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1917098446`
  * Other Info: `1917098446, which evaluates to: 2030-10-01 15:20:46.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1981395349`
  * Other Info: `1981395349, which evaluates to: 2032-10-14 19:35:49.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `2033195021`
  * Other Info: `2033195021, which evaluates to: 2034-06-06 08:23:41.`
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `2038834951`
  * Other Info: `2038834951, which evaluates to: 2034-08-10 15:02:31.`

Instances: 16

### Solution

Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.

### Reference


* [ https://cwe.mitre.org/data/definitions/200.html ](https://cwe.mitre.org/data/definitions/200.html)


#### CWE Id: [ 497 ](https://cwe.mitre.org/data/definitions/497.html)


#### WASC Id: 13

#### Source ID: 3

### [ Information Disclosure - Suspicious Comments ](https://www.zaproxy.org/docs/alerts/10027/)



##### Informational (Low)

### Description

The response appears to contain suspicious comments which may help an attacker.

* URL: http://juice-shop:3000/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `query`
  * Other Info: `The following pattern was used: \bQUERY\b and was detected in likely comment: "//owasp.org' target='_blank'>Open Worldwide Application Security Project (OWASP)</a> and is developed and maintained by voluntee", see evidence field for the suspicious comment/snippet.`
* URL: http://juice-shop:3000/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Query`
  * Other Info: `The following pattern was used: \bQUERY\b and was detected in likely comment: "//www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M0 256C0 397.4 114.6 512 256 512s256-114.6 256-256S397.4 0 256 0S0 114.6 0", see evidence field for the suspicious comment/snippet.`

Instances: 2

### Solution

Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.

### Reference



#### CWE Id: [ 615 ](https://cwe.mitre.org/data/definitions/615.html)


#### WASC Id: 13

#### Source ID: 3

### [ Modern Web Application ](https://www.zaproxy.org/docs/alerts/10109/)



##### Informational (Medium)

### Description

The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/build/routes/fileServer.js:43:13
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/build/routes/fileServer.js:59:18
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/build/routes/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:280:10
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:286:9
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:365:14
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/index.js:421:3
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/juice-shop/node_modules/express/lib/router/layer.js:95:5
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script src="//cdnjs.cloudflare.com/ajax/libs/cookieconsent2/3.1.0/cookieconsent.min.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`

Instances: 11

### Solution

This is an informational alert and so no changes are required.

### Reference




#### Source ID: 3

### [ Non-Storable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.

* URL: http://juice-shop:3000/ftp/encrypt.pyc
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `403`
  * Other Info: ``

Instances: 1

### Solution

The content may be marked as storable by ensuring that the following conditions are satisfied:
The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)
The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)
The "no-store" cache directive must not appear in the request or response header fields
For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response
For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)
In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:
It must contain an "Expires" header field
It must contain a "max-age" response directive
For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive
It must contain a "Cache Control Extension" that allows it to be cached
It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Storable and Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.

* URL: http://juice-shop:3000/robots.txt
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.`

Instances: 1

### Solution

Validate that the response does not contain sensitive, personal or user-specific information. If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:
Cache-Control: no-cache, no-store, must-revalidate, private
Pragma: no-cache
Expires: 0
This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Storable but Non-Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users.

* URL: http://juice-shop:3000
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/assets/public/favicon_js.ico
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/ftp/incident-support.kdbx
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/main.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/polyfills.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/runtime.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/sitemap.xml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/styles.css
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``
* URL: http://juice-shop:3000/vendor.js
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`
  * Other Info: ``

Instances: 9

### Solution



### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html)


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3


