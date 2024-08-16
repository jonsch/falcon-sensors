# Falcon Sensors

### Intent
The falcon sensor downloads are not easily accessible for CURL based reqeusts, in order to make these available for the items in-need I've added the sensors relevant to the most widely accepted range of instances for Linux that is applicable to. Using the "RAW" URL in conjunction with CURL -L (which allows redirects) you can easily fetch these sensors for ```dpkg``` or ```yum``` based installs.

------

### Customer Id Configuration
After setup, do forget to configure your customer ID or token if you have, for customer ID the following command is applicable -- be sure to swap the placeholder ID with your ```actual customer id```

```sudo /opt/CrowdStrike/falconctl -s --cid="<<YOUR-CUSTOMER-ID>>"```

------

### After running Customer Configuration 
You'll want to check the status and/or start your sensor by doing the following:

**Amazon Linux Instance:**
```sudo systemctl status falcon-sensor``` and ```sudo systemctl start faclon-sensor```

**Ubuntu based instances 14x-22x (maximum compatibility)**
```sudo service falcon-sensor status``` and ```sudo service falcon-sensor start```
