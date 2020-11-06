---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573584"
---
# <span data-ttu-id="941ca-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="941ca-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="941ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="941ca-102">SYNOPSIS</span></span>
<span data-ttu-id="941ca-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="941ca-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="941ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="941ca-104">SYNTAX</span></span>

### <span data-ttu-id="941ca-105">GetAllSubscriptions (standard)</span><span class="sxs-lookup"><span data-stu-id="941ca-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941ca-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="941ca-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941ca-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="941ca-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941ca-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="941ca-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="941ca-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="941ca-109">DESCRIPTION</span></span>
<span data-ttu-id="941ca-110">Cmdleten **Get-AzureRmApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="941ca-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="941ca-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="941ca-111">EXAMPLES</span></span>

### <span data-ttu-id="941ca-112">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="941ca-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="941ca-113">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="941ca-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="941ca-114">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="941ca-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="941ca-115">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="941ca-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="941ca-116">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="941ca-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="941ca-117">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="941ca-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="941ca-118">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="941ca-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="941ca-119">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="941ca-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="941ca-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="941ca-120">PARAMETERS</span></span>

### <span data-ttu-id="941ca-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="941ca-121">-Context</span></span>
<span data-ttu-id="941ca-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="941ca-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="941ca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941ca-123">-DefaultProfile</span></span>
<span data-ttu-id="941ca-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="941ca-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="941ca-125">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="941ca-125">-ProductId</span></span>
<span data-ttu-id="941ca-126">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="941ca-126">Specifies a product identifier.</span></span>
<span data-ttu-id="941ca-127">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="941ca-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="941ca-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="941ca-128">-SubscriptionId</span></span>
<span data-ttu-id="941ca-129">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="941ca-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="941ca-130">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="941ca-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="941ca-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="941ca-131">-UserId</span></span>
<span data-ttu-id="941ca-132">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="941ca-132">Specifies a user identifier.</span></span>
<span data-ttu-id="941ca-133">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="941ca-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="941ca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941ca-134">CommonParameters</span></span>
<span data-ttu-id="941ca-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941ca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941ca-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="941ca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941ca-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="941ca-137">INPUTS</span></span>

### <span data-ttu-id="941ca-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="941ca-138">None</span></span>
<span data-ttu-id="941ca-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="941ca-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="941ca-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="941ca-140">OUTPUTS</span></span>

### <span data-ttu-id="941ca-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="941ca-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="941ca-142">Information om prenumerationen i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="941ca-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="941ca-143">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="941ca-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="941ca-144">Listan med prenumerationer i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="941ca-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="941ca-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="941ca-145">NOTES</span></span>

## <span data-ttu-id="941ca-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="941ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="941ca-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="941ca-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="941ca-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="941ca-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="941ca-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="941ca-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


