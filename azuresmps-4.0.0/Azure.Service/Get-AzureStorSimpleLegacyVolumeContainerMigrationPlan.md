---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093282"
---
# <span data-ttu-id="59824-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="59824-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="59824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59824-102">SYNOPSIS</span></span>
<span data-ttu-id="59824-103">Hämtar migreringsåtgärder för äldre behållare.</span><span class="sxs-lookup"><span data-stu-id="59824-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="59824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59824-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="59824-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59824-105">DESCRIPTION</span></span>
<span data-ttu-id="59824-106">Cmdleten **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** hämtar migrations planer för äldre behållare.</span><span class="sxs-lookup"><span data-stu-id="59824-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="59824-107">Ange ett migreringsarkiv med dess gamla konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="59824-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="59824-108">Om det fortfarande pågår att det inte går att skapa en migrerings plan får denna cmdlet status för migreringsarkivet.</span><span class="sxs-lookup"><span data-stu-id="59824-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="59824-109">Om migreringen är slutförd returnerar denna cmdlet den faktiska migrations planen för uppsättningen med äldre behållare.</span><span class="sxs-lookup"><span data-stu-id="59824-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="59824-110">Om du inte anger parametern *LegacyConfigId* returnerar denna cmdlet en lista med konfigurations-ID: n.</span><span class="sxs-lookup"><span data-stu-id="59824-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="59824-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59824-111">EXAMPLES</span></span>

### <span data-ttu-id="59824-112">Exempel 1: få statusen för en plan</span><span class="sxs-lookup"><span data-stu-id="59824-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="59824-113">Det här kommandot får migreringens status.</span><span class="sxs-lookup"><span data-stu-id="59824-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="59824-114">Statusen inkluderar förväntad bandbredd, uppskattad tid och relaterad information.</span><span class="sxs-lookup"><span data-stu-id="59824-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="59824-115">Exempel 2: Hämta ID för befintliga abonnemang</span><span class="sxs-lookup"><span data-stu-id="59824-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="59824-116">Det här kommandot får alla konfigurations-ID: n för migrations planer.</span><span class="sxs-lookup"><span data-stu-id="59824-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="59824-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59824-117">PARAMETERS</span></span>

### <span data-ttu-id="59824-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="59824-118">-LegacyConfigId</span></span>
<span data-ttu-id="59824-119">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="59824-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="59824-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="59824-120">-LegacyContainerNames</span></span>
<span data-ttu-id="59824-121">Anger en matris med volym behållar namn för vilka denna cmdlet får ett migreringsarkiv.</span><span class="sxs-lookup"><span data-stu-id="59824-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="59824-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="59824-122">-Profile</span></span>
<span data-ttu-id="59824-123">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="59824-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="59824-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59824-124">CommonParameters</span></span>
<span data-ttu-id="59824-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59824-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59824-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59824-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59824-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59824-127">INPUTS</span></span>

### <span data-ttu-id="59824-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="59824-128">None</span></span>

## <span data-ttu-id="59824-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59824-129">OUTPUTS</span></span>

### <span data-ttu-id="59824-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="59824-130">MigrationPlanMsg</span></span>
<span data-ttu-id="59824-131">Denna cmdlet returnerar ett **MigrationPlanMsg** -objekt som innehåller status för jobbet för migrering, förmodad bandbredd i megabit per sekund och uppskattad tid i minuter.</span><span class="sxs-lookup"><span data-stu-id="59824-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="59824-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59824-132">NOTES</span></span>

## <span data-ttu-id="59824-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59824-133">RELATED LINKS</span></span>

[<span data-ttu-id="59824-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="59824-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


