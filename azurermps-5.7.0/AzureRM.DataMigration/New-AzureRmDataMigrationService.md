---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757687"
---
# New-AzureRmDataMigrationService

## Sammanfattning
Skapar en ny instans av Azure Database migration service.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## PROBLEMBESKRIVNING
New-AzureRmDataMigrationService-cmdleten skapar en ny instans av Azure Database migration service. Denna cmdlet tar upp namnet på den befintliga Azure Resource-gruppen, det unika namnet på den nya instansen av Azure Database migration service som ska skapas, den region där instansen är etablerad, namnet på DMS Worker-SKU och namnet på det virtuella Azure-undernät där tjänsten ska lagras. Det finns ingen parameter för prenumerations namnet eftersom det förväntas för användaren att ange standard abonnemang för Azure-inloggningssessionen eller EXECUTE Get-AzureRmSubscription-SubscriptionName "min prenumeration" | Select-AzureRmSubscription för att välja ett annat abonnemang.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

Det här exemplet visar hur du skapar en ny instans av Azure Database migration service med namnet TestService i området Central USA.


## MALLPARAMETRAR

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

### -Plats
Platsen för Azure Database migration service-instansen som ska skapas, som motsvarar ett Azure-område.

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

### -ResourceGroupName
Namnet på resurs gruppen.

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

### -ServiceName
Namnet på instansen för Azure Database migration service.

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

### -SKU
SKU för Azure Database migration service instans. Möjliga värden är Basic_1vCore Basic_2vCores GeneralPurpose_4vCores

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

### -VirtualSubnetId
Namnet på under nätet under det virtuella nätverk som ska användas för Azure Database migration service instans.

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




## VÄRDEN

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## ANMÄRKNINGAR

## RELATERADE LÄNKAR

