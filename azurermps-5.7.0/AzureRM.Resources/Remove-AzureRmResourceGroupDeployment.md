---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579420"
---
# <span data-ttu-id="e1936-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1936-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e1936-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1936-102">SYNOPSIS</span></span>
<span data-ttu-id="e1936-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e1936-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1936-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1936-104">SYNTAX</span></span>

### <span data-ttu-id="e1936-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="e1936-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1936-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e1936-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1936-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1936-107">DESCRIPTION</span></span>
<span data-ttu-id="e1936-108">Cmdleten **Remove-AzureRmResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e1936-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e1936-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1936-109">EXAMPLES</span></span>

## <span data-ttu-id="e1936-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1936-110">PARAMETERS</span></span>

### <span data-ttu-id="e1936-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1936-111">-ApiVersion</span></span>
<span data-ttu-id="e1936-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="e1936-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e1936-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="e1936-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1936-114">-DefaultProfile</span></span>
<span data-ttu-id="e1936-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e1936-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1936-116">-ID</span><span class="sxs-lookup"><span data-stu-id="e1936-116">-Id</span></span>
<span data-ttu-id="e1936-117">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e1936-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1936-118">-Name</span></span>
<span data-ttu-id="e1936-119">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e1936-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-120">-För</span><span class="sxs-lookup"><span data-stu-id="e1936-120">-Pre</span></span>
<span data-ttu-id="e1936-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1936-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1936-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1936-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1936-123">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e1936-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1936-124">-Confirm</span></span>
<span data-ttu-id="e1936-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1936-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1936-126">-WhatIf</span></span>
<span data-ttu-id="e1936-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1936-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1936-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1936-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1936-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1936-129">CommonParameters</span></span>
<span data-ttu-id="e1936-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1936-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1936-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1936-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1936-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1936-132">INPUTS</span></span>

### <span data-ttu-id="e1936-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="e1936-133">None</span></span>
<span data-ttu-id="e1936-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e1936-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1936-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1936-135">OUTPUTS</span></span>

### <span data-ttu-id="e1936-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1936-136">System.Boolean</span></span>

## <span data-ttu-id="e1936-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1936-137">NOTES</span></span>

## <span data-ttu-id="e1936-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1936-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1936-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1936-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e1936-140">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1936-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e1936-141">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1936-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e1936-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1936-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


