# Crear Azure ETL para Covid

<img src="assets/Azure_Datafactory_ETL.png"><br><br>

# Servicios Utilizados
<img src="assets/resourceGroupWithResources.png"><br><br>

# Pipeline
<img src="assets/pipelineIngestionCovid.png"><br><br>

# Activities
<h3 style="margin-left: 1em;">1. <strong>Validation</strong> : Valida la existencia de un archivo o carpeta en un origen de datos antes de continuar con el pipeline.</h3>
<img src="assets/activity_validation.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">2. <strong>Get Metadata</strong> : Obtiene detalle de un archivo o carpeta, como su tamaño, si existe, columnas, etc.</h3>
<img src="assets/activity_getMetadata.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">3. <strong>If Condition</strong> : Permite realizar operaciones condicionales dentro de un pipeline.</h3>
<img src="assets/activity_condition_1.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_condition_2.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">4. <strong>Notebook (BronzeToSilver)</strong> : Realiza proceso de tranformacion de la capa bronze hacia silver, en la pestaña <strong>"Settings"</strong> asignamos la ruta del notebook.</h3>
<img src="assets/activity_notebook_silver.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">5. <strong>Notebook (SilverToGold)</strong> : Realiza proceso de tranformacion de la capa silver hacia gold, en la pestaña <strong>"Settings"</strong> asignamos la ruta del notebook.</h3>
<img src="assets/activity_notebook_gold.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">6. <strong>Notebook (ProcessAndML)</strong> : Realiza el proceso de entrenamiento con ML, en la pestaña  <strong>"Settings"</strong> asignamos la ruta del notebook.</h3>
<img src="assets/activity_notebook_ml.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">7. <strong>CopyDataToDatawarehouse</strong> : Almacena los datos estructurados en datawarehouse, para este caso una base de datos.</h3>
<img src="assets/activity_asql_1.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_asql_2.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_asql_3.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_asql_4.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;">8. <strong>Visualización PowerBI</strong> : Permite visualizar los datos en un reporte.</h3>
<img src="assets/activity_apb_1.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_2.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_3.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_4.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_5.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_6.png" style="width: 80%; height: auto;"><br>
<img src="assets/activity_apb_7.png" style="width: 80%; height: auto;"><br>

<br><br>

# Adicional
<h3 style="margin-left: 1em;"><strong>Key Vault</strong> : Creamos los secretos que seran utilizados en los linkedservices.</h3>
<img src="assets/keyvault_1.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;"><strong>Triggers</strong> : Creamos un trigger, con una fecha y hora especifica que ejecutará automaticamente.</h3>
<img src="assets/trigger_1.png" style="width: 80%; height: auto;"><br>
<img src="assets/trigger_2.png" style="width: 80%; height: auto;"><br>

<h3 style="margin-left: 1em;"><strong>Insights</strong> : Creamos una alerta en monitorización datafactory.</h3>
<img src="assets/alert_1.png" style="width: 80%; height: auto;"><br>
<img src="assets/alert_2.png" style="width: 80%; height: auto;"><br>
<img src="assets/alert_3.png" style="width: 80%; height: auto;"><br>
<img src="assets/alert_4.png" style="width: 80%; height: auto;"><br>
<img src="assets/alert_5.png" style="width: 80%; height: auto;"><br>
<h3 style="margin-left: 1em;">- Si nos aparece el siguiente error debemos registrar insights a nuestra subscription.</h3>
<img src="assets/alert_6.png" style="width: 80%; height: auto;"><br>
<h3 style="margin-left: 1em;">- Si en el proceso de la condicion falla, enviará un correo.</h3>
<img src="assets/alert_7.png" style="width: 80%; height: auto;"><br>
<img src="assets/alert_8.png" style="width: 80%; height: auto;"><br>

<br>
<h3 style="margin-left: 1em;"><strong>Cost Mangement</strong></h3>
<img src="assets/cost_management_1.png" style="width: 80%; height: auto;"><br>