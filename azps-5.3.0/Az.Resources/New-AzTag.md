---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521360"
---
# <span data-ttu-id="0ec6c-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="0ec6c-101">New-AzTag</span></span>

## <span data-ttu-id="0ec6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ec6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec6c-103">Skapar en fördefinierad Azure-tagg eller lägger till värden i en befintlig tagg | Skapar eller uppdaterar hela uppsättningen taggar för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="0ec6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ec6c-104">SYNTAX</span></span>

### <span data-ttu-id="0ec6c-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ec6c-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ec6c-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ec6c-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="0ec6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ec6c-107">DESCRIPTION</span></span>

<span data-ttu-id="0ec6c-108">**CreatePredefinedTagSet**: den **nya-AzTag-** cmdleten skapar en fördefinierad Azure-tagg med ett valfritt fördefinierat värde.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="0ec6c-109">Du kan också använda det för att lägga till fler värden i befintliga fördefinierade taggar.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="0ec6c-110">Om du vill skapa en fördefinierad tagg anger du ett unikt taggnamn.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="0ec6c-111">Om du vill lägga till ett värde i en befintlig fördefinierad tagg anger du namnet på den befintliga taggen och det nya värdet.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="0ec6c-112">Denna cmdlet returnerar ett objekt som representerar den nya eller ändrade taggen med dess värden och antalet resurser som den har använts på.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="0ec6c-113">Modulerna för Azure-taggar som **New-AzTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="0ec6c-114">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="0ec6c-115">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="0ec6c-116">Om du vill använda en fördefinierad tagg för en resurs-eller resurs grupp använder du parametern *tagg* för New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="0ec6c-117">Om du vill söka efter resurs grupper med ett angivet taggnamn eller namn och värde använder du parametern *tagg* för Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0ec6c-118">Varje tagg har ett namn.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-118">Every tag has a name.</span></span>
<span data-ttu-id="0ec6c-119">Värdena är valfria.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-119">The values are optional.</span></span>
<span data-ttu-id="0ec6c-120">En fördefinierad Azure-tagg kan ha flera värden, men när du använder taggen i en resurs eller resurs grupp kan du använda taggnamnet och bara ett av dess värden.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="0ec6c-121">Du kan till exempel skapa ett fördefinierat avdelnings märke med ett värde för varje avdelning, till exempel ekonomi, mänskliga resurser och det.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="0ec6c-122">När du använder taggen avdelning för en resurs, kan du bara använda ett fördefinierat värde, till exempel ekonomi.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="0ec6c-123">**CreateByResourceIdParameterSet**: den **nya-AzTag-** cmdleten med en **ResourceID** skapar eller uppdaterar hela uppsättningen taggar för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="0ec6c-124">Med den här åtgärden kan du lägga till eller ersätta hela uppsättningen taggar för den angivna resursen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="0ec6c-125">Den angivna enheten kan innehålla högst 50 taggar.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="0ec6c-126">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ec6c-126">EXAMPLES</span></span>

### <span data-ttu-id="0ec6c-127">Exempel 1: skapa en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="0ec6c-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="0ec6c-128">Det här kommandot skapar en fördefinierad tagg med namnet FY2015.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="0ec6c-129">Den här taggen har inga värden.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-129">This tag has no values.</span></span>
<span data-ttu-id="0ec6c-130">Du kan använda en tagg utan värden för en resurs eller resurs grupp eller använda **ny-AzTag** för att lägga till värden i taggen.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="0ec6c-131">Du kan också ange ett värde när du använder taggen i resursen eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="0ec6c-132">Exempel 2: skapa en fördefinierad tagg med ett värde</span><span class="sxs-lookup"><span data-stu-id="0ec6c-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="0ec6c-133">Det här kommandot skapar en fördefinierad tagg med namnet avdelning med ett finansierings värde.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="0ec6c-134">Exempel 3: lägga till ett värde i en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="0ec6c-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="0ec6c-135">De här kommandona skapar en fördefinierad tagg med namnet avdelning med två värden.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="0ec6c-136">Om taggnamnet finns lägger **AzTag** till värdet till den befintliga taggen i stället för att skapa ett nytt.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="0ec6c-137">Exempel 4: använda en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="0ec6c-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="0ec6c-138">Kommandona i det här exemplet skapar och använder en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="0ec6c-139">Exempel 5: skapar eller uppdaterar hela uppsättningen Taggar i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="0ec6c-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="0ec6c-140">Det här kommandot skapar eller uppdaterar hela uppsättningen Taggar i prenumerationen med {subId}.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="0ec6c-141">Exempel 6: skapar eller uppdaterar hela uppsättningen taggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="0ec6c-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="0ec6c-142">Det här kommandot skapar eller uppdaterar hela uppsättningen taggar på resursen med {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="0ec6c-143">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ec6c-143">PARAMETERS</span></span>

### <span data-ttu-id="0ec6c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec6c-144">-DefaultProfile</span></span>
<span data-ttu-id="0ec6c-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ec6c-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ec6c-146">-Name</span></span>
<span data-ttu-id="0ec6c-147">Anger det fördefinierade taggnamnet.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="0ec6c-148">Om du vill skapa en ny fördefinierad tagg anger du ett unikt namn.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="0ec6c-149">Om du vill lägga till ett värde i en befintlig tagg anger du namnet på den befintliga taggen.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="0ec6c-150">Om en befintlig fördefinierad tagg har det angivna namnet lägger **AzTag** till det angivna värdet, om det finns något, till taggen med det namnet i stället för att skapa en ny tagg.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec6c-151">-Värde</span><span class="sxs-lookup"><span data-stu-id="0ec6c-151">-Value</span></span>
<span data-ttu-id="0ec6c-152">Anger ett fördefinierat taggvärde.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="0ec6c-153">Fördefinierade taggar kan ha flera värden, men det går bara att ange ett värde i varje kommando.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="0ec6c-154">Den här parametern är valfri eftersom taggar kan ha namn utan värden.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec6c-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ec6c-155">-ResourceId</span></span>
<span data-ttu-id="0ec6c-156">Resurs-ID för den entitet som är märkt.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="0ec6c-157">En resurs, en resurs grupp eller ett abonnemang kan märkas.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec6c-158">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0ec6c-158">-Tag</span></span>
<span data-ttu-id="0ec6c-159">Taggarna som ska placeras på resursen.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec6c-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ec6c-160">-Confirm</span></span>
<span data-ttu-id="0ec6c-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ec6c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ec6c-162">-WhatIf</span></span>
<span data-ttu-id="0ec6c-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ec6c-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ec6c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec6c-165">CommonParameters</span></span>
<span data-ttu-id="0ec6c-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec6c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec6c-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ec6c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec6c-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ec6c-168">INPUTS</span></span>

### <span data-ttu-id="0ec6c-169">System. String</span><span class="sxs-lookup"><span data-stu-id="0ec6c-169">System.String</span></span>

### <span data-ttu-id="0ec6c-170">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0ec6c-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ec6c-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ec6c-171">OUTPUTS</span></span>

### <span data-ttu-id="0ec6c-172">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag | Microsoft. Azure. commands. taggar. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="0ec6c-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="0ec6c-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ec6c-173">NOTES</span></span>

## <span data-ttu-id="0ec6c-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ec6c-174">RELATED LINKS</span></span>

[<span data-ttu-id="0ec6c-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="0ec6c-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="0ec6c-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="0ec6c-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="0ec6c-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="0ec6c-177">Update-AzTag</span></span>](./Update-AzTag.md)