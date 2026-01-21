# 🍃 UnderLeaf Deployment guide

UnderLeaf has two modes of deployment:

- Standalone deployment
- Docker container

It is recommended to use the Standalone deployment if the server has more resources, but docker container for horizontal scaling. 

## Standalone deployment

- Clone the repository, 
- Install dependencies, MikTex, Pandoc and Git
- Install python dependencies from requirements.txt
- Host the flaskapp via any web server, including Apache mod-wsgi, or Gunicorn. It may be on windows or linux.
- Assign TLS and a domain name
- Create a Github OAuth App, allow R/W access to Public and Private repositories
- Use the domain name set above for the app homepage and `<THE DOMAIN NAME>/callback` for callback URI
- Get the client id and client secret
- Add environment variables `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`
- Add environment variable `REDIRECT_URI` with the callback URI.
- The system is now ready to use.

