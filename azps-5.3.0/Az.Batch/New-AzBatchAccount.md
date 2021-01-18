---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: cd175baa39c329c301913f2abb5e70eaedcf45f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524766"
---
# New-AzBatchAccount

## Sammanfattning
Skapar ett batch-konto.

## FRÅGESYNTAXEN

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzBatchAccount** skapar ett Azure Batch-konto för angiven resurs grupp och plats.

## BESKRIVS

### Exempel 1: skapa ett batch-konto
```powershell
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Det här kommandot skapar ett batch-konto med namnet pfuller med resurs gruppen ResourceGroup03 på platsen för USA.

### Exempel 2

Skapar ett batch-konto. (automatiskt genererat)

<!-- Aladdin Generated Example -->
```powershell
New-AzBatchAccount -AccountName 'pfuller' -AutoStorageAccountId <String> -Location 'WestUS' -ResourceGroupName 'ResourceGroup03'
```

## MALLPARAMETRAR

### -AccountName
Anger namnet på det kommando konto som denna cmdlet skapar.
Namn på kommandofiler måste vara mellan 3 och 24 tecken långa och får endast innehålla siffror och gemener.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoStorageAccountId
Anger resurs-ID för det lagrings konto som ska användas för automatisk lagring.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Identiteten som är associerad med BatchAccount

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultId
Resurs-ID för Azure Key Vault som är kopplat till batch-kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyVaultUrl
Webb adressen för det Azure Key-valv som är kopplat till batch-kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger den region där den här cmdleten skapar kontot.
Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PoolAllocationMode
Tilldelnings läget för att skapa pooler i batch-kontot.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Åtkomst typen offentlig nätverk

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som den här cmdleten skapar för kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Nullable ' 1 [[Microsoft.Azure.Management.BatCH. Models. PoolAllocationMode, Microsoft.Azure.Management.BatCH, version = 9.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Collections. hash

## VÄRDEN

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccount](./Get-AzBatchAccount.md)

[Remove-AzBatchAccount](./Remove-AzBatchAccount.md)

[Set-AzBatchAccount](./Set-AzBatchAccount.md)

[Cmdlets för Azure Batch](/powershell/module/Az.Batch/)
