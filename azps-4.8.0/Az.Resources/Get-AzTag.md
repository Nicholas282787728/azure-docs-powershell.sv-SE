---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101995"
---
# <span data-ttu-id="8a643-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="8a643-101">Get-AzTag</span></span>

## <span data-ttu-id="8a643-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a643-102">SYNOPSIS</span></span>
<span data-ttu-id="8a643-103">Hämtar fördefinierade Azure-Taggar | Hämtar alla flaggor för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a643-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="8a643-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a643-104">SYNTAX</span></span>

### <span data-ttu-id="8a643-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a643-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a643-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a643-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a643-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a643-107">DESCRIPTION</span></span>

<span data-ttu-id="8a643-108">**GetPredefinedTagSet** : **Get-AzTag** -cmdleten får fördefinierade Azure-Taggar i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a643-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="8a643-109">Denna cmdlet returnerar grundläggande information om taggarna eller detaljerad information om taggarna och deras värden.</span><span class="sxs-lookup"><span data-stu-id="8a643-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="8a643-110">Alla utdatafiler innehåller en Count-egenskap som representerar antalet resurser och resurs grupper som taggarna och värdena har använts för.</span><span class="sxs-lookup"><span data-stu-id="8a643-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="8a643-111">Modulerna för Azure-taggar som **Get-AzTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="8a643-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="8a643-112">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="8a643-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="8a643-113">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a643-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="8a643-114">Använd New-AzTag cmdlet för att skapa en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="8a643-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="8a643-115">Om du vill använda en fördefinierad tagg för en resurs grupp använder du parametern *tagg* för New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a643-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="8a643-116">Om du vill söka efter resurs grupper för ett visst taggnamn eller namn och värde kan du använda parametern *tag* i Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a643-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="8a643-117">**GetByResourceIdParameterSet** : cmdleten **Get-AzTag** med en **ResourceID** får hela uppsättningen taggar för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="8a643-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="8a643-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a643-118">EXAMPLES</span></span>

### <span data-ttu-id="8a643-119">Exempel 1: Hämta alla fördefinierade Taggar</span><span class="sxs-lookup"><span data-stu-id="8a643-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="8a643-120">Det här kommandot får alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a643-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="8a643-121">Egenskapen Count visar hur många gånger märket har använts för resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a643-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="8a643-122">Exempel 2: Hämta ett märkord efter namn</span><span class="sxs-lookup"><span data-stu-id="8a643-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="8a643-123">Det här kommandot får detaljerad information om avdelnings märket och dess värden.</span><span class="sxs-lookup"><span data-stu-id="8a643-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="8a643-124">Egenskapen Count visar hur många gånger taggen och alla dess värden har kopplats till resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a643-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="8a643-125">Exempel 3: få värden för alla Taggar</span><span class="sxs-lookup"><span data-stu-id="8a643-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="8a643-126">Det här kommandot använder den *detaljerade* parametern för att få detaljerad information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a643-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="8a643-127">Om du använder en *detaljerad* parameter används parametern *Name* för varje tagg.</span><span class="sxs-lookup"><span data-stu-id="8a643-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="8a643-128">Exempel 4: Hämta hela uppsättningen taggar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="8a643-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="8a643-129">Det här kommandot får hela uppsättningen Taggar i prenumerationen med {subId}.</span><span class="sxs-lookup"><span data-stu-id="8a643-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="8a643-130">Exempel 5: Hämta hela uppsättningen taggar för en resurs</span><span class="sxs-lookup"><span data-stu-id="8a643-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="8a643-131">Det här kommandot får hela uppsättningen taggar på resursen med {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="8a643-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="8a643-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a643-132">PARAMETERS</span></span>

### <span data-ttu-id="8a643-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a643-133">-DefaultProfile</span></span>
<span data-ttu-id="8a643-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a643-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a643-135">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="8a643-135">-Detailed</span></span>
<span data-ttu-id="8a643-136">Anger att den här åtgärden lägger till information om tagg värden i resultatet.</span><span class="sxs-lookup"><span data-stu-id="8a643-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a643-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a643-137">-Name</span></span>
<span data-ttu-id="8a643-138">Namn på den fördefinierade taggen.</span><span class="sxs-lookup"><span data-stu-id="8a643-138">Name of the predefined tag.</span></span>
<span data-ttu-id="8a643-139">Som standard får **Get-AzTag** grundläggande information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8a643-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="8a643-140">När du anger parametern *Name* har den *detaljerade* parametern ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="8a643-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a643-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a643-141">-ResourceId</span></span>
<span data-ttu-id="8a643-142">Resurs-ID för den märkta enheten.</span><span class="sxs-lookup"><span data-stu-id="8a643-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="8a643-143">En resurs, en resurs grupp eller ett abonnemang kan märkas.</span><span class="sxs-lookup"><span data-stu-id="8a643-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a643-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a643-144">CommonParameters</span></span>
<span data-ttu-id="8a643-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a643-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a643-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a643-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a643-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a643-147">INPUTS</span></span>

### <span data-ttu-id="8a643-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8a643-148">System.String</span></span>

### <span data-ttu-id="8a643-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a643-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a643-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a643-150">OUTPUTS</span></span>

### <span data-ttu-id="8a643-151">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag | Microsoft. Azure. commands. taggar. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="8a643-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="8a643-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a643-152">NOTES</span></span>

## <span data-ttu-id="8a643-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a643-153">RELATED LINKS</span></span>

[<span data-ttu-id="8a643-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="8a643-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="8a643-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="8a643-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="8a643-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="8a643-156">Update-AzTag</span></span>](./Update-AzTag.md)
