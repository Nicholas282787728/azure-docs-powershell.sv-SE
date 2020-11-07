---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743393"
---
# <span data-ttu-id="49840-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="49840-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="49840-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49840-102">SYNOPSIS</span></span>
<span data-ttu-id="49840-103">Hämtar abonnemang.</span><span class="sxs-lookup"><span data-stu-id="49840-103">Gets subscriptions.</span></span>

## <span data-ttu-id="49840-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49840-104">SYNTAX</span></span>

### <span data-ttu-id="49840-105">GetAllSubscriptions (standard)</span><span class="sxs-lookup"><span data-stu-id="49840-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49840-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49840-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49840-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="49840-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49840-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="49840-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49840-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49840-109">DESCRIPTION</span></span>
<span data-ttu-id="49840-110">Cmdleten **Get-AzApiManagementSubscription** hämtar en angiven prenumeration, eller alla prenumerationer, om inget abonnemang har angetts.</span><span class="sxs-lookup"><span data-stu-id="49840-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="49840-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49840-111">EXAMPLES</span></span>

### <span data-ttu-id="49840-112">Exempel 1: Hämta alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="49840-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="49840-113">Det här kommandot får alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="49840-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="49840-114">Exempel 2: skaffa ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="49840-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="49840-115">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="49840-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="49840-116">Exempel 3: Hämta alla abonnemang för en användare</span><span class="sxs-lookup"><span data-stu-id="49840-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="49840-117">Det här kommandot får en användares abonnemang.</span><span class="sxs-lookup"><span data-stu-id="49840-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="49840-118">Exempel 4: Hämta alla abonnemang för en produkt</span><span class="sxs-lookup"><span data-stu-id="49840-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="49840-119">Det här kommandot får alla abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="49840-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="49840-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49840-120">PARAMETERS</span></span>

### <span data-ttu-id="49840-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="49840-121">-Context</span></span>
<span data-ttu-id="49840-122">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="49840-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="49840-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49840-123">-DefaultProfile</span></span>
<span data-ttu-id="49840-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49840-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49840-125">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="49840-125">-ProductId</span></span>
<span data-ttu-id="49840-126">Anger ett produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="49840-126">Specifies a product identifier.</span></span>
<span data-ttu-id="49840-127">Om det här alternativet anges hittar denna cmdlet alla abonnemang efter produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="49840-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="49840-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49840-128">-SubscriptionId</span></span>
<span data-ttu-id="49840-129">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="49840-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="49840-130">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="49840-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="49840-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="49840-131">-UserId</span></span>
<span data-ttu-id="49840-132">Anger ett användar-ID.</span><span class="sxs-lookup"><span data-stu-id="49840-132">Specifies a user identifier.</span></span>
<span data-ttu-id="49840-133">Om det här alternativet anges hittar denna cmdlet alla prenumerationer som ingår i användar-ID: n.</span><span class="sxs-lookup"><span data-stu-id="49840-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="49840-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49840-134">CommonParameters</span></span>
<span data-ttu-id="49840-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49840-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49840-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49840-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49840-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49840-137">INPUTS</span></span>

### <span data-ttu-id="49840-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49840-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49840-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49840-139">System.String</span></span>

## <span data-ttu-id="49840-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49840-140">OUTPUTS</span></span>

### <span data-ttu-id="49840-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="49840-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="49840-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49840-142">NOTES</span></span>

## <span data-ttu-id="49840-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49840-143">RELATED LINKS</span></span>

[<span data-ttu-id="49840-144">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="49840-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="49840-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="49840-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="49840-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="49840-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


