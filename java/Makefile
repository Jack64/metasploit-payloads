ADB=${ANDROID_HOME}/platform-tools/adb
ANDROID=${ANDROID_HOME}/tools/android
PACKAGE=com.metasploit.stage

all: android java

android:
		mvn package -Dandroid.sdk.path=${ANDROID_HOME} -Dandroid.ndk.path=${ANDROID_NDK_HOME} -Dandroid.release=true

java:
		mvn package

clean:
		mvn clean

android-api:
		${ANDROID}
 
android-devices:
		${ADB} devices
 
avd:
		${ANDROID} avd
 
android-run:
		${ADB} shell am start -a android.intent.action.MAIN -n ${PACKAGE}/.MainActivity
 
android-shell:
		${ADB} shell

logcat:
		${ADB} logcat

