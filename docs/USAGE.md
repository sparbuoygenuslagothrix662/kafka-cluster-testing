# Usage

Kafka Cluster Testing is distributed through the project website:
- https://kafkakombat.com/kafka-cluster-testing

Supported Apache Kafka versions: `3.0.0` through `4.2.0`.

## Minimal configuration idea

For most runs, the essential parameters are:
- bootstrap servers
- and, in Kerberos environments, principal and keytab

## Launching

```bash
./run.sh
./run.sh /path/to/kafka-cluster-testing.toml
```

## Report format

The utility produces a human-readable final report. Example:

![Kafka Cluster Testing report example](img/protocol.png)

```text
====================================================================
                 KAFKA CLUSTER TEST REPORT
====================================================================
RESULT:    OK
exitCode:  0
totalMs:   36449

Run:
  runId:      20260323-202126-kafka01.example.com
  startedAt:  2026-03-23T17:21:26.493501Z

Connection:
  protocol:   SASL_PLAINTEXT
  authMode:   auto
  bootstrap:
    - kafka01.example.com:9093
    - kafka02.example.com:9093
    - kafka03.example.com:9093

Test objects:
  consumerGroup:
    - kct.20260323-202126-kafka01.example.com
  topics:
    - kct.20260323-202126-kafka01.example.com.1
    - kct.20260323-202126-kafka01.example.com.2
    - kct.20260323-202126-kafka01.example.com.3

Steps:
  STATUS  STEP                 TOOK_MS  DETAILS
  ------  -------------------  -------  ----------------------------------------
  OK      AUTH_RESOLVE               0  mode=auto protocol=SASL_PLAINTEXT
                                        principal=kafka/client01.example.com@EXAMPLE.COM
                                        keytab=/etc/security/keytabs/kafka-client.keytab
  OK      CONNECT                  829  clusterId=INYl1VqlQx281uuTzdGDDw nodes=7
  OK      CREATE_TOPICS            902  created=[kct.20260323-202126-kafka01.example.com.1,
                                        kct.20260323-202126-kafka01.example.com.2,
                                        kct.20260323-202126-kafka01.example.com.3]
  OK      WAIT_TOPICS_READY         47  topicsReady=3
  OK      VALIDATE_TOPICS           11  partitions=1 replicationFactor=3
  OK      PRODUCE                 1763  topics=3 messagesPerTopic=5 total=15
  OK      WAIT_END_OFFSETS         160  endOffsetsReached>=5
  WARN    CONSUME_ASSIGN             0  assigned=[]
  SKIP    CONSUME                 5087  consumer_group_not_assigned_within_timeout: assigned=[] (non-fatal for
                                        cluster health)
  OK      GROUP_OFFSETS            220  reason=post_run mode=no_commits partitions=3;
                                        kct.20260323-202126-kafka01.example.com.1-0
                                        committed=-1 end=5 lag=-1;
                                        kct.20260323-202126-kafka01.example.com.2-0
                                        committed=-1 end=5 lag=-1;
                                        kct.20260323-202126-kafka01.example.com.3-0
                                        committed=-1 end=5 lag=-1 totalLag=0
  OK      CLEANUP_DELETE_TOPI      377  deleted=[kct.20260323-202126-kafka01.example.com.1,
                                        kct.20260323-202126-kafka01.example.com.2,
                                        kct.20260323-202126-kafka01.example.com.3]

====================================================================
```
