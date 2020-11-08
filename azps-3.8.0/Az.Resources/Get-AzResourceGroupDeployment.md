---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 1db46630ea4f864e1658eea8b789a79e6050fbbb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088726"
---
# <span data-ttu-id="989d4-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="989d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="989d4-102">SYNOPSIS</span></span>
<span data-ttu-id="989d4-103">Hämtar distributionerna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="989d4-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="989d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="989d4-104">SYNTAX</span></span>

### <span data-ttu-id="989d4-105">GetByResourceGroupDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="989d4-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989d4-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="989d4-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="989d4-107">DESCRIPTION</span></span>
<span data-ttu-id="989d4-108">Cmdleten **Get-AzResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="989d4-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="989d4-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="989d4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="989d4-110">Som standard får **Get-AzResourceGroupDeployment** alla distributioner för en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="989d4-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="989d4-111">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="989d4-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="989d4-112">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="989d4-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="989d4-113">En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="989d4-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="989d4-114">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="989d4-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="989d4-115">Du kan använda denna cmdlet för att spåra.</span><span class="sxs-lookup"><span data-stu-id="989d4-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="989d4-116">För fel sökning kan du använda denna cmdlet med Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="989d4-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="989d4-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="989d4-117">EXAMPLES</span></span>

### <span data-ttu-id="989d4-118">Exempel 1: Hämta alla distributioner för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="989d4-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="989d4-119">Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="989d4-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="989d4-120">Resultatet visar en distribution av en WordPress-blogg som använde en mall.</span><span class="sxs-lookup"><span data-stu-id="989d4-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="989d4-121">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="989d4-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="989d4-122">Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="989d4-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="989d4-123">Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzResourceGroup** eller **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="989d4-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="989d4-124">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="989d4-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="989d4-125">Exempel 3: Hämta distributioner av alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="989d4-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="989d4-126">Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="989d4-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="989d4-127">Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="989d4-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="989d4-128">Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName** , **DeploymentName** och **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="989d4-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="989d4-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="989d4-129">PARAMETERS</span></span>

### <span data-ttu-id="989d4-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="989d4-130">-ApiVersion</span></span>
<span data-ttu-id="989d4-131">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="989d4-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="989d4-132">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="989d4-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="989d4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989d4-133">-DefaultProfile</span></span>
<span data-ttu-id="989d4-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="989d4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="989d4-135">-ID</span><span class="sxs-lookup"><span data-stu-id="989d4-135">-Id</span></span>
<span data-ttu-id="989d4-136">Anger ID för den resurs grupps distribution som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="989d4-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="989d4-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="989d4-137">-Name</span></span>
<span data-ttu-id="989d4-138">Anger namnet på den distribution du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="989d4-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="989d4-139">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="989d4-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="989d4-140">-För</span><span class="sxs-lookup"><span data-stu-id="989d4-140">-Pre</span></span>
<span data-ttu-id="989d4-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="989d4-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="989d4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989d4-142">-ResourceGroupName</span></span>
<span data-ttu-id="989d4-143">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="989d4-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="989d4-144">Cmdleten får distributionerna för resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="989d4-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="989d4-145">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="989d4-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="989d4-146">Den här parametern är obligatorisk och du kan endast ange en resurs grupp för varje kommando.</span><span class="sxs-lookup"><span data-stu-id="989d4-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="989d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989d4-147">CommonParameters</span></span>
<span data-ttu-id="989d4-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989d4-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="989d4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989d4-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="989d4-150">INPUTS</span></span>

### <span data-ttu-id="989d4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="989d4-151">System.String</span></span>

## <span data-ttu-id="989d4-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="989d4-152">OUTPUTS</span></span>

### <span data-ttu-id="989d4-153">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-153">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="989d4-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="989d4-154">NOTES</span></span>

## <span data-ttu-id="989d4-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="989d4-155">RELATED LINKS</span></span>

[<span data-ttu-id="989d4-156">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="989d4-156">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="989d4-157">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="989d4-157">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="989d4-158">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-158">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="989d4-159">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-159">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="989d4-160">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-160">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="989d4-161">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="989d4-161">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

