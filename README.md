# approuter-tde

Inspired from [SAP Tutorial](https://developers.sap.com/tutorials/cp-connectivity-consume-odata-service-approuter.html)

## XSUAA
```
{
  "xsappname": "approuter-tde",
  "tenant-mode": "dedicated",
  "description": "Security profile of called application",
  "scopes": [
    {
      "name": "uaa.user",
      "description": "UAA"
    }
  ],
  "role-templates": [
    {
      "name": "Token_Exchange",
      "description": "UAA",
      "scope-references": [
        "uaa.user"
      ]
    }
  ]
}```