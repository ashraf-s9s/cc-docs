ClusterControl UI provides a modern web user interface to visualize the cluster and perform tasks like backup scheduling, configuration changes, adding nodes, rolling upgrades, etc. It requires a MySQL database called 'dcps', to store cluster information, users, roles and settings. It interacts with CMON controller via remote procedure call (RPC) or REST API interface.

You can install the ClusterControl UI independently on another server by using a helper script, `install-cc-ui.sh` available from the [Severalnines download page](http://www.severalnines.com/downloads/cmon/). To install the UI:

```bash
$ wget http://www.severalnines.com/downloads/cmon/install-cc-ui.sh 
$ chmod u+x install-cc-ui.sh 
$ sudo ./install-cc-ui.sh
```
> *Omit 'sudo' if you are running as root*

The ClusterControl UI can connect to multiple CMON Controller servers (if they have installed the CMONAPI) and provides a centralized view of the entire database infrastructure. Users just need to register the CMONAPI token and URL for a specific cluster on the Cluster Registrations page.

The ClusterControl UI will load the cluster in the database cluster list, similar to the screenshot below:

<image\>

Similar to the CMONAPI, the ClusterControl UI is running on Apache and located under `/var/www/html/clustercontrol` (Redhat and Ubuntu >14.04) or `/var/www/clustercontrol` (Debian + Ubuntu <14.04). The web server must support rule-based rewrite engine and must be able to follow symlinks. 

ClusterControl UI page can be accessed through following URL: 

**http or https://<ClusterControl IP address or hostname\>/clustercontrol**

Please refer to ClusterControl User Guide for MySQL documentation page for more details on the functionality available through the ClusterControl UI.