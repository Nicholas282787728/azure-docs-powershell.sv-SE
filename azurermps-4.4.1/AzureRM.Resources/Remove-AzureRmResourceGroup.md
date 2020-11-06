---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581295"
---
# <span data-ttu-id="f9994-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9994-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f9994-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9994-102">SYNOPSIS</span></span>
<span data-ttu-id="f9994-103">Tar bort en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f9994-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9994-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9994-104">SYNTAX</span></span>

### <span data-ttu-id="f9994-105">Visar resurs gruppen baserat på namnet.</span><span class="sxs-lookup"><span data-stu-id="f9994-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="f9994-106">Vis</span><span class="sxs-lookup"><span data-stu-id="f9994-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9994-107">Visar resurs gruppen baserat på ID.</span><span class="sxs-lookup"><span data-stu-id="f9994-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9994-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9994-108">DESCRIPTION</span></span>
<span data-ttu-id="f9994-109">Cmdleten **Remove-AzureRmResourceGroup** tar bort en Azure resurs grupp och dess resurser från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f9994-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="f9994-110">Använd Remove-AzureRmResource cmdlet för att ta bort en resurs, men lämna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9994-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="f9994-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9994-111">EXAMPLES</span></span>

### <span data-ttu-id="f9994-112">Exempel 1: ta bort en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f9994-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="f9994-113">Det här kommandot tar bort resurs gruppen ContosoRG01 från prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f9994-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="f9994-114">Cmdleten uppmanar dig att bekräfta och returnerar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f9994-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="f9994-115">Exempel 2: ta bort en resurs grupp utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="f9994-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="f9994-116">Det här kommandot använder cmdleten Get-AzureRmResourceGroup för att hämta resurs gruppen ContosoRG01 och skickar den sedan till **Remove-AzureRmResourceGroup** genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f9994-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="f9994-117">Den *utförliga* gemensamma parametern får statusinformation om åtgärden och *Force* -parametern gör att uppmaningen inte bekräftas.</span><span class="sxs-lookup"><span data-stu-id="f9994-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="f9994-118">Exempel 3: ta bort alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="f9994-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="f9994-119">Det här kommandot använder cmdleten **Get-AzureRmResourceGroup** för att hämta alla resurs grupper och skickar dem sedan för att **ta bort-AzureRmResourceGroup** med operatören.</span><span class="sxs-lookup"><span data-stu-id="f9994-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="f9994-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9994-120">PARAMETERS</span></span>

### <span data-ttu-id="f9994-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f9994-121">-ApiVersion</span></span>
<span data-ttu-id="f9994-122">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="f9994-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f9994-123">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="f9994-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f9994-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f9994-124">-Force</span></span>
<span data-ttu-id="f9994-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f9994-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9994-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f9994-126">-Id</span></span>
<span data-ttu-id="f9994-127">Anger ID för resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f9994-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="f9994-128">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="f9994-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9994-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9994-129">-Name</span></span>
<span data-ttu-id="f9994-130">Anger namnen på de resurs grupper som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f9994-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="f9994-131">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="f9994-131">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="f9994-132">-För</span><span class="sxs-lookup"><span data-stu-id="f9994-132">-Pre</span></span>
<span data-ttu-id="f9994-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f9994-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f9994-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9994-134">-Confirm</span></span>
<span data-ttu-id="f9994-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9994-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9994-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9994-136">-WhatIf</span></span>
<span data-ttu-id="f9994-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9994-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9994-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9994-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9994-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9994-139">-DefaultProfile</span></span>
<span data-ttu-id="f9994-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9994-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9994-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9994-141">CommonParameters</span></span>
<span data-ttu-id="f9994-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9994-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9994-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9994-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9994-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9994-144">INPUTS</span></span>

### <span data-ttu-id="f9994-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="f9994-145">None</span></span>

## <span data-ttu-id="f9994-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9994-146">OUTPUTS</span></span>

### <span data-ttu-id="f9994-147">Ingen</span><span class="sxs-lookup"><span data-stu-id="f9994-147">None</span></span>

## <span data-ttu-id="f9994-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9994-148">NOTES</span></span>

## <span data-ttu-id="f9994-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9994-149">RELATED LINKS</span></span>

[<span data-ttu-id="f9994-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9994-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="f9994-151">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9994-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="f9994-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9994-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


