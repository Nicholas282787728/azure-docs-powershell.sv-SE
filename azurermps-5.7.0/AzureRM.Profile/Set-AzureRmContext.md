---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583096"
---
# <span data-ttu-id="55bdf-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="55bdf-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="55bdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="55bdf-103">Anger klient organisation, prenumeration och miljö för cmdlets som ska användas i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="55bdf-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55bdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55bdf-104">SYNTAX</span></span>

### <span data-ttu-id="55bdf-105">Kontext (standard)</span><span class="sxs-lookup"><span data-stu-id="55bdf-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55bdf-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="55bdf-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55bdf-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="55bdf-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55bdf-108">Prenumerationsvy</span><span class="sxs-lookup"><span data-stu-id="55bdf-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55bdf-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="55bdf-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55bdf-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55bdf-110">DESCRIPTION</span></span>
<span data-ttu-id="55bdf-111">Med Set-AzureRmContext cmdlet anges autentiseringsinformation för de cmdlets som du kör i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="55bdf-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="55bdf-112">Kontexten inkluderar klient organisation, prenumeration och miljö information.</span><span class="sxs-lookup"><span data-stu-id="55bdf-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="55bdf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55bdf-113">EXAMPLES</span></span>

### <span data-ttu-id="55bdf-114">Exempel 1: Ange prenumerationens kontext</span><span class="sxs-lookup"><span data-stu-id="55bdf-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="55bdf-115">Det här kommandot anger sammanhanget för att använda den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="55bdf-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="55bdf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55bdf-116">PARAMETERS</span></span>

### <span data-ttu-id="55bdf-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="55bdf-117">-Context</span></span>
<span data-ttu-id="55bdf-118">Anger sammanhanget för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="55bdf-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bdf-119">-DefaultProfile</span></span>
<span data-ttu-id="55bdf-120">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55bdf-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55bdf-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="55bdf-121">-ExtendedProperty</span></span>
<span data-ttu-id="55bdf-122">Ytterligare kontext egenskaper</span><span class="sxs-lookup"><span data-stu-id="55bdf-122">Additional context properties</span></span>

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

### <span data-ttu-id="55bdf-123">-Force</span><span class="sxs-lookup"><span data-stu-id="55bdf-123">-Force</span></span>
<span data-ttu-id="55bdf-124">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="55bdf-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="55bdf-125">-Name</span></span>
<span data-ttu-id="55bdf-126">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="55bdf-126">Name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-127">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="55bdf-127">-Scope</span></span>
<span data-ttu-id="55bdf-128">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="55bdf-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-129">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="55bdf-129">-Subscription</span></span>
<span data-ttu-id="55bdf-130">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="55bdf-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="55bdf-131">-SubscriptionObject</span></span>
<span data-ttu-id="55bdf-132">Ett prenumerations objekt</span><span class="sxs-lookup"><span data-stu-id="55bdf-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-133">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="55bdf-133">-Tenant</span></span>
<span data-ttu-id="55bdf-134">Klient organisationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="55bdf-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="55bdf-135">-TenantObject</span></span>
<span data-ttu-id="55bdf-136">Ett klient organisations objekt</span><span class="sxs-lookup"><span data-stu-id="55bdf-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55bdf-137">-Confirm</span></span>
<span data-ttu-id="55bdf-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55bdf-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55bdf-139">-WhatIf</span></span>
<span data-ttu-id="55bdf-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55bdf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55bdf-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55bdf-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bdf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bdf-142">CommonParameters</span></span>
<span data-ttu-id="55bdf-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55bdf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bdf-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55bdf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bdf-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55bdf-145">INPUTS</span></span>

### <span data-ttu-id="55bdf-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="55bdf-146">PSAzureContext</span></span>
<span data-ttu-id="55bdf-147">Parametern ' context ' godkänner värdet av typen ' PSAzureContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="55bdf-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="55bdf-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55bdf-148">OUTPUTS</span></span>

### <span data-ttu-id="55bdf-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="55bdf-149">PSAzureContext</span></span>

## <span data-ttu-id="55bdf-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55bdf-150">NOTES</span></span>

## <span data-ttu-id="55bdf-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55bdf-151">RELATED LINKS</span></span>

[<span data-ttu-id="55bdf-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="55bdf-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

