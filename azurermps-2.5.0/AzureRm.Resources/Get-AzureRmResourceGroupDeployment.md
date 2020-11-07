---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 9da5ee691b440ee24933d658dec3c85b1a7c8ced
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928973"
---
# <span data-ttu-id="6e9c0-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="6e9c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e9c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9c0-103">Hämtar distributionerna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e9c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e9c0-104">SYNTAX</span></span>

### <span data-ttu-id="6e9c0-105">GetByResourceGroupDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="6e9c0-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e9c0-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6e9c0-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e9c0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e9c0-107">DESCRIPTION</span></span>
<span data-ttu-id="6e9c0-108">Cmdleten **Get-AzureRmResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="6e9c0-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="6e9c0-110">Som standard får **Get-AzureRmResourceGroupDeployment** alla distributioner för en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="6e9c0-111">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="6e9c0-112">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="6e9c0-113">En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="6e9c0-114">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="6e9c0-115">Du kan använda denna cmdlet för att spåra.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="6e9c0-116">För fel sökning kan du använda denna cmdlet med Get-AzureRmLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="6e9c0-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e9c0-117">EXAMPLES</span></span>

### <span data-ttu-id="6e9c0-118">Exempel 1: Hämta alla distributioner för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6e9c0-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="6e9c0-119">Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6e9c0-120">Resultatet visar en distribution av en WordPress-blogg som använde en mall.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="6e9c0-121">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="6e9c0-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="6e9c0-122">Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6e9c0-123">Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzureRmResourceGroup** eller **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="6e9c0-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="6e9c0-124">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="6e9c0-125">Exempel 3: Hämta distributioner av alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="6e9c0-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="6e9c0-126">Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="6e9c0-127">Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6e9c0-128">Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName** , **DeploymentName** och **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="6e9c0-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="6e9c0-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e9c0-129">PARAMETERS</span></span>

### <span data-ttu-id="6e9c0-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e9c0-130">-ApiVersion</span></span>
<span data-ttu-id="6e9c0-131">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6e9c0-132">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6e9c0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9c0-133">-DefaultProfile</span></span>
<span data-ttu-id="6e9c0-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6e9c0-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e9c0-135">-ID</span><span class="sxs-lookup"><span data-stu-id="6e9c0-135">-Id</span></span>
<span data-ttu-id="6e9c0-136">Anger ID för den resurs grupps distribution som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c0-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e9c0-137">-Name</span></span>
<span data-ttu-id="6e9c0-138">Anger namnet på den distribution du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="6e9c0-139">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c0-140">-För</span><span class="sxs-lookup"><span data-stu-id="6e9c0-140">-Pre</span></span>
<span data-ttu-id="6e9c0-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e9c0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e9c0-142">-ResourceGroupName</span></span>
<span data-ttu-id="6e9c0-143">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6e9c0-144">Cmdleten får distributionerna för resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="6e9c0-145">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="6e9c0-146">Den här parametern är obligatorisk och du kan endast ange en resurs grupp för varje kommando.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9c0-147">CommonParameters</span></span>
<span data-ttu-id="6e9c0-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9c0-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9c0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9c0-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e9c0-150">INPUTS</span></span>

### <span data-ttu-id="6e9c0-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="6e9c0-151">None</span></span>

## <span data-ttu-id="6e9c0-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e9c0-152">OUTPUTS</span></span>

### <span data-ttu-id="6e9c0-153">Microsoft. Azure. commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="6e9c0-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="6e9c0-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="6e9c0-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e9c0-155">NOTES</span></span>

## <span data-ttu-id="6e9c0-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e9c0-156">RELATED LINKS</span></span>

[<span data-ttu-id="6e9c0-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e9c0-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="6e9c0-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e9c0-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="6e9c0-159">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6e9c0-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6e9c0-161">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="6e9c0-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e9c0-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


