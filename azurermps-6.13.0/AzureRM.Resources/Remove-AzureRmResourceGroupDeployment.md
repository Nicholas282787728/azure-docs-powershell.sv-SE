---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 19662972e115acb0e3a194e14abf3f956d39035e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576100"
---
# <span data-ttu-id="d037d-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d037d-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d037d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d037d-102">SYNOPSIS</span></span>
<span data-ttu-id="d037d-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d037d-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d037d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d037d-104">SYNTAX</span></span>

### <span data-ttu-id="d037d-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="d037d-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d037d-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d037d-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d037d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d037d-107">DESCRIPTION</span></span>
<span data-ttu-id="d037d-108">Cmdleten **Remove-AzureRmResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d037d-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="d037d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d037d-109">EXAMPLES</span></span>

## <span data-ttu-id="d037d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d037d-110">PARAMETERS</span></span>

### <span data-ttu-id="d037d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d037d-111">-ApiVersion</span></span>
<span data-ttu-id="d037d-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="d037d-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d037d-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="d037d-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d037d-114">-DefaultProfile</span></span>
<span data-ttu-id="d037d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d037d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d037d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d037d-116">-Id</span></span>
<span data-ttu-id="d037d-117">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d037d-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d037d-118">-Name</span></span>
<span data-ttu-id="d037d-119">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d037d-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-120">-För</span><span class="sxs-lookup"><span data-stu-id="d037d-120">-Pre</span></span>
<span data-ttu-id="d037d-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d037d-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d037d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d037d-123">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d037d-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d037d-124">-Confirm</span></span>
<span data-ttu-id="d037d-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d037d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d037d-126">-WhatIf</span></span>
<span data-ttu-id="d037d-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d037d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d037d-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d037d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d037d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d037d-129">CommonParameters</span></span>
<span data-ttu-id="d037d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d037d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d037d-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d037d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d037d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d037d-132">INPUTS</span></span>

### <span data-ttu-id="d037d-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="d037d-133">None</span></span>

## <span data-ttu-id="d037d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d037d-134">OUTPUTS</span></span>

## <span data-ttu-id="d037d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d037d-135">NOTES</span></span>

## <span data-ttu-id="d037d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d037d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d037d-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d037d-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d037d-138">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d037d-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d037d-139">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d037d-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d037d-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d037d-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


