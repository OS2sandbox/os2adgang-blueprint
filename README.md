# os2adgang-blueprint

A declarative, production-ready blueprint for deploying **os2adgang** (Keycloak) via GitOps.

## 🚀 Overview
This repository provides a container definition and the corresponding Kubernetes manifests. It is designed to be a reference point to getting up and running in your own infratructure with you own instance of os2adgang, only providing your own relevant variabled via environment variables.

## 🏗 Structure
* `/Containerfile`: OCI-compliant build file.
* `/realms`: Contains a privider specific `realm.json`. Currently only a realm for Fælleskommunal Adgangsstyring is supplied


* `/deploy/base`:  manifests.. 
* `/themes: Custom themes
*  /providers`: Custom extensions copied into the build.

## 🛠 Usage for Platform Engineers

### 1. Build the Image
The image is pre-optimized. You only need to build and push it to your local registry:
`podman build -t <your-registry>/os2adgang:latest .`

### 2. Connect to GitOps (ArgoCD)
