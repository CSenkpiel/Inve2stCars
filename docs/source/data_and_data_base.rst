.. _data_and_data_base:

Data and Database
=================

Data of cars and PV HSS
------------------------------
**Database**

The required data can be found in respective "inputs" folder of cars and PV HSS.
The foundation for the Inve2st Framework is a PostgreSQL Database. Queries have been defined to be able to use the framework as flexible as possible, e.g. for choosing different scenario_IDs for different kinds of data. All queries can be found in the modules.Queries (:ref:`API`).

For Passenger cars if the database is installed locally by the user, the database needs to be set as TRUE (self.db_on = True) within the module investment_options.
If the data from the database should be written into the input folder the function needs to be set as True (self.write_data = True)

For PV HSS if data base connection exists it must be set to True (databaseconnection = True), otherwise to False. 
If connection to database exists, new scenario name can be chosen. If not please use Scenario name 'Default_Data'.

**Equipment Data**

To be able to use the framework without the database, equipment data is provided for different scenarios and aggregation levels. 

The data provided are the results of the database queries for specific settings. For instance for the case of Passenger cars the provided data can be found in …\\sozio_e2s_model\\Inve2st_Passenger_car\\inputs. 


The names of the folders are a combination of the settings for the queries:
investment_option _ aggregation_level _ (tec_none) _attribute_scenario _ probability_calc_type_main_sub


One exemplary set of input files (as csv) is described here:


.. toctree::
   :maxdepth: 2
   :glob:

   data_inputs/*


**Database Credentials**

To be able to connect to database, the login credentials should be set in credentials.json.

.. code-block:: JSON

	{
		"dbname": "sozio_e2s",
		"host": "db_host", 
		"user": "my_user", 
		"password" : "mypassword"
	}

Data of Power-to-Gas
------------------------------

All required Data is located in the "inputs" folder.
