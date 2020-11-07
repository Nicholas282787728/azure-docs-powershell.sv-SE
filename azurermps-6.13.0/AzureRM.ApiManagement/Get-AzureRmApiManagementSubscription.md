---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 8695d8866b83ed6cd7b29a3d94546da1114d3eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581836"
---
# <span data-ttu-id="59b02-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59b02-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="59b02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59b02-102">SYNOPSIS</span></span>
<span data-ttu-id="59b02-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="59b02-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59b02-104">SYNTAX</span></span>

### <span data-ttu-id="59b02-105">GetAllSubscriptions (standard)</span><span class="sxs-lookup"><span data-stu-id="59b02-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b02-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59b02-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b02-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="59b02-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b02-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="59b02-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b02-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59b02-109">DESCRIPTION</span></span>
<span data-ttu-id="59b02-110">Cmdleten **Get-AzureRmApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="59b02-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="59b02-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59b02-111">EXAMPLES</span></span>

### <span data-ttu-id="59b02-112">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="59b02-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="59b02-113">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="59b02-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="59b02-114">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="59b02-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="59b02-115">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="59b02-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="59b02-116">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="59b02-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="59b02-117">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="59b02-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="59b02-118">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="59b02-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="59b02-119">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="59b02-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="59b02-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59b02-120">PARAMETERS</span></span>

### <span data-ttu-id="59b02-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="59b02-121">-Context</span></span>
<span data-ttu-id="59b02-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="59b02-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59b02-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b02-123">-DefaultProfile</span></span>
<span data-ttu-id="59b02-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59b02-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b02-125">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="59b02-125">-ProductId</span></span>
<span data-ttu-id="59b02-126">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="59b02-126">Specifies a product identifier.</span></span>
<span data-ttu-id="59b02-127">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="59b02-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="59b02-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59b02-128">-SubscriptionId</span></span>
<span data-ttu-id="59b02-129">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="59b02-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="59b02-130">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="59b02-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="59b02-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="59b02-131">-UserId</span></span>
<span data-ttu-id="59b02-132">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="59b02-132">Specifies a user identifier.</span></span>
<span data-ttu-id="59b02-133">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="59b02-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="59b02-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b02-134">CommonParameters</span></span>
<span data-ttu-id="59b02-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b02-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b02-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b02-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b02-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59b02-137">INPUTS</span></span>

### <span data-ttu-id="59b02-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59b02-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59b02-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59b02-139">System.String</span></span>

## <span data-ttu-id="59b02-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59b02-140">OUTPUTS</span></span>

### <span data-ttu-id="59b02-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59b02-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="59b02-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59b02-142">NOTES</span></span>

## <span data-ttu-id="59b02-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59b02-143">RELATED LINKS</span></span>

[<span data-ttu-id="59b02-144">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59b02-144">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="59b02-145">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59b02-145">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="59b02-146">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59b02-146">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)

