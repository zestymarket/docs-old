---
description: These are the steps to integrate Zesty into a WebXR experience.
---

# WebXR Integration

## Before You Integrate

You will first need to create a Space NFT in order to get started checkout "For Creators" for more instructions.

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

## A-Frame

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-aframe-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/aframe-sdk'
```

Once installed, import the ZestyBanner component:

```
import * as Zesty from '@zestymarket/aframe-sdk';
```

#### Step 2

In the `<a-scene>`, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard" position="0 2 0"></a-entity>
```

To opt into enabling a beacon for your space, copy and paste:

```
<a-entity visible="true" zesty-banner="space: 0; creator: 0x0000000000000000000000000000000000000000; format: tall; style: standard; beacon: true" position="0 2 0"></a-entity>
```

## babylon.js

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-babylonjs-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/babylonjs-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/babylonjs-sdk';
```

#### Step 2

Make sure you have a reference to your scene and WebXRHelper (if applicable), then copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper);
```

Substitute variable names as needed. The last parameter for the WebXRHelper is optional.

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, scene, xrHelper, true);
```

## react-three-fiber

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-r3f-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/r3f-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/r3f-sdk';
```

#### Step 2

In your VR Canvas component, copy and paste:

```
<ZestyBanner space={'0'} creator={'0x0000000000000000000000000000000000000000'} format={'tall'} style={'standard'} position={[0, 2, 0]} />
```

To opt into enabling a beacon on your space, copy and paste:

```
<ZestyBanner space={'0'} creator={'0x0000000000000000000000000000000000000000'} format={'tall'} style={'standard'} beacon={true} position={[0, 2, 0]} />
```

## three.js

#### Step 1a

If you want to import the `<script>` tag, copy and paste this into the `<head>`:

```
<script src="https://ipfs.io/ipns/lib.zesty.market/zesty-threejs-sdk.js"></script>
```

#### Step 1b

If you are using it in an NPM project, install it like so:

```
npm install '@zestymarket/threejs-sdk'
```

Once installed, import the ZestyBanner component:

```
import ZestyBanner from '@zestymarket/threejs-sdk';
```

#### Step 2

In the your scene setup, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3);
scene.add(zestyBanner);
```

To opt into enabling a beacon on your space, copy and paste:

```
const zestyBanner = new ZestyBanner("0", "0x0000000000000000000000000000000000000000", "tall", "standard", 3, null, true);
scene.add(zestyBanner);
```

## Wonderland Engine

#### Step 1a

To just use the bundled file, download it by right-clicking this link and saving it into your project folder: [https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js](https://ipfs.io/ipns/lib.zesty.market/zesty-wonderland-sdk.js)

#### Step 1b

If you are using NPM in your Wonderland project, install it like so:

```
npm install '@zestymarket/wonderland-sdk'
```

#### Step 2

In your Wonderland project, open your Project Settings view and make sure that the SDK is being included in your JavaScript source paths.

#### Step 3

Create a new mesh, set its type to PrimitivePlane, and create a new material for it as well. Set the pipeline to either "Phong Opaque Textured" or "Flat Opaque Textured."

#### Step 4

Add the zesty-banner component to your mesh's object and fill in the following fields as such:

**creator**\
`0x0000000000000000000000000000000000000000`

**space**\
`0`

**format**\
`tall`

**style**\
`standard`

To opt into enabling a beacon on your space, simply check the "beacon" box on the zesty-banner component.