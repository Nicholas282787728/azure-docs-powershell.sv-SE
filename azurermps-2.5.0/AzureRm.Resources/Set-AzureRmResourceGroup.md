---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: 8070fd0dfc14396841865f726ef5a8d3a7630afa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928670"
---
# <span data-ttu-id="17173-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17173-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="17173-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17173-102">SYNOPSIS</span></span>
<span data-ttu-id="17173-103">Ändrar en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17173-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17173-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17173-104">SYNTAX</span></span>

### <span data-ttu-id="17173-105">SetByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="17173-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17173-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="17173-106">SetByResourceGroupId</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17173-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17173-107">DESCRIPTION</span></span>
<span data-ttu-id="17173-108">Cmdleten **set-AzureRmResourceGroup** ändrar egenskaperna för en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17173-108">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="17173-109">Du kan använda denna cmdlet för att lägga till, ändra eller ta bort de Azure-taggar som tillämpas på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17173-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="17173-110">Ange parametern *Name* för att identifiera resurs gruppen och *märkningen* för att ändra taggarna.</span><span class="sxs-lookup"><span data-stu-id="17173-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="17173-111">Du kan inte använda denna cmdlet för att ändra namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17173-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="17173-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17173-112">EXAMPLES</span></span>

### <span data-ttu-id="17173-113">Exempel 1: använda en tagg för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="17173-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="17173-114">Det här kommandot lägger till en avdelning med ett värde i en resurs grupp som inte har befintliga taggar.</span><span class="sxs-lookup"><span data-stu-id="17173-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="17173-115">Exempel 2: lägga till taggar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="17173-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="17173-116">I det här exemplet läggs en status tagg till med ett godkänt och en FY2016-tagg till en resurs grupp med befintliga taggar.</span><span class="sxs-lookup"><span data-stu-id="17173-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="17173-117">Eftersom de taggar du anger ersätter de befintliga taggarna måste du ta med de befintliga taggarna i den nya tag-samlingen eller förlora dem.</span><span class="sxs-lookup"><span data-stu-id="17173-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="17173-118">Det första kommandot får resurs gruppen ContosoRG och använder metoden dot för att hämta värdet på egenskapen Tags.</span><span class="sxs-lookup"><span data-stu-id="17173-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="17173-119">Kommandot lagrar taggarna i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="17173-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="17173-120">Det andra kommandot får taggarna i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="17173-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="17173-121">I det tredje kommandot används operatorn + = tilldelning för att lägga till status-och FY2016-Taggar i matrisen med taggar i variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="17173-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="17173-122">Det fjärde kommandot använder parametern *tagg* för **set-AzureRmResourceGroup** för att använda taggarna i $Tags-variabeln i resurs gruppen ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="17173-122">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="17173-123">Det femte kommandot får alla märkningar som används i ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="17173-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="17173-124">Resultatet visar att resurs gruppen har avdelnings märket och de två nya taggarna, status och FY2015.</span><span class="sxs-lookup"><span data-stu-id="17173-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="17173-125">Exempel 3: ta bort alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="17173-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="17173-126">Det här kommandot anger *märknings* parametern med ett tomt värde för hash-tabell för att ta bort alla Taggar från ContosoRG resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="17173-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="17173-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17173-127">PARAMETERS</span></span>

### <span data-ttu-id="17173-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="17173-128">-ApiVersion</span></span>
<span data-ttu-id="17173-129">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="17173-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="17173-130">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="17173-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="17173-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17173-131">-DefaultProfile</span></span>
<span data-ttu-id="17173-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="17173-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17173-133">-ID</span><span class="sxs-lookup"><span data-stu-id="17173-133">-Id</span></span>
<span data-ttu-id="17173-134">Anger ID: t för den resurs grupp som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="17173-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17173-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="17173-135">-Name</span></span>
<span data-ttu-id="17173-136">Anger namnet på den resurs grupp som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="17173-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17173-137">-För</span><span class="sxs-lookup"><span data-stu-id="17173-137">-Pre</span></span>
<span data-ttu-id="17173-138">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="17173-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="17173-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="17173-139">-Tag</span></span>
<span data-ttu-id="17173-140">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="17173-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="17173-141">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"} en tagg är ett namn värde par som du kan skapa och tillämpa på resurser och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="17173-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="17173-142">När du har tilldelat taggar till resurser och grupper kan du använda parametern *tagg* för Get-AzureRmResource och Get-AzureRmResourceGroup för att söka efter resurser och grupper efter taggnamn eller namn och värde.</span><span class="sxs-lookup"><span data-stu-id="17173-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="17173-143">Du kan använda taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="17173-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="17173-144">Om du vill lägga till eller ändra en tagg måste du ersätta samlingen med taggar för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="17173-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="17173-145">Om du vill ta bort en tagg anger du en hash-tabell med alla Taggar som för närvarande används i resurs gruppen, från **AzureRmResourceGroup** , förutom den tagg du vill ta bort.</span><span class="sxs-lookup"><span data-stu-id="17173-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="17173-146">Om du vill ta bort alla flaggor från en resurs grupp anger du en tom hash-tabell: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="17173-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="17173-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17173-147">CommonParameters</span></span>
<span data-ttu-id="17173-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17173-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17173-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17173-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17173-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17173-150">INPUTS</span></span>

### <span data-ttu-id="17173-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="17173-151">None</span></span>

## <span data-ttu-id="17173-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17173-152">OUTPUTS</span></span>

### <span data-ttu-id="17173-153">Microsoft. Azure. commands. Resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17173-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="17173-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17173-154">NOTES</span></span>

## <span data-ttu-id="17173-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17173-155">RELATED LINKS</span></span>

[<span data-ttu-id="17173-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="17173-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="17173-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17173-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="17173-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17173-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="17173-159">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17173-159">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
