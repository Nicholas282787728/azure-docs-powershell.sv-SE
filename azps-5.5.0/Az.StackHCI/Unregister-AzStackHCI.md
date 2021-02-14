---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e5ff59889b2b786d07699a5b9d46937372c0662f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210734"
---
# Unregister-AzStackHCI

## SYNOPSIS
Unregister-AzStackHCI bort den molnbaserade Microsoft.AzureStackHCI-resurs som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.
Den registrerade information som är tillgänglig i klustret används för att avregistrera klustret om inga parametrar överförs.

## SYNTAX

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Unregister-AzStackHCI bort den molnbaserade Microsoft.AzureStackHCI-resurs som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.
Den registrerade information som är tillgänglig i klustret används för att avregistrera klustret om inga parametrar överförs.

## EXEMPEL

### EXEMPEL 1
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
Skapa en anrop på en av klusternoden

### EXEMPEL 2
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
Skapa en anrop från noden för hantering

### EXEMPEL 3
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
Göra en anrop från WAC

### EXEMPEL 4
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
Använda alla parametrar

## PARAMETERS

### -AccountId
Anger ARM åtkomsttoken.
Om du anger detta tillsammans med ArmAccessToken och GraphAccessToken undviker du interaktiva Azure-inloggningar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Anger ARM åtkomsttoken.
Om du anger detta tillsammans med GraphAccessToken och AccountId undviker du interaktiva inloggningar i Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Datornamn
Anger en av klusternoden i det lokala kluster som registreras i Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Anger autentiseringsnamnet för Datornamn.
Standardvärdet är den aktuella användaren som kör Cmdleten.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Anger Azure-miljön.
Standardvärdet är AzureCloud.
Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Anger graph-åtkomsttoken.
Om du anger detta tillsammans med ArmAccessToken och AccountId undviker du interaktiva inloggningar i Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger Azure-resursgruppens namn.
Om inte anges \<LocalClusterName\> används -rg som resursgruppnamn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Anger resursnamnet för resursen som skapats i Azure.
Om namnet på det lokala klusternamnet inte anges används.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Anger Azure-prenumerationen som resursen ska skapas med

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Anger Azure TenantId.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication
Använd autentisering med enhetskod i stället för en interaktiv webbläsaruppfråga.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### PSCustomObject. Returnerar följande egenskaper i PSCustomObject
### Resultat: Lyckades eller misslyckades eller avbröts.
## ANTECKNINGAR

## RELATERADE LÄNKAR
