---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099003"
---
# <span data-ttu-id="49727-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="49727-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="49727-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49727-102">SYNOPSIS</span></span>
<span data-ttu-id="49727-103">Skapar ett migreringsarkiv.</span><span class="sxs-lookup"><span data-stu-id="49727-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="49727-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49727-104">SYNTAX</span></span>

### <span data-ttu-id="49727-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="49727-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="49727-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="49727-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="49727-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49727-107">DESCRIPTION</span></span>
<span data-ttu-id="49727-108">Cmdleten **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** börjar skapa ett migreringsarkiv.</span><span class="sxs-lookup"><span data-stu-id="49727-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="49727-109">Skapandet av ett migreringsarkiv är asynkront.</span><span class="sxs-lookup"><span data-stu-id="49727-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="49727-110">Använd cmdleten **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** för att se status för migreringsarkivet.</span><span class="sxs-lookup"><span data-stu-id="49727-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="49727-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49727-111">EXAMPLES</span></span>

### <span data-ttu-id="49727-112">Exempel 1: starta ett migreringsarkiv</span><span class="sxs-lookup"><span data-stu-id="49727-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="49727-113">Det här kommandot börjar skapa ett migreringsarkiv för den äldre behållaren med namnet OneSDKAzureCloud.</span><span class="sxs-lookup"><span data-stu-id="49727-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="49727-114">Kommandot returnerar ett meddelande om planens status och för att använda cmdleten **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** för uppdaterade uppgifter.</span><span class="sxs-lookup"><span data-stu-id="49727-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="49727-115">Exempel 2: starta ett migreringsarkiv för alla volym behållare</span><span class="sxs-lookup"><span data-stu-id="49727-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="49727-116">Det här kommandot börjar skapa ett migreringsarkiv för alla gamla volym behållare i konfigurations filen som importeras.</span><span class="sxs-lookup"><span data-stu-id="49727-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="49727-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49727-117">PARAMETERS</span></span>

### <span data-ttu-id="49727-118">-Alla</span><span class="sxs-lookup"><span data-stu-id="49727-118">-All</span></span>
<span data-ttu-id="49727-119">Anger att den här cmdleten ska börja uppskattad migrations tid för alla volym behållare i den importerade konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="49727-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="49727-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="49727-120">-LegacyConfigId</span></span>
<span data-ttu-id="49727-121">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="49727-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="49727-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="49727-122">-LegacyContainerNames</span></span>
<span data-ttu-id="49727-123">Anger en matris med volym behållar namn som du vill skapa ett migreringsarkiv för.</span><span class="sxs-lookup"><span data-stu-id="49727-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="49727-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="49727-124">-Profile</span></span>
<span data-ttu-id="49727-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="49727-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49727-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="49727-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49727-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49727-127">CommonParameters</span></span>
<span data-ttu-id="49727-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49727-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49727-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49727-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49727-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49727-130">INPUTS</span></span>

### <span data-ttu-id="49727-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="49727-131">None</span></span>

## <span data-ttu-id="49727-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49727-132">OUTPUTS</span></span>

### <span data-ttu-id="49727-133">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="49727-133">String</span></span>
<span data-ttu-id="49727-134">Denna cmdlet returnerar statusen för migreringsjobbet om den har startats.</span><span class="sxs-lookup"><span data-stu-id="49727-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="49727-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49727-135">NOTES</span></span>

## <span data-ttu-id="49727-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49727-136">RELATED LINKS</span></span>

[<span data-ttu-id="49727-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="49727-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


