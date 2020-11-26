---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272951"
---
# <span data-ttu-id="2a8bd-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a8bd-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="2a8bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8bd-103">Anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="2a8bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a8bd-104">SYNTAX</span></span>

### <span data-ttu-id="2a8bd-105">ByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="2a8bd-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a8bd-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="2a8bd-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a8bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a8bd-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8bd-108">Cmdleten **set-AzApiManagementSubscription** anger befintliga abonnemangs uppgifter.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="2a8bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a8bd-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8bd-110">Exempel 1: Ange tillstånd och primär-och sekundär nycklar för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="2a8bd-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="2a8bd-111">Det här kommandot anger de primära och sekundära nycklarna för ett abonnemang och aktiverar det.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="2a8bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a8bd-112">PARAMETERS</span></span>

### <span data-ttu-id="2a8bd-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2a8bd-113">-Context</span></span>
<span data-ttu-id="2a8bd-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8bd-115">-DefaultProfile</span></span>
<span data-ttu-id="2a8bd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a8bd-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="2a8bd-117">-ExpiresOn</span></span>
<span data-ttu-id="2a8bd-118">Anger ett förfallo datum för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="2a8bd-119">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2a8bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a8bd-120">-InputObject</span></span>
<span data-ttu-id="2a8bd-121">Instans av PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="2a8bd-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8bd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a8bd-123">-Name</span></span>
<span data-ttu-id="2a8bd-124">Anger ett prenumerations namn.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="2a8bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a8bd-125">-PassThru</span></span>
<span data-ttu-id="2a8bd-126">passthru</span><span class="sxs-lookup"><span data-stu-id="2a8bd-126">passthru</span></span>

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

### <span data-ttu-id="2a8bd-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2a8bd-127">-PrimaryKey</span></span>
<span data-ttu-id="2a8bd-128">Anger primär Key för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="2a8bd-129">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="2a8bd-130">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2a8bd-131">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="2a8bd-131">-Scope</span></span>
<span data-ttu-id="2a8bd-132">Omfattningen av prenumerationen, vare sig det är API-omfattning/apis/{apiId} eller produkt omfattning/products/{productId} eller globalt API-scope/Apis eller globalt scope/.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="2a8bd-133">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-133">This parameter is required.</span></span>

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

### <span data-ttu-id="2a8bd-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="2a8bd-134">-SecondaryKey</span></span>
<span data-ttu-id="2a8bd-135">Anger den sekundära abonnemangs tangenten.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="2a8bd-136">Den här parametern genereras automatiskt om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="2a8bd-137">Parametern måste vara 1 till 300 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2a8bd-138">-State</span><span class="sxs-lookup"><span data-stu-id="2a8bd-138">-State</span></span>
<span data-ttu-id="2a8bd-139">Anger abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-139">Specifies the subscription state.</span></span>
<span data-ttu-id="2a8bd-140">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2a8bd-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="2a8bd-141">-StateComment</span></span>
<span data-ttu-id="2a8bd-142">Anger kommentaren till abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="2a8bd-143">Standardvärdet för den här parametern är $Null.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2a8bd-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a8bd-144">-SubscriptionId</span></span>
<span data-ttu-id="2a8bd-145">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8bd-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="2a8bd-146">-UserId</span></span>
<span data-ttu-id="2a8bd-147">Ägaren till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-147">The owner of the subscription.</span></span> <span data-ttu-id="2a8bd-148">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="2a8bd-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a8bd-149">-Confirm</span></span>
<span data-ttu-id="2a8bd-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8bd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a8bd-151">-WhatIf</span></span>
<span data-ttu-id="2a8bd-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a8bd-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8bd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8bd-154">CommonParameters</span></span>
<span data-ttu-id="2a8bd-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8bd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8bd-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a8bd-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8bd-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a8bd-157">INPUTS</span></span>

### <span data-ttu-id="2a8bd-158">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a8bd-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a8bd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2a8bd-159">System.String</span></span>

### <span data-ttu-id="2a8bd-160">System. Nullable ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdletar. ApiManagement. ServiceManagement, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2a8bd-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2a8bd-161">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a8bd-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2a8bd-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a8bd-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a8bd-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a8bd-163">OUTPUTS</span></span>

### <span data-ttu-id="2a8bd-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a8bd-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="2a8bd-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a8bd-165">NOTES</span></span>

## <span data-ttu-id="2a8bd-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a8bd-166">RELATED LINKS</span></span>

[<span data-ttu-id="2a8bd-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a8bd-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="2a8bd-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a8bd-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="2a8bd-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a8bd-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

