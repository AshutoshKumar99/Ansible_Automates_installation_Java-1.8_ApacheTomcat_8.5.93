# Ansible Playbook: Setup Java and Tomcat Server

This Ansible playbook automates the installation and setup of Java 1.8 and Apache Tomcat 8.5.93 on target hosts. It is designed to work on all hosts specified in the inventory file.

## Prerequisites

Before running this playbook, ensure that you meet the following prerequisites:

- Ansible is installed on your control machine.
- Target hosts are accessible via SSH and have sudo privileges.

## Usage

Follow these steps to use the Ansible playbook:

1. Clone this repository or download the playbook file and inventory file to your Ansible control machine.

2. Edit the Ansible inventory file (`inventory`) to specify the target hosts where you want to set up Java and Tomcat. By default, the playbook uses all hosts, but you can modify it according to your needs.

3. Update the playbook variables in the `setup-java-tomcat.yml` file if necessary. These variables are defined under the `vars` section at the beginning of the playbook:

   - `tomcat_url`: The URL of the Tomcat package to download.
   - `tomcat_package`: The name of the Tomcat package (without the file extension).

4. Run the playbook using the following command:

   ```bash
   ansible-playbook -i inventory setup-java-tomcat.yml

Above command will execute the playbook on the specified target hosts.

Once the playbook run is completed successfully, you can access the Tomcat server's default page by opening your web browser and entering the following URL: http://Public_IPv4_address:8080

Make sure that port 8080 is open in the security group of the target machine to allow incoming web traffic.

Note: This playbook is designed for Debian-based systems (e.g., Ubuntu). You may need to modify it to work on other Linux distributions.
