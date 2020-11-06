---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577512"
---
# <span data-ttu-id="51033-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51033-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="51033-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51033-102">SYNOPSIS</span></span>
<span data-ttu-id="51033-103">Skapar en Azure-resurspost.</span><span class="sxs-lookup"><span data-stu-id="51033-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51033-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51033-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51033-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51033-105">DESCRIPTION</span></span>
<span data-ttu-id="51033-106">Cmdleten **New-AzureRmResourceGroup** skapar en Azure resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="51033-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="51033-107">Du kan skapa en resurs grupp med hjälp av ett namn och en plats och sedan använda New-AzureRmResource cmdlet för att skapa resurser som ska läggas till i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="51033-108">Använd New-AzureRmResourceGroupDeployment cmdlet för att lägga till en distribution i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="51033-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="51033-109">Använd cmdleten **New-AzureRmResource** om du vill lägga till en resurs i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="51033-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="51033-110">En Azure-resurs är en användardefinierad Azure-enhet, till exempel en databas server, en databas eller en webbplats.</span><span class="sxs-lookup"><span data-stu-id="51033-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="51033-111">En Azure-resurs grupp är en samling Azure-resurser som distribueras som en enhet.</span><span class="sxs-lookup"><span data-stu-id="51033-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="51033-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51033-112">EXAMPLES</span></span>

### <span data-ttu-id="51033-113">Exempel 1: skapa en tom resurs grupp</span><span class="sxs-lookup"><span data-stu-id="51033-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="51033-114">Det här kommandot skapar en resurs grupp som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="51033-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="51033-115">Du kan använda cmdletarna **New-AzureRmResource** eller **New-AzureRmResourceGroupDeployment** för att lägga till resurser och distributioner i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="51033-116">Exempel 2: skapa en resurs grupp med Taggar</span><span class="sxs-lookup"><span data-stu-id="51033-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="51033-117">Det här kommandot skapar en tom resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="51033-117">This command creates an empty resource group.</span></span> <span data-ttu-id="51033-118">Det här kommandot är samma som kommandot i exempel 1, förutom att det tilldelar taggar till resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="51033-119">Den första taggen, namngiven tom, kan användas för att identifiera resurs grupper som inte har några resurser.</span><span class="sxs-lookup"><span data-stu-id="51033-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="51033-120">Den andra taggen heter Department och har ett värde för marknadsföring.</span><span class="sxs-lookup"><span data-stu-id="51033-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="51033-121">Du kan använda en tagg som den här för att kategorisera resurs grupper för administration eller budgetering.</span><span class="sxs-lookup"><span data-stu-id="51033-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="51033-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51033-122">PARAMETERS</span></span>

### <span data-ttu-id="51033-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="51033-123">-ApiVersion</span></span>
<span data-ttu-id="51033-124">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="51033-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="51033-125">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="51033-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="51033-126">-Force</span><span class="sxs-lookup"><span data-stu-id="51033-126">-Force</span></span>
<span data-ttu-id="51033-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="51033-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51033-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="51033-128">-Location</span></span>
<span data-ttu-id="51033-129">Anger platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="51033-130">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="51033-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="51033-131">Du kan placera en resurs grupp på vilken plats som helst.</span><span class="sxs-lookup"><span data-stu-id="51033-131">You can place a resource group in any location.</span></span> <span data-ttu-id="51033-132">Resurs gruppen behöver inte finnas på samma plats som din Azure-prenumeration eller på samma plats som dess resurser.</span><span class="sxs-lookup"><span data-stu-id="51033-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="51033-133">Om du vill ta reda på vilken plats som har stöd för varje resurs typ använder du Get-AzureRmResourceProvider cmdlet med parametern *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="51033-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="51033-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="51033-134">-Name</span></span>
<span data-ttu-id="51033-135">Anger ett namn för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="51033-136">Resurs namnet måste vara unikt i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="51033-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="51033-137">Om det redan finns en resurs grupp med det namnet måste du bekräfta att du vill ersätta den befintliga resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="51033-138">-För</span><span class="sxs-lookup"><span data-stu-id="51033-138">-Pre</span></span>
<span data-ttu-id="51033-139">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="51033-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="51033-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="51033-140">-Tag</span></span>
<span data-ttu-id="51033-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="51033-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51033-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="51033-142">For example:</span></span>

<span data-ttu-id="51033-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="51033-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="51033-144">Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51033-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="51033-145">När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzureRmResource och Get-AzureRmResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde.</span><span class="sxs-lookup"><span data-stu-id="51033-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="51033-146">Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="51033-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="51033-147">Använd Get-AzureRMTag cmdlet för att få dina fördefinierade taggar.</span><span class="sxs-lookup"><span data-stu-id="51033-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="51033-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51033-148">-Confirm</span></span>
<span data-ttu-id="51033-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51033-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51033-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51033-150">-WhatIf</span></span>
<span data-ttu-id="51033-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51033-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51033-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51033-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51033-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51033-153">-DefaultProfile</span></span>
<span data-ttu-id="51033-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51033-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51033-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51033-155">CommonParameters</span></span>
<span data-ttu-id="51033-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51033-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51033-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51033-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51033-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51033-158">INPUTS</span></span>

### <span data-ttu-id="51033-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="51033-159">None</span></span>

## <span data-ttu-id="51033-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51033-160">OUTPUTS</span></span>

### <span data-ttu-id="51033-161">Microsoft. Azure. commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51033-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="51033-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51033-162">NOTES</span></span>

## <span data-ttu-id="51033-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51033-163">RELATED LINKS</span></span>

[<span data-ttu-id="51033-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="51033-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="51033-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51033-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="51033-166">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="51033-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="51033-167">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="51033-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="51033-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51033-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="51033-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51033-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
