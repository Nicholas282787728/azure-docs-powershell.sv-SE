---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756563"
---
# <span data-ttu-id="996b4-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="996b4-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="996b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="996b4-102">SYNOPSIS</span></span>
<span data-ttu-id="996b4-103">Hämtar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="996b4-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="996b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="996b4-104">SYNTAX</span></span>

### <span data-ttu-id="996b4-105">Visar resurs gruppen baserat på namnet.</span><span class="sxs-lookup"><span data-stu-id="996b4-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="996b4-106">Vis</span><span class="sxs-lookup"><span data-stu-id="996b4-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="996b4-107">Visar resurs gruppen baserat på ID.</span><span class="sxs-lookup"><span data-stu-id="996b4-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996b4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="996b4-108">DESCRIPTION</span></span>
<span data-ttu-id="996b4-109">Cmdleten **Get-AzureRmResourceGroup** får Azure resurs grupper i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="996b4-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="996b4-110">Du kan hämta alla resurs grupper eller ange en resurs grupp efter namn eller andra egenskaper.</span><span class="sxs-lookup"><span data-stu-id="996b4-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="996b4-111">Som standard får denna cmdlet alla resurs grupper i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="996b4-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="996b4-112">Mer information om Azure-resurser och Azure resurs grupper finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="996b4-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="996b4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="996b4-113">EXAMPLES</span></span>

### <span data-ttu-id="996b4-114">Exempel 1: skaffa en resurs grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="996b4-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="996b4-115">Det här kommandot får Azure-adressresursen i din prenumeration med namnet EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="996b4-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="996b4-116">Exempel 2: Hämta alla flaggor för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="996b4-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="996b4-117">Det här kommandot får resurs gruppen namnet ContosoRG och visar de taggar som är kopplade till gruppen.</span><span class="sxs-lookup"><span data-stu-id="996b4-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="996b4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="996b4-118">PARAMETERS</span></span>

### <span data-ttu-id="996b4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="996b4-119">-ApiVersion</span></span>
<span data-ttu-id="996b4-120">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="996b4-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="996b4-121">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="996b4-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="996b4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="996b4-122">-Id</span></span>
<span data-ttu-id="996b4-123">Anger ID för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="996b4-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="996b4-124">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="996b4-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="996b4-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="996b4-125">-Location</span></span>
<span data-ttu-id="996b4-126">Anger platsen för den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="996b4-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="996b4-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="996b4-127">-Name</span></span>
<span data-ttu-id="996b4-128">Anger namnet på den resurs grupp som ska visas.</span><span class="sxs-lookup"><span data-stu-id="996b4-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="996b4-129">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="996b4-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="996b4-130">-För</span><span class="sxs-lookup"><span data-stu-id="996b4-130">-Pre</span></span>
<span data-ttu-id="996b4-131">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="996b4-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="996b4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996b4-132">-DefaultProfile</span></span>
<span data-ttu-id="996b4-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="996b4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="996b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996b4-134">CommonParameters</span></span>
<span data-ttu-id="996b4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996b4-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996b4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996b4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="996b4-137">INPUTS</span></span>

### <span data-ttu-id="996b4-138">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="996b4-138">String</span></span>
<span data-ttu-id="996b4-139">Du kan ange indata för cmdleten med egenskaps namnet men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="996b4-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="996b4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="996b4-140">OUTPUTS</span></span>

### <span data-ttu-id="996b4-141">Microsoft. Azure. commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="996b4-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="996b4-142">Denna cmdlet returnerar resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="996b4-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="996b4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="996b4-143">NOTES</span></span>

## <span data-ttu-id="996b4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="996b4-144">RELATED LINKS</span></span>

[<span data-ttu-id="996b4-145">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="996b4-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="996b4-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="996b4-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="996b4-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="996b4-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


