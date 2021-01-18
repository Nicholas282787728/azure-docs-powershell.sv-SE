---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525076"
---
# <span data-ttu-id="27c4c-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27c4c-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="27c4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="27c4c-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="27c4c-103">Gets subscriptions.</span></span>

## <span data-ttu-id="27c4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27c4c-104">SYNTAX</span></span>

### <span data-ttu-id="27c4c-105">GetAllSubscriptions (standard)</span><span class="sxs-lookup"><span data-stu-id="27c4c-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27c4c-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27c4c-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="27c4c-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="27c4c-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="27c4c-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="27c4c-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c4c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27c4c-111">DESCRIPTION</span></span>
<span data-ttu-id="27c4c-112">Cmdleten **Get-AzApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="27c4c-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="27c4c-113">Nycklarna tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="27c4c-113">Keys will not be included into result details.</span></span> <span data-ttu-id="27c4c-114">Använd **Get-AzApiManagementSubscriptionKey** för att få nycklar.</span><span class="sxs-lookup"><span data-stu-id="27c4c-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="27c4c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27c4c-115">EXAMPLES</span></span>

### <span data-ttu-id="27c4c-116">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="27c4c-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="27c4c-117">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="27c4c-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="27c4c-118">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="27c4c-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="27c4c-119">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="27c4c-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="27c4c-120">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="27c4c-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="27c4c-121">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="27c4c-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="27c4c-122">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="27c4c-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="27c4c-123">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="27c4c-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="27c4c-124">Exempel 5: Hämta alla abonnemang för ett scope</span><span class="sxs-lookup"><span data-stu-id="27c4c-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="27c4c-125">Det här kommandot får alla prenumerationer som har kon figurer ATS för globalt API-scope</span><span class="sxs-lookup"><span data-stu-id="27c4c-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="27c4c-126">Exempel 6: Hämta alla abonnemang för en produkt och en användare</span><span class="sxs-lookup"><span data-stu-id="27c4c-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="27c4c-127">Det här kommandot får alla prenumerationer som har kon figurer ATS för globalt API-scope</span><span class="sxs-lookup"><span data-stu-id="27c4c-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="27c4c-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27c4c-128">PARAMETERS</span></span>

### <span data-ttu-id="27c4c-129">-Kontext</span><span class="sxs-lookup"><span data-stu-id="27c4c-129">-Context</span></span>
<span data-ttu-id="27c4c-130">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="27c4c-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="27c4c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c4c-131">-DefaultProfile</span></span>
<span data-ttu-id="27c4c-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27c4c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27c4c-133">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="27c4c-133">-ProductId</span></span>
<span data-ttu-id="27c4c-134">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="27c4c-134">Specifies a product identifier.</span></span>
<span data-ttu-id="27c4c-135">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="27c4c-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="27c4c-136">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="27c4c-136">-Scope</span></span>
<span data-ttu-id="27c4c-137">Omfattnings identifierare.</span><span class="sxs-lookup"><span data-stu-id="27c4c-137">Scope identifier.</span></span> <span data-ttu-id="27c4c-138">Omfattningen av prenumerationen, vare sig det är API-omfattning/apis/{apiId} eller produkt omfattning/products/{productId} eller globalt API-scope/Apis eller globalt scope/.</span><span class="sxs-lookup"><span data-stu-id="27c4c-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="27c4c-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27c4c-139">-SubscriptionId</span></span>
<span data-ttu-id="27c4c-140">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="27c4c-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="27c4c-141">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="27c4c-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="27c4c-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="27c4c-142">-UserId</span></span>
<span data-ttu-id="27c4c-143">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="27c4c-143">Specifies a user identifier.</span></span>
<span data-ttu-id="27c4c-144">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="27c4c-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="27c4c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c4c-145">CommonParameters</span></span>
<span data-ttu-id="27c4c-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c4c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c4c-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27c4c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c4c-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27c4c-148">INPUTS</span></span>

### <span data-ttu-id="27c4c-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="27c4c-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27c4c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="27c4c-150">System.String</span></span>

## <span data-ttu-id="27c4c-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27c4c-151">OUTPUTS</span></span>

### <span data-ttu-id="27c4c-152">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27c4c-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="27c4c-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27c4c-153">NOTES</span></span>

## <span data-ttu-id="27c4c-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27c4c-154">RELATED LINKS</span></span>

[<span data-ttu-id="27c4c-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27c4c-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="27c4c-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27c4c-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="27c4c-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="27c4c-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


