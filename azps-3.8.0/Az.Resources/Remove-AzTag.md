---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 1bbb2494ddbe6d355f38a719e3eaf08622b80169
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089514"
---
# <span data-ttu-id="297f5-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="297f5-101">Remove-AzTag</span></span>

## <span data-ttu-id="297f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="297f5-102">SYNOPSIS</span></span>
<span data-ttu-id="297f5-103">Tar bort fördefinierade Azure-taggar eller-värden | Tar bort hela uppsättningen taggar för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="297f5-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="297f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="297f5-104">SYNTAX</span></span>

### <span data-ttu-id="297f5-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="297f5-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f5-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297f5-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="297f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="297f5-107">DESCRIPTION</span></span>

<span data-ttu-id="297f5-108">**RemovePredefinedTagSet** : cmdleten **Remove-AzTag** tar bort fördefinierade Azure-Taggar och värden från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="297f5-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="297f5-109">Om du vill ta bort vissa värden från en fördefinierad tagg använder du *värde* -parametern.</span><span class="sxs-lookup"><span data-stu-id="297f5-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="297f5-110">Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden. Du kan inte ta bort en tagg eller ett värde som för närvarande används för en resurs-eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="297f5-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="297f5-111">Innan du använder **Remove-AzTag** kan du använda parametern *tag* i Set-AzResourceGroup cmdlet för att ta bort märket eller värdena från resursen eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="297f5-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="297f5-112">Modulerna för Azure-taggar som **tar bort-AzTag** är en del av kan hjälpa dig att hantera dina fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="297f5-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="297f5-113">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="297f5-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="297f5-114">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="297f5-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="297f5-115">**RemoveByResourceIdParameterSet** : cmdleten **Remove-AzTag** med en **ResourceID** tar bort hela uppsättningen Taggar i en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="297f5-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="297f5-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="297f5-116">EXAMPLES</span></span>

### <span data-ttu-id="297f5-117">Exempel 1: ta bort en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="297f5-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="297f5-118">Det här kommandot tar bort den fördefinierade taggen avdelning och alla dess värden.</span><span class="sxs-lookup"><span data-stu-id="297f5-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="297f5-119">Om taggen har lagts till i resurser eller resurs grupper Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="297f5-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="297f5-120">Exempel 2: ta bort ett värde från en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="297f5-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="297f5-121">Det här kommandot tar bort värdet HumanResources från det fördefinierade avdelnings märket.</span><span class="sxs-lookup"><span data-stu-id="297f5-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="297f5-122">Taggen tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="297f5-122">It does not delete the tag.</span></span>
<span data-ttu-id="297f5-123">Om värdet har kopplats till resurser eller resurs grupper Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="297f5-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="297f5-124">Exempel 3: tar bort hela uppsättningen Taggar i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="297f5-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

``` powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="297f5-125">Det här kommandot tar bort alla flaggor i prenumerationen med {subId}.</span><span class="sxs-lookup"><span data-stu-id="297f5-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="297f5-126">Objektet tas inte bort om det inte skickas i "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="297f5-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="297f5-127">Exempel 4: tar bort hela uppsättningen taggar på en resurs</span><span class="sxs-lookup"><span data-stu-id="297f5-127">Example 4: Deletes the entire set of tags on a resource</span></span>

``` powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="297f5-128">Det här kommandot tar bort alla flaggor på resursen med {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="297f5-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="297f5-129">Den returnerar den borttagna oject när du skickar "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="297f5-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="297f5-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="297f5-130">PARAMETERS</span></span>

### <span data-ttu-id="297f5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297f5-131">-DefaultProfile</span></span>
<span data-ttu-id="297f5-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="297f5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="297f5-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="297f5-133">-Name</span></span>
<span data-ttu-id="297f5-134">Anger namnet på den fördefinierade tagg som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="297f5-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="297f5-135">Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden.</span><span class="sxs-lookup"><span data-stu-id="297f5-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="297f5-136">Använd parametern *Value* för att ta bort markerade värden, men inte ta bort taggen.</span><span class="sxs-lookup"><span data-stu-id="297f5-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297f5-137">-Värde</span><span class="sxs-lookup"><span data-stu-id="297f5-137">-Value</span></span>
<span data-ttu-id="297f5-138">Tar bort angivna värden från den fördefinierade taggen, men tar inte bort taggen.</span><span class="sxs-lookup"><span data-stu-id="297f5-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297f5-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="297f5-139">-ResourceId</span></span>
<span data-ttu-id="297f5-140">Resurs-ID för den märkta enheten.</span><span class="sxs-lookup"><span data-stu-id="297f5-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="297f5-141">En resurs, en resurs grupp eller ett abonnemang kan märkas.</span><span class="sxs-lookup"><span data-stu-id="297f5-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297f5-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="297f5-142">-PassThru</span></span>
<span data-ttu-id="297f5-143">Returnerar ett objekt som representerar den borttagna taggen eller den resulterande taggen med borttagen värde.</span><span class="sxs-lookup"><span data-stu-id="297f5-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297f5-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="297f5-144">-Confirm</span></span>
<span data-ttu-id="297f5-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="297f5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297f5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297f5-146">-WhatIf</span></span>
<span data-ttu-id="297f5-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="297f5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297f5-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="297f5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297f5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297f5-149">CommonParameters</span></span>
<span data-ttu-id="297f5-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297f5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297f5-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="297f5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297f5-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="297f5-152">INPUTS</span></span>

### <span data-ttu-id="297f5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="297f5-153">System.String</span></span>

### <span data-ttu-id="297f5-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="297f5-154">System.String[]</span></span>

### <span data-ttu-id="297f5-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="297f5-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="297f5-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="297f5-156">OUTPUTS</span></span>

### <span data-ttu-id="297f5-157">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag | Microsoft. Azure. commands. taggar. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="297f5-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="297f5-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="297f5-158">NOTES</span></span>

## <span data-ttu-id="297f5-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="297f5-159">RELATED LINKS</span></span>

[<span data-ttu-id="297f5-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="297f5-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="297f5-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="297f5-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="297f5-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="297f5-162">Update-AzTag</span></span>](./Update-AzTag.md)
