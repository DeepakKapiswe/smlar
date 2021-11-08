# mac Os installation help
you may encounter `postgres.h file not found` error on macOs 10.11+ 
we need a workaround for it

first of all we need to have the postgres installed on our machine
then we need to find the postgres.h file
generally you will find it inside (for version 12.X)

`/usr/local/Cellar/postgresql@12/12.X/include/postgresql/server`

once you discover the file we need to create a link first with the command 

`ln -s /usr/local/Cellar/postgresql@12/12.X/include/postgresql/server /usr/local/Cellar/postgresql@12/12.X/include/server`

remember to change the version number according to your version

just it then you are done

go and download the setup files by running 

#> git clone https://github.com/DeepakKapiswe/smlar.git

#> cd smlar

#> make USE_PGXS=1  && make USE_PGXS=1 install


then to test run `psql`

and do

#> $psql> CREATE EXTENSION smlar;

you are done !
enjoy !!
