---
type: page
title: Estimated Self-sufficiency Period
listed: true
slug: test
---published

**_Calculating Battery Capacity_**

To calculate the minimum required battery capacity, we will need to first set the number of days of autonomy. This simply means the number of days that the gateway can be powered without sunshine and just from the battery capacity alone. For most locations, the maximum number of continuous raining days is three so it is a good rule of thumb to set the days of autonomy to three.

Another specification that needs to be determined is the Depth of Discharge (DoD). It is not recommended to discharge 100% of the batteries’ total capacity as it drastically reduces its lifetime. This is why battery manufacturers recommend a certain DoD for their batteries. For example, a 100Ah battery with 80% recommended DoD can only use 80Ah or 80% of its total capacity on one cycle. Choosing a lower depth of discharge will allow the battery to last longer, but it will require you to have a larger battery capacity. For example, a battery bank may have 10,000 cycles at 20% DoD but only 800 cycles at 90% DoD. Unless otherwise specified by the battery manufacturer, it has been shown that using 80% DoD is the best in terms of maximizing the battery capacity and prolonging the battery’s lifetime.

The __LoRaWAN**®** Gateway__ for this example consumes 500mA at 12V. This means that its energy consumption is:

_0.5Ah at 12V per hour_

For one full day, it will need:

_24hrs x 0.5Ah = 12Ah at 12V_

Since we will need 3 days of autonomy, the required energy becomes:

_12Ah at 12V x  3 days = 36Ah at 12V_

Taking into account the depth of discharge, the minimum required battery capacity becomes:

_36Ah/0.8 = 45Ah at 12V = 540Wh_

**_Calculating Solar Panel Rating_**

Since this set-up makes use of a solar panel, it is a good practice to also know the rating of the solar panel you are going to use.

The amount of energy that a solar panel can produce depends on the irradiance (energy from the sun per unit area) on your specific location. To know this value for your location, you can go to the [NASA POWER Data Access Viewer](https://power.larc.nasa.gov/data-access-viewer/) website (Prediction of Worldwide Energy Resources) website. Set up the values in the window as follows:

1. Choose User Community - **SSE-Renewable Energy**
2. Choose a Temporal Average - **Climatology**
3. Enter Lat/Lon or Add a Pint to Map - **Example value in Figure 1**
4. Select Time Extent - **Leave as is**
5. Select Output File Format - **CSV for example**
6. Select Parameters - **Tilted Solar Panel**
7. Submit and Process - **Submit**

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1589496714\/29516\/n2lvxt3z9a6la6pxjnnd.jpg",
        "mode": "responsive",
        "width": 3829,
        "height": 1945,
        "caption": "Figure 1: NASA tool configuration"
    }
}]$

Once you click "Submit" you will be presented with the window in Figure 2. Select "Solar Irradiance for Equatorial Facing Tilted Surfaces (Set of Surfaces)" from the drop down menu and click "CSV". You file should start downloading.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1589496834\/29516\/sn2vqzpcnwi5m9mr27wr.jpg",
        "mode": "responsive",
        "width": 975,
        "height": 1611,
        "caption": null
    }
}]$

To maximize the energy produced by the solar panel, it must be pointed to the Equator (South for locations in the Northern Hemisphere and vice versa) at a tilt angle that is equal to your location’s latitude. The NASA Power website shows the different irradiance levels for different tilt angles of your solar panels. For this example, let us assume that we have an irradiance of 5.0 based on our tilt angle.

We will need to set the worst-case scenario where we have the minimum number of sunshine days per our maximum number of continuous rainy days. To maximize our system’s reliability, we can set 2 sunshine days per 3 continuous rainy days. This means that in these 2 sunshine days, our solar panel must be able to produce energy for our gateway and fully charge the batteries. The total of this energy is equal to:

_432Wh (36Ah at 12V) + 288Wh (0.5Ah at 12V for 2 days) = 720Wh_

_720Wh/5 (irradiance)/0.8 (correction for efficiency) = 180W_

Since this is for 2 days:

**_180W/2 = 90W ≈ 100W_**

