---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583496"
---
# <span data-ttu-id="cd4da-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="cd4da-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="cd4da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd4da-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4da-103">Tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="cd4da-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd4da-104">SYNTAX</span></span>

### <span data-ttu-id="cd4da-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="cd4da-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4da-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd4da-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4da-107">ByName</span><span class="sxs-lookup"><span data-stu-id="cd4da-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd4da-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd4da-108">DESCRIPTION</span></span>
<span data-ttu-id="cd4da-109">Cmdleten **Remove-AzureRmRecoveryServicesAsrvCenter** tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="cd4da-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="cd4da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd4da-110">EXAMPLES</span></span>

### <span data-ttu-id="cd4da-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd4da-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="cd4da-112">Tar bort vCenter-servern från ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="cd4da-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="cd4da-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd4da-113">PARAMETERS</span></span>

### <span data-ttu-id="cd4da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4da-114">-DefaultProfile</span></span>
<span data-ttu-id="cd4da-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd4da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4da-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="cd4da-116">-Fabric</span></span>
<span data-ttu-id="cd4da-117">ASR Fabric-objekt som representerar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="cd4da-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="cd4da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd4da-118">-InputObject</span></span>
<span data-ttu-id="cd4da-119">ASR vCenter-objekt som representerar vCenter-servern som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cd4da-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="cd4da-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd4da-120">-Name</span></span>
<span data-ttu-id="cd4da-121">Namn på vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="cd4da-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="cd4da-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd4da-122">-ResourceId</span></span>
<span data-ttu-id="cd4da-123">Anger resourceId för vCenter som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cd4da-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="cd4da-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd4da-124">-Confirm</span></span>
<span data-ttu-id="cd4da-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd4da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4da-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4da-126">-WhatIf</span></span>
<span data-ttu-id="cd4da-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd4da-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd4da-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd4da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4da-129">CommonParameters</span></span>
<span data-ttu-id="cd4da-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4da-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4da-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd4da-132">INPUTS</span></span>

### <span data-ttu-id="cd4da-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="cd4da-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="cd4da-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd4da-134">OUTPUTS</span></span>

### <span data-ttu-id="cd4da-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd4da-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cd4da-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd4da-136">NOTES</span></span>

## <span data-ttu-id="cd4da-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd4da-137">RELATED LINKS</span></span>
