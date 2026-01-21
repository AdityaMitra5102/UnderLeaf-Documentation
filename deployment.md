# 🍃 UnderLeaf Deployment guide

## Repository

UnderLeaf is available on Github [AdityaMitra5102/UnderLeaf](https://github.com/AdityaMitra5102/UnderLeaf), or the homepage is visible at [Homepage](https://underleaf.pages.dev)

UnderLeaf has three modes of deployment:

- Standalone deployment
- Docker container
- Managed service deployment

It is recommended to use the Standalone deployment if the server has more resources, but docker container for horizontal scaling. 

## Standalone deployment

- Clone the repository. 
- Install dependencies, MikTex, Pandoc and Git
- Install python dependencies from requirements.txt
- Host the flaskapp via any web server, including Apache mod-wsgi, or Gunicorn. It may be on windows or linux.
- Assign TLS and a domain name
- Create a Github OAuth App, allow R/W access to Public and Private repositories [Guide](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app)
- Use the domain name set above for the app homepage and `<THE DOMAIN NAME>/callback` for callback URI
- Get the client id and client secret
- Add environment variables `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`
- Add environment variable `REDIRECT_URI` with the callback URI.
- The system is now ready to use.

## Docker deployment

- Clone the repository.
- You may modify the exposed port on the dockerfile. 
- Build docker container from the dockerfile
- Assign TLS and a domain name
- Create a Github OAuth App, allow R/W access to Public and Private repositories [Guide](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app)
- Use the domain name set above for the app homepage and `<THE DOMAIN NAME>/callback` for callback URI
- Get the client id and client secret
- Add environment variables `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`
- Add environment variable `REDIRECT_URI` with the callback URI.
- Deploy the docker container.
- The system is now ready to use.

## Managed service deployment

The system can be deployed on various managed services like HF Spaces, Heroku, Render, and more. For managed services, it is recommended to use the Docker based deployment.



### Made by Cryptane (2026) 