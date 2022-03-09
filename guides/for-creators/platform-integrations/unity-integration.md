# Unity Integration

Repository: [https://github.com/zestymarket/sdk/tree/main/unity](https://github.com/zestymarket/sdk/tree/main/unity)

## Before You Integrate

You will first need to create a Space NFT in order to get started checkout "For Creators" for more instructions.

{% content-ref url="../create-space.md" %}
[.](./)
{% endcontent-ref %}

## Instructions

**Step 1**

Download the [zesty-unity-sdk package](https://ipfs.io/ipns/lib.zesty.market/zesty-unity-sdk.unitypackage).

**Step 2**

Open your Unity project and import the package through `Assets > Import Package > Custom Package`.

**Step 3**

Add the ZestySDK prefab to your hierarchy.

**Step 4**

Right click the "Banner" in your hierarchy, click properties and configure your banner.

![](https://i.imgur.com/5rd6OnP.png)

Add the Banner prefab and configure the space ID, creator ID, format, and style based on your space details from the Zesty marketplace.

To opt into enabling a beacon on your space, simply check the "Enable Beacon" box on the zesty-banner component. This will allow you to see analytics like space visits and banner clicks within the Zesty app.
