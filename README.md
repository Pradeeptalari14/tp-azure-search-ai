# Azure Cognitive Search AI Studio

This repository contains the target configuration and SRE runtime files compiled by the **Azure Cognitive Search AI Studio** dashboard module.

## 🚀 Description
Build and tune Azure Cognitive Search indexes with integrated Azure OpenAI embeddings. Generate search index schemas, indexing pull pipelines, and vector semantic configs.

## 🛠️ Specification Matrix
- **Primary Configuration File**: `/config/search_config.json`
- **Execution Command**: `curl -X PUT "https://service.search.windows.net/indexes/index?api-version=2023-11-01" -H "Content-Type: application/json" -d @search_config.json`
- **Validation Command**: `az search index show --name index --service-name service`

## 📋 How to Run & Validate

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Pradeeptalari14/tp-azure-search-ai.git
   cd tp-azure-search-ai
   ```

2. **Run Execution Target:**
   ```bash
   curl -X PUT "https://service.search.windows.net/indexes/index?api-version=2023-11-01" -H "Content-Type: application/json" -d @search_config.json
   ```

3. **Verify Runtime Stability:**
   ```bash
   az search index show --name index --service-name service
   ```

## 🔐 Security & Best Practices
* **Secret Isolation**: Use organization-level secrets (or SSM parameter hooks) rather than hardcoded environment variables inside files.
* **Pull Request Lifecycles**: Protect default branch merges with validation checks before merging code changes.
