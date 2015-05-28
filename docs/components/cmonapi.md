The CMONAPI is a RESTful interface, and exposes all ClusterControl functionality as well as monitoring data stored in the CMON DB. Each CMONAPI connects to one CMON DB instance. Several instances of the ClusterControl UI can connect to one CMONAPI as long as they utilize the correct CMONAPI token and URL. The CMON token is automatically generated during installation and is stored inside `config/bootstrap.php`.

By default, the CMONAPI is running on Apache and located under `/var/www/html/cmonapi` (Redhat) or `/var/www/cmonapi` (Debian). The value is relative to `wwwroot` value defined in CMON configuration file. The web server must support rule-based rewrite engine and able to follow symlinks.

The CMONAPI page can be accessed through following URL:

**http or https://<ClusterControl IP address or hostname\>/cmonapi**

Both ClusterControl CMONAPI and UI must be running on the same version to avoid misinterpretation of request and response data. For instance, ClusterControl UI version 1.2.5 needs to connect to the CMONAPI version 1.2.5.

> *We are gradually in the process of migrating all functionalities in REST API to RPC interface. Kindly expect the REST API will be deprecated in the near future.*