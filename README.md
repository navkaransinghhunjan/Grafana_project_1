A simple demo project that sets up a complete monitoring and visualization stack using Prometheus, Grafana, and Node Exporter (for system metrics). You'll monitor the metrics of your system and visualize them in Grafana.
Steps to Create the Demo Project

Prerequisites:
        Install Docker and Docker Compose.

Project Structure:


    grafana-demo/
    │
    ├── docker-compose.yml
    ├── prometheus/
    │   └── prometheus.yml
    └── grafana/
        └── dashboards/
            └── system_metrics.json

  Step 1: Define docker-compose.yml

This file sets up Prometheus, Node Exporter, and Grafana as services.


 Step 2: Configure Prometheus (prometheus/prometheus.yml)

Prometheus needs to scrape metrics from Node Exporter, so configure it as follows:

 Step 3: Run the Project

    docker-compose up -d
 
 Step 4: Create dashboard


1. Open Grafana: Open your Grafana instance in a browser (e.g., http://localhost:3000).

2. Go to Dashboards: On the left-hand sidebar, click Dashboards (the four squares icon), then click on Manage.

3.  Click Import: In the top right corner, click the Import button.

4.  Upload the Dashboard JSON File:
        If you have a JSON file with the dashboard's configuration, click on Upload JSON file and select the file from your local machine.
        Alternatively, you can paste the JSON directly into the Paste JSON text box.
        If you have a dashboard ID from Grafana's dashboard repository, you can paste it into the Grafana.com Dashboard field.

5. Set Prometheus as Data Source: If the dashboard uses Prometheus as the data source, ensure that you select your Prometheus instance as the data source when prompted.

6. Click Import: After configuring the data source, click Import to complete the process.

Explore and Enjoy
--------------------------------------------------------------------------------------------END-------------------------------------------------------------------------------------------------------
