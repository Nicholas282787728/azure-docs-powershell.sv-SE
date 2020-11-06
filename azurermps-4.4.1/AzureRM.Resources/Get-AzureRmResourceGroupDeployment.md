---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581336"
---
# <span data-ttu-id="8808e-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8808e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8808e-102">SYNOPSIS</span></span>
<span data-ttu-id="8808e-103">Hämtar distributionerna i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8808e-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8808e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8808e-104">SYNTAX</span></span>

### <span data-ttu-id="8808e-105">Parametern för distributions namn.</span><span class="sxs-lookup"><span data-stu-id="8808e-105">The deployment name parameter set.</span></span> <span data-ttu-id="8808e-106">Vis</span><span class="sxs-lookup"><span data-stu-id="8808e-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8808e-107">Parametern distributions-ID.</span><span class="sxs-lookup"><span data-stu-id="8808e-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8808e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8808e-108">DESCRIPTION</span></span>
<span data-ttu-id="8808e-109">Cmdleten **Get-AzureRmResourceGroupDeployment** hämtar distributionerna i en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8808e-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="8808e-110">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="8808e-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="8808e-111">Som standard får **Get-AzureRmResourceGroupDeployment** alla distributioner för en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8808e-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="8808e-112">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="8808e-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="8808e-113">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="8808e-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="8808e-114">En distribution är den åtgärd som gör resurserna i resurs gruppen tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="8808e-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="8808e-115">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8808e-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="8808e-116">Du kan använda denna cmdlet för att spåra.</span><span class="sxs-lookup"><span data-stu-id="8808e-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="8808e-117">För fel sökning kan du använda denna cmdlet med Get-AzureRmLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8808e-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="8808e-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8808e-118">EXAMPLES</span></span>

### <span data-ttu-id="8808e-119">Exempel 1: Hämta alla distributioner för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8808e-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="8808e-120">Det här kommandot får alla distributioner för resurs gruppen ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="8808e-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8808e-121">Resultatet visar en distribution av en WordPress-blogg som använde en mall.</span><span class="sxs-lookup"><span data-stu-id="8808e-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="8808e-122">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="8808e-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="8808e-123">Det här kommandot får DeployWebsite01 distributionen av ContosoLabsRG-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8808e-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8808e-124">Du kan tilldela en distribution ett namn när du skapar den med hjälp av cmdletarna **New-AzureRmResourceGroup** eller **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="8808e-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="8808e-125">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="8808e-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="8808e-126">Exempel 3: Hämta distributioner av alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="8808e-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="8808e-127">Det här kommandot får alla resurs grupper i ditt abonnemang med hjälp av Get-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8808e-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="8808e-128">Kommandot skickar resurs grupperna till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="8808e-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8808e-129">Den aktuella cmdleten hämtar alla resurs grupper i prenumerationen och skickar resultaten till Format-Table cmdlet för att visa deras egenskaps värden för **ResourceGroupName** , **DeploymentName** och **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="8808e-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="8808e-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8808e-130">PARAMETERS</span></span>

### <span data-ttu-id="8808e-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8808e-131">-ApiVersion</span></span>
<span data-ttu-id="8808e-132">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="8808e-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8808e-133">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="8808e-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8808e-134">-ID</span><span class="sxs-lookup"><span data-stu-id="8808e-134">-Id</span></span>
<span data-ttu-id="8808e-135">Anger ID för den resurs grupps distribution som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="8808e-135">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="8808e-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="8808e-136">-Name</span></span>
<span data-ttu-id="8808e-137">Anger namnet på den distribution du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="8808e-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="8808e-138">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="8808e-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8808e-139">-För</span><span class="sxs-lookup"><span data-stu-id="8808e-139">-Pre</span></span>
<span data-ttu-id="8808e-140">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8808e-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8808e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8808e-141">-ResourceGroupName</span></span>
<span data-ttu-id="8808e-142">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8808e-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8808e-143">Cmdleten får distributionerna för resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8808e-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="8808e-144">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="8808e-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="8808e-145">Den här parametern är obligatorisk och du kan endast ange en resurs grupp för varje kommando.</span><span class="sxs-lookup"><span data-stu-id="8808e-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8808e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8808e-146">-DefaultProfile</span></span>
<span data-ttu-id="8808e-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8808e-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8808e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8808e-148">CommonParameters</span></span>
<span data-ttu-id="8808e-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8808e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8808e-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8808e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8808e-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8808e-151">INPUTS</span></span>

### <span data-ttu-id="8808e-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="8808e-152">None</span></span>

## <span data-ttu-id="8808e-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8808e-153">OUTPUTS</span></span>

### <span data-ttu-id="8808e-154">Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="8808e-155">Cmdleten returnerar distributioner av resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="8808e-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="8808e-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8808e-156">NOTES</span></span>

## <span data-ttu-id="8808e-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8808e-157">RELATED LINKS</span></span>

[<span data-ttu-id="8808e-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8808e-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="8808e-159">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8808e-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8808e-160">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8808e-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8808e-162">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8808e-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8808e-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


