---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757463"
---
# <span data-ttu-id="335f1-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="335f1-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="335f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="335f1-102">SYNOPSIS</span></span>
<span data-ttu-id="335f1-103">Ändrar en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335f1-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="335f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="335f1-104">SYNTAX</span></span>

### <span data-ttu-id="335f1-105">Visar resurs gruppen baserat på namnet.</span><span class="sxs-lookup"><span data-stu-id="335f1-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="335f1-106">Vis</span><span class="sxs-lookup"><span data-stu-id="335f1-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="335f1-107">Visar resurs gruppen baserat på ID.</span><span class="sxs-lookup"><span data-stu-id="335f1-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="335f1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="335f1-108">DESCRIPTION</span></span>
<span data-ttu-id="335f1-109">Cmdleten **set-AzureRmResourceGroup** ändrar egenskaperna för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335f1-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="335f1-110">Du kan använda denna cmdlet för att lägga till, ändra eller ta bort de Azure-taggar som tillämpas på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335f1-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="335f1-111">Ange parametern *Name* för att identifiera resurs gruppen och *märkningen* för att ändra taggarna.</span><span class="sxs-lookup"><span data-stu-id="335f1-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="335f1-112">Du kan inte använda denna cmdlet för att ändra namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335f1-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="335f1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="335f1-113">EXAMPLES</span></span>

### <span data-ttu-id="335f1-114">Exempel 1: använda en tagg för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="335f1-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="335f1-115">Det här kommandot lägger till en avdelning med ett värde i en resurs grupp som inte har befintliga taggar.</span><span class="sxs-lookup"><span data-stu-id="335f1-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="335f1-116">Exempel 2: lägga till taggar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="335f1-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="335f1-117">I det här exemplet läggs en status tagg till med ett godkänt och en FY2016-tagg till en resurs grupp med befintliga taggar.</span><span class="sxs-lookup"><span data-stu-id="335f1-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="335f1-118">Eftersom de taggar du anger ersätter de befintliga taggarna måste du ta med de befintliga taggarna i den nya tag-samlingen eller förlora dem.</span><span class="sxs-lookup"><span data-stu-id="335f1-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="335f1-119">Det första kommandot får resurs gruppen ContosoRG och använder metoden dot för att hämta värdet på egenskapen Tags.</span><span class="sxs-lookup"><span data-stu-id="335f1-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="335f1-120">Kommandot lagrar taggarna i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="335f1-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="335f1-121">Det andra kommandot får taggarna i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="335f1-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="335f1-122">I det tredje kommandot används operatorn + = tilldelning för att lägga till status-och FY2016-Taggar i matrisen med taggar i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="335f1-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="335f1-123">Det fjärde kommandot använder parametern *tagg* för **set-AzureRmResourceGroup** för att använda taggarna i $Tags-variabeln i resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="335f1-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="335f1-124">Det femte kommandot får alla märkningar som används i ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="335f1-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="335f1-125">Resultatet visar att resurs gruppen har avdelnings märket och de två nya taggarna, status och FY2015.</span><span class="sxs-lookup"><span data-stu-id="335f1-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="335f1-126">Exempel 3: ta bort alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="335f1-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="335f1-127">Det här kommandot anger *märknings* parametern med ett tomt värde för hash-tabell för att ta bort alla Taggar från ContosoRG resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="335f1-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="335f1-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="335f1-128">PARAMETERS</span></span>

### <span data-ttu-id="335f1-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="335f1-129">-ApiVersion</span></span>
<span data-ttu-id="335f1-130">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="335f1-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="335f1-131">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="335f1-131">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="335f1-132">-ID</span><span class="sxs-lookup"><span data-stu-id="335f1-132">-Id</span></span>
<span data-ttu-id="335f1-133">Anger ID: t för den resurs grupp som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="335f1-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="335f1-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="335f1-134">-Name</span></span>
<span data-ttu-id="335f1-135">Anger namnet på den resurs grupp som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="335f1-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335f1-136">-För</span><span class="sxs-lookup"><span data-stu-id="335f1-136">-Pre</span></span>
<span data-ttu-id="335f1-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="335f1-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="335f1-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="335f1-138">-Tag</span></span>
<span data-ttu-id="335f1-139">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="335f1-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="335f1-140">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="335f1-140">For example:</span></span>

<span data-ttu-id="335f1-141">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="335f1-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="335f1-142">En tagg är ett namn värde par som du kan skapa och använda i resurser och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="335f1-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="335f1-143">När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzureRmResource och Get-AzureRmResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde.</span><span class="sxs-lookup"><span data-stu-id="335f1-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="335f1-144">Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="335f1-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="335f1-145">Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="335f1-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="335f1-146">Om du vill ta bort en tagg anger du en hash-tabell med alla Taggar som för närvarande används i resurs gruppen, från **AzureRmResourceGroup** , förutom den tagg du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="335f1-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="335f1-147">Om du vill ta bort alla flaggor från en resurs grupp anger du en tom hash-tabell: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="335f1-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="335f1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335f1-148">-DefaultProfile</span></span>
<span data-ttu-id="335f1-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="335f1-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="335f1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335f1-150">CommonParameters</span></span>
<span data-ttu-id="335f1-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335f1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335f1-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="335f1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335f1-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="335f1-153">INPUTS</span></span>

### <span data-ttu-id="335f1-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="335f1-154">None</span></span>

## <span data-ttu-id="335f1-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="335f1-155">OUTPUTS</span></span>

### <span data-ttu-id="335f1-156">Microsoft. Azure. commands. Resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="335f1-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="335f1-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="335f1-157">NOTES</span></span>

## <span data-ttu-id="335f1-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="335f1-158">RELATED LINKS</span></span>

[<span data-ttu-id="335f1-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="335f1-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="335f1-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="335f1-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="335f1-161">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="335f1-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="335f1-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="335f1-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
