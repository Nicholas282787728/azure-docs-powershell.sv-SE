---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574735"
---
# Get-AzureRmBackupJob

## Sammanfattning
Hämtar säkerhets kopierings jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### FiltersSet (standard)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmBackupJob** får Azure Backup-jobb för ett specifikt valv.

## BESKRIVS

### Exempel 1: Hämta alla jobb i ett säkerhets kopierings valv
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får alla jobb för valvet i $Vault.

### Exempel 2: Hämta färdiga jobb
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Det här kommandot hämtar jobb från valvet i $Vault.

### Exempel 3: Hämta misslyckade jobb under den senaste veckan
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Det här kommandot hämtar misslyckade jobb från förra veckan från valvet i $Vault.
Parametern *från* anger en tid sju dagar förr.
Kommandot anger inte ett värde för parametern *to* .
Därför används standardvärdet för den aktuella tiden.

### Exempel 4: Avsök säkerhets kopiering för ett pågående jobb som är klart
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Det här skriptet utför det första jobbet som pågår tills jobbet är klart.

Den första raden i skriptet får alla jobb i $Vault som pågår och lagrar sedan de jobben i $Jobs mat ris variabeln.

Den andra raden sparar det första jobbet från $Jobs matris i $Job variabel.

Den tredje raden startar en **while** -slinga som kontrollerar jobbets aktuella status tills jobbet är klart.
Om du vill ha information om nyckelordet **while** skriver du `Get-Help about_While` .

**While** -slingan skriver ett meddelande till konsolen, väntar i tio sekunder och uppdaterar variabeln $Job.
Skriptet uppdaterar $Job-variabeln genom att använda det befintliga värdet för $Job och den aktuella cmdleten för att få aktuell status för jobbet.
Om du vill ha information om Windows PowerShell-cmdletar skriver du `Get-Help Write-Host` och `Get-Help Start-Sleep` .

Den sista raden i skriptet visar att skriptet är klart.

## MALLPARAMETRAR

### -Från
Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.
Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.
Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobb
Anger ett jobb som den här cmdleten får.
Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Anger ID för ett jobb som den här cmdleten får.
ID är **InstanceID** -egenskapen för ett **AzureRmBackupJob** -objekt.
För att få ett **AzureRmBackupJob** -objekt, Använd Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Åtgärd
Anger en åtgärd för de jobb som denna cmdlet får.
De acceptabla värdena för den här parametern är:

- Reservdomänkontrollant 
- ConfigureBackup 
- DeleteBackupData 
- Registrera dig 
- Terställa 
- Låsa upp 
- Avregistrera

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Anger en status för de jobb som denna cmdlet får.
De acceptabla värdena för den här parametern är:

- Inaktive
- Startade
- Annullerats
- Brusdämpande
- Rätta
- CompletedWithWarnings 

Du kan ange den här parametern för att hitta alla pågående jobb eller alla misslyckade jobb.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -För att
Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.
Standardvärdet är den aktuella system tiden.
Om du anger den här parametern måste du också ange parametern *från* .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Skriv
Anger den typ av behållare för vilken denna cmdlet ska säkerhetskopiera jobb.
För närvarande är det enda värdet som stöds AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valv
Anger det säkerhets kopierings valv som denna cmdlet hämtar jobb för.
Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRmBackupVault

## VÄRDEN

### AzureRmBackupJob[]
Denna cmdlet returnerar en eller flera säkerhets kopierings jobb.

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Stopp-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


