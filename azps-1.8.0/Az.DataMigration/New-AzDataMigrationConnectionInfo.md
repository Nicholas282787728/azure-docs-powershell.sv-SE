---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: 871b6c09832e4b857a616c93cc33102f2dd0ad8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916817"
---
# New-AzDataMigrationConnectionInfo

## Sammanfattning
Skapar en ny anslutnings information ett objekt som anger Server typ och namn för anslutning.

## FRÅGESYNTAXEN

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
New-AzDataMigrationConnectionInfo cmdlet skapar ny en anslutnings information som anger Server typen för anslutning. 

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

I det föregående exemplet skapas en ny anslutnings information med parametern SQL as ServerType.

## MALLPARAMETRAR

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

### -ServerType
Fasttext som beskriver Server typen som du vill ansluta till. Funktioner som stöds för närvarande är SQL för SQL Server, Azure SQL-hanterad instans, MongoDb, CosmosDb och Azure SQL Database. 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
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

### Microsoft. Azure. Management. DataMigration. Models. ConnectionInfo

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
