# Environment provisioning

* VM with consul
* Don't provide a consul config by default
* On the VM is the provisioning service which can provide provisioning information
  based on authenticated requests
  *
* Bootstrapping
  * Start provisioning VM first, no consul cluster will be found
  * Service starts and tries to contact other provisioning services on a given
    DNS address.
    * If there is no response it assumes the master provisioning role
      * Contact DNS server and register for the master provisioning role
      * Use the default environment configuration for consul
      * Do not restart consul until a consul server connects for the environment
    * If there is a response then connect to the other provisioning service
      * Get consul information
      * Update config files
      * Restart consul