# Serve your application securely with nginx+modsecurity

1. Start a centos8 container

2. Compile nginx with modsecurity and Use all Core Rule Set(crs)

3. Serve nginx with https protocol

4. Configure all of things using ansible playbook.Such as nginx.conf or modsecurity.conf.

5. Use 3 of least [OWASP TOP 10](#https://owasp.org/Top10/) for testing on your application.

> Ps: Use our [flask web application project](#https://github.com/fatihusta/intern-projects/tree/main/flask-web-app-project) for this