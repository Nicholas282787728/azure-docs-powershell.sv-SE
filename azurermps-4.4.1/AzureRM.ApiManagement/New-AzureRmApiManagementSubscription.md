---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583879"
---
# <span data-ttu-id="d255b-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d255b-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d255b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d255b-102">SYNOPSIS</span></span>
<span data-ttu-id="d255b-103">Skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d255b-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d255b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d255b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d255b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d255b-105">DESCRIPTION</span></span>
<span data-ttu-id="d255b-106">Cmdleten **New-AzureRmApiManagementSubscription** skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d255b-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="d255b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d255b-107">EXAMPLES</span></span>

### <span data-ttu-id="d255b-108">Exempel 1: abonnera på en användare för en produkt</span><span class="sxs-lookup"><span data-stu-id="d255b-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="d255b-109">Det här kommandot prenumererar på en befintlig användare till en produkt.</span><span class="sxs-lookup"><span data-stu-id="d255b-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="d255b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d255b-110">PARAMETERS</span></span>

### <span data-ttu-id="d255b-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d255b-111">-Context</span></span>
<span data-ttu-id="d255b-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d255b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d255b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d255b-113">-Name</span></span>
<span data-ttu-id="d255b-114">Anger prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="d255b-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="d255b-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d255b-115">-PrimaryKey</span></span>
<span data-ttu-id="d255b-116">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d255b-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="d255b-117">Om den här parametern inte anges genereras den automatiskt.</span><span class="sxs-lookup"><span data-stu-id="d255b-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="d255b-118">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d255b-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d255b-119">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="d255b-119">-ProductId</span></span>
<span data-ttu-id="d255b-120">Anger ID: t för den produkt som du ska abonnera på.</span><span class="sxs-lookup"><span data-stu-id="d255b-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="d255b-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d255b-121">-SecondaryKey</span></span>
<span data-ttu-id="d255b-122">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="d255b-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="d255b-123">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="d255b-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="d255b-124">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="d255b-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d255b-125">-State</span><span class="sxs-lookup"><span data-stu-id="d255b-125">-State</span></span>
<span data-ttu-id="d255b-126">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d255b-126">Specifies the subscription state.</span></span>
<span data-ttu-id="d255b-127">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="d255b-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="d255b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d255b-128">-SubscriptionId</span></span>
<span data-ttu-id="d255b-129">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="d255b-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="d255b-130">Den här parametern skapas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="d255b-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="d255b-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="d255b-131">-UserId</span></span>
<span data-ttu-id="d255b-132">Anger abonnent-ID.</span><span class="sxs-lookup"><span data-stu-id="d255b-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="d255b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d255b-133">-DefaultProfile</span></span>
<span data-ttu-id="d255b-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d255b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d255b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d255b-135">CommonParameters</span></span>
<span data-ttu-id="d255b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d255b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d255b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d255b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d255b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d255b-138">INPUTS</span></span>

## <span data-ttu-id="d255b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d255b-139">OUTPUTS</span></span>

### <span data-ttu-id="d255b-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d255b-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="d255b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d255b-141">NOTES</span></span>

## <span data-ttu-id="d255b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d255b-142">RELATED LINKS</span></span>

[<span data-ttu-id="d255b-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d255b-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d255b-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d255b-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d255b-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d255b-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


