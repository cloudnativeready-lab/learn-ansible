# Learn Ansible 

## 🎯 Project Overview

This repository is designed to help you learn Ansible automation using a microservices-based application that consists of multiple components, making it an excellent candidate for learning infrastructure automation with Ansible.

## 🚀 Learning Objectives

By the end of this course, you will be able to:

- **Understand Ansible Fundamentals**: Playbooks, roles, inventories, and variables
- **Automate Infrastructure**: Deploy and configure servers automatically
- **Manage Multi-Tier Applications**: Handle complex application deployments
- **Implement Best Practices**: Use roles, templates, and proper organization
- **Troubleshoot and Debug**: Learn effective debugging techniques
- **Scale Automation**: Apply patterns for large-scale deployments

## 📋 Prerequisites

Before starting this course, ensure you have:

- Basic Linux command-line knowledge
- Understanding of web applications and microservices
- Familiarity with YAML syntax
- A Linux environment (Ubuntu/CentOS/RHEL recommended)
- At least 4GB RAM and 20GB free disk space


## 🎓 Learning Path

### Phase 1: Ansible Basics (Week 1)
1. **Environment Setup**
   - Install Ansible
   - Configure SSH keys
   - Create test environment

2. **Core Concepts**
   - Inventory management
   - Ad-hoc commands
   - Basic playbook structure
   - Variables and facts

### Phase 2: Playbook Development (Week 2)
1. **Common Server Setup**
   - User management
   - Package installation
   - Security hardening
   - Service configuration

2. **Role Development**
   - Role structure
   - Dependencies
   - Handlers
   - Conditionals

### Phase 3: Application Deployment (Week 3)
1. **Database Layer**
   - MongoDB installation
   - Redis configuration
   - Data persistence

2. **Application Services**
   - Node.js applications
   - Java applications
   - Python applications
   - Go applications

### Phase 4: Advanced Topics (Week 4)
1. **Templates and Variables**
   - Jinja2 templating
   - Dynamic configurations
   - Environment-specific settings

2. **Testing and Validation**
   - Syntax checking
   - Dry-run mode
   - Integration testing

## 🛠️ Quick Start

### 1. Clone the Repository
```bash
git clone <repository-url>
cd learn-ansible
```

### 2. Set Up Your Environment
```bash
# Install Ansible
sudo apt update
sudo apt install ansible -y

# Verify installation
ansible --version
```

### 3. Configure Inventory
```bash
# Edit inventory/hosts
vim inventory/hosts

# Add your target servers
[webservers]
web1 ansible_host=192.168.1.10
web2 ansible_host=192.168.1.11

[databases]
db1 ansible_host=192.168.1.20
```

### 4. Test Connection
```bash
# Test SSH connectivity
ansible all -m ping

# Check facts
ansible all -m setup
```

### 5. Run Your First Playbook
```bash
# Run common setup
ansible-playbook -i inventory/hosts playbooks/common.yml

# Deploy RoboShop
ansible-playbook -i inventory/hosts playbooks/robshop.yml
```

## 📚 Key Ansible Concepts Covered

### 1. **Inventory Management**
- Static vs dynamic inventories
- Group organization
- Variable assignment

### 2. **Playbooks**
- YAML syntax
- Task organization
- Error handling
- Conditionals and loops

### 3. **Roles**
- Role structure
- Dependencies
- Default variables
- Handlers

### 4. **Templates**
- Jinja2 syntax
- Variable substitution
- Conditional rendering
- File management

### 5. **Variables**
- Global variables
- Host variables
- Group variables
- Facts and custom facts

## 🔧 Common Commands

```bash
# Check syntax
ansible-playbook --syntax-check playbook.yml

# Dry run
ansible-playbook --check playbook.yml

# Verbose output
ansible-playbook -v playbook.yml

# Limit to specific hosts
ansible-playbook --limit=webservers playbook.yml

# Run with extra variables
ansible-playbook -e "variable=value" playbook.yml
```

## 🐛 Troubleshooting

### Common Issues:
1. **SSH Connection Problems**
   - Verify SSH keys are properly configured
   - Check firewall settings
   - Ensure target user has sudo privileges

2. **Permission Errors**
   - Use `become: yes` for privileged tasks
   - Verify sudo configuration
   - Check file permissions

3. **Variable Issues**
   - Use `ansible-playbook -v` for verbose output
   - Check variable precedence
   - Verify variable syntax

## 📖 Additional Resources

- [Ansible Official Documentation](https://docs.ansible.com/)
- [Ansible Best Practices](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)
- [Jinja2 Template Designer Documentation](https://jinja.palletsprojects.com/)
- [YAML Syntax Guide](https://yaml.org/spec/)

## 🤝 Contributing

Feel free to contribute to this learning repository by:
- Reporting issues
- Suggesting improvements
- Adding new examples
- Improving documentation

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🎉 Next Steps

After completing this course, you can:
- Explore Ansible Tower/AWX for enterprise automation
- Learn about Ansible collections
- Dive into network automation
- Study cloud automation (AWS, Azure, GCP)
- Contribute to open-source Ansible projects

---

**Happy Learning! 🚀**

*Remember: Practice makes perfect. Don't hesitate to experiment and break things - that's how you learn!*

