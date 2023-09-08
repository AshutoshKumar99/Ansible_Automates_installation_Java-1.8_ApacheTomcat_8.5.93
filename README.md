# Ansible Playbook: Setup Java and Tomcat Server

This Ansible playbook automates the installation and setup of Java 1.8 and Apache Tomcat 8.5.93 on target hosts. It is designed to work on all hosts specified in the inventory file.

## Prerequisites

- Ansible installed on the control machine.
- Target hosts must be accessible via SSH with sudo privileges.

## Usage

1. Clone this repository or download the playbook file and inventory file to your Ansible control machine.

2. Edit the Ansible inventory file to specify the target hosts where you want to set up Java and Tomcat. By default, the playbook uses `all` hosts, but you can modify it according to your needs.

3. Update the playbook variables in the `setup-java-tomcat.yml` file if necessary. The variables are defined under the `vars` section at the beginning of the playbook:

   - `tomcat_url`: The URL of the Tomcat package to download.
   - `tomcat_package`: The name of the Tomcat package (without the file extension).

4. Run the playbook using the following command:

   ```bash
   ansible-playbook -i inventory setupTomcat_withVars.yml

5. Once playbook run is completed, open your broweser and hit Public IPv4 address:8080 to access tomcat default page

6. Make sure port 8080 is open in security group of target machine.
