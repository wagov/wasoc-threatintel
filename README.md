# wasoc-tip
OpenCTI build for WA SOC threat intel

OpenCTI compose file sourced from [OpenCTI docker swarm deployment](https://github.com/OpenCTI-Platform/docker#docker-swarm)

## nginx basic auth proxy

For Microsoft Sentinel to access OpenCTI TAXII feeds, a proxy needs to sit in front of OpenCTI Taxii feed and do the header based authentication, as sentinel tries to basic auth via http header which OpenCTI doesn't support. This can be worked around with basic auth on a proxy in front of OpenCTI. Simplest way to get this going is just a container pointing to some local config.

The opencti.conf file (get the bearer token from opencti profile page)
```
server {
	listen 8090 default_server;
	listen [::]:8090 default_server;

	location / {
		proxy_pass http://localhost:8080;
		proxy_set_header Host $host;
		proxy_set_header Authorization "Bearer ...";
		auth_basic "login required";
		auth_basic_user_file /etc/nginx/conf.d/opencti.htpasswd; 
	}
}
```
The password file was created using htpasswd under linux like `htpasswd -c opencti.htpasswd opencti`