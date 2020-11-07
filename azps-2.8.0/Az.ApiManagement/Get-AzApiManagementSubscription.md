---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745820"
---
# <span data-ttu-id="da728-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="da728-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="da728-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da728-102">SYNOPSIS</span></span>
<span data-ttu-id="da728-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="da728-103">Gets subscriptions.</span></span>

## <span data-ttu-id="da728-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da728-104">SYNTAX</span></span>

### <span data-ttu-id="da728-105">GetAllSubscriptions (standard)</span><span class="sxs-lookup"><span data-stu-id="da728-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da728-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da728-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da728-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="da728-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da728-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="da728-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da728-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="da728-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da728-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="da728-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da728-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da728-111">DESCRIPTION</span></span>
<span data-ttu-id="da728-112">Cmdleten **Get-AzApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="da728-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="da728-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da728-113">EXAMPLES</span></span>

### <span data-ttu-id="da728-114">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="da728-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="da728-115">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="da728-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="da728-116">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="da728-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="da728-117">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="da728-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="da728-118">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="da728-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="da728-119">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="da728-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="da728-120">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="da728-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="da728-121">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="da728-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="da728-122">Exempel 5: Hämta alla abonnemang för ett scope</span><span class="sxs-lookup"><span data-stu-id="da728-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="da728-123">Det här kommandot får alla prenumerationer som har kon figurer ATS för globalt API-scope</span><span class="sxs-lookup"><span data-stu-id="da728-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="da728-124">Exempel 5: Hämta alla prenumerationer för en produkt och en användare</span><span class="sxs-lookup"><span data-stu-id="da728-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="da728-125">Det här kommandot får alla prenumerationer som har kon figurer ATS för globalt API-scope</span><span class="sxs-lookup"><span data-stu-id="da728-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="da728-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da728-126">PARAMETERS</span></span>

### <span data-ttu-id="da728-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="da728-127">-Context</span></span>
<span data-ttu-id="da728-128">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="da728-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="da728-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da728-129">-DefaultProfile</span></span>
<span data-ttu-id="da728-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da728-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da728-131">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="da728-131">-ProductId</span></span>
<span data-ttu-id="da728-132">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="da728-132">Specifies a product identifier.</span></span>
<span data-ttu-id="da728-133">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="da728-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da728-134">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="da728-134">-Scope</span></span>
<span data-ttu-id="da728-135">Omfattnings identifierare.</span><span class="sxs-lookup"><span data-stu-id="da728-135">Scope identifier.</span></span> <span data-ttu-id="da728-136">Omfattningen av prenumerationen, vare sig det är API-omfattning/apis/{apiId} eller produkt omfattning/products/{productId} eller globalt API-scope/Apis eller globalt scope/.</span><span class="sxs-lookup"><span data-stu-id="da728-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da728-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da728-137">-SubscriptionId</span></span>
<span data-ttu-id="da728-138">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="da728-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="da728-139">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="da728-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da728-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="da728-140">-UserId</span></span>
<span data-ttu-id="da728-141">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="da728-141">Specifies a user identifier.</span></span>
<span data-ttu-id="da728-142">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="da728-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da728-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da728-143">CommonParameters</span></span>
<span data-ttu-id="da728-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da728-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da728-145">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da728-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da728-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da728-146">INPUTS</span></span>

### <span data-ttu-id="da728-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da728-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da728-148">System. String</span><span class="sxs-lookup"><span data-stu-id="da728-148">System.String</span></span>

## <span data-ttu-id="da728-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da728-149">OUTPUTS</span></span>

### <span data-ttu-id="da728-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="da728-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="da728-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da728-151">NOTES</span></span>

## <span data-ttu-id="da728-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da728-152">RELATED LINKS</span></span>

[<span data-ttu-id="da728-153">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="da728-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="da728-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="da728-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="da728-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="da728-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


