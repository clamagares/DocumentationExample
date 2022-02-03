![nrc](https://user-images.githubusercontent.com/55964909/125176016-409c4e80-e19e-11eb-8ef1-8315dc6e3e34.jpg)

# [Core](https://nrc-no.github.io/core/)
A case management tool for the humanitarian sector - keep track of beneficiaries and services.

- [ARCHITECTURE](ARCHITECTURE.md): get to know the repository content

## Getting started:

Docker and kuberentes Files for the Twilio Survey app.

### Setup

#### 1. Construct Image

for construct a image
```bash
cd /latam-twilio-survey
docker build -f TwilioEncuestas.DockerFile -t <name (latam-twilio-survey)> .
```

**note**, all the following commands are run from the `api` directory, unless otherwise specified


#### 2. Run Image (you only have to do this once)

```bash
docker-compose up -d
```

### Endpoints:
 - webService: [http://localhost:8381](http://localhost:9000)
 

## Running tests

-- For Test the following GET Request returns the server Hour 
 ```bash
curl http://localhost:8381/config/horas/
 ```

With the git hook installed, tests will run locally automatically before every push. If any tests fail, the push operation will be aborted.

You can run tests manually: with `make test-iam`, `make test-cms`, `make test-attachments` and `make test-e2e`

Or via the run configurations available in Goland.

