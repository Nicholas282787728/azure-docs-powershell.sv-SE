---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756573"
---
# <span data-ttu-id="c97dc-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c97dc-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="c97dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c97dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c97dc-103">Anger klient organisation, prenumeration och miljö för cmdlets som ska användas i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="c97dc-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c97dc-104">SYNTAX</span></span>

### <span data-ttu-id="c97dc-105">Kontext (standard)</span><span class="sxs-lookup"><span data-stu-id="c97dc-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c97dc-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="c97dc-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c97dc-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c97dc-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c97dc-108">Prenumerationsvy</span><span class="sxs-lookup"><span data-stu-id="c97dc-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c97dc-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="c97dc-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c97dc-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c97dc-110">DESCRIPTION</span></span>
<span data-ttu-id="c97dc-111">Med Set-AzureRmContext cmdlet anges autentiseringsinformation för de cmdlets som du kör i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="c97dc-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="c97dc-112">Kontexten inkluderar klient organisation, prenumeration och miljö information.</span><span class="sxs-lookup"><span data-stu-id="c97dc-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="c97dc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c97dc-113">EXAMPLES</span></span>

### <span data-ttu-id="c97dc-114">Exempel 1: Ange prenumerationens kontext</span><span class="sxs-lookup"><span data-stu-id="c97dc-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="c97dc-115">Det här kommandot anger sammanhanget för att använda den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c97dc-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="c97dc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c97dc-116">PARAMETERS</span></span>

### <span data-ttu-id="c97dc-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c97dc-117">-Context</span></span>
<span data-ttu-id="c97dc-118">Anger sammanhanget för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="c97dc-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97dc-119">-DefaultProfile</span></span>
<span data-ttu-id="c97dc-120">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c97dc-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97dc-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="c97dc-121">-ExtendedProperty</span></span>
<span data-ttu-id="c97dc-122">Ytterligare kontext egenskaper</span><span class="sxs-lookup"><span data-stu-id="c97dc-122">Additional context properties</span></span>

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

### <span data-ttu-id="c97dc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c97dc-123">-Force</span></span>
<span data-ttu-id="c97dc-124">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="c97dc-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="c97dc-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c97dc-125">-Name</span></span>
<span data-ttu-id="c97dc-126">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="c97dc-126">Name of the context</span></span>

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

### <span data-ttu-id="c97dc-127">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c97dc-127">-Scope</span></span>
<span data-ttu-id="c97dc-128">Avgör omfattningen av kontext ändringar, till exempel wheher ändringar gäller endast för cusrrent-processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="c97dc-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c97dc-129">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="c97dc-129">-Subscription</span></span>
<span data-ttu-id="c97dc-130">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="c97dc-130">Subscription Name or Id</span></span>

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

### <span data-ttu-id="c97dc-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c97dc-131">-SubscriptionObject</span></span>
<span data-ttu-id="c97dc-132">Ett prenumerations objekt</span><span class="sxs-lookup"><span data-stu-id="c97dc-132">A subscription object</span></span>

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

### <span data-ttu-id="c97dc-133">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="c97dc-133">-Tenant</span></span>
<span data-ttu-id="c97dc-134">Klient organisationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="c97dc-134">Tenant name or ID</span></span>

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

### <span data-ttu-id="c97dc-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="c97dc-135">-TenantObject</span></span>
<span data-ttu-id="c97dc-136">Ett klient organisations objekt</span><span class="sxs-lookup"><span data-stu-id="c97dc-136">A Tenant Object</span></span>

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

### <span data-ttu-id="c97dc-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c97dc-137">-Confirm</span></span>
<span data-ttu-id="c97dc-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c97dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97dc-139">-WhatIf</span></span>
<span data-ttu-id="c97dc-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c97dc-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c97dc-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c97dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97dc-142">CommonParameters</span></span>
<span data-ttu-id="c97dc-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97dc-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97dc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97dc-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c97dc-145">INPUTS</span></span>

### <span data-ttu-id="c97dc-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c97dc-146">PSAzureContext</span></span>
<span data-ttu-id="c97dc-147">Parametern ' context ' godkänner värdet av typen ' PSAzureContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c97dc-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="c97dc-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c97dc-148">OUTPUTS</span></span>

### <span data-ttu-id="c97dc-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c97dc-149">PSAzureContext</span></span>

## <span data-ttu-id="c97dc-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c97dc-150">NOTES</span></span>

## <span data-ttu-id="c97dc-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c97dc-151">RELATED LINKS</span></span>

[<span data-ttu-id="c97dc-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="c97dc-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

