---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 673aa943263a789e7d8be0a63634ddd176e09cae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573580"
---
# <span data-ttu-id="ff701-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ff701-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="ff701-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff701-102">SYNOPSIS</span></span>
<span data-ttu-id="ff701-103">Skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="ff701-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff701-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff701-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff701-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff701-105">DESCRIPTION</span></span>
<span data-ttu-id="ff701-106">Cmdleten **New-AzureRmApiManagementProduct** skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="ff701-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="ff701-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff701-107">EXAMPLES</span></span>

### <span data-ttu-id="ff701-108">Exempel 1: skapa en produkt som inte kräver ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="ff701-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="ff701-109">Det här kommandot skapar en API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="ff701-109">This command creates an API Management product.</span></span>
<span data-ttu-id="ff701-110">Det krävs inget abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ff701-110">No subscription is required.</span></span>

### <span data-ttu-id="ff701-111">Exempel 2: skapa en produkt som kräver ett abonnemang och godkännande</span><span class="sxs-lookup"><span data-stu-id="ff701-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="ff701-112">Det här kommandot skapar en produkt.</span><span class="sxs-lookup"><span data-stu-id="ff701-112">This command creates a product.</span></span>
<span data-ttu-id="ff701-113">Ett abonnemang och godkännande krävs.</span><span class="sxs-lookup"><span data-stu-id="ff701-113">A subscription and approval are required.</span></span>
<span data-ttu-id="ff701-114">Det här kommandot anger meddelandets tids period till 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="ff701-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="ff701-115">Abonnemangets längd är inställd på ett år.</span><span class="sxs-lookup"><span data-stu-id="ff701-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="ff701-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff701-116">PARAMETERS</span></span>

### <span data-ttu-id="ff701-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="ff701-117">-ApprovalRequired</span></span>
<span data-ttu-id="ff701-118">Anger om prenumerationen på produkten kräver godkännande eller inte.</span><span class="sxs-lookup"><span data-stu-id="ff701-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="ff701-119">Denna parameter är **$false**.</span><span class="sxs-lookup"><span data-stu-id="ff701-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ff701-120">-Context</span></span>
<span data-ttu-id="ff701-121">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ff701-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff701-122">-DefaultProfile</span></span>
<span data-ttu-id="ff701-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff701-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ff701-124">-Description</span></span>
<span data-ttu-id="ff701-125">Anger produktbeskrivningen.</span><span class="sxs-lookup"><span data-stu-id="ff701-125">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="ff701-126">-LegalTerms</span></span>
<span data-ttu-id="ff701-127">Anger juridisk användnings villkoren för produkten.</span><span class="sxs-lookup"><span data-stu-id="ff701-127">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-128">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="ff701-128">-ProductId</span></span>
<span data-ttu-id="ff701-129">Anger identifieraren för ny produkt.</span><span class="sxs-lookup"><span data-stu-id="ff701-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="ff701-130">Om du inte anger den här parametern genereras en ny produkt.</span><span class="sxs-lookup"><span data-stu-id="ff701-130">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-131">-State</span><span class="sxs-lookup"><span data-stu-id="ff701-131">-State</span></span>
<span data-ttu-id="ff701-132">Anger produktens status.</span><span class="sxs-lookup"><span data-stu-id="ff701-132">Specifies the product state.</span></span>
<span data-ttu-id="ff701-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ff701-133">psdx_paramvalues</span></span>

- <span data-ttu-id="ff701-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="ff701-134">NotPublished</span></span>
- <span data-ttu-id="ff701-135">Opublicera</span><span class="sxs-lookup"><span data-stu-id="ff701-135">Published</span></span> 

<span data-ttu-id="ff701-136">Standardvärdet är NotPublished.</span><span class="sxs-lookup"><span data-stu-id="ff701-136">The default value is NotPublished.</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-137">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="ff701-137">-SubscriptionRequired</span></span>
<span data-ttu-id="ff701-138">Anger om produkten kräver ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ff701-138">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="ff701-139">Standardvärdet är **$True**.</span><span class="sxs-lookup"><span data-stu-id="ff701-139">The default value is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-140">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="ff701-140">-SubscriptionsLimit</span></span>
<span data-ttu-id="ff701-141">Anger maximalt antal samtidiga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="ff701-141">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="ff701-142">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="ff701-142">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-143">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="ff701-143">-Title</span></span>
<span data-ttu-id="ff701-144">Anger produkt rubriken.</span><span class="sxs-lookup"><span data-stu-id="ff701-144">Specifies the product title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff701-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff701-145">CommonParameters</span></span>
<span data-ttu-id="ff701-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff701-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff701-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff701-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff701-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff701-148">INPUTS</span></span>

### <span data-ttu-id="ff701-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff701-149">None</span></span>
<span data-ttu-id="ff701-150">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ff701-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff701-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff701-151">OUTPUTS</span></span>

### <span data-ttu-id="ff701-152">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ff701-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="ff701-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff701-153">NOTES</span></span>

## <span data-ttu-id="ff701-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff701-154">RELATED LINKS</span></span>

[<span data-ttu-id="ff701-155">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ff701-155">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="ff701-156">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ff701-156">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="ff701-157">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ff701-157">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


