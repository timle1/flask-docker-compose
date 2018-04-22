Different projects to play with:
## Test by unit test
```bash
cd docker-flask-compose-mysql
docker-compose build
docker-compose up
```
open another tab in terminal and run
```bash
docker exec -it counterapp_web_1 python tests.py
```

## Walkthrough via pdb
```bash
cd docker-flask-compose-mongodb
```
uncomment `import pdb; pdb.set_trace()` in `counter/views.py`
then in terminal
```bash
docker-compose build
docker-compose up -d db
docker-compose run --service-ports web
```
open browser and go to `http://localhost:5000/`
in terminal:
- next line, n
- continue to end, c