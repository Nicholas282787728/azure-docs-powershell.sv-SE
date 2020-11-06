---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583904"
---
# <span data-ttu-id="f7796-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f7796-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="f7796-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7796-102">SYNOPSIS</span></span>
<span data-ttu-id="f7796-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f7796-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7796-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7796-104">SYNTAX</span></span>

### <span data-ttu-id="f7796-105">Hämta alla prenumerationer (standard)</span><span class="sxs-lookup"><span data-stu-id="f7796-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7796-106">Få med subsctiption-ID</span><span class="sxs-lookup"><span data-stu-id="f7796-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7796-107">Få med användar-ID</span><span class="sxs-lookup"><span data-stu-id="f7796-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7796-108">Få utifrån produkt-ID</span><span class="sxs-lookup"><span data-stu-id="f7796-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7796-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7796-109">DESCRIPTION</span></span>
<span data-ttu-id="f7796-110">Cmdleten **Get-AzureRmApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="f7796-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="f7796-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7796-111">EXAMPLES</span></span>

### <span data-ttu-id="f7796-112">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="f7796-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="f7796-113">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="f7796-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="f7796-114">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="f7796-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="f7796-115">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="f7796-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="f7796-116">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="f7796-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="f7796-117">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f7796-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="f7796-118">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="f7796-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="f7796-119">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="f7796-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="f7796-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7796-120">PARAMETERS</span></span>

### <span data-ttu-id="f7796-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f7796-121">-Context</span></span>
<span data-ttu-id="f7796-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f7796-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f7796-123">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="f7796-123">-ProductId</span></span>
<span data-ttu-id="f7796-124">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="f7796-124">Specifies a product identifier.</span></span>
<span data-ttu-id="f7796-125">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="f7796-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7796-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7796-126">-SubscriptionId</span></span>
<span data-ttu-id="f7796-127">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="f7796-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="f7796-128">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="f7796-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7796-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="f7796-129">-UserId</span></span>
<span data-ttu-id="f7796-130">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="f7796-130">Specifies a user identifier.</span></span>
<span data-ttu-id="f7796-131">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="f7796-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7796-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7796-132">-DefaultProfile</span></span>
<span data-ttu-id="f7796-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7796-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7796-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7796-134">CommonParameters</span></span>
<span data-ttu-id="f7796-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7796-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7796-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7796-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7796-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7796-137">INPUTS</span></span>

## <span data-ttu-id="f7796-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7796-138">OUTPUTS</span></span>

### <span data-ttu-id="f7796-139">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="f7796-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="f7796-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7796-140">NOTES</span></span>

## <span data-ttu-id="f7796-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7796-141">RELATED LINKS</span></span>

[<span data-ttu-id="f7796-142">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f7796-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="f7796-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f7796-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="f7796-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f7796-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


