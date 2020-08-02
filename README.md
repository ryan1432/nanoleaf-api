<h2 align="Center">  NanoLeaf <<i>Local API</i>>  </h2>

## Table of Contents 
 1. Getting Started 
 2. Setting your Environment 
 3. File Content 


        .
        ├── ...
        ├── NanoLeaf Getting Started    # Folder
        │   ├── Add an API user         # POST | Create an API user
        ├── Basic                       # Folder
        │   └── Get controller info     # GET | Get controller info
        │   └── Turn on                 # PUT | Turn NanoLeaf on
        │   └── Turn off                # PUT | Turn NanoLeaf off
        │   └── List Effects            # GET | List installed effects
        │   └── Activte Effect          # PUT | Activate an effect
        │   └── Identify                # PUT | Identify your NanoLeaf
        ├── ...
        ├── Auth                       # Folder (coming soon)
        ├── State                      # Folder (coming soon)
        ├── Effects                    # Folder (coming soon)
        ├── Layout                     # Folder (coming soon)
        ├── Rhythm                     # Folder (coming soon)
        └── ...




## Getting Started
 - Import NanoLeaf JSON file 
 - Find the IP address of your NanoLeaf (MAC Address will always start with ```00:55:da``` ) and update your environment.
 - Add an api user

 ### Add an API User
    A user is authorized to access the OpenAPI if they can demonstrate physical access of the Light Panels. 

    ### Generate an authorization token

    1. On the Nanoleaf controller, hold the on-off button for 5-7 seconds until the LED starts flashing in a pattern.
    2. From the Postman app or your own app, send a POST request to the authorization endpoint within 30 seconds of activating pairing, like this (substituting the IP address and port for your central controller):

    `http://xx.xx.xx.xx:16021/api/v1/new`

    > **Finding your IP:** The IP address of your Nanoleaf can be found using your router (MAC Address will always start with `00:55:da` ). Once you have the Nanoleaf connected to your WiFi, go to your router webpage and browse the devices connected to your network. Once you find your Nanoleaf, you can see the IP assigned to the device. 

    > Remember if you're accessing the Nanoleaf at a local IP address, like when your router assigns a local IP address to the connected devices, both the Nanoleaf device and the client accessing the Nanoleaf (Postman) must be on the same local network. For example, both the Nanoleaf and laptop with Postman should be connected to the same WiFi network.

    The result returned will be a 32-character authorization token that you will use in all of your subsequent calls.


    **Note:** In this request's test script, the auth token value will be set as an environment variable called `authToken`. If you already have an authorization token that you'd like to use, update your environment with the token.

     

## Setting your Environment 
 - These examples will be from Insomnia API
 - Base Environment ```{"ipAddress":"xx.xx.xx.xxL18021","authToken":"XXXXX"} ```


<h2 align="Center">  More updates coming soon </h2>
