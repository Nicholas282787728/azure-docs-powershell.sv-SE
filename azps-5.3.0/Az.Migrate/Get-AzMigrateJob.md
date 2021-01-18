---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525920"
---
# Get-AzMigrateJob

## Sammanfattning
Hämtar statusen för ett Azure Migrate-jobb.

## FRÅGESYNTAXEN

### ListByName (standard)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzMigrateJob cmdlet retrives status för ett Azure Migrate-jobb.

## BESKRIVS

### Exempel 1: get per jobb-ID
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Då hämtas ett jobb efter ID.

### Exempel 2: lista efter resurs grupp och projekt
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Det här får alla jobb i ett projekt.

### Exempel 3: Hämta efter resurs grupp, projekt och jobbnamn
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Detta får ett specifikt jobb.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Alternativ för OData-filter.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Anger jobbobjektet för den replikerande servern.
För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobID
Anger det jobb-ID som informationen måste hämtas för.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Jobb-ID

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
Anger det Azure Migrate-projekt där servrar replikeras.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Projektetsnamn
Namnet på det migrerande projektet.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
Anger resurs gruppen för Azure Migrate-projektet i det aktuella abonnemanget.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen där Recovery Services-valvet finns.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IJob

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <IJob> : anger jobbobjektet för den replikerande servern.
  - `[Location <String>]`: Resurs plats
  - `[ActivityId <String>]`: Aktivitets-ID.
  - `[AllowedAction <String[]>]`: Den tillåtna åtgärden som jobbet är.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: De påverkade objekt egenskaperna som käll Server, käll moln, mål server, mål moln etc. baserat på informationen i arbets flödes objekt.
    - `[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[EndTime <DateTime?>]`: Slut tiden.
  - `[Error <IJobErrorDetails[]>]`: Felen.
    - `[CreationTime <DateTime?>]`: Fel när jobbet skapades.
    - `[ErrorLevel <String>]`: Fel nivå fel.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Felkoden.
    - `[ProviderErrorDetailErrorId <String>]`: Leverantörens fel-ID.
    - `[ProviderErrorDetailErrorMessage <String>]`: Fel meddelandet.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Möjliga orsaker till felet.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Rekommenderad åtgärd för att åtgärda felet.
    - `[ServiceErrorDetailActivityId <String>]`: Aktivitets-ID.
    - `[ServiceErrorDetailCode <String>]`: Felkod.
    - `[ServiceErrorDetailMessage <String>]`: Fel meddelande.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Möjliga orsaker till felet.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Rekommenderad åtgärd för att åtgärda felet.
    - `[TaskId <String>]`: Aktivitetens ID.
  - `[FriendlyName <String>]`: Visnings namn.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: Start tiden.
  - `[State <String>]`: Jobbets status. Det är ett av följande värden – NotStarted, InProgress, lyckades, misslyckades, annullerat, upphävt eller annat.
  - `[StateDescription <String>]`: Beskrivningen av jobbets status. För att det ska vara klart kan beskrivningen kunna genomföras, PartiallySucceeded, CompletedWithInformation eller hoppas över.
  - `[TargetInstanceType <String>]`: Den påverkade objekts typen {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} klass.
  - `[TargetObjectId <String>]`: Det påverkade objekt-ID.
  - `[TargetObjectName <String>]`: Namnet på det aktuella objektet.
  - `[Task <IAsrTask[]>]`: Aktiviteterna.
    - `[AllowedAction <String[]>]`: De uppgifter som gäller för den här uppgiften.
    - `[CustomDetailInstanceType <String>]`: Typen av aktivitets information.
    - `[EndTime <DateTime?>]`: Slut tiden.
    - `[Error <IJobErrorDetails[]>]`: Information om aktivitets fel.
    - `[FriendlyName <String>]`: Namnet.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Underordnade aktiviteter.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Typen av aktivitets information.
    - `[Name <String>]`: Det unika aktivitets namnet.
    - `[StartTime <DateTime?>]`: Start tiden.
    - `[State <String>]`: Tillståndet. Det är ett av följande värden – NotStarted, InProgress, lyckades, misslyckades, annullerat, upphävt eller annat.
    - `[StateDescription <String>]`: Beskrivningen av uppgifts tillståndet. Till exempel: om du lyckas kan du beskriva en beskrivning, PartiallySucceeded, CompletedWithInformation eller hoppa över.
    - `[TaskId <String>]`: ID.
    - `[TaskType <String>]`: Typen av uppgift. Informationen i egenskapen CustomDetails är beroende av den här typen.

## RELATERADE LÄNKAR

