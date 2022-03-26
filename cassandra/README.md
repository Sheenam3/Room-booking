Most applications deployed to Kubernetes should be cloud native and rely on external resources for their data (or state). However since Cassandra is a database we can use Stateful sets and Persistent Volumes to ensure resiliency in our database.

