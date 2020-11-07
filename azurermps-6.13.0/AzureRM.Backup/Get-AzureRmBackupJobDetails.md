---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755720"
---
# Get-AzureRmBackupJobDetails

## Sammanfattning
Hämtar information om ett säkerhets kopierings jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### JobsFiltersSet (standard)
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdFiltersSet
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmBackupJobDetails** hämtar information om ett Azure Backup-jobb.
Du kan använda denna cmdlet för att samla in information om ett jobb som Miss lyckas.

## BESKRIVS

### Exempel 1: Visa information om ett misslyckat jobb
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .
Kommandot lagrar objektet i $Vault variabel.
Det andra kommandot hämtar misslyckade jobb från valvet i $Vault och lagrar dem sedan i $Jobs mat ris variabel.
Det tredje jobbet får information om det första jobbet i $Jobs variabel och lagrar sedan informationen i $JobDetails variabel.
Det sista kommandot visar egenskapen **ErrorDetails** för $JobDetails med standardsyntaxen för dot.

### Exempel 2: Visa den rekommenderade åtgärden för ett misslyckat jobb
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

Det här kommandot visar den rekommenderade åtgärden från den $JobDetails variabel som skapades i det första exemplet.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Jobb
Anger ett jobb som denna cmdlet får information om.
Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Anger ID för ett jobb som denna cmdlet hämtar information om.
ID är **InstanceID** -egenskapen för ett **AzureRmBackupJob** -objekt.
För att få ett **AzureRmBackupJob** -objekt, Använd Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valv
Anger det säkerhets kopierings valv som denna cmdlet hämtar jobb uppgifter för.
Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
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

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob
Parametrar: Job (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJobDetails

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


