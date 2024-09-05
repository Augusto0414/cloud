# cloud

docker login
docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=Cloud202402' -p 1433:1433 --name sql2022 -d mcr.microsoft.
com/mssql/server:2022-latest
docker commit abb056 cloud2024:v1  
docker tag cloud2024:v1 augusto04/cloud2024:v1.0.0                                    19 docker push augusto04/cloud2024:v1.0.0   

docker pull augusto04/cloud2024:v1.0.0

docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=Cloud202402' -p 1434:1433 --name sql2024 -d augusto04/cloud2024:v1.0.0