---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224255"
---
# Get-AzMigrateJob

## SYNOPSIS
Hämtar statusen för ett Azure Migrate-jobb.

## SYNTAX

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

## BESKRIVNING
Cmdleten Get-AzMigrateJob status för ett Azure Migrate-jobb.

## EXEMPEL

### Exempel 1: Hämta via jobb-ID
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

Då hämtas ett jobb med hjälp av id:t.

### Exempel 2: Lista efter resursgrupp och projekt
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

Det får alla jobb i ett projekt.

### Exempel 3: Hämta efter resursgrupp, projekt och jobbnamn
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

Det här får ett särskilt jobb.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
OData-filteralternativ.

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
Skapa genom att gå till avsnittet NOTES för INPUTOBJECT-egenskaper och skapa en hash-tabell.

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
Anger det jobb-ID som informationen ska hämtas för.

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

### -Jobbnamn
Jobbidentifierare

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
Anger Azure Migrate Project där servrarna replikeras.

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

### -Projektnamn
Namnet på migreringsprojektet.

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
Anger resursgruppen för Azure Migrate Project i den aktuella prenumerationen.

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
Namnet på resursgruppen där valv för återställningstjänster finns.

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
Azure-prenumerations-ID.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.migrate.models.api20180110.i Enl

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT: <IJob> Anger jobbobjektet för den replikerande servern.
  - `[Location <String>]`: Resursplats
  - `[ActivityId <String>]`: Aktivitets-ID.
  - `[AllowedAction <String[]>]`: Åtgärden Tillåts.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Det påverkade objektets egenskaper som källserver, källmoln, målserver, målmoln osv. baserat på information om arbetsflödets objekt.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[EndTime <DateTime?>]`: Sluttiden.
  - `[Error <IJobErrorDetails[]>]`: Felen.
    - `[CreationTime <DateTime?>]`: Skapandetiden för fel i jobbet.
    - `[ErrorLevel <String>]`: Felnivå.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Felkoden.
    - `[ProviderErrorDetailErrorId <String>]`: Leverantörsfel-ID.
    - `[ProviderErrorDetailErrorMessage <String>]`: Felmeddelandet.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Möjliga orsaker till felet.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Den rekommenderade åtgärden för att lösa felet.
    - `[ServiceErrorDetailActivityId <String>]`: Aktivitets-ID.
    - `[ServiceErrorDetailCode <String>]`: Felkod.
    - `[ServiceErrorDetailMessage <String>]`: Felmeddelande.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Möjliga orsaker till fel.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Rekommenderad åtgärd för att lösa fel.
    - `[TaskId <String>]`: Id för aktiviteten.
  - `[FriendlyName <String>]`: Visningsnamnet.
  - `[ScenarioName <String>]`: ScenarioNamn.
  - `[StartTime <DateTime?>]`: Starttiden.
  - `[State <String>]`: Status för jobbet. Det är ett av dessa värden: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.
  - `[StateDescription <String>]`: Beskrivning av statusen för jobbet. For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.
  - `[TargetInstanceType <String>]`: Typen av det påverkade objektet som är av typen {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.
  - `[TargetObjectId <String>]`: Det aktuella objekt-ID:t.
  - `[TargetObjectName <String>]`: Namnet på det påverkade objektet.
  - `[Task <IAsrTask[]>]`: Uppgifterna.
    - `[AllowedAction <String[]>]`: Den delstat/de åtgärder som är tillämpliga för den här aktiviteten.
    - `[CustomDetailInstanceType <String>]`: Typen av uppgiftsinformation.
    - `[EndTime <DateTime?>]`: Sluttiden.
    - `[Error <IJobErrorDetails[]>]`: Information om uppgiftsfelet.
    - `[FriendlyName <String>]`: Namnet.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Underordnade aktiviteter.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Typen av uppgiftsinformation.
    - `[Name <String>]`: Det unika aktivitetsnamnet.
    - `[StartTime <DateTime?>]`: Starttiden.
    - `[State <String>]`: Delstat. Det är ett av dessa värden: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.
    - `[StateDescription <String>]`: Beskrivning av aktivitetstillståndet. Till exempel – I läget Lyckades kan beskrivningen vara Slutförd, Delvis Tillbildad, SlutfördMedInformation eller Överhoppad.
    - `[TaskId <String>]`: Id.
    - `[TaskType <String>]`: Typ av aktivitet. Information i egenskapen AnpassadDetaljer beror på den här typen.

## RELATERADE LÄNKAR

