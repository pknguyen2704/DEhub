# Helm

- add repository 
helm repo add <repository_name> <repository_link>

## Definition

## Components
1. chart
Chart = gói ứng dụng Helm. Bao gồm toàn bộ:

Template YAML của Kubernetes

Giá trị cấu hình

Metadata

Hook, thư viện, subchart
2. Release

Release = một phiên bản đã cài đặt của chart trên Kubernetes.

Ví dụ:

Chart tên nginx

Bạn install lần 1: release: nginx-dev

Install lần 2: release: nginx-prod

👉 Cùng một chart có thể deploy nhiều lần với tên khác nhau.
## install a chart
To install a chart, you can run the helm install command. Helm has several ways to find and install a chart, but the easiest is to use the bitnami charts.

## Quy trình làm việc với một helm chart
1. Install chart
helm install myapp ./mychart

2. Upgrade
helm upgrade myapp ./mychart

3. Rollback
helm rollback myapp 1

4. Render template không apply
helm template myapp ./mychart

5. Xem release
helm list --all-namespaces