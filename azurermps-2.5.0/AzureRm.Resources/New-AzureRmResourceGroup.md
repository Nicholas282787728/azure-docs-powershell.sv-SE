---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: dd115a7d0445a7b07557b884dd2c7413f5269d00
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930834"
---
# <span data-ttu-id="88a6f-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a6f-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="88a6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="88a6f-103">Skapar en Azure-resurspost.</span><span class="sxs-lookup"><span data-stu-id="88a6f-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88a6f-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="88a6f-106">Cmdleten **New-AzureRmResourceGroup** skapar en Azure resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="88a6f-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="88a6f-107">Du kan skapa en resurs grupp med hjälp av ett namn och en plats och sedan använda New-AzureRmResource cmdlet för att skapa resurser som ska läggas till i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="88a6f-108">Använd New-AzureRmResourceGroupDeployment cmdlet för att lägga till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="88a6f-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="88a6f-109">Använd cmdleten **New-AzureRmResource** om du vill lägga till en resurs i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="88a6f-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="88a6f-110">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="88a6f-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="88a6f-111">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="88a6f-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="88a6f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88a6f-112">EXAMPLES</span></span>

### <span data-ttu-id="88a6f-113">Exempel 1: skapa en tom resurs grupp</span><span class="sxs-lookup"><span data-stu-id="88a6f-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="88a6f-114">Det här kommandot skapar en resurs grupp som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="88a6f-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="88a6f-115">Du kan använda cmdletarna **New-AzureRmResource** eller **New-AzureRmResourceGroupDeployment** för att lägga till resurser och distributioner i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="88a6f-116">Exempel 2: skapa en tom resurs grupp med hjälp av positions parametrar</span><span class="sxs-lookup"><span data-stu-id="88a6f-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="88a6f-117">Det här kommandot skapar en resurs grupp som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="88a6f-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="88a6f-118">Exempel 3: skapa en resurs grupp med Taggar</span><span class="sxs-lookup"><span data-stu-id="88a6f-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="88a6f-119">Det här kommandot skapar en tom resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="88a6f-119">This command creates an empty resource group.</span></span> <span data-ttu-id="88a6f-120">Det här kommandot är samma som kommandot i exempel 1, förutom att det tilldelar taggar till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="88a6f-121">Den första taggen, namngiven tom, kan användas för att identifiera resurs grupper som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="88a6f-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="88a6f-122">Den andra taggen heter Department och har ett värde för marknadsföring.</span><span class="sxs-lookup"><span data-stu-id="88a6f-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="88a6f-123">Du kan använda en tagg som den här för att kategorisera resurs grupper för administration eller budgetering.</span><span class="sxs-lookup"><span data-stu-id="88a6f-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="88a6f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88a6f-124">PARAMETERS</span></span>

### <span data-ttu-id="88a6f-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88a6f-125">-ApiVersion</span></span>
<span data-ttu-id="88a6f-126">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="88a6f-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="88a6f-127">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="88a6f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a6f-128">-DefaultProfile</span></span>
<span data-ttu-id="88a6f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="88a6f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88a6f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="88a6f-130">-Force</span></span>
<span data-ttu-id="88a6f-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="88a6f-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88a6f-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="88a6f-132">-Location</span></span>
<span data-ttu-id="88a6f-133">Anger platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="88a6f-134">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="88a6f-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="88a6f-135">Du kan placera en resurs grupp på vilken plats som helst.</span><span class="sxs-lookup"><span data-stu-id="88a6f-135">You can place a resource group in any location.</span></span> <span data-ttu-id="88a6f-136">Resurs gruppen behöver inte finnas på samma plats som din Azure-prenumeration eller på samma plats som dess resurser.</span><span class="sxs-lookup"><span data-stu-id="88a6f-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="88a6f-137">Om du vill ta reda på vilken plats som har stöd för varje resurs typ använder du Get-AzureRmResourceProvider cmdlet med parametern *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="88a6f-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a6f-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="88a6f-138">-Name</span></span>
<span data-ttu-id="88a6f-139">Anger ett namn för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="88a6f-140">Resurs namnet måste vara unikt i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="88a6f-141">Om det redan finns en resurs grupp med det namnet måste du bekräfta att du vill ersätta den befintliga resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a6f-142">-För</span><span class="sxs-lookup"><span data-stu-id="88a6f-142">-Pre</span></span>
<span data-ttu-id="88a6f-143">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="88a6f-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88a6f-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="88a6f-144">-Tag</span></span>
<span data-ttu-id="88a6f-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="88a6f-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88a6f-146">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a6f-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="88a6f-147">När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzureRmResource och Get-AzureRmResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde.</span><span class="sxs-lookup"><span data-stu-id="88a6f-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="88a6f-148">Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="88a6f-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="88a6f-149">Använd Get-AzureRMTag cmdlet för att få dina fördefinierade taggar.</span><span class="sxs-lookup"><span data-stu-id="88a6f-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a6f-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88a6f-150">-Confirm</span></span>
<span data-ttu-id="88a6f-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88a6f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a6f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a6f-152">-WhatIf</span></span>
<span data-ttu-id="88a6f-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88a6f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a6f-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88a6f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a6f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a6f-155">CommonParameters</span></span>
<span data-ttu-id="88a6f-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a6f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a6f-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a6f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a6f-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88a6f-158">INPUTS</span></span>

### <span data-ttu-id="88a6f-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="88a6f-159">None</span></span>

## <span data-ttu-id="88a6f-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88a6f-160">OUTPUTS</span></span>

### <span data-ttu-id="88a6f-161">Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a6f-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="88a6f-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88a6f-162">NOTES</span></span>

## <span data-ttu-id="88a6f-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88a6f-163">RELATED LINKS</span></span>

[<span data-ttu-id="88a6f-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="88a6f-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="88a6f-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a6f-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="88a6f-166">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="88a6f-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="88a6f-167">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88a6f-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="88a6f-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a6f-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="88a6f-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a6f-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
