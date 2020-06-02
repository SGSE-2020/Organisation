# Einrichten von CI

Dieses Dokument beschreibt die Schritte, die getätigt werden müssen, um das Frontend und das Backend im Kubernetes Cluster zu deployen.

---

Folgende Bedingungen muss das Microservice Repository erfüllen:

1. Der Microservice muss in Frontend und Backend aufgeteilt sein, wobei sich das Frontend im Ordner *frontend* und das Backend im Ordner *backend* befindet.
2. Der *frontend* und der *backend* Ordner müssen beide ein Dockerfile beinhalten, welches ein Frontend bzw Backend Image erstellt.
3. Es muss über Github Actions ein Workflow erstellt werden, welcher den Inhalt der *workflow.yml* enthält.
4. Die Dateien *deployment.yaml*, *service.yaml* und *kustomization.yaml*.
5. Der Microservice wird immer dann deployt, wenn Änderungen auf den Master gepusht werden.

**Achtung**: In den Dateien *workflow.yml*, *deployment.yaml*, *service.yaml* und *kustomization.yaml* muss *MSSERVICE* durch den Namen des jeweiligen Microservices ersetzt werden.<br>Beispiel für das Repository MS_Restaurants: restaurants