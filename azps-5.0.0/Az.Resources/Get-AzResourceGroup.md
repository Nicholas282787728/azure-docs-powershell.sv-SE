---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322955"
---
# <span data-ttu-id="de54d-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de54d-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="de54d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de54d-102">SYNOPSIS</span></span>
<span data-ttu-id="de54d-103">Hämtar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="de54d-103">Gets resource groups.</span></span>

## <span data-ttu-id="de54d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de54d-104">SYNTAX</span></span>

### <span data-ttu-id="de54d-105">GetByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="de54d-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de54d-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="de54d-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de54d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de54d-107">DESCRIPTION</span></span>
<span data-ttu-id="de54d-108">Cmdleten **Get-AzResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="de54d-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="de54d-109">Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="de54d-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="de54d-110">Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="de54d-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="de54d-111">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de54d-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="de54d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de54d-112">EXAMPLES</span></span>

### <span data-ttu-id="de54d-113">Exempel 1: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="de54d-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="de54d-114">Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="de54d-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="de54d-115">Exempel 2: Hämta alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="de54d-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="de54d-116">Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="de54d-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="de54d-117">Exempel 3: Hämta resurs grupper baserat på tagg</span><span class="sxs-lookup"><span data-stu-id="de54d-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="de54d-118">Exempel 4: Visa resurs grupper efter plats</span><span class="sxs-lookup"><span data-stu-id="de54d-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="de54d-119">Exempel 5: Visa namnen på alla resurs grupper på en viss plats</span><span class="sxs-lookup"><span data-stu-id="de54d-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="de54d-120">Exempel 6: Visa resurs grupper vars namn börjar med webb servern</span><span class="sxs-lookup"><span data-stu-id="de54d-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="de54d-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de54d-121">PARAMETERS</span></span>

### <span data-ttu-id="de54d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de54d-122">-ApiVersion</span></span>
<span data-ttu-id="de54d-123">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="de54d-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="de54d-124">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="de54d-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="de54d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de54d-125">-DefaultProfile</span></span>
<span data-ttu-id="de54d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="de54d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de54d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="de54d-127">-Id</span></span>
<span data-ttu-id="de54d-128">Anger ID för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="de54d-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="de54d-129">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="de54d-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="de54d-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="de54d-130">-Location</span></span>
<span data-ttu-id="de54d-131">Anger platsen för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="de54d-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="de54d-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="de54d-132">-Name</span></span>
<span data-ttu-id="de54d-133">Anger namnet på den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="de54d-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="de54d-134">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="de54d-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="de54d-135">-För</span><span class="sxs-lookup"><span data-stu-id="de54d-135">-Pre</span></span>
<span data-ttu-id="de54d-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="de54d-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="de54d-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="de54d-137">-Tag</span></span>
<span data-ttu-id="de54d-138">Den HTML-kod som resurs grupper ska filtreras efter.</span><span class="sxs-lookup"><span data-stu-id="de54d-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="de54d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de54d-139">CommonParameters</span></span>
<span data-ttu-id="de54d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de54d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de54d-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de54d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de54d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de54d-142">INPUTS</span></span>

### <span data-ttu-id="de54d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="de54d-143">System.String</span></span>

### <span data-ttu-id="de54d-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="de54d-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de54d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de54d-145">OUTPUTS</span></span>

### <span data-ttu-id="de54d-146">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de54d-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="de54d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de54d-147">NOTES</span></span>

## <span data-ttu-id="de54d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de54d-148">RELATED LINKS</span></span>

[<span data-ttu-id="de54d-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de54d-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="de54d-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de54d-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="de54d-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de54d-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

