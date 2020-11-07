---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: ce672284a3d9887fe52c33081f04a86e1e072405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920087"
---
# <span data-ttu-id="11cbf-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="11cbf-101">Get-AzTag</span></span>

## <span data-ttu-id="11cbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="11cbf-103">Hämtar fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="11cbf-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="11cbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11cbf-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11cbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="11cbf-106">Cmdleten **Get-AzTag** får fördefinierade Azure-Taggar i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="11cbf-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="11cbf-107">Denna cmdlet returnerar grundläggande information om taggarna eller detaljerad information om taggarna och deras värden.</span><span class="sxs-lookup"><span data-stu-id="11cbf-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="11cbf-108">Alla utdatafiler innehåller en Count-egenskap som representerar antalet resurser och resurs grupper som taggarna och värdena har använts för.</span><span class="sxs-lookup"><span data-stu-id="11cbf-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="11cbf-109">Modulerna för Azure-taggar som **Get-AzTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="11cbf-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="11cbf-110">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="11cbf-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="11cbf-111">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="11cbf-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="11cbf-112">Använd New-AzTag cmdlet för att skapa en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="11cbf-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="11cbf-113">Om du vill använda en fördefinierad tagg för en resurs grupp använder du parametern *tagg* för New-AzTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11cbf-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="11cbf-114">Om du vill söka efter resurs grupper för ett visst taggnamn eller namn och värde kan du använda parametern *tag* i Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11cbf-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="11cbf-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11cbf-115">EXAMPLES</span></span>

### <span data-ttu-id="11cbf-116">Exempel 1: Hämta alla fördefinierade Taggar</span><span class="sxs-lookup"><span data-stu-id="11cbf-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="11cbf-117">Det här kommandot får alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cbf-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="11cbf-118">Egenskapen Count visar hur många gånger märket har använts för resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cbf-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="11cbf-119">Exempel 2: Hämta ett märkord efter namn</span><span class="sxs-lookup"><span data-stu-id="11cbf-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="11cbf-120">Det här kommandot får detaljerad information om avdelnings märket och dess värden.</span><span class="sxs-lookup"><span data-stu-id="11cbf-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="11cbf-121">Egenskapen Count visar hur många gånger taggen och alla dess värden har kopplats till resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cbf-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="11cbf-122">Exempel 3: få värden för alla Taggar</span><span class="sxs-lookup"><span data-stu-id="11cbf-122">Example 3: Get values of all tags</span></span>
```
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

<span data-ttu-id="11cbf-123">Det här kommandot använder den *detaljerade* parametern för att få detaljerad information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cbf-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="11cbf-124">Om du använder en *detaljerad* parameter används parametern *Name* för varje tagg.</span><span class="sxs-lookup"><span data-stu-id="11cbf-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="11cbf-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11cbf-125">PARAMETERS</span></span>

### <span data-ttu-id="11cbf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cbf-126">-DefaultProfile</span></span>
<span data-ttu-id="11cbf-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11cbf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11cbf-128">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="11cbf-128">-Detailed</span></span>
<span data-ttu-id="11cbf-129">Anger att den här åtgärden lägger till information om tagg värden i resultatet.</span><span class="sxs-lookup"><span data-stu-id="11cbf-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="11cbf-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="11cbf-130">-Name</span></span>
<span data-ttu-id="11cbf-131">Anger namnet på etiketten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="11cbf-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="11cbf-132">Som standard får **Get-AzTag** grundläggande information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="11cbf-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="11cbf-133">När du anger parametern *Name* har den *detaljerade* parametern ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="11cbf-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11cbf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cbf-134">CommonParameters</span></span>
<span data-ttu-id="11cbf-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cbf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cbf-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cbf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cbf-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11cbf-137">INPUTS</span></span>

### <span data-ttu-id="11cbf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="11cbf-138">System.String</span></span>

### <span data-ttu-id="11cbf-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11cbf-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11cbf-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11cbf-140">OUTPUTS</span></span>

### <span data-ttu-id="11cbf-141">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag</span><span class="sxs-lookup"><span data-stu-id="11cbf-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="11cbf-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11cbf-142">NOTES</span></span>

## <span data-ttu-id="11cbf-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11cbf-143">RELATED LINKS</span></span>

[<span data-ttu-id="11cbf-144">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="11cbf-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="11cbf-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="11cbf-145">Remove-AzTag</span></span>](./Remove-AzTag.md)


