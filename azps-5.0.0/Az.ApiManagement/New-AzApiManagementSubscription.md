---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271104"
---
# <span data-ttu-id="b3a93-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a93-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="b3a93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3a93-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a93-103">Skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b3a93-103">Creates a subscription.</span></span>

## <span data-ttu-id="b3a93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3a93-104">SYNTAX</span></span>

### <span data-ttu-id="b3a93-105">OldSubscriptionModel (standard)</span><span class="sxs-lookup"><span data-stu-id="b3a93-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a93-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="b3a93-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a93-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3a93-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a93-108">Cmdleten **New-AzApiManagementSubscription** skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b3a93-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="b3a93-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3a93-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a93-110">Exempel 1: abonnera på en användare för en produkt</span><span class="sxs-lookup"><span data-stu-id="b3a93-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="b3a93-111">Det här kommandot prenumererar på en befintlig användare till en produkt.</span><span class="sxs-lookup"><span data-stu-id="b3a93-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="b3a93-112">Exempel 2: skapa ett abonnemang för alla API-omfattningar</span><span class="sxs-lookup"><span data-stu-id="b3a93-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="b3a93-113">Exempel 3: skapa ett abonnemang för produkt omfattningen</span><span class="sxs-lookup"><span data-stu-id="b3a93-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="b3a93-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3a93-114">PARAMETERS</span></span>

### <span data-ttu-id="b3a93-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="b3a93-115">-AllowTracing</span></span>
<span data-ttu-id="b3a93-116">Flagga som avgör om spårning kan aktive ras på prenumerations nivån.</span><span class="sxs-lookup"><span data-stu-id="b3a93-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="b3a93-117">Det här är valfri parameter och standard är $null.</span><span class="sxs-lookup"><span data-stu-id="b3a93-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="b3a93-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b3a93-118">-Context</span></span>
<span data-ttu-id="b3a93-119">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b3a93-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b3a93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a93-120">-DefaultProfile</span></span>
<span data-ttu-id="b3a93-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3a93-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3a93-122">-Name</span></span>
<span data-ttu-id="b3a93-123">Anger prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="b3a93-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="b3a93-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b3a93-124">-PrimaryKey</span></span>
<span data-ttu-id="b3a93-125">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3a93-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b3a93-126">Om den här parametern inte anges genereras den automatiskt.</span><span class="sxs-lookup"><span data-stu-id="b3a93-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="b3a93-127">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="b3a93-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b3a93-128">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="b3a93-128">-ProductId</span></span>
<span data-ttu-id="b3a93-129">Anger ID: t för den produkt som du ska abonnera på.</span><span class="sxs-lookup"><span data-stu-id="b3a93-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a93-130">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b3a93-130">-Scope</span></span>
<span data-ttu-id="b3a93-131">Omfattningen av prenumerationen, vare sig det är API-omfattning/apis/{apiId} eller produkt omfattning/products/{productId} eller globalt API-scope/Apis eller globalt scope/.</span><span class="sxs-lookup"><span data-stu-id="b3a93-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="b3a93-132">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b3a93-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a93-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b3a93-133">-SecondaryKey</span></span>
<span data-ttu-id="b3a93-134">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="b3a93-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b3a93-135">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="b3a93-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="b3a93-136">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="b3a93-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b3a93-137">-State</span><span class="sxs-lookup"><span data-stu-id="b3a93-137">-State</span></span>
<span data-ttu-id="b3a93-138">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3a93-138">Specifies the subscription state.</span></span>
<span data-ttu-id="b3a93-139">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="b3a93-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="b3a93-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3a93-140">-SubscriptionId</span></span>
<span data-ttu-id="b3a93-141">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="b3a93-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="b3a93-142">Den här parametern skapas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="b3a93-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="b3a93-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="b3a93-143">-UserId</span></span>
<span data-ttu-id="b3a93-144">Anger abonnent-ID.</span><span class="sxs-lookup"><span data-stu-id="b3a93-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a93-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a93-145">CommonParameters</span></span>
<span data-ttu-id="b3a93-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a93-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a93-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3a93-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a93-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3a93-148">INPUTS</span></span>

### <span data-ttu-id="b3a93-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3a93-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3a93-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a93-150">System.String</span></span>

### <span data-ttu-id="b3a93-151">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b3a93-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b3a93-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3a93-152">OUTPUTS</span></span>

### <span data-ttu-id="b3a93-153">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a93-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="b3a93-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3a93-154">NOTES</span></span>

## <span data-ttu-id="b3a93-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3a93-155">RELATED LINKS</span></span>

[<span data-ttu-id="b3a93-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a93-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="b3a93-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a93-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="b3a93-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b3a93-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)

