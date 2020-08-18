

# Frequently asked questions about Dynamics 365 Connected Store

## Are all IP cameras supported?

[See the list of supported cameras](install-cameras.md#supported-cameras).

## Can I use my existing analog CCTV cameras?

[See the list of supported cameras](install-cameras.md#supported-cameras).

## Can I reconfigure an existing skill zone if I have already reached the 10-zone limit?

Yes, if you need a new skill zone, you can reconfigure an existing zone. Zones can only be reconfigured for the same skill category, however. For example, you can reconfigure an existing Display Effectiveness zone as a new Display Effectiveness zone but not as a new Shopper Analytics or Queue Management zone. You can’t add more than 10 zones. 

>[!NOTE]
>When you rename a skill zone, all data associated with the previous zone name will be associated with the new zone name. 

## My Display Effectiveness skill zone has lower average dwell time than expected

Make sure to create the largest skill zone that you can, covering the specific floor area that you’re interested in, but **excluding** areas that you’re not interested in. This increases the accuracy of the data collected and prevents false positives from areas you don’t want to track. Be careful placing the corners of your polygon to make sure they’re not outside the area you want to track. 

[See tips for drawing skill zones](mobile-app-add-camera-skill-zones.md#tips-for-drawing-skill-zones).

