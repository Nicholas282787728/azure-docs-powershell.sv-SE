---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577281"
---
# <span data-ttu-id="ade1e-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ade1e-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="ade1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ade1e-102">SYNOPSIS</span></span>
<span data-ttu-id="ade1e-103">Skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ade1e-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ade1e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ade1e-105">DESCRIPTION</span></span>
<span data-ttu-id="ade1e-106">Cmdleten **New-AzureRmApiManagementSubscription** skapar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ade1e-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="ade1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ade1e-107">EXAMPLES</span></span>

### <span data-ttu-id="ade1e-108">Exempel 1: abonnera på en användare för en produkt</span><span class="sxs-lookup"><span data-stu-id="ade1e-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="ade1e-109">Det här kommandot prenumererar på en befintlig användare till en produkt.</span><span class="sxs-lookup"><span data-stu-id="ade1e-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="ade1e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ade1e-110">PARAMETERS</span></span>

### <span data-ttu-id="ade1e-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ade1e-111">-Context</span></span>
<span data-ttu-id="ade1e-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ade1e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ade1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade1e-113">-DefaultProfile</span></span>
<span data-ttu-id="ade1e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ade1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ade1e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ade1e-115">-Name</span></span>
<span data-ttu-id="ade1e-116">Anger prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="ade1e-116">Specifies the subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ade1e-117">-PrimaryKey</span></span>
<span data-ttu-id="ade1e-118">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ade1e-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ade1e-119">Om den här parametern inte anges genereras den automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ade1e-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="ade1e-120">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="ade1e-120">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-121">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="ade1e-121">-ProductId</span></span>
<span data-ttu-id="ade1e-122">Anger ID: t för den produkt som du ska abonnera på.</span><span class="sxs-lookup"><span data-stu-id="ade1e-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ade1e-123">-SecondaryKey</span></span>
<span data-ttu-id="ade1e-124">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="ade1e-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ade1e-125">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="ade1e-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="ade1e-126">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="ade1e-126">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-127">-State</span><span class="sxs-lookup"><span data-stu-id="ade1e-127">-State</span></span>
<span data-ttu-id="ade1e-128">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ade1e-128">Specifies the subscription state.</span></span>
<span data-ttu-id="ade1e-129">Standardvärdet är $Null.</span><span class="sxs-lookup"><span data-stu-id="ade1e-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ade1e-130">-SubscriptionId</span></span>
<span data-ttu-id="ade1e-131">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="ade1e-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="ade1e-132">Den här parametern skapas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="ade1e-132">This parameter is generated if not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="ade1e-133">-UserId</span></span>
<span data-ttu-id="ade1e-134">Anger abonnent-ID.</span><span class="sxs-lookup"><span data-stu-id="ade1e-134">Specifies the subscriber ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade1e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade1e-135">CommonParameters</span></span>
<span data-ttu-id="ade1e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade1e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade1e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade1e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade1e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ade1e-138">INPUTS</span></span>

### <span data-ttu-id="ade1e-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="ade1e-139">None</span></span>
<span data-ttu-id="ade1e-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ade1e-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ade1e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ade1e-141">OUTPUTS</span></span>

### <span data-ttu-id="ade1e-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ade1e-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ade1e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ade1e-143">NOTES</span></span>

## <span data-ttu-id="ade1e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ade1e-144">RELATED LINKS</span></span>

[<span data-ttu-id="ade1e-145">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ade1e-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ade1e-146">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ade1e-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ade1e-147">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ade1e-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


