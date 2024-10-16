# Azure Functions - HTTP Trigger and Queue Triggers with Database Integration

## Overview

This project contains three Azure Functions:
1. **HTTP Trigger**: Receives an HTTP request, scrapes a webpage, and sends page URLs to an Azure Queue (`smc-queue1`).
2. **Queue Trigger 1**: Processes URLs from `smc-queue1`, scrapes data, and sends results to another queue (`smc-queue2`).
3. **Queue Trigger 2**: Processes messages from `smc-queue2`, extracts detailed information, and stores it in an Azure SQL Database.

## Setup

### Environment Variables

- **Storage**: `AzureWebJobsStorage`
- **Queue Names**: 
  - `smc-queue1`
  - `smc-queue2`
- **Database**:
  - `DbServer`
  - `DbName`
  - `DbUsername`
  - `DbPassword`
  - `DbTableName`

#### Scraped Fields:
- **Protestor**
- **Solicitation Number**
- **Outcome**
- **Filed Date**
- **Due Date**
- **Case Type**
- **Agency**
- **File Number**
- **GAO Attorney**
- **Recommendations**
- **Recommendations for Executive Action**
- **GAO Contacts**
- **Decision Date**
- **Published Date**
- **Publicly Released Date**


## Dependencies

Install the required Python packages listed in `requirements.txt`:

```bash
pip install -r requirements.txt


