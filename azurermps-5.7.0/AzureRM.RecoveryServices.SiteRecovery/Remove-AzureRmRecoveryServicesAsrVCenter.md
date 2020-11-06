---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576467"
---
# <span data-ttu-id="ae40e-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="ae40e-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="ae40e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae40e-102">SYNOPSIS</span></span>
<span data-ttu-id="ae40e-103">Tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="ae40e-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae40e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae40e-104">SYNTAX</span></span>

### <span data-ttu-id="ae40e-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="ae40e-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae40e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae40e-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae40e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ae40e-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae40e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae40e-108">DESCRIPTION</span></span>
<span data-ttu-id="ae40e-109">Cmdleten **Remove-AzureRmRecoveryServicesAsrvCenter** tar bort vCenter-servern från ASR-Fabric och slutar upptäcka virtuella datorer från vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="ae40e-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="ae40e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae40e-110">EXAMPLES</span></span>

### <span data-ttu-id="ae40e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae40e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="ae40e-112">Tar bort vCenter-servern från ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="ae40e-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="ae40e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae40e-113">PARAMETERS</span></span>

### <span data-ttu-id="ae40e-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae40e-114">-Confirm</span></span>
<span data-ttu-id="ae40e-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae40e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae40e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae40e-116">-DefaultProfile</span></span>
<span data-ttu-id="ae40e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae40e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae40e-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="ae40e-118">-Fabric</span></span>
<span data-ttu-id="ae40e-119">ASR Fabric-objekt som representerar konfigurations servern.</span><span class="sxs-lookup"><span data-stu-id="ae40e-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae40e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae40e-120">-InputObject</span></span>
<span data-ttu-id="ae40e-121">ASR vCenter-objekt som representerar vCenter-servern som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ae40e-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae40e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae40e-122">-Name</span></span>
<span data-ttu-id="ae40e-123">Namn på vCenter-servern.</span><span class="sxs-lookup"><span data-stu-id="ae40e-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae40e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae40e-124">-ResourceId</span></span>
<span data-ttu-id="ae40e-125">Anger resourceId för vCenter som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ae40e-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae40e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae40e-126">-WhatIf</span></span>
<span data-ttu-id="ae40e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae40e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae40e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae40e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae40e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae40e-129">CommonParameters</span></span>
<span data-ttu-id="ae40e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae40e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae40e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae40e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae40e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae40e-132">INPUTS</span></span>

### <span data-ttu-id="ae40e-133">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="ae40e-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="ae40e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae40e-134">OUTPUTS</span></span>

### <span data-ttu-id="ae40e-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae40e-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ae40e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae40e-136">NOTES</span></span>

## <span data-ttu-id="ae40e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae40e-137">RELATED LINKS</span></span>
