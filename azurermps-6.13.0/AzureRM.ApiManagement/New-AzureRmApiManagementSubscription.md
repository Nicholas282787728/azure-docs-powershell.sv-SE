---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573076"
---
# <span data-ttu-id="13dd9-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="13dd9-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="13dd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="13dd9-103">Skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="13dd9-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13dd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13dd9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13dd9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="13dd9-106">Cmdleten **New-AzureRmApiManagementSubscription** skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="13dd9-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="13dd9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="13dd9-108">Exempel 1: abonnera på en användare för en produkt</span><span class="sxs-lookup"><span data-stu-id="13dd9-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="13dd9-109">Det här kommandot prenumererar på en befintlig användare till en produkt.</span><span class="sxs-lookup"><span data-stu-id="13dd9-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="13dd9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13dd9-110">PARAMETERS</span></span>

### <span data-ttu-id="13dd9-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="13dd9-111">-Context</span></span>
<span data-ttu-id="13dd9-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="13dd9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="13dd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13dd9-113">-DefaultProfile</span></span>
<span data-ttu-id="13dd9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13dd9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13dd9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="13dd9-115">-Name</span></span>
<span data-ttu-id="13dd9-116">Anger prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="13dd9-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="13dd9-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="13dd9-117">-PrimaryKey</span></span>
<span data-ttu-id="13dd9-118">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="13dd9-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="13dd9-119">Om den här parametern inte anges genereras den automatiskt.</span><span class="sxs-lookup"><span data-stu-id="13dd9-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="13dd9-120">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="13dd9-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="13dd9-121">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="13dd9-121">-ProductId</span></span>
<span data-ttu-id="13dd9-122">Anger ID: t för den produkt som du ska abonnera på.</span><span class="sxs-lookup"><span data-stu-id="13dd9-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="13dd9-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="13dd9-123">-SecondaryKey</span></span>
<span data-ttu-id="13dd9-124">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="13dd9-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="13dd9-125">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="13dd9-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="13dd9-126">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="13dd9-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="13dd9-127">-State</span><span class="sxs-lookup"><span data-stu-id="13dd9-127">-State</span></span>
<span data-ttu-id="13dd9-128">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="13dd9-128">Specifies the subscription state.</span></span>
<span data-ttu-id="13dd9-129">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="13dd9-129">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13dd9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13dd9-130">-SubscriptionId</span></span>
<span data-ttu-id="13dd9-131">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="13dd9-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="13dd9-132">Den här parametern skapas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="13dd9-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="13dd9-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="13dd9-133">-UserId</span></span>
<span data-ttu-id="13dd9-134">Anger abonnent-ID.</span><span class="sxs-lookup"><span data-stu-id="13dd9-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="13dd9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13dd9-135">CommonParameters</span></span>
<span data-ttu-id="13dd9-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13dd9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13dd9-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13dd9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13dd9-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13dd9-138">INPUTS</span></span>

### <span data-ttu-id="13dd9-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="13dd9-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="13dd9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="13dd9-140">System.String</span></span>

### <span data-ttu-id="13dd9-141">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13dd9-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13dd9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13dd9-142">OUTPUTS</span></span>

### <span data-ttu-id="13dd9-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="13dd9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="13dd9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13dd9-144">NOTES</span></span>

## <span data-ttu-id="13dd9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13dd9-145">RELATED LINKS</span></span>

[<span data-ttu-id="13dd9-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="13dd9-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="13dd9-147">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="13dd9-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="13dd9-148">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="13dd9-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


