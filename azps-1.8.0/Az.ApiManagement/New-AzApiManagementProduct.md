---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1eef13c2227a2cc4da50f63b9ad3cc11b6969a1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917846"
---
# <span data-ttu-id="4222e-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4222e-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="4222e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4222e-102">SYNOPSIS</span></span>
<span data-ttu-id="4222e-103">Skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="4222e-103">Creates an API Management product.</span></span>

## <span data-ttu-id="4222e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4222e-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4222e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4222e-105">DESCRIPTION</span></span>
<span data-ttu-id="4222e-106">Cmdleten **New-AzApiManagementProduct** skapar en API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="4222e-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="4222e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4222e-107">EXAMPLES</span></span>

### <span data-ttu-id="4222e-108">Exempel 1: skapa en produkt som inte kräver ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4222e-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="4222e-109">Det här kommandot skapar en API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="4222e-109">This command creates an API Management product.</span></span>
<span data-ttu-id="4222e-110">Det krävs inget abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4222e-110">No subscription is required.</span></span>

### <span data-ttu-id="4222e-111">Exempel 2: skapa en produkt som kräver ett abonnemang och godkännande</span><span class="sxs-lookup"><span data-stu-id="4222e-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="4222e-112">Det här kommandot skapar en produkt.</span><span class="sxs-lookup"><span data-stu-id="4222e-112">This command creates a product.</span></span>
<span data-ttu-id="4222e-113">Ett abonnemang och godkännande krävs.</span><span class="sxs-lookup"><span data-stu-id="4222e-113">A subscription and approval are required.</span></span>
<span data-ttu-id="4222e-114">Det här kommandot anger meddelandets tids period till 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="4222e-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="4222e-115">Abonnemangets längd är inställd på ett år.</span><span class="sxs-lookup"><span data-stu-id="4222e-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="4222e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4222e-116">PARAMETERS</span></span>

### <span data-ttu-id="4222e-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="4222e-117">-ApprovalRequired</span></span>
<span data-ttu-id="4222e-118">Anger om prenumerationen på produkten kräver godkännande eller inte.</span><span class="sxs-lookup"><span data-stu-id="4222e-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="4222e-119">Denna parameter är **$false**.</span><span class="sxs-lookup"><span data-stu-id="4222e-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="4222e-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4222e-120">-Context</span></span>
<span data-ttu-id="4222e-121">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4222e-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4222e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4222e-122">-DefaultProfile</span></span>
<span data-ttu-id="4222e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4222e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4222e-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4222e-124">-Description</span></span>
<span data-ttu-id="4222e-125">Anger produktbeskrivningen.</span><span class="sxs-lookup"><span data-stu-id="4222e-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="4222e-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="4222e-126">-LegalTerms</span></span>
<span data-ttu-id="4222e-127">Anger juridisk användnings villkoren för produkten.</span><span class="sxs-lookup"><span data-stu-id="4222e-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="4222e-128">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="4222e-128">-ProductId</span></span>
<span data-ttu-id="4222e-129">Anger identifieraren för ny produkt.</span><span class="sxs-lookup"><span data-stu-id="4222e-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="4222e-130">Om du inte anger den här parametern genereras en ny produkt.</span><span class="sxs-lookup"><span data-stu-id="4222e-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="4222e-131">-State</span><span class="sxs-lookup"><span data-stu-id="4222e-131">-State</span></span>
<span data-ttu-id="4222e-132">Anger produktens status.</span><span class="sxs-lookup"><span data-stu-id="4222e-132">Specifies the product state.</span></span>
<span data-ttu-id="4222e-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="4222e-133">psdx_paramvalues</span></span>
- <span data-ttu-id="4222e-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="4222e-134">NotPublished</span></span>
- <span data-ttu-id="4222e-135">Publicerade standardvärdet är NotPublished.</span><span class="sxs-lookup"><span data-stu-id="4222e-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="4222e-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="4222e-136">-SubscriptionRequired</span></span>
<span data-ttu-id="4222e-137">Anger om produkten kräver ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4222e-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="4222e-138">Standardvärdet är **$True**.</span><span class="sxs-lookup"><span data-stu-id="4222e-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="4222e-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="4222e-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="4222e-140">Anger maximalt antal samtidiga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="4222e-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="4222e-141">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="4222e-141">The default value is 1.</span></span>

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

### <span data-ttu-id="4222e-142">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="4222e-142">-Title</span></span>
<span data-ttu-id="4222e-143">Anger produkt rubriken.</span><span class="sxs-lookup"><span data-stu-id="4222e-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="4222e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4222e-144">CommonParameters</span></span>
<span data-ttu-id="4222e-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4222e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4222e-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4222e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4222e-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4222e-147">INPUTS</span></span>

### <span data-ttu-id="4222e-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4222e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4222e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4222e-149">System.String</span></span>

### <span data-ttu-id="4222e-150">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4222e-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4222e-151">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4222e-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4222e-152">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4222e-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4222e-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4222e-153">OUTPUTS</span></span>

### <span data-ttu-id="4222e-154">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4222e-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="4222e-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4222e-155">NOTES</span></span>

## <span data-ttu-id="4222e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4222e-156">RELATED LINKS</span></span>

[<span data-ttu-id="4222e-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4222e-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="4222e-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4222e-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="4222e-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4222e-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


