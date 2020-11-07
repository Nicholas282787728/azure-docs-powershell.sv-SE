---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: da66d0cacbddbeb53972308faa681bde42c813d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923810"
---
# <span data-ttu-id="2c0c4-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c0c4-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="2c0c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0c4-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="2c0c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c0c4-104">SYNTAX</span></span>

### <span data-ttu-id="2c0c4-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="2c0c4-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c0c4-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2c0c4-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c0c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c0c4-107">DESCRIPTION</span></span>
<span data-ttu-id="2c0c4-108">Cmdleten **Remove-AzResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="2c0c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c0c4-109">EXAMPLES</span></span>

## <span data-ttu-id="2c0c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="2c0c4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2c0c4-111">-ApiVersion</span></span>
<span data-ttu-id="2c0c4-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2c0c4-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2c0c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0c4-114">-DefaultProfile</span></span>
<span data-ttu-id="2c0c4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2c0c4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0c4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2c0c4-116">-Id</span></span>
<span data-ttu-id="2c0c4-117">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="2c0c4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c0c4-118">-Name</span></span>
<span data-ttu-id="2c0c4-119">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="2c0c4-120">-För</span><span class="sxs-lookup"><span data-stu-id="2c0c4-120">-Pre</span></span>
<span data-ttu-id="2c0c4-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2c0c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c0c4-123">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="2c0c4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c0c4-124">-Confirm</span></span>
<span data-ttu-id="2c0c4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c0c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c0c4-126">-WhatIf</span></span>
<span data-ttu-id="2c0c4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c0c4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c0c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0c4-129">CommonParameters</span></span>
<span data-ttu-id="2c0c4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0c4-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c0c4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0c4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c0c4-132">INPUTS</span></span>

### <span data-ttu-id="2c0c4-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="2c0c4-133">None</span></span>

## <span data-ttu-id="2c0c4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c0c4-134">OUTPUTS</span></span>

## <span data-ttu-id="2c0c4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c0c4-135">NOTES</span></span>

## <span data-ttu-id="2c0c4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c0c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="2c0c4-137">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c0c4-137">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="2c0c4-138">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c0c4-138">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="2c0c4-139">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c0c4-139">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="2c0c4-140">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c0c4-140">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


