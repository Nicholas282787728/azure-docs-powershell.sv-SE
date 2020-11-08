---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260916"
---
# Unregister-AzStackHCI

## Sammanfattning
Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.
Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.

## FRÅGESYNTAXEN

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.
Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.

## BESKRIVS

### EXEMPEL 1
```
Invoking on one of the cluster node
```

C:\PS \> -AzStackHCI resultat: lyckades

### EXEMPEL 2
```
Invoking from the management node
```

C:\PS \> Unregistered-AzStackHCI-ComputerName ClusterNode1 result: lyckades

### EXEMPEL 3
```
Invoking from WAC
```

C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultat: lyckades

### EXEMPEL 4
```
Invoking with all the parameters
```

C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential result: lyckades

## MALLPARAMETRAR

### -SubscriptionId
Anger Azure-abonnemanget för att skapa resursen

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Anger resurs namnet på resursen som har skapats i Azure.
Om det inte anges används det lokala kluster namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Anger Azure TenantId.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på Azure Resource-gruppen.
Om ej angivet \<LocalClusterName\> -RG kommer att användas som resurs grupps namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Anger ARM-åtkomsttoken.
Om du anger detta tillsammans med GraphAccessToken och AccountId undviks Azure interaktiv inloggning.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Anger Graph-åtkomsttoken.
Om du anger detta tillsammans med ArmAccessToken och AccountId undviks Azure interaktiv inloggning.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Anger ARM-åtkomsttoken.
Genom att ange detta tillsammans med ArmAccessToken och GraphAccessToken undviker du Azure interaktiv inloggning.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Anger Azure-miljön.
Standard är AzureCloud.
Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Anger en av klusternoderna i det lokala klustret som registreras på Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autentiseringsuppgift
Anger autentiseringsuppgifter för dator namnet.
Standard är den aktuella användaren som kör cmdleten.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

## VÄRDEN

### PSCustomObject. Returnerar följande egenskaper i PSCustomObject
### Resultat: lyckades eller misslyckades eller avbröts.
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
