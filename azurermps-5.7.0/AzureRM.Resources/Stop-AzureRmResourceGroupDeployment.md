---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583032"
---
# <span data-ttu-id="49eb9-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="49eb9-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="49eb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="49eb9-103">Avbryter en resurs grupps distribution.</span><span class="sxs-lookup"><span data-stu-id="49eb9-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49eb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49eb9-104">SYNTAX</span></span>

### <span data-ttu-id="49eb9-105">StopByResourceGroupDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="49eb9-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49eb9-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="49eb9-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49eb9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="49eb9-108">Cmdleten **Stop-AzureRmResourceGroupDeployment** avbryter en Azure Resource Group-distribution som har startat men inte slutförts.</span><span class="sxs-lookup"><span data-stu-id="49eb9-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="49eb9-109">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="49eb9-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="49eb9-110">En Azure-resurs är en användardefinierad enhet, till exempel en webbplats, databas eller databas server.</span><span class="sxs-lookup"><span data-stu-id="49eb9-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="49eb9-111">En resurs grupp är en samling resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="49eb9-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="49eb9-112">Använd New-AzureRmResourceGroupDeployment cmdlet för att distribuera en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="49eb9-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="49eb9-113">New-AzureRmResource-cmdleten skapar en ny resurs men den utlöser inte en distributions åtgärd för en resurs grupp som denna cmdlet kan stoppa.</span><span class="sxs-lookup"><span data-stu-id="49eb9-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="49eb9-114">Denna cmdlet stoppar bara en drift sättning.</span><span class="sxs-lookup"><span data-stu-id="49eb9-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="49eb9-115">Använd parametern *namn* för att stoppa en specifik distribution.</span><span class="sxs-lookup"><span data-stu-id="49eb9-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="49eb9-116">Om du utelämnar parametern *Name* söker **Stop-AzureRmResourceGroupDeployment** efter en pågående installation och stoppar den.</span><span class="sxs-lookup"><span data-stu-id="49eb9-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="49eb9-117">Om en cmdlet hittar mer än en drifts distribution Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="49eb9-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="49eb9-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49eb9-118">EXAMPLES</span></span>

## <span data-ttu-id="49eb9-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49eb9-119">PARAMETERS</span></span>

### <span data-ttu-id="49eb9-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49eb9-120">-ApiVersion</span></span>
<span data-ttu-id="49eb9-121">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="49eb9-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="49eb9-122">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="49eb9-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="49eb9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49eb9-123">-DefaultProfile</span></span>
<span data-ttu-id="49eb9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="49eb9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49eb9-125">-ID</span><span class="sxs-lookup"><span data-stu-id="49eb9-125">-Id</span></span>
<span data-ttu-id="49eb9-126">Anger ID för den resurs grupps distribution du vill stoppa.</span><span class="sxs-lookup"><span data-stu-id="49eb9-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49eb9-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="49eb9-127">-Name</span></span>
<span data-ttu-id="49eb9-128">Anger namnet på den resurs grupps distribution du vill stoppa.</span><span class="sxs-lookup"><span data-stu-id="49eb9-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="49eb9-129">Om du inte anger den här parametern söker den här cmdleten efter en distribuerad distribution i resurs gruppen och stoppar den.</span><span class="sxs-lookup"><span data-stu-id="49eb9-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="49eb9-130">Om det finns fler än en distribuerad distribution Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="49eb9-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="49eb9-131">Använd Get-AzureRmResourceGroupDeployment cmdlet för att få distributions namnet.</span><span class="sxs-lookup"><span data-stu-id="49eb9-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb9-132">-För</span><span class="sxs-lookup"><span data-stu-id="49eb9-132">-Pre</span></span>
<span data-ttu-id="49eb9-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="49eb9-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="49eb9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49eb9-134">-ResourceGroupName</span></span>
<span data-ttu-id="49eb9-135">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="49eb9-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="49eb9-136">Denna cmdlet stoppar distributionen av resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="49eb9-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49eb9-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49eb9-137">-Confirm</span></span>
<span data-ttu-id="49eb9-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49eb9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49eb9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49eb9-139">-WhatIf</span></span>
<span data-ttu-id="49eb9-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49eb9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49eb9-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49eb9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49eb9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49eb9-142">CommonParameters</span></span>
<span data-ttu-id="49eb9-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49eb9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49eb9-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49eb9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49eb9-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49eb9-145">INPUTS</span></span>

### <span data-ttu-id="49eb9-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="49eb9-146">None</span></span>

## <span data-ttu-id="49eb9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49eb9-147">OUTPUTS</span></span>

### <span data-ttu-id="49eb9-148">Returtyp</span><span class="sxs-lookup"><span data-stu-id="49eb9-148">Boolean</span></span>

## <span data-ttu-id="49eb9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49eb9-149">NOTES</span></span>

## <span data-ttu-id="49eb9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49eb9-150">RELATED LINKS</span></span>

[<span data-ttu-id="49eb9-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="49eb9-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="49eb9-152">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49eb9-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="49eb9-153">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49eb9-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="49eb9-154">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="49eb9-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="49eb9-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="49eb9-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="49eb9-156">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="49eb9-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


