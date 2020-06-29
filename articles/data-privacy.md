

# Data and Privacy

Microsoft Dynamic 365 Connected Store has three components, and each is designed with compliance, security, and privacy in mind. 
￼
**- Connected Store Edge  gateway** – A managed Azure Stack Edge gateway installed in the retail store that runs computer vision AI model(s) to convert camera streams from 
existing or new cameras into observational data sent to the cloud.

**- Connected Store Cloud and Web application** – A  Software-as-a-service (SaaS) cloud service running on Azure and Connected Store web application that correlates 
observational data from the Connected Store Edge  gateway with business data to provide insights and recommended actions for the retailer.

**- Connected Store Mobile application** – A mobile app to provide customers a consumer-class onboarding experience to setup the edge gateway and assist customers’ 
configuration of cameras to deliver camera feed to the edge gateway.

The Connected Store Edge  gateway processes video data from the in-store camera locally on the device, makes AI data inferences without identifying or tracking 
individuals to generate observational data. The edge gateway sends the data inferences to the Connected Store Cloud so that the observational data can be correlated 
with the retailer’s business data (e.g. store business hours, camera zone name) to generate actionable insights regarding retail operations.  Customers can then use the 
Connected Store Web application to view this data stored in the Connected Store Cloud for shopping analytics, display effectiveness and queue management insights.

## What data does Connected Store process?  

The following types of data are processed to provide the service:
 
**On the Connected Store Edge Gateway in the retail store:**

**- Video stream** – The video stream from customers’ in-store cameras is processed in memory, in real time, on the Connected Store Edge gateway to generate Inference Data. 
This data is not stored on the gateway, nor sent to Microsoft’s cloud.

**- Inference data** – This is event data output by containerized AI models that describe an inferred event. Event data includes data such as a time stamp, notation about the 
type of event (e.g. "entry" or "exit" into a frame), a rectangle “bounding box” that coordinates the area tracked within the camera frame, a confidence  score for the 
detection, and a pseudonymous Identifier that matches each paired entry & exit event. 

**- Connected Store Edge gateway configuration information.** This sets up camera connections and customizes the parameters for the AI model inferences.  To configure cameras, 
the Connected Store mobile application uses a camera snapshot.  These images are passed through to the mobile app and not cached. The configuration data also includes: data 
relating to the Connected Store Edge gateway appliance (e.g., name, IP address); a list of customer-managed cameras on the store’s private network which send video data to the 
edge gateway (e.g., name, IP address, MAC addresses, credentials); camera’s skill and zone configuration parameters for the AI models (e.g., camera zone name and coordinates; 
AI skill model to use for a specific camera zone).  

**- Telemetry for monitoring edge health.** Data for operating the service is collected from the edge appliance and containers such as error codes, Edge gateway status, 
Container health (CPU, Memory, etc.).
 
**In the Connected Store Cloud and Web Application**

- Inference data – The inference data output by AI edge models and described above is sent to the Connected Store cloud for further processing.

- Observational data - The inference data is aggregated and is used in reporting that is available to customers through the web application. Observational data may include: 

   - Time stamp - summarized by hour or other time interval
   
   - Value - the number over that hour

   - Measurement type - entries, exists, dwell time, occupancy

   - Aggregation Type - total, average, maximum, minimum

   - Zone - Front Entrance, Isle 1 display, etc.

Order information – This is the information tied to the customer’s account and provides details around the Edge hardware ordered and where it was shipped. This includes 
data points such as Company name, Shipping address, Shipping status info, Contact info, and Device serial number.  

- Telemetry. This is information about the health of the Edge gateway, the Cloud Service, and the Connected Store mobile application.
 
**In the mobile application**

- Edge gateway configuration information - *described above*

- Store configuration - *described above*

## How does Connected Store process data?

Microsoft Dynamics 365 Connected Store processes data as instructed by the customer to provide the Connected Store solution.  

Customers use the Connected Store Mobile app to configure camera streams to send to the Connected Store Edge  gateway for processing and define the zone view and AI 
skills (e.g., end cap display effectiveness) to apply for each camera. After the Edge gateway configuration is completed, customers can stream their video data directly 
to the Connected Store Edge  gateway on customers’ premises for AI inferencing. 

The AI inferencing does not require any sound recording and the video feed from customers’ cameras only includes image data. No video data leaves the premises and no 
video data is stored on the edge gateway disk or sent to the Microsoft’s cloud. The AI data inferencing is performed locally in-memory on the Connected Store Edge  
Gateway. No video footage is stored on the edge gateway and the data inferencing occurs near real-time. 

The AI models running on customers’ premises are not trained with the video data unless a customer specifically instructs Microsoft to do so and provides Microsoft 
additional access to its video feed to enhance the underlying models.

The AI models detect and track people’s movements in the video feed based on algorithms that identify the presence of one or more humans and generates events when a person 
moves in or out of designated zones in the camera’s field of view and outputs the coordinates of the person’s body bounding box.  For each bounding box movement detected in a 
camera zone, the AI model outputs inference data including the following:

- Bounding box coordinates of person’s body

- Event type (e.g. zone entry or exit, directional line crossing)

- Pseudonymous identifier to track bounding box 

- Confidence score for the detection

This inferenced data is sent to Microsoft’s cloud for further processing and aggregation with other customer data and configuration data to deliver insights that are 
accessible via the Connected Store web application.  

Customer data processed in the Microsoft cloud is used to provide you the Connected Store service, including by providing insights about your retail locations, and also to 
improve and troubleshoot the Connected Store Cloud  service and other operations incident to delivering the services (for example, managing your account, internal 
reporting, and improving core functionality such as privacy and accessibility).
