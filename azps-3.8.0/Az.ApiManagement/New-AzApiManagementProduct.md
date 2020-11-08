---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089951"
---
# <span data-ttu-id="76995-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="76995-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="76995-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76995-102">SYNOPSIS</span></span>
<span data-ttu-id="76995-103">Skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="76995-103">Creates an API Management product.</span></span>

## <span data-ttu-id="76995-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76995-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76995-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76995-105">DESCRIPTION</span></span>
<span data-ttu-id="76995-106">Cmdleten **New-AzApiManagementProduct** skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="76995-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="76995-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76995-107">EXAMPLES</span></span>

### <span data-ttu-id="76995-108">Exempel 1: skapa en produkt som inte kräver ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="76995-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="76995-109">Det här kommandot skapar en API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="76995-109">This command creates an API Management product.</span></span>
<span data-ttu-id="76995-110">Det krävs inget abonnemang.</span><span class="sxs-lookup"><span data-stu-id="76995-110">No subscription is required.</span></span>

### <span data-ttu-id="76995-111">Exempel 2: skapa en produkt som kräver ett abonnemang och godkännande</span><span class="sxs-lookup"><span data-stu-id="76995-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="76995-112">Det här kommandot skapar en produkt.</span><span class="sxs-lookup"><span data-stu-id="76995-112">This command creates a product.</span></span>
<span data-ttu-id="76995-113">Ett abonnemang och godkännande krävs.</span><span class="sxs-lookup"><span data-stu-id="76995-113">A subscription and approval are required.</span></span>
<span data-ttu-id="76995-114">Det här kommandot anger meddelandets tids period till 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="76995-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="76995-115">Abonnemangets längd är inställd på ett år.</span><span class="sxs-lookup"><span data-stu-id="76995-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="76995-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76995-116">PARAMETERS</span></span>

### <span data-ttu-id="76995-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="76995-117">-ApprovalRequired</span></span>
<span data-ttu-id="76995-118">Anger om prenumerationen på produkten kräver godkännande eller inte.</span><span class="sxs-lookup"><span data-stu-id="76995-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="76995-119">Denna parameter är **$false**.</span><span class="sxs-lookup"><span data-stu-id="76995-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="76995-120">-Context</span></span>
<span data-ttu-id="76995-121">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="76995-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76995-122">-DefaultProfile</span></span>
<span data-ttu-id="76995-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76995-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76995-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="76995-124">-Description</span></span>
<span data-ttu-id="76995-125">Anger produktbeskrivningen.</span><span class="sxs-lookup"><span data-stu-id="76995-125">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="76995-126">-LegalTerms</span></span>
<span data-ttu-id="76995-127">Anger juridisk användnings villkoren för produkten.</span><span class="sxs-lookup"><span data-stu-id="76995-127">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-128">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="76995-128">-ProductId</span></span>
<span data-ttu-id="76995-129">Anger identifieraren för ny produkt.</span><span class="sxs-lookup"><span data-stu-id="76995-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="76995-130">Om du inte anger den här parametern genereras en ny produkt.</span><span class="sxs-lookup"><span data-stu-id="76995-130">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-131">-State</span><span class="sxs-lookup"><span data-stu-id="76995-131">-State</span></span>
<span data-ttu-id="76995-132">Anger produktens status.</span><span class="sxs-lookup"><span data-stu-id="76995-132">Specifies the product state.</span></span>
<span data-ttu-id="76995-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="76995-133">psdx_paramvalues</span></span>
- <span data-ttu-id="76995-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="76995-134">NotPublished</span></span>
- <span data-ttu-id="76995-135">Publicerade standardvärdet är NotPublished.</span><span class="sxs-lookup"><span data-stu-id="76995-135">Published The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="76995-136">-SubscriptionRequired</span></span>
<span data-ttu-id="76995-137">Anger om produkten kräver ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="76995-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="76995-138">Standardvärdet är **$True**.</span><span class="sxs-lookup"><span data-stu-id="76995-138">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="76995-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="76995-140">Anger maximalt antal samtidiga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="76995-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="76995-141">Standardvärdet är inget.</span><span class="sxs-lookup"><span data-stu-id="76995-141">The default value is None.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-142">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="76995-142">-Title</span></span>
<span data-ttu-id="76995-143">Anger produkt rubriken.</span><span class="sxs-lookup"><span data-stu-id="76995-143">Specifies the product title.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76995-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76995-144">CommonParameters</span></span>
<span data-ttu-id="76995-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76995-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76995-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76995-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76995-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76995-147">INPUTS</span></span>

### <span data-ttu-id="76995-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76995-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76995-149">System. String</span><span class="sxs-lookup"><span data-stu-id="76995-149">System.String</span></span>

### <span data-ttu-id="76995-150">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="76995-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="76995-151">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="76995-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="76995-152">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="76995-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="76995-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76995-153">OUTPUTS</span></span>

### <span data-ttu-id="76995-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="76995-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="76995-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76995-155">NOTES</span></span>

## <span data-ttu-id="76995-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76995-156">RELATED LINKS</span></span>

[<span data-ttu-id="76995-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="76995-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="76995-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="76995-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="76995-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="76995-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)

