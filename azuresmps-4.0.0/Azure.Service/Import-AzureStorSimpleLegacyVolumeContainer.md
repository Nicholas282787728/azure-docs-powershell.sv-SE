---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099488"
---
# <span data-ttu-id="2d22d-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="2d22d-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="2d22d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d22d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d22d-103">Startar migreringen av volym behållare.</span><span class="sxs-lookup"><span data-stu-id="2d22d-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="2d22d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d22d-104">SYNTAX</span></span>

### <span data-ttu-id="2d22d-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="2d22d-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2d22d-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="2d22d-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d22d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d22d-107">DESCRIPTION</span></span>
<span data-ttu-id="2d22d-108">Cmdleten **import-AzureStorSimpleLegacyVolumeContainer** startar migreringen av volym behållare från en äldre apparat till mål apparaten.</span><span class="sxs-lookup"><span data-stu-id="2d22d-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="2d22d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d22d-109">EXAMPLES</span></span>

### <span data-ttu-id="2d22d-110">Exempel 1: importera en äldre volym behållare</span><span class="sxs-lookup"><span data-stu-id="2d22d-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="2d22d-111">Det här kommandot importerar en äldre volym behållare för den namngivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="2d22d-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="2d22d-112">Cmdleten startar importen och returnerar sedan ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="2d22d-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="2d22d-113">Exempel 2: importera alla gamla volym behållare</span><span class="sxs-lookup"><span data-stu-id="2d22d-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="2d22d-114">Det här kommandot importerar alla gamla volym behållare från konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="2d22d-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="2d22d-115">Cmdleten startar importen och returnerar sedan ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="2d22d-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="2d22d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d22d-116">PARAMETERS</span></span>

### <span data-ttu-id="2d22d-117">-Alla</span><span class="sxs-lookup"><span data-stu-id="2d22d-117">-All</span></span>
<span data-ttu-id="2d22d-118">Anger att denna cmdlet importerar alla volym behållare i den importerade konfigurations filen till mål enheten.</span><span class="sxs-lookup"><span data-stu-id="2d22d-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="2d22d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2d22d-119">-Force</span></span>
<span data-ttu-id="2d22d-120">Anger att denna cmdlet importerar volym behållaren på en annan enhet, även om volymen är importerad på en annan enhet.</span><span class="sxs-lookup"><span data-stu-id="2d22d-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

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

### <span data-ttu-id="2d22d-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="2d22d-121">-LegacyConfigId</span></span>
<span data-ttu-id="2d22d-122">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d22d-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="2d22d-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="2d22d-123">-LegacyContainerNames</span></span>
<span data-ttu-id="2d22d-124">Anger en matris med volym behållar namn som migrations planen gäller för.</span><span class="sxs-lookup"><span data-stu-id="2d22d-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="2d22d-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="2d22d-125">-Profile</span></span>
<span data-ttu-id="2d22d-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2d22d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d22d-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2d22d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d22d-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="2d22d-128">-SkipACRs</span></span>
<span data-ttu-id="2d22d-129">Anger att importen hoppar över åtkomst kontroll poster för migrering.</span><span class="sxs-lookup"><span data-stu-id="2d22d-129">Indicates that the import process skips access control records for migration.</span></span>

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

### <span data-ttu-id="2d22d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d22d-130">CommonParameters</span></span>
<span data-ttu-id="2d22d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d22d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d22d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d22d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d22d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d22d-133">INPUTS</span></span>

## <span data-ttu-id="2d22d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d22d-134">OUTPUTS</span></span>

### <span data-ttu-id="2d22d-135">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="2d22d-135">String</span></span>
<span data-ttu-id="2d22d-136">Det här kommandot returnerar statusen för åtgärden beställnings import volym om den har startats.</span><span class="sxs-lookup"><span data-stu-id="2d22d-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="2d22d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d22d-137">NOTES</span></span>

## <span data-ttu-id="2d22d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d22d-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d22d-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="2d22d-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="2d22d-140">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="2d22d-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


