# Redis_Kots
**Maifests YAML file's description**
*	application.yaml -- Contains metadata about the application
*	support-bundle.yaml -- Custom data to include in a support bundle
*	config.yaml  -- User facing config option to enable Ingress control
*	preflight.yaml -- preflight check for the application
*	replicated-app.yaml  --  Additional metadata lik status check, graph for the application
*	config-map.yaml  -- redis Config file map
*	deployment.yaml -- redis database deployment file
*	ingress.yaml  -- ingress for redisinsight deployment
*	redis-insight-deploy.yaml  -- redisinsight database deployment file
*	service-redis-insight.yaml -- Cluster IP service for redisinsight
*	service.yaml --  Cluster IP service for redis database

**Deployment**

**Existing Cluster:**
* curl https://kots.io/install | bash
* kubectl kots install qa-donkey/unstable

**Embedded Cluster:**
* curl -sSL https://k8s.kurl.sh/qa-donkey-unstable | sudo bash

**To access KOTS application**
* Once the application is deployed successfully. Use the http://NodeIP:8800 address to access KOTS GUI in your browser to view your deployment cluster configuration monitoring etc. 
* In the Dashboard under the Application you can click the Go to **Redis_Insight** to open a new browser for redis GUI manager or you can do by using NODEIP:80 to access the GUI. It doesnt need any password. 
* To add your redis DB  container to redis insight GUI. In your k8 control plane server run **kubectl get svc |grep redis-svc** to get the cluster ip and port and use that IP/port to add redis DB in the redis insight GUI.  
