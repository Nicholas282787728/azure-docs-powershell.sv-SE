---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093426"
---
# <span data-ttu-id="de236-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="de236-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="de236-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de236-102">SYNOPSIS</span></span>
<span data-ttu-id="de236-103">Initierar commit eller återställning av volym behållarna som migreras.</span><span class="sxs-lookup"><span data-stu-id="de236-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="de236-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de236-104">SYNTAX</span></span>

### <span data-ttu-id="de236-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="de236-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="de236-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="de236-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="de236-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de236-107">DESCRIPTION</span></span>
<span data-ttu-id="de236-108">Cmdleten **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** initierar eller återställningen av volym behållarna som migreras som en del av en bakåtkompatibel migrering.</span><span class="sxs-lookup"><span data-stu-id="de236-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="de236-109">Återställningen återställer apparaten till den ursprungliga ägande rätten.</span><span class="sxs-lookup"><span data-stu-id="de236-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="de236-110">Commit tilldelar ägandes Kap till mål apparaten.</span><span class="sxs-lookup"><span data-stu-id="de236-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="de236-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de236-111">EXAMPLES</span></span>

### <span data-ttu-id="de236-112">Exempel 1: initiera en Commit-åtgärd på en viss volym behållare</span><span class="sxs-lookup"><span data-stu-id="de236-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="de236-113">Det här kommandot initierar en Commit-åtgärd på den angivna volym behållaren för det angivna gamla konfigurations-ID: t.</span><span class="sxs-lookup"><span data-stu-id="de236-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="de236-114">Använd cmdleten **Get-AzureStorSimpleLegacyVolumeContainerStatus** för att se status för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="de236-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="de236-115">Exempel 2: initiera en återställnings åtgärd på en specifik volym behållare</span><span class="sxs-lookup"><span data-stu-id="de236-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="de236-116">Det här kommandot initierar en återställnings åtgärd på den angivna volym behållaren för det angivna gamla konfigurations-ID: t.</span><span class="sxs-lookup"><span data-stu-id="de236-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="de236-117">Exempel 3: initiera en Commit-åtgärd i alla volym behållare</span><span class="sxs-lookup"><span data-stu-id="de236-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="de236-118">Det här kommandot initierar en Commit-åtgärd för den angivna bakåtkompatibla konfigurations-ID: t.</span><span class="sxs-lookup"><span data-stu-id="de236-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="de236-119">Exempel 4: påbörja en återställnings åtgärd för alla volym behållare</span><span class="sxs-lookup"><span data-stu-id="de236-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="de236-120">Det här kommandot initierar en återställnings åtgärd för alla volym behållare för det angivna gamla konfigurations-ID: t.</span><span class="sxs-lookup"><span data-stu-id="de236-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="de236-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de236-121">PARAMETERS</span></span>

### <span data-ttu-id="de236-122">-Alla</span><span class="sxs-lookup"><span data-stu-id="de236-122">-All</span></span>
<span data-ttu-id="de236-123">Anger att denna cmdlet initierar en återställning eller commit för alla volym behållare i den importerade konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="de236-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de236-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="de236-124">-LegacyConfigId</span></span>
<span data-ttu-id="de236-125">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="de236-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="de236-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="de236-126">-LegacyContainerNames</span></span>
<span data-ttu-id="de236-127">Anger en matris med volym behållar namn som migrations planen gäller för.</span><span class="sxs-lookup"><span data-stu-id="de236-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de236-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="de236-128">-MigrationOperation</span></span>
<span data-ttu-id="de236-129">Anger om denna cmdlet utför en commit eller återställning.</span><span class="sxs-lookup"><span data-stu-id="de236-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="de236-130">Giltiga värden är: Commit och rollback.</span><span class="sxs-lookup"><span data-stu-id="de236-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="de236-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="de236-131">-Profile</span></span>
<span data-ttu-id="de236-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="de236-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de236-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="de236-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de236-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de236-134">CommonParameters</span></span>
<span data-ttu-id="de236-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de236-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de236-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de236-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de236-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de236-137">INPUTS</span></span>

## <span data-ttu-id="de236-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de236-138">OUTPUTS</span></span>

## <span data-ttu-id="de236-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de236-139">NOTES</span></span>

## <span data-ttu-id="de236-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de236-140">RELATED LINKS</span></span>

[<span data-ttu-id="de236-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="de236-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="de236-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="de236-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="de236-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="de236-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


