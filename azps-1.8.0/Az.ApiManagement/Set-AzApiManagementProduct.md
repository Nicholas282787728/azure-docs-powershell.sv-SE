---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917669"
---
# <span data-ttu-id="3d864-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d864-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="3d864-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d864-102">SYNOPSIS</span></span>
<span data-ttu-id="3d864-103">Anger produkt informationen för API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="3d864-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="3d864-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d864-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d864-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d864-105">DESCRIPTION</span></span>
<span data-ttu-id="3d864-106">Cmdleten **set-AzApiManagementProduct** anger produkt informationen för API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="3d864-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="3d864-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d864-107">EXAMPLES</span></span>

### <span data-ttu-id="3d864-108">Exempel 1: uppdatera produkt informationen</span><span class="sxs-lookup"><span data-stu-id="3d864-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="3d864-109">Det här kommandot uppdaterar produkt informationen för API-hanteringen, kräver en prenumeration och avpubliceras sedan.</span><span class="sxs-lookup"><span data-stu-id="3d864-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="3d864-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d864-110">PARAMETERS</span></span>

### <span data-ttu-id="3d864-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="3d864-111">-ApprovalRequired</span></span>
<span data-ttu-id="3d864-112">Anger om prenumerationen på produkten kräver godkännande.</span><span class="sxs-lookup"><span data-stu-id="3d864-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="3d864-113">Standardvärdet är **$false**.</span><span class="sxs-lookup"><span data-stu-id="3d864-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="3d864-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3d864-114">-Context</span></span>
<span data-ttu-id="3d864-115">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="3d864-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3d864-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d864-116">-DefaultProfile</span></span>
<span data-ttu-id="3d864-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d864-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d864-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3d864-118">-Description</span></span>
<span data-ttu-id="3d864-119">Anger produktbeskrivningen.</span><span class="sxs-lookup"><span data-stu-id="3d864-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="3d864-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="3d864-120">-LegalTerms</span></span>
<span data-ttu-id="3d864-121">Anger juridisk användnings villkoren för produkten.</span><span class="sxs-lookup"><span data-stu-id="3d864-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="3d864-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d864-122">-PassThru</span></span>
<span data-ttu-id="3d864-123">passthru</span><span class="sxs-lookup"><span data-stu-id="3d864-123">passthru</span></span>

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

### <span data-ttu-id="3d864-124">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="3d864-124">-ProductId</span></span>
<span data-ttu-id="3d864-125">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="3d864-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="3d864-126">-State</span><span class="sxs-lookup"><span data-stu-id="3d864-126">-State</span></span>
<span data-ttu-id="3d864-127">Anger produktens status.</span><span class="sxs-lookup"><span data-stu-id="3d864-127">Specifies the product state.</span></span>
<span data-ttu-id="3d864-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="3d864-128">psdx_paramvalues</span></span>
- <span data-ttu-id="3d864-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="3d864-129">NotPublished</span></span>
- <span data-ttu-id="3d864-130">Opublicera</span><span class="sxs-lookup"><span data-stu-id="3d864-130">Published</span></span>

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

### <span data-ttu-id="3d864-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="3d864-131">-SubscriptionRequired</span></span>
<span data-ttu-id="3d864-132">Anger om produkten kräver ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3d864-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="3d864-133">Standardvärdet för den här parametern är **$True**.</span><span class="sxs-lookup"><span data-stu-id="3d864-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="3d864-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="3d864-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="3d864-135">Anger maximalt antal samtidiga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="3d864-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="3d864-136">Standardvärdet för den här parametern är 1.</span><span class="sxs-lookup"><span data-stu-id="3d864-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="3d864-137">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="3d864-137">-Title</span></span>
<span data-ttu-id="3d864-138">Anger produkt namnet som denna cmdlet ställer in.</span><span class="sxs-lookup"><span data-stu-id="3d864-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="3d864-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d864-139">CommonParameters</span></span>
<span data-ttu-id="3d864-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d864-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d864-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d864-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d864-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d864-142">INPUTS</span></span>

### <span data-ttu-id="3d864-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d864-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d864-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3d864-144">System.String</span></span>

### <span data-ttu-id="3d864-145">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d864-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3d864-146">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d864-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3d864-147">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3d864-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3d864-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d864-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d864-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d864-149">OUTPUTS</span></span>

### <span data-ttu-id="3d864-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d864-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="3d864-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d864-151">NOTES</span></span>

## <span data-ttu-id="3d864-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d864-152">RELATED LINKS</span></span>

[<span data-ttu-id="3d864-153">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d864-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="3d864-154">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d864-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="3d864-155">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d864-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


