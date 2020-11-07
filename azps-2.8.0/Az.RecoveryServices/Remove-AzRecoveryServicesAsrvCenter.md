---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919704"
---
# <span data-ttu-id="5d10c-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="5d10c-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="5d10c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d10c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d10c-103">Tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="5d10c-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="5d10c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d10c-104">SYNTAX</span></span>

### <span data-ttu-id="5d10c-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="5d10c-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d10c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d10c-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d10c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5d10c-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d10c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d10c-108">DESCRIPTION</span></span>
<span data-ttu-id="5d10c-109">Cmdleten **Remove-AzRecoveryServicesAsrvCenter** tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="5d10c-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="5d10c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d10c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d10c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5d10c-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="5d10c-112">Tar bort vCenter-servern från ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="5d10c-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="5d10c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d10c-113">PARAMETERS</span></span>

### <span data-ttu-id="5d10c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d10c-114">-DefaultProfile</span></span>
<span data-ttu-id="5d10c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d10c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="5d10c-116">-Fabric</span></span>
<span data-ttu-id="5d10c-117">ASR Fabric-objekt som representerar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="5d10c-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d10c-118">-InputObject</span></span>
<span data-ttu-id="5d10c-119">ASR vCenter-objekt som representerar vCenter-servern som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5d10c-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d10c-120">-Name</span></span>
<span data-ttu-id="5d10c-121">Namn på vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="5d10c-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d10c-122">-ResourceId</span></span>
<span data-ttu-id="5d10c-123">Anger resourceId för vCenter som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5d10c-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d10c-124">-Confirm</span></span>
<span data-ttu-id="5d10c-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d10c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d10c-126">-WhatIf</span></span>
<span data-ttu-id="5d10c-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d10c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d10c-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d10c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d10c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d10c-129">CommonParameters</span></span>
<span data-ttu-id="5d10c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d10c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d10c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d10c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d10c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d10c-132">INPUTS</span></span>

### <span data-ttu-id="5d10c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5d10c-133">System.String</span></span>

### <span data-ttu-id="5d10c-134">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="5d10c-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="5d10c-135">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5d10c-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5d10c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d10c-136">OUTPUTS</span></span>

### <span data-ttu-id="5d10c-137">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5d10c-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5d10c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d10c-138">NOTES</span></span>

## <span data-ttu-id="5d10c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d10c-139">RELATED LINKS</span></span>
