CX Core 
B2C & B2B Accelerators with OMS (formerly b2c_b2b_acc_oms). For Kyma integration + ApiRegistry, event sending is turned off by default by apiregistryservices.events.exporting=false property. Optionally and before initialization, deployment.api.endpoint property should be set to a server url reachable by kyma instead of https://localhost:9002.
 Platform Setup:
   1. Setup platform using command ./install.sh -r cx-sapmart setup -A initAdminPassword=nimda
   2. Initialize platform using command ./install.sh -r cx-sapmart initialize -A initAdminPassword=nimda
   3. Start platform using command ./install.sh -r cx-sapmart start
