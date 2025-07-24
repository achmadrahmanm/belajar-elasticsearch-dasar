# Elasticsearch (ELK) Implementation for PropNex

## Project Overview
- **ELK Stack URL**: [https://kibana.propnex.id](https://kibana.propnex.id)
- **Production Application**: [PropNexPlus.com](https://propnexplus.com)
- **Implementation Date**: [Insert Date]
- **Maintained by**: Admin & IT Staff only

## Key Implementations

### 1. Elasticsearch Configuration
- Configured snapshot repositories with proper filesystem permissions
- Implemented secure backup strategies
- Resolved repository access issues (`repository_verification_exception`)

### 2. System Administration
```bash

# Commands mastered for administration:
sudo chown -R elasticsearch:elasticsearch /mnt/backup-hdd/backup-nvme/elastic/first_backup
sudo chmod -R 755 /mnt/backup-hdd/backup-nvme/elastic/first_backup
sudo systemctl restart elasticsearch
curl -X POST "localhost:9200/_snapshot/first_backup/_verify"
