---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 8e93847c3a6d993c689d0ac8c40327ddfcbe76af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583132"
---
# New-AzureRmMlOpCluster

## Sammanfattning
Skapar ett nytt operationalization-kluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### CreateWithInputObject
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateWithParameters
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Skapar ett nytt operationalization-kluster. Detta skapar ett kluster objekt, en behållar tjänst om det behövs, Application Insights och ett Azure-behållarobjekt.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

Skapar ett nytt operationalization-kluster med Azure Container-tjänsten och Kubernetes som Orchestrator.

### Exempel 2
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

Skapar ett nytt operationalization-kluster lokalt. Detta skapar ett Azure-behållarobjekt, Application Insights och Storage-konto, men skapar inte en behållar tjänst.

## MALLPARAMETRAR

### -AgentCount
Antalet agent-noder i ACS-klustret.

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgentVmSize
Antalet agent-noder i ACS-klustret.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContainerRegistry
Den URI till Azure-behållarobjektet som ska användas i stället för att skapa en.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientId
Huvud-ID för ACS-klustrets tjänst.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterType
Kluster typen operationalization.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beskrivning
Antalet huvudnoder i ACS-klustret.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationAdditionalProperties
Ytterligare egenskaper för den globala tjänst konfigurationen.

```yaml
Type: Hashtable
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GlobalServiceConfigurationETag
Konfigurationens ETag för uppdateringar.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Kluster egenskaperna för operationalization.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Operationalization-klustrets plats.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MasterCount
Antalet huvudnoder i ACS-klustret.

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på operationalization-klustret.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrchestratorType
ACS-klustrets Orchestrator-typ.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen för operationalization-klustret.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Secret
Huvud hemlighet för ACS-klustrets säkerhets tjänst.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
SSL-certifikatets data i PEM-format kodat som base64-sträng.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCName
CName för SSL-certifikatet.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslKey
SSL-PEM kodas som base64-sträng.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslStatus
SSL-status.
Möjliga värden är "Enabled" och "Disabled".

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
Den URI till lagrings kontot som ska användas i stället för att skapa ett.

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

