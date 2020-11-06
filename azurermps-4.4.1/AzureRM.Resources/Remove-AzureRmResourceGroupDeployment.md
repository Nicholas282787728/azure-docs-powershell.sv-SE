---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581292"
---
# <span data-ttu-id="61851-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="61851-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="61851-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61851-102">SYNOPSIS</span></span>
<span data-ttu-id="61851-103">Tar bort en resurs grupps distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="61851-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61851-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61851-104">SYNTAX</span></span>

### <span data-ttu-id="61851-105">Parametern för distributions namn.</span><span class="sxs-lookup"><span data-stu-id="61851-105">The deployment name parameter set.</span></span> <span data-ttu-id="61851-106">Vis</span><span class="sxs-lookup"><span data-stu-id="61851-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61851-107">Parametern distributions-ID.</span><span class="sxs-lookup"><span data-stu-id="61851-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61851-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61851-108">DESCRIPTION</span></span>
<span data-ttu-id="61851-109">Cmdleten **Remove-AzureRmResourceGroupDeployment** tar bort en Azure Resource Group-distribution och eventuella associerade åtgärder.</span><span class="sxs-lookup"><span data-stu-id="61851-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="61851-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61851-110">EXAMPLES</span></span>

## <span data-ttu-id="61851-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61851-111">PARAMETERS</span></span>

### <span data-ttu-id="61851-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="61851-112">-ApiVersion</span></span>
<span data-ttu-id="61851-113">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="61851-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="61851-114">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="61851-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="61851-115">-ID</span><span class="sxs-lookup"><span data-stu-id="61851-115">-Id</span></span>
<span data-ttu-id="61851-116">Anger ID för den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="61851-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61851-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="61851-117">-Name</span></span>
<span data-ttu-id="61851-118">Anger namnet på den resurs grupps distribution som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="61851-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61851-119">-För</span><span class="sxs-lookup"><span data-stu-id="61851-119">-Pre</span></span>
<span data-ttu-id="61851-120">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="61851-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="61851-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61851-121">-ResourceGroupName</span></span>
<span data-ttu-id="61851-122">Anger namnet på resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="61851-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61851-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="61851-123">-Confirm</span></span>
<span data-ttu-id="61851-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="61851-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61851-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61851-125">-WhatIf</span></span>
<span data-ttu-id="61851-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="61851-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61851-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="61851-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61851-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61851-128">-DefaultProfile</span></span>
<span data-ttu-id="61851-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61851-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61851-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61851-130">CommonParameters</span></span>
<span data-ttu-id="61851-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61851-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61851-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61851-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61851-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61851-133">INPUTS</span></span>

## <span data-ttu-id="61851-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61851-134">OUTPUTS</span></span>

### <span data-ttu-id="61851-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61851-135">System.Boolean</span></span>

## <span data-ttu-id="61851-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61851-136">NOTES</span></span>

## <span data-ttu-id="61851-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61851-137">RELATED LINKS</span></span>

[<span data-ttu-id="61851-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="61851-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="61851-139">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="61851-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="61851-140">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="61851-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="61851-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="61851-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


