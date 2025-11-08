# Nginx Proxy Manager反向代理 + Prometheu + Grafana + Node Exporter 监控docker项目

## 配置说明
nginx 服务器上不进行计算任务，只是作为反向代理功能对机器的要求不高。因此1c1g的服务器也能满足nginx的使用
Prometheu 目前机器配置要求不知，有待测试。

## 1. 项目介绍

Nginx Proxy Manager是一个基于Nginx的反向代理管理工具，它可以帮助用户轻松地管理和配置反向代理服务器。通过docker 容器化部署Nginx Proxy Manager，用户可以轻松地添加、删除和修改反向代理规则，并且可以实时查看代理服务器的状态和日志。

Prometheu + Grafana + Node Exporter 监控docker项目，可以实时监控docker容器的运行状态，包括CPU、内存、磁盘、网络等指标，并提供可视化的监控界面，方便用户了解和优化docker容器的性能。

## 2. 项目结构

本项目包含以下脚本：
1. `1_install-docker.sh`：用于快速安装docker、docker-compose、等工具
2. `2_swapon.sh`：用于虚拟化内存2G，提升docker性能
3. `docker-compose.yml`：用于统一安装docker-compose 项目
4. `prometheus/prometheus.yml`：用于部署安装prometheus项目
5. `alertmanager/alertmanager.myl`：用于部署安装alertmanager项目
6. `nginx/nginx.conf`：nginx反向代理配置文件
7. `README.md`：项目说明文档

