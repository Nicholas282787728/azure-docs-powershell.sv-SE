---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583191"
---
# Get-AzureRmDataMigrationProject

## Sammanfattning
Hämtar egenskaperna för ett Azure Database migration Project.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ComponentNameParameterSet (standard)
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### ComponentObjectParameterSet
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### ResourceIdParameterSet
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## PROBLEMBESKRIVNING
Get-AzureRmDataMigrationProject cmdlet hämtar egenskaperna för ett Azure Database migration Project.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

Exemplet ovan hämtar ett Azure Database migration-projekt med namnet TestProject i resurs gruppen som heter testResourceGroup och under tjänst heter testService

### Exempel 2
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

Exemplet ovan hämtar Azure Database migration Project baserat på PSProject-indataparameter som skickades. 


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

### -InputObject
PSDataMigrationService-objekt.

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på projektet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
DataMigrationService resurs-ID.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Tjänst namn för data migration.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## KOSTNADS

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
System. String


## VÄRDEN

### System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataMigration. Models. PSProject, Microsoft. Azure. commands. DataMigration, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]


## ANMÄRKNINGAR

## RELATERADE LÄNKAR

