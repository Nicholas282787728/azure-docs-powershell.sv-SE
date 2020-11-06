---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575893"
---
# <span data-ttu-id="e9e23-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e9e23-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="e9e23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9e23-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e23-103">Tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="e9e23-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9e23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9e23-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9e23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9e23-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e23-106">Cmdleten **Remove-AzureRmRecoveryServicesAsrFabric** tar bort den angivna Azure Site Recovery-Fabric från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="e9e23-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="e9e23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9e23-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e23-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9e23-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="e9e23-109">Börjar ta bort angiven Fabric och returnerar det ASR-jobb som användes för att spåra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e9e23-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e9e23-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9e23-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e23-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e9e23-111">-Force</span></span>
<span data-ttu-id="e9e23-112">Tvinga kommandot att köras utan ytterligare en varning.</span><span class="sxs-lookup"><span data-stu-id="e9e23-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="e9e23-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9e23-113">-InputObject</span></span>
<span data-ttu-id="e9e23-114">Indatavärdet till cmdleten: det ASR Fabric-objekt som motsvarar infrastruktur resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e9e23-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9e23-115">-Confirm</span></span>
<span data-ttu-id="e9e23-116">Ange om du vill bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e9e23-116">Specify if confirmation is required.</span></span> <span data-ttu-id="e9e23-117">Ange värdet för parametern Confirm till $false för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="e9e23-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e23-118">-WhatIf</span></span>
<span data-ttu-id="e9e23-119">Visar vad som händer om cmdleten körs utan att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9e23-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e23-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e23-120">CommonParameters</span></span>
<span data-ttu-id="e9e23-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e23-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e23-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e23-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e23-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9e23-123">INPUTS</span></span>

### <span data-ttu-id="e9e23-124">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e9e23-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e9e23-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9e23-125">OUTPUTS</span></span>

### <span data-ttu-id="e9e23-126">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e9e23-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e9e23-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9e23-127">NOTES</span></span>

## <span data-ttu-id="e9e23-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9e23-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9e23-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e9e23-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="e9e23-130">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e9e23-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
