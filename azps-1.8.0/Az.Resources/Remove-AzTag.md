---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: f9afc10613024d99cfa6b03b260324b3e5d22586
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747051"
---
# <span data-ttu-id="9b03f-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b03f-101">Remove-AzTag</span></span>

## <span data-ttu-id="9b03f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b03f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b03f-103">Tar bort fördefinierade Azure-taggar eller-värden.</span><span class="sxs-lookup"><span data-stu-id="9b03f-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="9b03f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b03f-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b03f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b03f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b03f-106">Cmdleten **Remove-AzTag** tar bort fördefinierade Azure-Taggar och värden från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9b03f-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="9b03f-107">Om du vill ta bort vissa värden från en fördefinierad tagg använder du *värde* -parametern.</span><span class="sxs-lookup"><span data-stu-id="9b03f-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="9b03f-108">Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden. Du kan inte ta bort en tagg eller ett värde som för närvarande används för en resurs-eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9b03f-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="9b03f-109">Innan du använder **Remove-AzTag** kan du använda parametern *tag* i Set-AzResourceGroup cmdlet för att ta bort märket eller värdena från resursen eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9b03f-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="9b03f-110">Modulerna för Azure-taggar som **tar bort-AzTag** är en del av kan hjälpa dig att hantera dina fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="9b03f-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="9b03f-111">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="9b03f-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="9b03f-112">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9b03f-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="9b03f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b03f-113">EXAMPLES</span></span>

### <span data-ttu-id="9b03f-114">Exempel 1: ta bort en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="9b03f-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="9b03f-115">Det här kommandot tar bort den fördefinierade taggen avdelning och alla dess resurser.</span><span class="sxs-lookup"><span data-stu-id="9b03f-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="9b03f-116">Om taggen har lagts till i resurser eller resurs grupper Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="9b03f-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="9b03f-117">Exempel 2: ta bort ett värde från en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="9b03f-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="9b03f-118">Det här kommandot tar bort värdet HumanResources från det fördefinierade avdelnings märket.</span><span class="sxs-lookup"><span data-stu-id="9b03f-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="9b03f-119">Taggen tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="9b03f-119">It does not delete the tag.</span></span>
<span data-ttu-id="9b03f-120">Om värdet har kopplats till resurser eller resurs grupper Miss lyckas kommandot.</span><span class="sxs-lookup"><span data-stu-id="9b03f-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="9b03f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b03f-121">PARAMETERS</span></span>

### <span data-ttu-id="9b03f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b03f-122">-DefaultProfile</span></span>
<span data-ttu-id="9b03f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b03f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b03f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b03f-124">-Name</span></span>
<span data-ttu-id="9b03f-125">Anger namnet på den tagg som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9b03f-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="9b03f-126">Som standard tar **Remove-AzTag** bort den angivna taggen och alla dess värden.</span><span class="sxs-lookup"><span data-stu-id="9b03f-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="9b03f-127">Använd parametern *Value* för att ta bort markerade värden, men inte ta bort taggen.</span><span class="sxs-lookup"><span data-stu-id="9b03f-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b03f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b03f-128">-PassThru</span></span>
<span data-ttu-id="9b03f-129">Returnerar ett objekt som representerar den borttagna taggen eller den resulterande taggen med borttagen värde.</span><span class="sxs-lookup"><span data-stu-id="9b03f-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="9b03f-130">-Värde</span><span class="sxs-lookup"><span data-stu-id="9b03f-130">-Value</span></span>
<span data-ttu-id="9b03f-131">Tar bort angivna värden från den fördefinierade taggen, men tar inte bort taggen.</span><span class="sxs-lookup"><span data-stu-id="9b03f-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b03f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b03f-132">-Confirm</span></span>
<span data-ttu-id="9b03f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b03f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b03f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b03f-134">-WhatIf</span></span>
<span data-ttu-id="9b03f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b03f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b03f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b03f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b03f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b03f-137">CommonParameters</span></span>
<span data-ttu-id="9b03f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b03f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b03f-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b03f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b03f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b03f-140">INPUTS</span></span>

### <span data-ttu-id="9b03f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b03f-141">System.String</span></span>

### <span data-ttu-id="9b03f-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="9b03f-142">System.String[]</span></span>

### <span data-ttu-id="9b03f-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b03f-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b03f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b03f-144">OUTPUTS</span></span>

### <span data-ttu-id="9b03f-145">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag</span><span class="sxs-lookup"><span data-stu-id="9b03f-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="9b03f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b03f-146">NOTES</span></span>

## <span data-ttu-id="9b03f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b03f-147">RELATED LINKS</span></span>

[<span data-ttu-id="9b03f-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b03f-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="9b03f-149">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="9b03f-149">New-AzTag</span></span>](./New-AzTag.md)


