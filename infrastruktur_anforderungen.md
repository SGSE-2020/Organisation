## Infrastruktur Anforderungen



### MS_Tierarzt

|         | Frontend       | Backend         | Datenbank           |
| ------- | -------------- | --------------- | ------------------- |
| Image   | `nginx:latest` | `golang:latest` | `couchebase:latest` |
| CPU     | 8-Core CPU     | 1-Core CPU      | 2-Core CPU          |
| RAM     | 8 GB           | 2 GB            | 4 GB                |
| Storage | 80 GB          | 0 GB            | 8 GB                |

### MS_Notarzt

|         | Frontend       | Backend         | Datenbank        |
| ------- | -------------- | --------------- | ---------------- |
| Image   | `nginx:latest` | `nodejs:latest` | `mongodb:latest` |
| CPU     | 4-Core CPU     | 8-Core CPU      | 3-Core CPU       |
| RAM     | 4 GB           | 8 GB            | 2 GB             |
| Storage | 4 GB           | 10 GB           | 20 GB            |



### MS_Supermarkt

|         | Frontend   | Backend    | Datenbank  |
| ------- | ---------- | ---------- | ---------- |
| Image   | `<>`       | `<>`       | `<>`       |
| CPU     | 4-Core CPU | 8-Core CPU | 3-Core CPU |
| RAM     | 4 GB       | 8 GB       | 2 GB       |
| Storage | 4 GB       | 10 GB      | 20 GB      |

### MS_Parkplatz

|         | Frontend       | Backend        | Datenbank      | Cache                |
| ------- | -------------- | -------------- | -------------- | -------------------- |
| Image   | `nginx:alpine` | `node:latest`  | `mysql:8.0.20` | `redis:6.0.1-alpine` | 
| CPU     | 1 Core         | 1 Core         |  1 Core        |  2 Cores             |
| RAM     | 1 GB           | 1 GB           |  2 GB          |  4 GB                |
| Storage | No Persistence | No Persistence | 10 GB          | 10 GB                |

### MS_ÖPNV

|         | Frontend       | Backend         | Datenbank           |
| ------- | -------------- | --------------- | ------------------- |
| Image   | `nginx:latest` | `golang:latest` | `postgresql:latest` |
| CPU     | 4-Core CPU     | 1-Core CPU      | 1-Core CPU          |
| RAM     | 4 GB           | 2 GB            | 2 GB                |
| Storage | 5 GB           | 5 GB            | 5 GB                |

