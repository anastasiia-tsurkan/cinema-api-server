﻿# Cinema API service
API service for cinema management written on DRF. With functionality for ordering tickets.

### Features:
- JWT authenticated
- Admin panel /admin/
- Documentation is located via /api/doc/swagger/
- Managing orders and tickets
- Media files on movie image (stored in docker )
- Creating movies with actors, genres
- Filtering movies and movie sessions
- Docker app starts only when db is available ( custom command via management/commands )

### Installing using GitHub:
- Install Postgres and create DB
```
git clone https://github.com/anastasiia-tsurkan/cinema-api-server.git
cd cinema-api-server
python3 -m venv venv
source venv/bin/activate # for Unix-based system
venv\Scripts\activate # for Windows
pip install -r requirements.txt
```
open .env.sample and change environment variables on yours! Rename the file from .env.sample to .env
```
python3 manage.py migrate
python3 manage.py runserver
```

### Run with Docker:
Docker should be installed
```
docker-compose build
docker-compose up
```
### Getting access instruction:
- Create a user via /api/user/register/
- Get user token via /api/user/token/
- Authorize with it on /api/doc/swagger/ OR
- Install ModHeader browser extension and create a Request header with the value ```Bearer <Your access tokekn>```
