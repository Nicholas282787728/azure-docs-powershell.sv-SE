---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574064"
---
# <span data-ttu-id="09301-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09301-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="09301-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09301-102">SYNOPSIS</span></span>
<span data-ttu-id="09301-103">Anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="09301-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09301-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09301-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09301-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09301-105">DESCRIPTION</span></span>
<span data-ttu-id="09301-106">Cmdleten **set-AzureRmApiManagementSubscription** anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="09301-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="09301-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09301-107">EXAMPLES</span></span>

### <span data-ttu-id="09301-108">Exempel 1: Ange tillstånd och primär-och sekundär nycklar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="09301-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="09301-109">Det här kommandot anger de primära och sekundära nycklarna för ett abonnemang och aktiverar det.</span><span class="sxs-lookup"><span data-stu-id="09301-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="09301-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09301-110">PARAMETERS</span></span>

### <span data-ttu-id="09301-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="09301-111">-Context</span></span>
<span data-ttu-id="09301-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="09301-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="09301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09301-113">-DefaultProfile</span></span>
<span data-ttu-id="09301-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09301-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09301-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="09301-115">-ExpiresOn</span></span>
<span data-ttu-id="09301-116">Anger ett förfallo datum för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09301-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="09301-117">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="09301-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="09301-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="09301-118">-Name</span></span>
<span data-ttu-id="09301-119">Anger ett prenumerations namn.</span><span class="sxs-lookup"><span data-stu-id="09301-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="09301-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09301-120">-PassThru</span></span>
<span data-ttu-id="09301-121">passthru</span><span class="sxs-lookup"><span data-stu-id="09301-121">passthru</span></span>

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

### <span data-ttu-id="09301-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="09301-122">-PrimaryKey</span></span>
<span data-ttu-id="09301-123">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09301-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="09301-124">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="09301-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="09301-125">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="09301-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="09301-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="09301-126">-SecondaryKey</span></span>
<span data-ttu-id="09301-127">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="09301-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="09301-128">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="09301-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="09301-129">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="09301-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="09301-130">-State</span><span class="sxs-lookup"><span data-stu-id="09301-130">-State</span></span>
<span data-ttu-id="09301-131">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09301-131">Specifies the subscription state.</span></span>
<span data-ttu-id="09301-132">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="09301-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="09301-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="09301-133">-StateComment</span></span>
<span data-ttu-id="09301-134">Anger kommentaren till abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="09301-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="09301-135">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="09301-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="09301-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09301-136">-SubscriptionId</span></span>
<span data-ttu-id="09301-137">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="09301-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="09301-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09301-138">CommonParameters</span></span>
<span data-ttu-id="09301-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09301-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09301-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09301-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09301-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09301-141">INPUTS</span></span>

### <span data-ttu-id="09301-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09301-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09301-143">System. String</span><span class="sxs-lookup"><span data-stu-id="09301-143">System.String</span></span>

### <span data-ttu-id="09301-144">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, version = 6.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="09301-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="09301-145">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="09301-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="09301-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="09301-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="09301-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09301-147">OUTPUTS</span></span>

### <span data-ttu-id="09301-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09301-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="09301-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09301-149">NOTES</span></span>

## <span data-ttu-id="09301-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09301-150">RELATED LINKS</span></span>

[<span data-ttu-id="09301-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09301-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="09301-152">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09301-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="09301-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09301-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


