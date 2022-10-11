# ZAP Scanning Report


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 6 |
| Informational | 5 |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| CSP: Wildcard Directive | Medium | 2 |
| Content Security Policy (CSP) Header Not Set | Medium | 4 |
| A Server Error response code was returned by the server | Low | 68 |
| Application Error Disclosure | Low | 3 |
| Permissions Policy Header Not Set | Low | 5 |
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 10 |
| Unexpected Content-Type was returned | Low | 59 |
| X-Content-Type-Options Header Missing | Low | 8 |
| A Client Error response code was returned by the server | Informational | 5 |
| Non-Storable Content | Informational | 4 |
| Re-examine Cache-control Directives | Informational | 8 |
| Storable and Cacheable Content | Informational | 5 |
| Storable but Non-Cacheable Content | Informational | 1 |




## Alert Detail



### [ CSP: Wildcard Directive ](https://www.zaproxy.org/docs/alerts/10055/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks. Including (but not limited to) Cross Site Scripting (XSS), and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs
  * Method: `GET`
  * Parameter: `Content-Security-Policy`
  * Attack: ``
  * Evidence: `default-src 'none'`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: `Content-Security-Policy`
  * Attack: ``
  * Evidence: `default-src 'none'`

Instances: 2

### Solution

Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.

### Reference


