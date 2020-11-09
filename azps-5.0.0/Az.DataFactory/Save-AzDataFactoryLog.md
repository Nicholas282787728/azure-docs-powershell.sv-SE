---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320864"
---
# Save-AzDataFactoryLog

## Sammanfattning
Laddar ned loggfiler från Azure HDInsight-bearbetning.

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Save-AzDataFactoryLog-** filer som är associerade med Azure HDInsight-bearbetning av gris-eller registrerings projekt eller för anpassade aktiviteter till din lokala hård disk.
Du kör först Get-AzDataFactoryRun cmdlet för att få ett ID för en aktivitet som körs för en data sektor och sedan använda ID: t för att hämta loggfiler från den binära Large Object (BLOB) som är kopplad till HDInsight-klustret.
Om du inte anger parametern *DownloadLogs* returnerar cmdleten bara platsen för loggfilerna.
Om du anger *DownloadLogs* utan att ange en utdatakatalogen ( *utdataparameter* ) hämtas loggfilerna till mappen standard dokument.
Om du anger *DownloadLogs* tillsammans med en utdatafil ( *utdata* ) hämtas loggfilerna till den angivna mappen.

## BESKRIVS

### Exempel 1: spara loggfiler i en viss mapp
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Det här kommandot sparar loggfiler för aktiviteten som körs med ID-numret för 841b77c9-d56c-48D1-99a3-8c16c3e77d39 där aktiviteten tillhör en pipeline i data fabriken med namnet LogProcessingFactory i resurs gruppen med namnet ADF.
Loggfilerna sparas i mappen C:\Test.

### Exempel 2: spara loggfiler i mappen standard dokument
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Det här kommandot sparar loggfiler i mappen dokument (standard).

### Exempel 3: Hämta sökvägen till loggfilerna
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Det här kommandot returnerar platsen för loggfilerna.
Observera att *DownloadLogs* inte har angetts.

## MALLPARAMETRAR

### -DataFactory
Anger ett **PSDataFactory** -objekt.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Anger namnet på en data fabrik.
Denna cmdlet laddar ned loggfiler för data fabriken som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -DownloadLogs
Anger att denna cmdlet laddar ned loggfilerna till din lokala dator.
Om mappen *utdatafil* inte anges sparas filer i mappen dokument under en undermapp.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för aktivitets körningen för data sektorn.
Använd Get-AzDataFactoryRun cmdlet för att hämta ett ID.

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

### -Utdata
Anger den mapp där de hämtade loggfilerna sparas.

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

### -ResourceGroupName
Anger namnet på en Azure-adressresurs.
Denna cmdlet skapar en data fabrik som tillhör den grupp som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## VÄRDEN

### Microsoft. Azure. commands. DataFactories. Models. PSRunLogInfo

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer

## RELATERADE LÄNKAR

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


