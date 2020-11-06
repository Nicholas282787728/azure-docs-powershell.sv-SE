---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581563"
---
# Backup-AzureRmApiManagement

## Sammanfattning
Säkerhetskopierar en API-hanterings tjänst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureRmApiManagement** cmdlet säkerhetskopierar en instans av en Azure API Management-tjänst.
Denna cmdlet lagrar säkerhets kopian som en Azure Storage blob.

## BESKRIVS

### Exempel 1: säkerhetskopiera en API-hanterings tjänst
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.

## MALLPARAMETRAR

### -Namn
Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Anger att den här cmdleten returnerar det säkerhetskopierade **PsApiManagement** -objektet, om åtgärden lyckas.

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

### -ResourceGroupName
Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Anger en kontext för lagrings anslutning.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetBlobName
Anger namnet på blobben för säkerhets kopian.
Om blobben inte finns skapar den här cmdlet den.
Denna cmdlet skapar ett standardvärde baserat på följande mönster: 

{Name}-{ÅÅÅÅ-MM-dd-HH-mm}. apimbackup

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetContainerName
Anger namnet på behållaren för blobben för säkerhets kopian.
Om behållaren inte finns skapar den här cmdlet den.

```yaml
Type: System.String
Parameter Sets: (All)
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[New-AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Återställ-AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


