To start this project ,

1.You need to have python3.6 or Higher versions and pip3 (python3.6 version)

2.You need MongoDB 3.8 or higher 


3. run the following command -

	>>> pip3 install -r requirements.txt


4.CKYC2>CKYC>setings.py


5.DATABASE_LOCAL='ABC_DB'  // name of your database (example 'ABC_DB')

6.CENTRAL_SERVER='********'  // ip_address of ckyc-central-server which should be different ipaddress of client application

7.BANK_NAME='XYZ_Bank'  // name of your bank (example 'SBI','UBI')

8.CKYC_AUTH_TOKEN='***********************'  // give the token that is generated by central_server to you.


9.DATABASES = {
    'default': {
        ..........,
        'NAME': 'DATABASE_LOCAL',
        ...........,
    }
}


10. Download the policy file (.xml) from central server and copy at folder "/ckyc_client/xml_to_html/xml_file"
11. Open "ckyc_client/xml_to_html/py_file/field.py" and replace the  "field.xml" at line number 6 with the policy file generated in step 10
    Repeat the same in "ckyc_client/xml_to_html/py_file/update.py" file.

12.now do migrations using following :

	>>> python3 manage.py makemigrations 
	>>> python3 manage.py migrate

11.Then goto project folder and run the server using following cmd
	>>> python3 manage.py runserver 0:8000

