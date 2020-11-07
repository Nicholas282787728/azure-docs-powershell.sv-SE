---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754896"
---
# <span data-ttu-id="7a41c-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a41c-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7a41c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a41c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a41c-103">Anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="7a41c-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="7a41c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a41c-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a41c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a41c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a41c-106">Cmdleten **set-AzApiManagementSubscription** anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="7a41c-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="7a41c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a41c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a41c-108">Exempel 1: Ange tillstånd och primär-och sekundär nycklar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="7a41c-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="7a41c-109">Det här kommandot anger de primära och sekundära nycklarna för ett abonnemang och aktiverar det.</span><span class="sxs-lookup"><span data-stu-id="7a41c-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="7a41c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a41c-110">PARAMETERS</span></span>

### <span data-ttu-id="7a41c-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7a41c-111">-Context</span></span>
<span data-ttu-id="7a41c-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7a41c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7a41c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a41c-113">-DefaultProfile</span></span>
<span data-ttu-id="7a41c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a41c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a41c-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="7a41c-115">-ExpiresOn</span></span>
<span data-ttu-id="7a41c-116">Anger ett förfallo datum för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7a41c-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="7a41c-117">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="7a41c-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a41c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a41c-118">-Name</span></span>
<span data-ttu-id="7a41c-119">Anger ett prenumerations namn.</span><span class="sxs-lookup"><span data-stu-id="7a41c-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="7a41c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a41c-120">-PassThru</span></span>
<span data-ttu-id="7a41c-121">passthru</span><span class="sxs-lookup"><span data-stu-id="7a41c-121">passthru</span></span>

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

### <span data-ttu-id="7a41c-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7a41c-122">-PrimaryKey</span></span>
<span data-ttu-id="7a41c-123">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7a41c-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7a41c-124">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="7a41c-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7a41c-125">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="7a41c-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a41c-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7a41c-126">-SecondaryKey</span></span>
<span data-ttu-id="7a41c-127">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="7a41c-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7a41c-128">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="7a41c-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7a41c-129">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="7a41c-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a41c-130">-State</span><span class="sxs-lookup"><span data-stu-id="7a41c-130">-State</span></span>
<span data-ttu-id="7a41c-131">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7a41c-131">Specifies the subscription state.</span></span>
<span data-ttu-id="7a41c-132">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="7a41c-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a41c-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="7a41c-133">-StateComment</span></span>
<span data-ttu-id="7a41c-134">Anger kommentaren till abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7a41c-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="7a41c-135">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="7a41c-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a41c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a41c-136">-SubscriptionId</span></span>
<span data-ttu-id="7a41c-137">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="7a41c-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="7a41c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a41c-138">CommonParameters</span></span>
<span data-ttu-id="7a41c-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a41c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a41c-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a41c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a41c-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a41c-141">INPUTS</span></span>

### <span data-ttu-id="7a41c-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a41c-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a41c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a41c-143">System.String</span></span>

### <span data-ttu-id="7a41c-144">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7a41c-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7a41c-145">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a41c-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7a41c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a41c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a41c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a41c-147">OUTPUTS</span></span>

### <span data-ttu-id="7a41c-148">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a41c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7a41c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a41c-149">NOTES</span></span>

## <span data-ttu-id="7a41c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a41c-150">RELATED LINKS</span></span>

[<span data-ttu-id="7a41c-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a41c-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7a41c-152">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a41c-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="7a41c-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a41c-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


