# Infrastructure as Code (Bicep)
```bicep
resource cognitiveService 'Microsoft.CognitiveServices/accounts@2023-05-01' = {
  name: 'ai-enterprise-service'
  location: resourceGroup().location
  kind: 'OpenAI'
  sku: { name: 'S0' }
}
```