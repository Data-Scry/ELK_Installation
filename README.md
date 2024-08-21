---

# ELK Stack Setup Guide

This project contains scripts to automate the installation and configuration of the ELK (Elasticsearch, Logstash, Kibana) stack across multiple nodes. The setup includes separate nodes for Elasticsearch data and master roles, as well as Kibana.

## Repository Structure

- **install_elastic_search.sh**  
  A general script for installing Elasticsearch on a single node. This script is a template that you can modify based on the specific roles and configurations needed for different nodes.

- **install_elastic_search_data_1.sh**  
  Installs and configures Elasticsearch on `data-1` node, designated as a data node.

- **install_elastic_search_data_2.sh**  
  Installs and configures Elasticsearch on `data-2` node, designated as a data node.

- **install_elastic_search_master_1.sh**  
  Installs and configures Elasticsearch on `master-1` node, designated as a master node.

- **install_elastic_search_master_2.sh**  
  Installs and configures Elasticsearch on `master-2` node, designated as a master node.

- **install_kibana.sh**  
  Installs and configures Kibana on the designated node.

## Installation Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Execute the Installation Scripts**
   - For each node (master/data/Kibana), run the corresponding script on the respective machine. Make sure to give execution permissions to the scripts before running them:
     ```
     chmod +x install_elastic_search_data_1.sh
     ./install_elastic_search_data_1.sh
     ```

   - Follow the same steps for other nodes, replacing `install_elastic_search_data_1.sh` with the respective script.

3. **Post-Installation Configuration**
   - Ensure all nodes are properly connected within the Elasticsearch cluster. Check the Elasticsearch logs to verify the cluster's health and status.
   - Access Kibana through your browser at `http://<kibana-node-ip>:5601`.

## Notes

- This setup assumes that each script is executed on a separate node designated for that role.
- Elasticsearch installation script is the same for all node, we are just following our architecture.
- If needed, additional configurations, like setting up security (TLS, authentication), can be added based on your requirements.

## Contributing

If you encounter issues or have improvements to suggest, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to adjust the text based on any specific details or instructions relevant to your project.
