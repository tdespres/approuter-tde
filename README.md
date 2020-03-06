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
}
```

## Create zip file
```
  foreach ($file in @("xs-app.json",".npmrc", "package.json")){
 if (-not (Test-Path $file)) { Write-Warning "$file does not exist" }
  }
  Compress-Archive -Force -Path .\* -DestinationPath approuter.zip
```