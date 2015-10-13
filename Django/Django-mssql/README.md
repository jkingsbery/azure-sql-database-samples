#Instructions



1. Install SQL Server Native client and SQL Server Management Studio

	a) Downlowd SQL Server Native client from the [here]() if you are on a x86 machine and [here]() if you are on a x64 machine.


	b) Download SQL Server Management Studio from [here]()      
		

	d) Install the SQL Server - Azure SQL DB adapter

        sudo pip install django-mssql


2. Git clone this project


        git clone https://github.com/Azure/azure-sql-database-samples.git


3. cd into the azure-sql-database-samples/Django/Django-mssql folder


4. Run setup.py. example: python setup.py yourserver.database.windows.net database username password


        python setup.py servername datbasename username password
        
        
   
5. Edit settings.py with your database settings. Make sure you change your credentials.
        
        
		DATABASES = {
		    'default': {
		        'NAME': 'yourdatabasename',
		        'ENGINE': 'sqlserver_ado',
		        'HOST': 'yourserver.database.windows.net',
		        'USER': 'yourusername',
		        'PASSWORD': 'password',
		        'OPTIONS': {
		            'provider' : 'SQLOLEDB'
		        }
		    }
		}


7. Run django migrations

        python manage.py migrate

7. Run your django app

        python manage.py runserver



	

