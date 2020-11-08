---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099780"
---
# <span data-ttu-id="9d5db-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="9d5db-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="9d5db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d5db-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5db-103">Hämtar flytt statusen för volym behållarna.</span><span class="sxs-lookup"><span data-stu-id="9d5db-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="9d5db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d5db-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d5db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d5db-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5db-106">Cmdleten **Get-AzureStorSimpleLegacyVolumeContainerStatus** får volym behållarna.</span><span class="sxs-lookup"><span data-stu-id="9d5db-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="9d5db-107">Denna cmdlet returnerar statusinformation som inkluderar om migreringen av volym behållarna fortfarande pågår, är slutförd eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="9d5db-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="9d5db-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d5db-108">EXAMPLES</span></span>

### <span data-ttu-id="9d5db-109">Exempel 1: Hämta status för en misslyckad migrering</span><span class="sxs-lookup"><span data-stu-id="9d5db-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="9d5db-110">Det här kommandot får flytt statusen för den namngivna gamla behållaren.</span><span class="sxs-lookup"><span data-stu-id="9d5db-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="9d5db-111">Resultatet visar att migreringen misslyckades.</span><span class="sxs-lookup"><span data-stu-id="9d5db-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="9d5db-112">Exempel 2: Hämta status för en migrering pågår</span><span class="sxs-lookup"><span data-stu-id="9d5db-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="9d5db-113">Det här kommandot får flytt statusen för den namngivna gamla behållaren.</span><span class="sxs-lookup"><span data-stu-id="9d5db-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="9d5db-114">Resultatet visar att migreringen pågår.</span><span class="sxs-lookup"><span data-stu-id="9d5db-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="9d5db-115">Exempel 3: Hämta status för en slutförd migrering</span><span class="sxs-lookup"><span data-stu-id="9d5db-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="9d5db-116">Det här kommandot får flytt statusen för den namngivna gamla behållaren.</span><span class="sxs-lookup"><span data-stu-id="9d5db-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="9d5db-117">Resultatet visar att migreringen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="9d5db-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="9d5db-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d5db-118">PARAMETERS</span></span>

### <span data-ttu-id="9d5db-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="9d5db-119">-LegacyConfigId</span></span>
<span data-ttu-id="9d5db-120">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9d5db-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="9d5db-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="9d5db-121">-LegacyContainerNames</span></span>
<span data-ttu-id="9d5db-122">Anger en matris med volym behållar namn som migrations planen gäller för.</span><span class="sxs-lookup"><span data-stu-id="9d5db-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5db-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d5db-123">-Profile</span></span>
<span data-ttu-id="9d5db-124">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="9d5db-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5db-125">CommonParameters</span></span>
<span data-ttu-id="9d5db-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5db-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5db-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5db-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d5db-128">INPUTS</span></span>

## <span data-ttu-id="9d5db-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d5db-129">OUTPUTS</span></span>

## <span data-ttu-id="9d5db-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d5db-130">NOTES</span></span>

## <span data-ttu-id="9d5db-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d5db-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d5db-132">Bekräfta-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="9d5db-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="9d5db-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="9d5db-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


