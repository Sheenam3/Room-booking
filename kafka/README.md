# Zookeeper
The manifest creates an ensemble of three ZooKeeper servers using a StatefulSet, zk; a Headless Service, zk-hs, to control the domain of the ensemble; a Service, zk-cs, that clients can use to connect to the ready ZooKeeper instances; and a PodDisruptionBugdet, zk-pdb, that allows for one planned disruption. (Note that while this ensemble is suitable for demonstration purposes, it isn’t sized correctly for production use.)



# Kafka Cluster
The manifest creates a three broker cluster using the kafka StatefulSet, a Headless Service, kafka-hs, to control the domain of the brokers; and a PodDisruptionBudget, kafka-pdb, that allows for one planned disruption. The brokers are configured to use the ZooKeeper ensemble we created above by connecting through the zk-cs Service. As with the ZooKeeper ensemble deployed above, this Kafka cluster is fine for demonstration purposes, but it’s probably not sized correctly for production use.

