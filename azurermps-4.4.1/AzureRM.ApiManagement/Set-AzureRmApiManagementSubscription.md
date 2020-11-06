---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574750"
---
# <span data-ttu-id="38f0d-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="38f0d-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="38f0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="38f0d-103">Anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="38f0d-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38f0d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38f0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="38f0d-106">Cmdleten **set-AzureRmApiManagementSubscription** anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="38f0d-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="38f0d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="38f0d-108">Exempel 1: Ange tillstånd och primär-och sekundär nycklar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="38f0d-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="38f0d-109">Det här kommandot anger de primära och sekundära nycklarna för ett abonnemang och aktiverar det.</span><span class="sxs-lookup"><span data-stu-id="38f0d-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="38f0d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38f0d-110">PARAMETERS</span></span>

### <span data-ttu-id="38f0d-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="38f0d-111">-Context</span></span>
<span data-ttu-id="38f0d-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="38f0d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="38f0d-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="38f0d-113">-ExpiresOn</span></span>
<span data-ttu-id="38f0d-114">Anger ett förfallo datum för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="38f0d-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="38f0d-115">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="38f0d-115">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f0d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="38f0d-116">-Name</span></span>
<span data-ttu-id="38f0d-117">Anger ett prenumerations namn.</span><span class="sxs-lookup"><span data-stu-id="38f0d-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="38f0d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38f0d-118">-PassThru</span></span>
<span data-ttu-id="38f0d-119">passthru</span><span class="sxs-lookup"><span data-stu-id="38f0d-119">passthru</span></span>

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

### <span data-ttu-id="38f0d-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="38f0d-120">-PrimaryKey</span></span>
<span data-ttu-id="38f0d-121">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="38f0d-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="38f0d-122">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="38f0d-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="38f0d-123">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="38f0d-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="38f0d-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="38f0d-124">-SecondaryKey</span></span>
<span data-ttu-id="38f0d-125">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="38f0d-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="38f0d-126">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="38f0d-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="38f0d-127">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="38f0d-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="38f0d-128">-State</span><span class="sxs-lookup"><span data-stu-id="38f0d-128">-State</span></span>
<span data-ttu-id="38f0d-129">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="38f0d-129">Specifies the subscription state.</span></span>
<span data-ttu-id="38f0d-130">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="38f0d-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="38f0d-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="38f0d-131">-StateComment</span></span>
<span data-ttu-id="38f0d-132">Anger kommentaren till abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="38f0d-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="38f0d-133">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="38f0d-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="38f0d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38f0d-134">-SubscriptionId</span></span>
<span data-ttu-id="38f0d-135">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="38f0d-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="38f0d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f0d-136">-DefaultProfile</span></span>
<span data-ttu-id="38f0d-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38f0d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f0d-138">CommonParameters</span></span>
<span data-ttu-id="38f0d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f0d-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f0d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f0d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38f0d-141">INPUTS</span></span>

## <span data-ttu-id="38f0d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38f0d-142">OUTPUTS</span></span>

### <span data-ttu-id="38f0d-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="38f0d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="38f0d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38f0d-144">NOTES</span></span>

## <span data-ttu-id="38f0d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38f0d-145">RELATED LINKS</span></span>

[<span data-ttu-id="38f0d-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="38f0d-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="38f0d-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="38f0d-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="38f0d-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="38f0d-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


