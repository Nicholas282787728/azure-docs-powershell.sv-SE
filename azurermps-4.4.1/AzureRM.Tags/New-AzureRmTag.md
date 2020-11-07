---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756826"
---
# <span data-ttu-id="f4337-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f4337-101">New-AzureRmTag</span></span>

## <span data-ttu-id="f4337-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4337-102">SYNOPSIS</span></span>
<span data-ttu-id="f4337-103">Skapar en fördefinierad Azure-tagg eller lägger till värden i en befintlig tagg.</span><span class="sxs-lookup"><span data-stu-id="f4337-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4337-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4337-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4337-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4337-105">DESCRIPTION</span></span>
<span data-ttu-id="f4337-106">Cmdleten **New-AzureRmTag** skapar en fördefinierad Azure-tagg med ett valfritt fördefinierat värde.</span><span class="sxs-lookup"><span data-stu-id="f4337-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="f4337-107">Du kan också använda det för att lägga till fler värden i befintliga fördefinierade taggar.</span><span class="sxs-lookup"><span data-stu-id="f4337-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="f4337-108">Om du vill skapa en fördefinierad tagg anger du ett unikt taggnamn.</span><span class="sxs-lookup"><span data-stu-id="f4337-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="f4337-109">Om du vill lägga till ett värde i en befintlig fördefinierad tagg anger du namnet på den befintliga taggen och det nya värdet.</span><span class="sxs-lookup"><span data-stu-id="f4337-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="f4337-110">Denna cmdlet returnerar ett objekt som representerar den nya eller ändrade taggen med dess värden och antalet resurser som den har använts på.</span><span class="sxs-lookup"><span data-stu-id="f4337-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="f4337-111">Modulerna för Azure-taggar som **New-AzureRmTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="f4337-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="f4337-112">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="f4337-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="f4337-113">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f4337-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="f4337-114">Om prenumerationen innehåller fördefinierade koder kan du inte använda odefinierade taggar eller värden i en resurs eller resurs grupp i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f4337-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="f4337-115">Om du vill använda en fördefinierad tagg för en resurs-eller resurs grupp använder du parametern *tagg* för New-AzureRmTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4337-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="f4337-116">Om du vill söka efter resurs grupper med ett angivet taggnamn eller namn och värde använder du parametern *tagg* för Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4337-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="f4337-117">Varje tagg har ett namn.</span><span class="sxs-lookup"><span data-stu-id="f4337-117">Every tag has a name.</span></span>
<span data-ttu-id="f4337-118">Värdena är valfria.</span><span class="sxs-lookup"><span data-stu-id="f4337-118">The values are optional.</span></span>
<span data-ttu-id="f4337-119">En fördefinierad Azure-tagg kan ha flera värden, men när du använder taggen i en resurs eller resurs grupp kan du använda taggnamnet och bara ett av dess värden.</span><span class="sxs-lookup"><span data-stu-id="f4337-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="f4337-120">Du kan till exempel skapa ett fördefinierat avdelnings märke med ett värde för varje avdelning, till exempel ekonomi, mänskliga resurser och det.</span><span class="sxs-lookup"><span data-stu-id="f4337-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="f4337-121">När du använder taggen avdelning för en resurs, kan du bara använda ett fördefinierat värde, till exempel ekonomi.</span><span class="sxs-lookup"><span data-stu-id="f4337-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="f4337-122">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4337-122">EXAMPLES</span></span>

### <span data-ttu-id="f4337-123">Exempel 1: skapa en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="f4337-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="f4337-124">Det här kommandot skapar en fördefinierad tagg med namnet FY2015.</span><span class="sxs-lookup"><span data-stu-id="f4337-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="f4337-125">Den här taggen har inga värden.</span><span class="sxs-lookup"><span data-stu-id="f4337-125">This tag has no values.</span></span>
<span data-ttu-id="f4337-126">Du kan använda en tagg utan värden för en resurs eller resurs grupp eller använda **ny-AzureRmTag** för att lägga till värden i taggen.</span><span class="sxs-lookup"><span data-stu-id="f4337-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="f4337-127">Du kan också ange ett värde när du använder taggen i resursen eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4337-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="f4337-128">Exempel 2: skapa en fördefinierad tagg med ett värde</span><span class="sxs-lookup"><span data-stu-id="f4337-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="f4337-129">Det här kommandot skapar en fördefinierad tagg med namnet avdelning med ett finansierings värde.</span><span class="sxs-lookup"><span data-stu-id="f4337-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="f4337-130">Exempel 3: lägga till ett värde i en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="f4337-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="f4337-131">De här kommandona skapar en fördefinierad tagg med namnet avdelning med två värden.</span><span class="sxs-lookup"><span data-stu-id="f4337-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="f4337-132">Om taggnamnet finns lägger **AzureRmTag** till värdet till den befintliga taggen i stället för att skapa ett nytt.</span><span class="sxs-lookup"><span data-stu-id="f4337-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="f4337-133">Exempel 4: använda en fördefinierad tagg</span><span class="sxs-lookup"><span data-stu-id="f4337-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="f4337-134">Kommandona i det här exemplet skapar och använder en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="f4337-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="f4337-135">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4337-135">PARAMETERS</span></span>

### <span data-ttu-id="f4337-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4337-136">-Name</span></span>
<span data-ttu-id="f4337-137">Anger taggnamnet.</span><span class="sxs-lookup"><span data-stu-id="f4337-137">Specifies the tag name.</span></span>
<span data-ttu-id="f4337-138">Om du vill skapa en ny fördefinierad tagg anger du ett unikt namn.</span><span class="sxs-lookup"><span data-stu-id="f4337-138">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="f4337-139">Om du vill lägga till ett värde i en befintlig tagg anger du namnet på den befintliga taggen.</span><span class="sxs-lookup"><span data-stu-id="f4337-139">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="f4337-140">Om en befintlig fördefinierad tagg har det angivna namnet lägger **AzureRmTag** till det angivna värdet, om det finns något, till taggen med det namnet i stället för att skapa en ny tagg.</span><span class="sxs-lookup"><span data-stu-id="f4337-140">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="f4337-141">-Värde</span><span class="sxs-lookup"><span data-stu-id="f4337-141">-Value</span></span>
<span data-ttu-id="f4337-142">Anger ett taggvärde.</span><span class="sxs-lookup"><span data-stu-id="f4337-142">Specifies a tag value.</span></span>
<span data-ttu-id="f4337-143">Fördefinierade taggar kan ha flera värden, men det går bara att ange ett värde i varje kommando.</span><span class="sxs-lookup"><span data-stu-id="f4337-143">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="f4337-144">Den här parametern är valfri eftersom taggar kan ha namn utan värden.</span><span class="sxs-lookup"><span data-stu-id="f4337-144">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="f4337-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4337-145">-DefaultProfile</span></span>
<span data-ttu-id="f4337-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4337-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4337-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4337-147">CommonParameters</span></span>
<span data-ttu-id="f4337-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4337-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4337-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4337-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4337-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4337-150">INPUTS</span></span>

### <span data-ttu-id="f4337-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="f4337-151">None</span></span>

## <span data-ttu-id="f4337-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4337-152">OUTPUTS</span></span>

### <span data-ttu-id="f4337-153">Microsoft. Azure. commands. taggar. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="f4337-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="f4337-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4337-154">NOTES</span></span>

## <span data-ttu-id="f4337-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4337-155">RELATED LINKS</span></span>

[<span data-ttu-id="f4337-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f4337-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="f4337-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f4337-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


