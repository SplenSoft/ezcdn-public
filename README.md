# Easy Content Delivery Network for Unity

![UnityAssetStoreBanner_EZCDN_card](https://github.com/SplenSoft/ezcdn-public/assets/4369778/4dd1520c-a52b-46be-8b42-5cb4d536d778)

An addressables-free suite that automatically handles the Unity Cloud Content Delivery API and packaging/deploying assetbundles while providing several tools to make asset management easy.

## Getting Started

You can [download the package on the Unity Asset Store](https://u3d.as/3eTj).

Here's a video tutorial: 

### Enabling Unity Cloud Content Delivery (CCD)
If you've already set up Unity Services with CCD in your project, you can skip to the next section.
* [Follow the steps here](https://docs.unity.com/ugs/manual/ccd/manual/UnityCCDDashboard) to enable CCD for your project. You can stop when you get to the 'Buckets' section.


### Install the package and configure
* [Get the package from the Unity Asset Store](https://u3d.as/3eTj) and install it into your project. If you need help with this, refer to the [official documentation](https://docs.unity3d.com/Manual/AssetPackagesPurchase.html)
* If you've installed the package correctly, there will be a new Menu at the top of the screen called SplenSoft, if it wasn't there already
* Using that menu, navigate to SplenSoft -> AssetBundles -> Settings

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/a1cfb5d0-4cb6-4f86-877e-ec55f8d867ff)

You need to fill out your Project ID and API key.

#### Get your project ID
* Go to the [Unity Cloud Dashboard](https://cloud.unity.com/) (and sign in, if needed) and click your project. The Project ID will be on that page

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/9e14c8d2-726a-4fc0-a908-d219c3ae1dc3)

#### Get your API key
* Go to the [Unity Cloud Dashboard Products Page](https://cloud.unity.com/home/products) and click Cloud Content Delivery
* On the left nav bar, click 'API Key'

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/dd4ea1ad-ac8a-480f-92e6-5dadf491de59)

* Back in the Unity project, click Manage Environments in the Asset Bundle Manager Settings window

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/3c9ebf80-c365-4fee-972f-7247330655e7)

#### Get your environment IDs
* Go to the [Unity Cloud Dashboard](https://cloud.unity.com/) (and sign in, if needed) and click your project
* Scroll down to the bottom of the page and click 'Environments'. Your keys will appear here

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/16b0fd7e-c99a-4a2a-938e-322c7321ef37)

The default environment is 'production', but you may add as many as you wish. Typically, developers use non-production environments for testing.
Once you're done entering your environments information, you may close the Environment Settings Window.

### Configure your runtimes

Back in the settings window, you can now configure all the runtimes your project will run on. Don't forget to include your editor for testing!

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/5c18fcfb-f0d6-4970-bd32-4cb712739509)

Generally speaking, the choices are mostly obvious for [Platform](https://docs.unity3d.com/ScriptReference/RuntimePlatform.html) and [Build Target](https://docs.unity3d.com/ScriptReference/BuildTarget.html).

### Generate Buckets
You can now click "Generate Buckets"! (Advanced users - if you've already set up buckets on the Unity Dashboard, you can check the 'Manually Enter Ids' button and use your existing Bucket ids. You can skip this section.)

The Unity CLI will now run in the background and set up your new buckets. Check the console log for any errors. If you've set everything up correctly, you should see your new Bucket Ids in the settings window.

![image](https://github.com/SplenSoft/ezcdn-public/assets/4369778/afc4da62-27a9-4cb8-91de-8de6059bc7b9)

That's it! EZ-CDN is now set up and is ready to use in your game design. You can go back and modify these settings at any time.

## Designing your game


