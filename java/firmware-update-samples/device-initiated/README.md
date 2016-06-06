Firmware Update Samples

Following sample (present in this project) demonstrate the Device Initiated Firmware Update activity, through IBM Watson IoT Platform.

Prerequisites

git
maven
Java 7+

Register Device in IBM Watson IoT Platform

Follow the steps in this recipe to register your device in Watson IoT Platform if not registered already. And copy the registration details, like the following,

Organization-ID = [Your Organization ID]
Device-Type = [Your Device Type]
Device-ID = [Your Device ID]
Authentication-Method = token
Authentication-Token = [Your Device Token]
We need these details to connect the device to IBM Watson IoT Platform.

Build & Run the sample using Eclipse

You must have installed the Eclipse Maven plugin, to import & run the samples in eclipse. Go to the next step, if you want to run manually.

Building the sample - Required if you want to run the samples outside of Eclipse

Clone the device-samples project using git clone as follows,

git clone https://github.com/ibm-messaging/iot-device-samples.git

Navigate to the device-samples project,

cd iot-device-samples\java\device-samples

Run the maven build as follows,

mvn clean package

This will download the Java Client library for Watson IoT Platform, other required dependencies and starts the building process. Once built, the sample can be located in the target directory, for example, target\ibmiot-device-samples-0.0.1.jar.

Running the Registered device sample outside Eclipse

Navigate to target/classes directory and modify device.properties file with the registration details that you noted in the previous step.

Run the sample using the following command,

mvn exec:java -Dexec.mainClass="com.ibm.iotf.sample.client.device.DeviceEventPublishWithCounter"

Observe that the sample connects to Watson IoT Platform Registered service and publishes an event every second. You can view the same by going to the platform dashboard.
