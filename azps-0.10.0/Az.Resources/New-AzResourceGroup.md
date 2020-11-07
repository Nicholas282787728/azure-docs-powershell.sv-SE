---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: b0d9d23b9563c38a985adfa3d12dfc2854319512
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923913"
---
# <span data-ttu-id="d8677-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8677-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="d8677-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8677-102">SYNOPSIS</span></span>
<span data-ttu-id="d8677-103">Skapar en Azure-resurspost.</span><span class="sxs-lookup"><span data-stu-id="d8677-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="d8677-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8677-104">SYNTAX</span></span>

```
New-AzResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8677-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8677-105">DESCRIPTION</span></span>
<span data-ttu-id="d8677-106">Cmdleten **New-AzResourceGroup** skapar en Azure resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8677-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="d8677-107">Du kan skapa en resurs grupp med hjälp av ett namn och en plats och sedan använda New-AzResource cmdlet för att skapa resurser som ska läggas till i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="d8677-108">Använd New-AzResourceGroupDeployment cmdlet för att lägga till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8677-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="d8677-109">Använd cmdleten **New-AzResource** om du vill lägga till en resurs i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8677-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="d8677-110">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="d8677-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="d8677-111">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="d8677-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="d8677-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8677-112">EXAMPLES</span></span>

### <span data-ttu-id="d8677-113">Exempel 1: skapa en tom resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d8677-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="d8677-114">Det här kommandot skapar en resurs grupp som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="d8677-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="d8677-115">Du kan använda cmdletarna **New-AzResource** eller **New-AzResourceGroupDeployment** för att lägga till resurser och distributioner i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="d8677-116">Exempel 2: skapa en tom resurs grupp med hjälp av positions parametrar</span><span class="sxs-lookup"><span data-stu-id="d8677-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="d8677-117">Det här kommandot skapar en resurs grupp som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="d8677-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="d8677-118">Exempel 3: skapa en resurs grupp med Taggar</span><span class="sxs-lookup"><span data-stu-id="d8677-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="d8677-119">Det här kommandot skapar en tom resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8677-119">This command creates an empty resource group.</span></span> <span data-ttu-id="d8677-120">Det här kommandot är samma som kommandot i exempel 1, förutom att det tilldelar taggar till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="d8677-121">Den första taggen, namngiven tom, kan användas för att identifiera resurs grupper som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="d8677-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="d8677-122">Den andra taggen heter Department och har ett värde för marknadsföring.</span><span class="sxs-lookup"><span data-stu-id="d8677-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="d8677-123">Du kan använda en tagg som den här för att kategorisera resurs grupper för administration eller budgetering.</span><span class="sxs-lookup"><span data-stu-id="d8677-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="d8677-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8677-124">PARAMETERS</span></span>

### <span data-ttu-id="d8677-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8677-125">-ApiVersion</span></span>
<span data-ttu-id="d8677-126">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="d8677-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d8677-127">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="d8677-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d8677-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8677-128">-DefaultProfile</span></span>
<span data-ttu-id="d8677-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8677-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8677-130">-Force</span><span class="sxs-lookup"><span data-stu-id="d8677-130">-Force</span></span>
<span data-ttu-id="d8677-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8677-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8677-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="d8677-132">-Location</span></span>
<span data-ttu-id="d8677-133">Anger platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="d8677-134">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="d8677-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="d8677-135">Du kan placera en resurs grupp på vilken plats som helst.</span><span class="sxs-lookup"><span data-stu-id="d8677-135">You can place a resource group in any location.</span></span> <span data-ttu-id="d8677-136">Resurs gruppen behöver inte finnas på samma plats som din Azure-prenumeration eller på samma plats som dess resurser.</span><span class="sxs-lookup"><span data-stu-id="d8677-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="d8677-137">Om du vill ta reda på vilken plats som har stöd för varje resurs typ använder du Get-AzResourceProvider cmdlet med parametern *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="d8677-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="d8677-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8677-138">-Name</span></span>
<span data-ttu-id="d8677-139">Anger ett namn för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="d8677-140">Resurs namnet måste vara unikt i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d8677-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="d8677-141">Om det redan finns en resurs grupp med det namnet måste du bekräfta att du vill ersätta den befintliga resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="d8677-142">-För</span><span class="sxs-lookup"><span data-stu-id="d8677-142">-Pre</span></span>
<span data-ttu-id="d8677-143">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d8677-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8677-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d8677-144">-Tag</span></span>
<span data-ttu-id="d8677-145">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d8677-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8677-146">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8677-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="d8677-147">När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzResource och Get-AzResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde.</span><span class="sxs-lookup"><span data-stu-id="d8677-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="d8677-148">Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="d8677-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="d8677-149">Använd Get-AzTag cmdlet för att få dina fördefinierade taggar.</span><span class="sxs-lookup"><span data-stu-id="d8677-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="d8677-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8677-150">-Confirm</span></span>
<span data-ttu-id="d8677-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8677-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8677-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8677-152">-WhatIf</span></span>
<span data-ttu-id="d8677-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8677-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8677-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8677-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8677-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8677-155">CommonParameters</span></span>
<span data-ttu-id="d8677-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8677-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8677-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8677-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8677-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8677-158">INPUTS</span></span>

### <span data-ttu-id="d8677-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="d8677-159">None</span></span>

## <span data-ttu-id="d8677-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8677-160">OUTPUTS</span></span>

### <span data-ttu-id="d8677-161">Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8677-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="d8677-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8677-162">NOTES</span></span>

## <span data-ttu-id="d8677-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8677-163">RELATED LINKS</span></span>

[<span data-ttu-id="d8677-164">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d8677-164">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="d8677-165">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8677-165">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="d8677-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="d8677-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="d8677-167">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d8677-167">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="d8677-168">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8677-168">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="d8677-169">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8677-169">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
