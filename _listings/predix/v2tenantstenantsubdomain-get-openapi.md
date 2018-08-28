---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Tenant Management Lookup Tenant by Subdomain
  description: Lookup tenant by subdomain.
  version: 1.0.0
host: predix-tms.run.aws-usw02-pr.ice.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/tenant/profile:
    get:
      summary: Lookup Tenant by Subdomain
      description: Lookup tenant by subdomain.
      operationId: getTenantBySubdomainUsingGET
      x-api-path-slug: v1tenantprofile-get
      parameters:
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - By
      - Subdomain
  /v1/tenant/profile/service/{serviceName}:
    get:
      summary: Lookup Tenant service by Subdomain
      description: Lookup tenant service by subdomain.
      operationId: getTenantServiceBySubdomainUsingGET
      x-api-path-slug: v1tenantprofileserviceservicename-get
      parameters:
      - in: path
        name: serviceName
        description: serviceName
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - Service
      - By
      - Subdomain
  /v2/tenants/{tenantSubdomain}:
    get:
      summary: Lookup Tenant by Subdomain
      description: Lookup tenant by subdomain.
      operationId: getTenantProfileBySubdomainUsingGET
      x-api-path-slug: v2tenantstenantsubdomain-get
      parameters:
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - By
      - Subdomain
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---