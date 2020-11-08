---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088278"
---
# Update-AzCosmosDBAccount

## Sammanfattning
Uppdatera ett CosmosDB.

## FRÅGESYNTAXEN

### ByNameParameterSet (standard)
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectParameterSet
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Uppdatera egenskaperna för ett CosmosDB-konto. Det går inte att uppdatera konto områden simulataneously med andra egenskaper.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

Uppdaterade DefaultConsistencyLevel till "Strong", aktiverat AutomaticFailover, aktiverat MultipleWriteLocations och aktiverat VirtualNetwork för CosmosDB-konto med namn accountName. 

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### -DefaultConsistencyLevel
Standard konsekvens nivå för Cosmos DB-databasnamn.
Godkända värden: BoundedStaleness, ConsistentPrefix, nysession, Strong

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableKeyBasedMetadataWriteAccess
Inaktivera Skriv åtgärder för metadataegenskaper (databaser, behållare, genomflöde) via konto nycklar

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticFailover
Aktiverar automatisk redundans av Skriv regionen i den sällsynta händelsen att regionen inte är tillgänglig på grund av ett avbrott.
Automatisk redundans ger en ny Skriv region för kontot och väljs utifrån de prioriteter som kon figurer ATS för kontot.
Godkända värden: falskt, sant

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableMultipleWriteLocations
Aktivera flera Skriv platser.
Godkända värden: falskt, sant

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableVirtualNetwork
Aktiverar virtuellt nätverk på Cosmos DB Database-konto.
Godkända värden: falskt, sant

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
CosmosDB

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IpRangeFilter
Stöd för brand väggar.
Anger uppsättningen IP-adresser eller IP-adressintervall i CIDR-format som ska ingå som tillåten lista över klient-IP för ett visst databas konto

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxStalenessIntervalInSeconds
När det här värdet används med utgångs punkt som är bundet till inaktivitet representerar det tids mängd inaktuellt (i TimeSpan) som tolereras.
Det tillåtna intervallet för det här värdet är 5-86400.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxStalenessPrefix
När det används med avgränsad utgångs konsekvens representerar det här värdet antalet begärda föråldrade förfrågningar.
Det tillåtna intervallet för det här värdet är 1-2 147 483 647.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namn på Cosmos DB-databas.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccess
Om åtkomst för offentlig slut punkt tillåts för den här servern. Möjliga värden är: ' Enabled ', ' disabled '

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resurs gruppen.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ResourceId för resursen.

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
En produkt kod med taggar som par med nyckelord-värde.
Använd en tom sträng för att ta bort en befintlig tagg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRule
Matris med sträng värden för ACL för virtuella nätverk.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRuleObject
Matris med PSVirtualNetworkRuleObjects för virtuella nätverk.

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. commands. CosmosDB. Models. PSCorsRule []

## VÄRDEN

### Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
