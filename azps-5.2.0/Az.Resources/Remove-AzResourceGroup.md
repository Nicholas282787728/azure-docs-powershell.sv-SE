---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389580"
---
# <span data-ttu-id="410c6-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="410c6-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="410c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="410c6-102">SYNOPSIS</span></span>
<span data-ttu-id="410c6-103">Tar bort en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="410c6-103">Removes a resource group.</span></span>

## <span data-ttu-id="410c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="410c6-104">SYNTAX</span></span>

### <span data-ttu-id="410c6-105">RemoveByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="410c6-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="410c6-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="410c6-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="410c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="410c6-107">DESCRIPTION</span></span>
<span data-ttu-id="410c6-108">Cmdleten **Remove-AzResourceGroup** tar bort en Azure resurs grupp och dess resurser från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="410c6-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="410c6-109">Använd Remove-AzResource cmdlet för att ta bort en resurs, men lämna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="410c6-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="410c6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="410c6-110">EXAMPLES</span></span>

### <span data-ttu-id="410c6-111">Exempel 1: ta bort en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="410c6-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="410c6-112">Det här kommandot tar bort resurs gruppen ContosoRG01 från prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="410c6-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="410c6-113">Cmdleten uppmanar dig att bekräfta och returnerar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="410c6-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="410c6-114">Exempel 2: ta bort en resurs grupp utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="410c6-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="410c6-115">Det här kommandot använder cmdleten Get-AzResourceGroup för att hämta resurs gruppen ContosoRG01 och skickar den sedan till **Remove-AzResourceGroup** genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="410c6-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="410c6-116">Parametern *Force* gör att det inte går att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="410c6-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="410c6-117">Exempel 3: ta bort alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="410c6-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="410c6-118">Det här kommandot använder cmdleten **Get-AzResourceGroup** för att hämta alla resurs grupper och skickar dem sedan för att **ta bort-AzResourceGroup** med operatören.</span><span class="sxs-lookup"><span data-stu-id="410c6-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="410c6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="410c6-119">PARAMETERS</span></span>

### <span data-ttu-id="410c6-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="410c6-120">-ApiVersion</span></span>
<span data-ttu-id="410c6-121">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="410c6-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="410c6-122">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="410c6-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="410c6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="410c6-123">-AsJob</span></span>
<span data-ttu-id="410c6-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="410c6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="410c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410c6-125">-DefaultProfile</span></span>
<span data-ttu-id="410c6-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="410c6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="410c6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="410c6-127">-Force</span></span>
<span data-ttu-id="410c6-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="410c6-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="410c6-129">-ID</span><span class="sxs-lookup"><span data-stu-id="410c6-129">-Id</span></span>
<span data-ttu-id="410c6-130">Anger ID för resurs gruppen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="410c6-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="410c6-131">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="410c6-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410c6-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="410c6-132">-Name</span></span>
<span data-ttu-id="410c6-133">Anger namnen på de resurs grupper som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="410c6-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="410c6-134">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="410c6-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410c6-135">-För</span><span class="sxs-lookup"><span data-stu-id="410c6-135">-Pre</span></span>
<span data-ttu-id="410c6-136">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="410c6-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="410c6-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="410c6-137">-Confirm</span></span>
<span data-ttu-id="410c6-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="410c6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="410c6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="410c6-139">-WhatIf</span></span>
<span data-ttu-id="410c6-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="410c6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="410c6-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="410c6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="410c6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410c6-142">CommonParameters</span></span>
<span data-ttu-id="410c6-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="410c6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410c6-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="410c6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410c6-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="410c6-145">INPUTS</span></span>

### <span data-ttu-id="410c6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="410c6-146">System.String</span></span>

## <span data-ttu-id="410c6-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="410c6-147">OUTPUTS</span></span>

### <span data-ttu-id="410c6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="410c6-148">System.Boolean</span></span>

## <span data-ttu-id="410c6-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="410c6-149">NOTES</span></span>

## <span data-ttu-id="410c6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="410c6-150">RELATED LINKS</span></span>

[<span data-ttu-id="410c6-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="410c6-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="410c6-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="410c6-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="410c6-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="410c6-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


