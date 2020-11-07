---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917842"
---
# <span data-ttu-id="9c340-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c340-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="9c340-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c340-102">SYNOPSIS</span></span>
<span data-ttu-id="9c340-103">Skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9c340-103">Creates a subscription.</span></span>

## <span data-ttu-id="9c340-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c340-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c340-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c340-105">DESCRIPTION</span></span>
<span data-ttu-id="9c340-106">Cmdleten **New-AzApiManagementSubscription** skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9c340-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="9c340-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c340-107">EXAMPLES</span></span>

### <span data-ttu-id="9c340-108">Exempel 1: abonnera på en användare för en produkt</span><span class="sxs-lookup"><span data-stu-id="9c340-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="9c340-109">Det här kommandot prenumererar på en befintlig användare till en produkt.</span><span class="sxs-lookup"><span data-stu-id="9c340-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="9c340-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c340-110">PARAMETERS</span></span>

### <span data-ttu-id="9c340-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9c340-111">-Context</span></span>
<span data-ttu-id="9c340-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9c340-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9c340-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c340-113">-DefaultProfile</span></span>
<span data-ttu-id="9c340-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c340-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c340-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c340-115">-Name</span></span>
<span data-ttu-id="9c340-116">Anger prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="9c340-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="9c340-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9c340-117">-PrimaryKey</span></span>
<span data-ttu-id="9c340-118">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9c340-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="9c340-119">Om den här parametern inte anges genereras den automatiskt.</span><span class="sxs-lookup"><span data-stu-id="9c340-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="9c340-120">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9c340-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9c340-121">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="9c340-121">-ProductId</span></span>
<span data-ttu-id="9c340-122">Anger ID: t för den produkt som du ska abonnera på.</span><span class="sxs-lookup"><span data-stu-id="9c340-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="9c340-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9c340-123">-SecondaryKey</span></span>
<span data-ttu-id="9c340-124">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="9c340-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="9c340-125">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="9c340-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="9c340-126">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="9c340-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9c340-127">-State</span><span class="sxs-lookup"><span data-stu-id="9c340-127">-State</span></span>
<span data-ttu-id="9c340-128">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9c340-128">Specifies the subscription state.</span></span>
<span data-ttu-id="9c340-129">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="9c340-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="9c340-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c340-130">-SubscriptionId</span></span>
<span data-ttu-id="9c340-131">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="9c340-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="9c340-132">Den här parametern skapas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="9c340-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="9c340-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="9c340-133">-UserId</span></span>
<span data-ttu-id="9c340-134">Anger abonnent-ID.</span><span class="sxs-lookup"><span data-stu-id="9c340-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="9c340-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c340-135">CommonParameters</span></span>
<span data-ttu-id="9c340-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c340-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c340-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c340-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c340-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c340-138">INPUTS</span></span>

### <span data-ttu-id="9c340-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9c340-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9c340-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9c340-140">System.String</span></span>

### <span data-ttu-id="9c340-141">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c340-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c340-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c340-142">OUTPUTS</span></span>

### <span data-ttu-id="9c340-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c340-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="9c340-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c340-144">NOTES</span></span>

## <span data-ttu-id="9c340-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c340-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c340-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c340-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="9c340-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c340-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="9c340-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9c340-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


