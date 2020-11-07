---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755356"
---
# <span data-ttu-id="d53b3-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d53b3-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="d53b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d53b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d53b3-103">Anger produkt informationen för API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="d53b3-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d53b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d53b3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d53b3-105">DESCRIPTION</span></span>
<span data-ttu-id="d53b3-106">Cmdleten **set-AzureRmApiManagementProduct** anger produkt informationen för API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="d53b3-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="d53b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d53b3-107">EXAMPLES</span></span>

### <span data-ttu-id="d53b3-108">Exempel 1: uppdatera produkt informationen</span><span class="sxs-lookup"><span data-stu-id="d53b3-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="d53b3-109">Det här kommandot uppdaterar produkt informationen för API-hanteringen, kräver en prenumeration och avpubliceras sedan.</span><span class="sxs-lookup"><span data-stu-id="d53b3-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="d53b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d53b3-110">PARAMETERS</span></span>

### <span data-ttu-id="d53b3-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="d53b3-111">-ApprovalRequired</span></span>
<span data-ttu-id="d53b3-112">Anger om prenumerationen på produkten kräver godkännande.</span><span class="sxs-lookup"><span data-stu-id="d53b3-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="d53b3-113">Standardvärdet är **$false**.</span><span class="sxs-lookup"><span data-stu-id="d53b3-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="d53b3-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d53b3-114">-Context</span></span>
<span data-ttu-id="d53b3-115">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="d53b3-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d53b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53b3-116">-DefaultProfile</span></span>
<span data-ttu-id="d53b3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d53b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d53b3-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d53b3-118">-Description</span></span>
<span data-ttu-id="d53b3-119">Anger produktbeskrivningen.</span><span class="sxs-lookup"><span data-stu-id="d53b3-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="d53b3-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="d53b3-120">-LegalTerms</span></span>
<span data-ttu-id="d53b3-121">Anger juridisk användnings villkoren för produkten.</span><span class="sxs-lookup"><span data-stu-id="d53b3-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="d53b3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d53b3-122">-PassThru</span></span>
<span data-ttu-id="d53b3-123">passthru</span><span class="sxs-lookup"><span data-stu-id="d53b3-123">passthru</span></span>

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

### <span data-ttu-id="d53b3-124">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="d53b3-124">-ProductId</span></span>
<span data-ttu-id="d53b3-125">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="d53b3-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="d53b3-126">-State</span><span class="sxs-lookup"><span data-stu-id="d53b3-126">-State</span></span>
<span data-ttu-id="d53b3-127">Anger produktens status.</span><span class="sxs-lookup"><span data-stu-id="d53b3-127">Specifies the product state.</span></span>
<span data-ttu-id="d53b3-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d53b3-128">psdx_paramvalues</span></span>
- <span data-ttu-id="d53b3-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="d53b3-129">NotPublished</span></span>
- <span data-ttu-id="d53b3-130">Opublicera</span><span class="sxs-lookup"><span data-stu-id="d53b3-130">Published</span></span>

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

### <span data-ttu-id="d53b3-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d53b3-131">-SubscriptionRequired</span></span>
<span data-ttu-id="d53b3-132">Anger om produkten kräver ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d53b3-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="d53b3-133">Standardvärdet för den här parametern är **$True**.</span><span class="sxs-lookup"><span data-stu-id="d53b3-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="d53b3-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="d53b3-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="d53b3-135">Anger maximalt antal samtidiga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="d53b3-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="d53b3-136">Standardvärdet för den här parametern är 1.</span><span class="sxs-lookup"><span data-stu-id="d53b3-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="d53b3-137">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="d53b3-137">-Title</span></span>
<span data-ttu-id="d53b3-138">Anger produkt namnet som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="d53b3-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="d53b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53b3-139">CommonParameters</span></span>
<span data-ttu-id="d53b3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53b3-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53b3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53b3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d53b3-142">INPUTS</span></span>

### <span data-ttu-id="d53b3-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d53b3-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d53b3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d53b3-144">System.String</span></span>

### <span data-ttu-id="d53b3-145">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d53b3-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d53b3-146">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d53b3-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d53b3-147">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d53b3-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d53b3-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d53b3-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d53b3-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d53b3-149">OUTPUTS</span></span>

### <span data-ttu-id="d53b3-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d53b3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="d53b3-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d53b3-151">NOTES</span></span>

## <span data-ttu-id="d53b3-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d53b3-152">RELATED LINKS</span></span>

[<span data-ttu-id="d53b3-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d53b3-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d53b3-154">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d53b3-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d53b3-155">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d53b3-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


