---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089717"
---
# <span data-ttu-id="6808b-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="6808b-101">Set-AzContext</span></span>

## <span data-ttu-id="6808b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6808b-102">SYNOPSIS</span></span>
<span data-ttu-id="6808b-103">Anger klient organisation, prenumeration och miljö för cmdlets som ska användas i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="6808b-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="6808b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6808b-104">SYNTAX</span></span>

### <span data-ttu-id="6808b-105">Kontext (standard)</span><span class="sxs-lookup"><span data-stu-id="6808b-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6808b-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="6808b-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6808b-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="6808b-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6808b-108">Prenumerationsvy</span><span class="sxs-lookup"><span data-stu-id="6808b-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6808b-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="6808b-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6808b-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6808b-110">DESCRIPTION</span></span>
<span data-ttu-id="6808b-111">Med Set-AzContext cmdlet anges autentiseringsinformation för de cmdlets som du kör i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="6808b-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="6808b-112">Kontexten inkluderar klient organisation, prenumeration och miljö information.</span><span class="sxs-lookup"><span data-stu-id="6808b-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="6808b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6808b-113">EXAMPLES</span></span>

### <span data-ttu-id="6808b-114">Exempel 1: Ange prenumerationens kontext</span><span class="sxs-lookup"><span data-stu-id="6808b-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="6808b-115">Det här kommandot anger sammanhanget för att använda den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6808b-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="6808b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6808b-116">PARAMETERS</span></span>

### <span data-ttu-id="6808b-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6808b-117">-Context</span></span>
<span data-ttu-id="6808b-118">Anger sammanhanget för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="6808b-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6808b-119">-DefaultProfile</span></span>
<span data-ttu-id="6808b-120">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6808b-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6808b-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="6808b-121">-ExtendedProperty</span></span>
<span data-ttu-id="6808b-122">Ytterligare kontext egenskaper</span><span class="sxs-lookup"><span data-stu-id="6808b-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6808b-123">-Force</span></span>
<span data-ttu-id="6808b-124">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="6808b-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6808b-125">-Name</span></span>
<span data-ttu-id="6808b-126">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="6808b-126">Name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-127">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6808b-127">-Scope</span></span>
<span data-ttu-id="6808b-128">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="6808b-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-129">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="6808b-129">-Subscription</span></span>
<span data-ttu-id="6808b-130">Namn eller ID för den prenumeration som kontexten ska vara inställd på.</span><span class="sxs-lookup"><span data-stu-id="6808b-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="6808b-131">Den här parametern har alias till-SubscriptionName och-SubscriptionId, så för tydlighetens skull kan något av följande användas i stället för-Subscription när namn respektive ID anges.</span><span class="sxs-lookup"><span data-stu-id="6808b-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="6808b-132">-SubscriptionObject</span></span>
<span data-ttu-id="6808b-133">Ett prenumerations objekt</span><span class="sxs-lookup"><span data-stu-id="6808b-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-134">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="6808b-134">-Tenant</span></span>
<span data-ttu-id="6808b-135">Klient organisationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="6808b-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="6808b-136">-TenantObject</span></span>
<span data-ttu-id="6808b-137">Ett klient organisations objekt</span><span class="sxs-lookup"><span data-stu-id="6808b-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6808b-138">-Confirm</span></span>
<span data-ttu-id="6808b-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6808b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6808b-140">-WhatIf</span></span>
<span data-ttu-id="6808b-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6808b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6808b-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6808b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6808b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6808b-143">CommonParameters</span></span>
<span data-ttu-id="6808b-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6808b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6808b-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6808b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6808b-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6808b-146">INPUTS</span></span>

### <span data-ttu-id="6808b-147">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6808b-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="6808b-148">Microsoft. Azure. commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="6808b-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="6808b-149">Microsoft. Azure. commands. Profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6808b-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="6808b-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6808b-150">OUTPUTS</span></span>

### <span data-ttu-id="6808b-151">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6808b-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6808b-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6808b-152">NOTES</span></span>

## <span data-ttu-id="6808b-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6808b-153">RELATED LINKS</span></span>

[<span data-ttu-id="6808b-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="6808b-154">Get-AzContext</span></span>](./Get-AzContext.md)
