---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584827"
---
# <span data-ttu-id="4af9f-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4af9f-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="4af9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4af9f-102">SYNOPSIS</span></span>
<span data-ttu-id="4af9f-103">Hämtar fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="4af9f-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4af9f-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4af9f-105">DESCRIPTION</span></span>
<span data-ttu-id="4af9f-106">Cmdleten **Get-AzureRmTag** får fördefinierade Azure-Taggar i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4af9f-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="4af9f-107">Denna cmdlet returnerar grundläggande information om taggarna eller detaljerad information om taggarna och deras värden.</span><span class="sxs-lookup"><span data-stu-id="4af9f-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="4af9f-108">Alla utdatafiler innehåller en Count-egenskap som representerar antalet resurser och resurs grupper som taggarna och värdena har använts för.</span><span class="sxs-lookup"><span data-stu-id="4af9f-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="4af9f-109">Modulerna för Azure-taggar som **Get-AzureRMTag** är en del av kan hjälpa dig att hantera fördefinierade Azure-taggar.</span><span class="sxs-lookup"><span data-stu-id="4af9f-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="4af9f-110">En Azure-tagg är ett namn värde par som du kan använda för att kategorisera dina Azure-resurser och resurs grupper, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna och grupperna.</span><span class="sxs-lookup"><span data-stu-id="4af9f-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="4af9f-111">Du kan definiera och använda taggar i ett enda steg, men fördefinierade Taggar låter dig fastställa standard, konsekventa, förutsägbara namn och värden för taggarna i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4af9f-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="4af9f-112">Använd New-AzureRmTag cmdlet för att skapa en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="4af9f-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="4af9f-113">Om du vill använda en fördefinierad tagg för en resurs grupp använder du parametern *tagg* för New-AzureRmTag cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af9f-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="4af9f-114">Om du vill söka efter resurs grupper för ett visst taggnamn eller namn och värde kan du använda parametern *tag* i Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af9f-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="4af9f-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4af9f-115">EXAMPLES</span></span>

### <span data-ttu-id="4af9f-116">Exempel 1: Hämta alla fördefinierade Taggar</span><span class="sxs-lookup"><span data-stu-id="4af9f-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="4af9f-117">Det här kommandot får alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4af9f-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="4af9f-118">Egenskapen Count visar hur många gånger märket har använts för resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4af9f-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="4af9f-119">Exempel 2: Hämta ett märkord efter namn</span><span class="sxs-lookup"><span data-stu-id="4af9f-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="4af9f-120">Det här kommandot får detaljerad information om avdelnings märket och dess värden.</span><span class="sxs-lookup"><span data-stu-id="4af9f-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="4af9f-121">Egenskapen Count visar hur många gånger taggen och alla dess värden har kopplats till resurser och resurs grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4af9f-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="4af9f-122">Exempel 3: få värden för alla Taggar</span><span class="sxs-lookup"><span data-stu-id="4af9f-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="4af9f-123">Det här kommandot använder den *detaljerade* parametern för att få detaljerad information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4af9f-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="4af9f-124">Om du använder en *detaljerad* parameter används parametern *Name* för varje tagg.</span><span class="sxs-lookup"><span data-stu-id="4af9f-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="4af9f-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4af9f-125">PARAMETERS</span></span>

### <span data-ttu-id="4af9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af9f-126">-DefaultProfile</span></span>
<span data-ttu-id="4af9f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4af9f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af9f-128">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="4af9f-128">-Detailed</span></span>
<span data-ttu-id="4af9f-129">Anger att den här åtgärden lägger till information om tagg värden i resultatet.</span><span class="sxs-lookup"><span data-stu-id="4af9f-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="4af9f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="4af9f-130">-Name</span></span>
<span data-ttu-id="4af9f-131">Anger namnet på etiketten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4af9f-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="4af9f-132">Som standard får **Get-AzureRmTag** grundläggande information om alla fördefinierade Taggar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4af9f-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="4af9f-133">När du anger parametern *Name* har den *detaljerade* parametern ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="4af9f-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="4af9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af9f-134">CommonParameters</span></span>
<span data-ttu-id="4af9f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af9f-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af9f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af9f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4af9f-137">INPUTS</span></span>

### <span data-ttu-id="4af9f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4af9f-138">System.String</span></span>

### <span data-ttu-id="4af9f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4af9f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4af9f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4af9f-140">OUTPUTS</span></span>

### <span data-ttu-id="4af9f-141">Microsoft. Azure. commands. ResourceManager. Common. taggar. PSTag</span><span class="sxs-lookup"><span data-stu-id="4af9f-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="4af9f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4af9f-142">NOTES</span></span>

## <span data-ttu-id="4af9f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4af9f-143">RELATED LINKS</span></span>

[<span data-ttu-id="4af9f-144">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4af9f-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="4af9f-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="4af9f-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


