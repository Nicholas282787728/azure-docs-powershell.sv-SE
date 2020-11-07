---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: 0fd004cdb727a0e665fd9b867854b3b8e4054c9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758362"
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
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

Det här kommandot säkerhetskopierar en API-hanterings tjänst till en lagrings-blob.

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

### -Namn
Anger namnet på den API-hanterings distribution som denna cmdlet säkerhetskopierar.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: String
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
Type: IStorageContext
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: 

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
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[New-AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Återställ-AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


