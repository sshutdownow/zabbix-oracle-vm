# zabbix-oracle-vm
Template Oracle VM (SNMP) for ZABBIX
==============

This template uses the SNMP to monitoring Oracle VM Server.


Items
-----
  * ovs Version
  * ovs Type
  * ovs Serverpool Name
  * ovs Manager UUID
  * ovs Free Memory
  * ovs Cluster Type
  * ovs Cluster Storage
  * ovs Cluster State
  * ovs Agent State

Triggers
--------
  * ovsClusterState changed.
  * ovsFreeMemory very low
  * ovsAgentState changed
  * ovsType changed
    
Graphs
------

  * no graphs

Installation
------------
1. Setup and startup SNMP on Oracle VM Server, please, use official documentation http://docs.oracle.com/cd/E64076_01/E64083/html/vmadm-config-snmp.html to do it.
2. Copy MIB file **/usr/share/snmp/mibs/ORACLE-OVS-MIB.txt** from OVS to zabbix host.
3. Restart zabbix.
4. Import **zbx-ovm-template.xml** file into Zabbix.
5. Associate **Template SNMP Oracle VM Server** template to the host. Set right value for {$SNMP_COMMUNITY} macros.

### Requirements

This template was tested for Zabbix 3.2.0 and higher.

### Copyright

  Copyright (c) 2017 Igor Popov

License
-------
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

### Authors

  Igor Popov
  (ipopovi |at| gmail |dot| com)
