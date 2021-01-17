---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398155"
---
# <span data-ttu-id="a4b50-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a4b50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4b50-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b50-103">Hämtar distributionerna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4b50-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="a4b50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4b50-104">SYNTAX</span></span>

### <span data-ttu-id="a4b50-105">GetByResourceGroupDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="a4b50-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b50-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a4b50-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4b50-107">DESCRIPTION</span></span>
<span data-ttu-id="a4b50-108">Cmdleten **Get-AzResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4b50-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="a4b50-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="a4b50-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a4b50-110">Som standard får **Get-AzResourceGroupDeployment** alla distributioner för en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4b50-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="a4b50-111">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="a4b50-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="a4b50-112">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="a4b50-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="a4b50-113">En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="a4b50-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="a4b50-114">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b50-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a4b50-115">Du kan använda denna cmdlet för att spåra.</span><span class="sxs-lookup"><span data-stu-id="a4b50-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="a4b50-116">För fel sökning kan du använda denna cmdlet med Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b50-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="a4b50-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4b50-117">EXAMPLES</span></span>

### <span data-ttu-id="a4b50-118">Exempel 1: Hämta alla distributioner för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a4b50-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="a4b50-119">Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="a4b50-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="a4b50-120">Resultatet visar en distribution av en WordPress-blogg som använde en mall.</span><span class="sxs-lookup"><span data-stu-id="a4b50-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="a4b50-121">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="a4b50-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="a4b50-122">Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4b50-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="a4b50-123">Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzResourceGroup** eller **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="a4b50-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="a4b50-124">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="a4b50-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="a4b50-125">Exempel 3: Hämta distributioner av alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="a4b50-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="a4b50-126">Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b50-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a4b50-127">Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="a4b50-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a4b50-128">Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName**, **DeploymentName** och **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="a4b50-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="a4b50-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4b50-129">PARAMETERS</span></span>

### <span data-ttu-id="a4b50-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b50-130">-DefaultProfile</span></span>
<span data-ttu-id="a4b50-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4b50-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b50-132">-ID</span><span class="sxs-lookup"><span data-stu-id="a4b50-132">-Id</span></span>
<span data-ttu-id="a4b50-133">Anger ID för den resurs grupps distribution som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="a4b50-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="a4b50-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4b50-134">-Name</span></span>
<span data-ttu-id="a4b50-135">Anger namnet på den distribution du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="a4b50-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="a4b50-136">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="a4b50-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a4b50-137">-För</span><span class="sxs-lookup"><span data-stu-id="a4b50-137">-Pre</span></span>
<span data-ttu-id="a4b50-138">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a4b50-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a4b50-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b50-139">-ResourceGroupName</span></span>
<span data-ttu-id="a4b50-140">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4b50-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a4b50-141">Cmdleten får distributionerna för resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a4b50-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="a4b50-142">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="a4b50-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="a4b50-143">Den här parametern är obligatorisk och du kan endast ange en resurs grupp för varje kommando.</span><span class="sxs-lookup"><span data-stu-id="a4b50-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="a4b50-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b50-144">CommonParameters</span></span>
<span data-ttu-id="a4b50-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b50-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b50-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b50-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b50-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4b50-147">INPUTS</span></span>

### <span data-ttu-id="a4b50-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b50-148">System.String</span></span>

## <span data-ttu-id="a4b50-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4b50-149">OUTPUTS</span></span>

### <span data-ttu-id="a4b50-150">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="a4b50-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4b50-151">NOTES</span></span>

## <span data-ttu-id="a4b50-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4b50-152">RELATED LINKS</span></span>

[<span data-ttu-id="a4b50-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4b50-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="a4b50-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4b50-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a4b50-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a4b50-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="a4b50-157">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a4b50-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4b50-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


