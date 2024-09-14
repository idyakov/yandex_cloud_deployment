This code creates the following infrastructure:

Network and subnet for all resources.
Security group for access control.
Server for 1C with 16 GB RAM and 240 GB SSD disk.
Server for Bitrix24.
Separate web server for the "store".
PostgreSQL cluster for 1C and Bitrix databases.

Important points:

You will need to specify values for variables such as cloud_id, folder_id, ubuntu_image_id, public_key_path, and passwords for databases.
Resource settings (e.g., number of cores) may require adjustment depending on your specific needs.
The security group is configured to allow SSH access. For production environments, it is recommended to restrict access to only specific IP addresses.
For VPN setup, you will need additional configuration that can be added to this code.

To deploy this infrastructure:

Save this code in a file with a .tf extension.
Create a terraform.tfvars file and specify values for all variables in it.
Run the following commands:

Copyterraform init
terraform plan
terraform apply
After deployment, you will need to configure the servers, install the necessary software (1C, Bitrix24), and set up the database connection.
