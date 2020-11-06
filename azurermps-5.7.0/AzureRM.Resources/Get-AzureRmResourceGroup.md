---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583067"
---
# <span data-ttu-id="583de-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="583de-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="583de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="583de-102">SYNOPSIS</span></span>
<span data-ttu-id="583de-103">Hämtar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="583de-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="583de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="583de-104">SYNTAX</span></span>

### <span data-ttu-id="583de-105">GetByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="583de-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="583de-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="583de-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="583de-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="583de-107">DESCRIPTION</span></span>
<span data-ttu-id="583de-108">Cmdleten **Get-AzureRmResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="583de-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="583de-109">Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="583de-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="583de-110">Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="583de-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="583de-111">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="583de-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="583de-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="583de-112">EXAMPLES</span></span>

### <span data-ttu-id="583de-113">Exempel 1: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="583de-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="583de-114">Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="583de-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="583de-115">Exempel 2: Hämta alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="583de-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="583de-116">Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="583de-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="583de-117">Exempel 3: Visa resurs grupper efter plats</span><span class="sxs-lookup"><span data-stu-id="583de-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="583de-118">Exempel 4: Visa namnen på alla resurs grupper på en viss plats</span><span class="sxs-lookup"><span data-stu-id="583de-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="583de-119">Exempel 5: Visa resurs grupper vars namn börjar med webserver</span><span class="sxs-lookup"><span data-stu-id="583de-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="583de-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="583de-120">PARAMETERS</span></span>

### <span data-ttu-id="583de-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="583de-121">-ApiVersion</span></span>
<span data-ttu-id="583de-122">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="583de-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="583de-123">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="583de-123">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583de-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583de-124">-DefaultProfile</span></span>
<span data-ttu-id="583de-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="583de-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583de-126">-ID</span><span class="sxs-lookup"><span data-stu-id="583de-126">-Id</span></span>
<span data-ttu-id="583de-127">Anger ID för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="583de-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="583de-128">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="583de-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583de-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="583de-129">-Location</span></span>
<span data-ttu-id="583de-130">Anger platsen för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="583de-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583de-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="583de-131">-Name</span></span>
<span data-ttu-id="583de-132">Anger namnet på den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="583de-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="583de-133">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="583de-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583de-134">-För</span><span class="sxs-lookup"><span data-stu-id="583de-134">-Pre</span></span>
<span data-ttu-id="583de-135">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="583de-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583de-136">CommonParameters</span></span>
<span data-ttu-id="583de-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583de-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583de-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583de-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="583de-139">INPUTS</span></span>

### <span data-ttu-id="583de-140">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="583de-140">String</span></span>
<span data-ttu-id="583de-141">Du kan ange indata för cmdleten med egenskaps namnet men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="583de-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="583de-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="583de-142">OUTPUTS</span></span>

### <span data-ttu-id="583de-143">Microsoft. Azure. commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="583de-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="583de-144">Denna cmdlet returnerar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="583de-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="583de-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="583de-145">NOTES</span></span>

## <span data-ttu-id="583de-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="583de-146">RELATED LINKS</span></span>

[<span data-ttu-id="583de-147">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="583de-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="583de-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="583de-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="583de-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="583de-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


