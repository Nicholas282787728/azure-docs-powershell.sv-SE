---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: dc619aacd4089ce854eb5d342c2308a38a60cb28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091642"
---
# <span data-ttu-id="b685b-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b685b-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="b685b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b685b-102">SYNOPSIS</span></span>
<span data-ttu-id="b685b-103">Hämtar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="b685b-103">Gets resource groups.</span></span>

## <span data-ttu-id="b685b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b685b-104">SYNTAX</span></span>

### <span data-ttu-id="b685b-105">GetByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="b685b-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b685b-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b685b-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b685b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b685b-107">DESCRIPTION</span></span>
<span data-ttu-id="b685b-108">Cmdleten **Get-AzResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b685b-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="b685b-109">Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b685b-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="b685b-110">Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b685b-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="b685b-111">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b685b-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="b685b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b685b-112">EXAMPLES</span></span>

### <span data-ttu-id="b685b-113">Exempel 1: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="b685b-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="b685b-114">Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="b685b-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="b685b-115">Exempel 2: Hämta alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b685b-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="b685b-116">Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="b685b-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="b685b-117">Exempel 3: Visa resurs grupper efter plats</span><span class="sxs-lookup"><span data-stu-id="b685b-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="b685b-118">Exempel 4: Visa namnen på alla resurs grupper på en viss plats</span><span class="sxs-lookup"><span data-stu-id="b685b-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="b685b-119">Exempel 5: Visa resurs grupper vars namn börjar med webserver</span><span class="sxs-lookup"><span data-stu-id="b685b-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="b685b-120">Exempel 6: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="b685b-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="b685b-121">Det här kommandot får Azure-adressresursen i din prenumeration som börjar med "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="b685b-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="b685b-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b685b-122">PARAMETERS</span></span>

### <span data-ttu-id="b685b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b685b-123">-ApiVersion</span></span>
<span data-ttu-id="b685b-124">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="b685b-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b685b-125">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="b685b-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b685b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b685b-126">-DefaultProfile</span></span>
<span data-ttu-id="b685b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b685b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b685b-128">-ID</span><span class="sxs-lookup"><span data-stu-id="b685b-128">-Id</span></span>
<span data-ttu-id="b685b-129">Anger ID för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b685b-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="b685b-130">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="b685b-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="b685b-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="b685b-131">-Location</span></span>
<span data-ttu-id="b685b-132">Anger platsen för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b685b-132">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="b685b-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="b685b-133">-Name</span></span>
<span data-ttu-id="b685b-134">Anger namnet på den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b685b-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="b685b-135">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="b685b-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="b685b-136">-För</span><span class="sxs-lookup"><span data-stu-id="b685b-136">-Pre</span></span>
<span data-ttu-id="b685b-137">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b685b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b685b-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b685b-138">-Tag</span></span>
<span data-ttu-id="b685b-139">Den HTML-kod som resurs grupper ska filtreras efter.</span><span class="sxs-lookup"><span data-stu-id="b685b-139">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="b685b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b685b-140">CommonParameters</span></span>
<span data-ttu-id="b685b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b685b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b685b-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b685b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b685b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b685b-143">INPUTS</span></span>

### <span data-ttu-id="b685b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b685b-144">System.String</span></span>

### <span data-ttu-id="b685b-145">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b685b-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b685b-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b685b-146">OUTPUTS</span></span>

### <span data-ttu-id="b685b-147">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b685b-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="b685b-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b685b-148">NOTES</span></span>

## <span data-ttu-id="b685b-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b685b-149">RELATED LINKS</span></span>

[<span data-ttu-id="b685b-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b685b-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b685b-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b685b-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="b685b-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b685b-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


