# ai.cerb.CerbAuth
A Cerb API authentication extension for Paw.cloud on macOS

## Installation

1. In Paw, navigate to **Paw > Extensions > Manage Extensions**.

2. Copy the `Extensions Directory:` to the clipboard.

3. Open a Terminal.app window and navigate to that directory.
~~~
USERNAME=`whoami`
cd "/Users/${USERNAME}/Library/Containers/com.luckymarmot.Paw/Data/Library/Application Support/com.luckymarmot.Paw/Extensions"
~~~

4. Clone the project:
~~~
git clone https://github.com/cerb/ai.cerb.CerbAuth.git
~~~

5. In Paw's Manage Extensions popup, click the **Reload Installed Extensions** button.

![image](https://user-images.githubusercontent.com/18315304/28976253-07917520-78f2-11e7-9359-936253916686.png)

## Usage

You can use dynamic values to store Cerb's base URL, API access key, and API secret key.  Use "environments" to store those values for multiple Cerb installations (e.g. dev, staging, production).  Switch to **Environments** in the left sidebar and click **Manage>>**.

![image](https://user-images.githubusercontent.com/18315304/28976518-03b3c40c-78f3-11e7-82b9-885fd24d632c.png)

When creating a new HTTP request in Paw, add a `Cerb-Auth:` header to your request and use the **Cerb-Auth Signature Header** dynamic value provided by this extension.  Set the access and secret keys using the dynamic values you defined above.

![image](https://user-images.githubusercontent.com/18315304/28976355-607a6192-78f2-11e7-88ba-9fea47a6fa75.png)

Your requests should now be securely signed using your Cerb API credentials.
