---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093287"
---
# <span data-ttu-id="be143-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="be143-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="be143-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be143-102">SYNOPSIS</span></span>
<span data-ttu-id="be143-103">Hämtar volym behållar grupperna för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="be143-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="be143-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be143-104">SYNTAX</span></span>

### <span data-ttu-id="be143-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="be143-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="be143-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="be143-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="be143-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be143-107">DESCRIPTION</span></span>
<span data-ttu-id="be143-108">Cmdleten **Get-AzureStorSimpleFailoverVolumeContainers** hämtar volym behållar grupperna för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="be143-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="be143-109">Skicka en enda **VolumeContainer** -grupp eller en matris med **VolumeContainer** -grupper till cmdleten **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="be143-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="be143-110">Endast grupper som har ett värde för $True för egenskapen **IsDCGroupEligibleForDR** är berättigade till redundans.</span><span class="sxs-lookup"><span data-stu-id="be143-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="be143-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be143-111">EXAMPLES</span></span>

### <span data-ttu-id="be143-112">Exempel 1: Hämta volym behållare för redundans</span><span class="sxs-lookup"><span data-stu-id="be143-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="be143-113">Det här kommandot får volym behållare för redundans.</span><span class="sxs-lookup"><span data-stu-id="be143-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="be143-114">Endast DCGroups som har ett $True värde för egenskapen **IsDCGroupEligibleForDR** kan användas för redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="be143-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="be143-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be143-115">PARAMETERS</span></span>

### <span data-ttu-id="be143-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="be143-116">-DeviceId</span></span>
<span data-ttu-id="be143-117">Anger instans-ID för den StorSimple-enhet som cmdleten ska köras på.</span><span class="sxs-lookup"><span data-stu-id="be143-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be143-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="be143-118">-DeviceName</span></span>
<span data-ttu-id="be143-119">Anger namnet på den StorSimple-enhet som cmdleten ska köras på.</span><span class="sxs-lookup"><span data-stu-id="be143-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be143-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="be143-120">-Profile</span></span>
<span data-ttu-id="be143-121">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="be143-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="be143-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be143-122">CommonParameters</span></span>
<span data-ttu-id="be143-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be143-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be143-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be143-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be143-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be143-125">INPUTS</span></span>

## <span data-ttu-id="be143-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be143-126">OUTPUTS</span></span>

### <span data-ttu-id="be143-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="be143-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="be143-128">Denna cmdlet returnerar en lista med **VolumeContainer** Groups.</span><span class="sxs-lookup"><span data-stu-id="be143-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="be143-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be143-129">NOTES</span></span>

## <span data-ttu-id="be143-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be143-130">RELATED LINKS</span></span>

[<span data-ttu-id="be143-131">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="be143-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="be143-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="be143-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


