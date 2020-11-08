---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099783"
---
# <span data-ttu-id="4371d-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="4371d-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="4371d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4371d-102">SYNOPSIS</span></span>
<span data-ttu-id="4371d-103">Hämtar statusen för en genomförande eller återställning.</span><span class="sxs-lookup"><span data-stu-id="4371d-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="4371d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4371d-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4371d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4371d-105">DESCRIPTION</span></span>
<span data-ttu-id="4371d-106">Cmdleten **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** får statusen för commit eller rollback-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4371d-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="4371d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4371d-107">EXAMPLES</span></span>

### <span data-ttu-id="4371d-108">Exempel 1: få statusen för en slutförd Commit-åtgärd</span><span class="sxs-lookup"><span data-stu-id="4371d-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="4371d-109">Det här kommandot får statusen för en Commit-åtgärd för den namngivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="4371d-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="4371d-110">Åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="4371d-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="4371d-111">Exempel 2: få statusen för en slutförd återställnings åtgärd</span><span class="sxs-lookup"><span data-stu-id="4371d-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="4371d-112">Det här kommandot får statusen för en återställnings åtgärd för den namngivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="4371d-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="4371d-113">Åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="4371d-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="4371d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4371d-114">PARAMETERS</span></span>

### <span data-ttu-id="4371d-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="4371d-115">-LegacyConfigId</span></span>
<span data-ttu-id="4371d-116">Anger det unika ID: t för den äldre utrustningens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4371d-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="4371d-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="4371d-117">-LegacyContainerNames</span></span>
<span data-ttu-id="4371d-118">Anger en matris med volym behållar namn som migrations planen gäller för.</span><span class="sxs-lookup"><span data-stu-id="4371d-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="4371d-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="4371d-119">-Profile</span></span>
<span data-ttu-id="4371d-120">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="4371d-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4371d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4371d-121">CommonParameters</span></span>
<span data-ttu-id="4371d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4371d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4371d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4371d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4371d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4371d-124">INPUTS</span></span>

### <span data-ttu-id="4371d-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="4371d-125">None</span></span>

## <span data-ttu-id="4371d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4371d-126">OUTPUTS</span></span>

### <span data-ttu-id="4371d-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="4371d-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="4371d-128">Denna cmdlet returnerar statusen för den bekräftade migreringen som utförs.</span><span class="sxs-lookup"><span data-stu-id="4371d-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="4371d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4371d-129">NOTES</span></span>

## <span data-ttu-id="4371d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4371d-130">RELATED LINKS</span></span>

[<span data-ttu-id="4371d-131">Bekräfta-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="4371d-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="4371d-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="4371d-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