* [ http://www.w3.org/TR/CSP2/ ](http://www.w3.org/TR/CSP2/)
* [ http://www.w3.org/TR/CSP/ ](http://www.w3.org/TR/CSP/)
* [ http://caniuse.com/#search=content+security+policy ](http://caniuse.com/#search=content+security+policy)
* [ http://content-security-policy.com/ ](http://content-security-policy.com/)
* [ https://github.com/shapesecurity/salvation ](https://github.com/shapesecurity/salvation)
* [ https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources ](https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Content Security Policy (CSP) Header Not Set ](https://www.zaproxy.org/docs/alerts/10038/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``

Instances: 4

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy ](https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy)
* [ https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
* [ http://www.w3.org/TR/CSP/ ](http://www.w3.org/TR/CSP/)
* [ http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html ](http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html)
* [ http://www.html5rocks.com/en/tutorials/security/content-security-policy/ ](http://www.html5rocks.com/en/tutorials/security/content-security-policy/)
* [ http://caniuse.com/#feat=contentsecuritypolicy ](http://caniuse.com/#feat=contentsecuritypolicy)
* [ http://content-security-policy.com/ ](http://content-security-policy.com/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ A Server Error response code was returned by the server ](https://www.zaproxy.org/docs/alerts/100000/)



##### Low (High)

### Description

A response code of 500 was returned by the server.
This may indicate that the application is failing to handle unexpected input correctly.
Raised by the 'Alert on HTTP Response Code Error' script

* URL: https://api-service-edilsondmorais.cloud.okteto.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/give-me-the-secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/give-me-the-secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 503`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time/
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500`

Instances: 68

### Solution



### Reference



#### CWE Id: [ 388 ](https://cwe.mitre.org/data/definitions/388.html)


#### WASC Id: 20

#### Source ID: 4

### [ Application Error Disclosure ](https://www.zaproxy.org/docs/alerts/90022/)



##### Low (Medium)

### Description

This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500 Internal Server Error`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500 Internal Server Error`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 500 Internal Server Error`

Instances: 3

### Solution

Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.

### Reference



#### CWE Id: [ 200 ](https://cwe.mitre.org/data/definitions/200.html)


#### WASC Id: 13

#### Source ID: 3

### [ Permissions Policy Header Not Set ](https://www.zaproxy.org/docs/alerts/10063/)



##### Low (Medium)

### Description

Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``

Instances: 5

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy)
* [ https://developers.google.com/web/updates/2018/06/feature-policy ](https://developers.google.com/web/updates/2018/06/feature-policy)
* [ https://scotthelme.co.uk/a-new-security-header-feature-policy/ ](https://scotthelme.co.uk/a-new-security-header-feature-policy/)
* [ https://w3c.github.io/webappsec-feature-policy/ ](https://w3c.github.io/webappsec-feature-policy/)
* [ https://www.smashingmagazine.com/2018/12/feature-policy/ ](https://www.smashingmagazine.com/2018/12/feature-policy/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) ](https://www.zaproxy.org/docs/alerts/10037/)



##### Low (Medium)

### Description

The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/1.2
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unhealth
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`

Instances: 10

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.

### Reference


* [ http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx ](http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx)
* [ http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html ](http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html)


#### CWE Id: [ 200 ](https://cwe.mitre.org/data/definitions/200.html)


#### WASC Id: 13

#### Source ID: 3

### [ Unexpected Content-Type was returned ](https://www.zaproxy.org/docs/alerts/100001/)



##### Low (High)

### Description

A Content-Type of text/html was returned by the server.
This is not one of the types expected to be returned by an API.
Raised by the 'Alert on Unexpected Content Types' script

* URL: https://api-service-edilsondmorais.cloud.okteto.net
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/.htaccess
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/8811678772161753886
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/docs/9062942731782119073
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/give-me-the-secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/give-me-the-secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/.htaccess
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/8444898673429539833
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/whoami/
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login/
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time/
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `text/html`

Instances: 59

### Solution



### Reference




#### Source ID: 4

### [ X-Content-Type-Options Header Missing ](https://www.zaproxy.org/docs/alerts/10021/)



##### Low (Medium)

### Description

The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/1.2
  * Method: `PUT`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unhealth
  * Method: `PUT`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: `X-Content-Type-Options`
  * Attack: ``
  * Evidence: ``

Instances: 8

### Solution

Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.

### Reference


* [ http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx ](http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ A Client Error response code was returned by the server ](https://www.zaproxy.org/docs/alerts/100000/)



##### Informational (High)

### Description

A response code of 404 was returned by the server.
This may indicate that the application is failing to handle unexpected input correctly.
Raised by the 'Alert on HTTP Response Code Error' script

* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/.htaccess
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 400`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/8444898673429539833
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 400`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/secret/secret
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 400`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 404`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login/
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HTTP/1.1 404`

Instances: 5

### Solution



### Reference



#### CWE Id: [ 388 ](https://cwe.mitre.org/data/definitions/388.html)


#### WASC Id: 20

#### Source ID: 4

### [ Non-Storable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/echo/msg
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `500`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/1.2
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `PUT `
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unhealth
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `PUT `
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: ``
  * Attack: ``
  * Evidence: `PUT `

Instances: 4

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


* [ https://tools.ietf.org/html/rfc7234 ](https://tools.ietf.org/html/rfc7234)
* [ https://tools.ietf.org/html/rfc7231 ](https://tools.ietf.org/html/rfc7231)
* [ http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234) ](http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234))


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Re-examine Cache-control Directives ](https://www.zaproxy.org/docs/alerts/10015/)



##### Informational (Low)

### Description

The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content. For static assets like css, js, or image files this might be intended, however, the resources should be reviewed to ensure that no sensitive content will be cached.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: `public, max-age=0`
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/stress/resource/time/1.2/interval/1.2/cycles/1.2
  * Method: `PUT`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unhealth
  * Method: `PUT`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/unreadyfor/time
  * Method: `PUT`
  * Parameter: `Cache-Control`
  * Attack: ``
  * Evidence: ``

Instances: 8

### Solution

For secure content, ensure the cache-control HTTP header is set with "no-cache, no-store, must-revalidate". If an asset should be cached consider setting the directives "public, max-age, immutable".

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching)
* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control)
* [ https://grayduck.mn/2021/09/13/cache-control-recommendations/ ](https://grayduck.mn/2021/09/13/cache-control-recommendations/)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### WASC Id: 13

#### Source ID: 3

### [ Storable and Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.

* URL: https://api-service-edilsondmorais.cloud.okteto.net/celsius/1.2/fahrenheit
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/fahrenheit/1.2/celsius
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/health
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/ready
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
* URL: https://api-service-edilsondmorais.cloud.okteto.net/login
  * Method: `POST`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``

Instances: 5

### Solution

Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:
Cache-Control: no-cache, no-store, must-revalidate, private
Pragma: no-cache
Expires: 0
This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. 

### Reference


* [ https://tools.ietf.org/html/rfc7234 ](https://tools.ietf.org/html/rfc7234)
* [ https://tools.ietf.org/html/rfc7231 ](https://tools.ietf.org/html/rfc7231)
* [ http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234) ](http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234))


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3

### [ Storable but Non-Cacheable Content ](https://www.zaproxy.org/docs/alerts/10049/)



##### Informational (Medium)

### Description

The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. 

* URL: https://api-service-edilsondmorais.cloud.okteto.net/openapi.yaml
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `max-age=0`

Instances: 1

### Solution



### Reference


* [ https://tools.ietf.org/html/rfc7234 ](https://tools.ietf.org/html/rfc7234)
* [ https://tools.ietf.org/html/rfc7231 ](https://tools.ietf.org/html/rfc7231)
* [ http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234) ](http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234))


#### CWE Id: [ 524 ](https://cwe.mitre.org/data/definitions/524.html)


#### WASC Id: 13

#### Source ID: 3


