---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920098"
---
# <span data-ttu-id="0ef85-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ef85-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="0ef85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ef85-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef85-103">Hämtar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="0ef85-103">Gets resource groups.</span></span>

## <span data-ttu-id="0ef85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ef85-104">SYNTAX</span></span>

### <span data-ttu-id="0ef85-105">GetByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="0ef85-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ef85-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="0ef85-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ef85-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ef85-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef85-108">Cmdleten **Get-AzResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0ef85-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="0ef85-109">Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0ef85-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="0ef85-110">Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0ef85-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="0ef85-111">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef85-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="0ef85-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ef85-112">EXAMPLES</span></span>

### <span data-ttu-id="0ef85-113">Exempel 1: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="0ef85-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="0ef85-114">Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="0ef85-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="0ef85-115">Exempel 2: Hämta alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0ef85-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="0ef85-116">Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="0ef85-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="0ef85-117">Exempel 3: Visa resurs grupper efter plats</span><span class="sxs-lookup"><span data-stu-id="0ef85-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="0ef85-118">Exempel 4: Visa namnen på alla resurs grupper på en viss plats</span><span class="sxs-lookup"><span data-stu-id="0ef85-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="0ef85-119">Exempel 5: Visa resurs grupper vars namn börjar med webserver</span><span class="sxs-lookup"><span data-stu-id="0ef85-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="0ef85-120">Exempel 6: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="0ef85-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="0ef85-121">Det här kommandot får Azure-adressresursen i din prenumeration som börjar med "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="0ef85-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="0ef85-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ef85-122">PARAMETERS</span></span>

### <span data-ttu-id="0ef85-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0ef85-123">-ApiVersion</span></span>
<span data-ttu-id="0ef85-124">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="0ef85-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0ef85-125">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="0ef85-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0ef85-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef85-126">-DefaultProfile</span></span>
<span data-ttu-id="0ef85-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0ef85-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ef85-128">-ID</span><span class="sxs-lookup"><span data-stu-id="0ef85-128">-Id</span></span>
<span data-ttu-id="0ef85-129">Anger ID för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0ef85-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="0ef85-130">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="0ef85-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef85-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="0ef85-131">-Location</span></span>
<span data-ttu-id="0ef85-132">Anger platsen för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0ef85-132">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef85-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ef85-133">-Name</span></span>
<span data-ttu-id="0ef85-134">Anger namnet på den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0ef85-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="0ef85-135">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="0ef85-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0ef85-136">-För</span><span class="sxs-lookup"><span data-stu-id="0ef85-136">-Pre</span></span>
<span data-ttu-id="0ef85-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0ef85-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0ef85-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0ef85-138">-Tag</span></span>
<span data-ttu-id="0ef85-139">Den HTML-kod som resurs grupper ska filtreras efter.</span><span class="sxs-lookup"><span data-stu-id="0ef85-139">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef85-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef85-140">CommonParameters</span></span>
<span data-ttu-id="0ef85-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef85-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef85-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ef85-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef85-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ef85-143">INPUTS</span></span>

### <span data-ttu-id="0ef85-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef85-144">System.String</span></span>

### <span data-ttu-id="0ef85-145">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0ef85-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ef85-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ef85-146">OUTPUTS</span></span>

### <span data-ttu-id="0ef85-147">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ef85-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="0ef85-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ef85-148">NOTES</span></span>

## <span data-ttu-id="0ef85-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ef85-149">RELATED LINKS</span></span>

[<span data-ttu-id="0ef85-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ef85-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="0ef85-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ef85-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="0ef85-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ef85-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


