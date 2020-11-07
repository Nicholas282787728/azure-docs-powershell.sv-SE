---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757248"
---
# <span data-ttu-id="bf17c-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="bf17c-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="bf17c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf17c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf17c-103">Kopplar från ett kopplat Azure-konto och tar bort alla autentiseringsuppgifter och kontexter som är kopplade till kontot.</span><span class="sxs-lookup"><span data-stu-id="bf17c-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf17c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf17c-104">SYNTAX</span></span>

### <span data-ttu-id="bf17c-105">ContextName (standard)</span><span class="sxs-lookup"><span data-stu-id="bf17c-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf17c-106">Användar</span><span class="sxs-lookup"><span data-stu-id="bf17c-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf17c-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bf17c-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf17c-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bf17c-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf17c-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="bf17c-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf17c-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf17c-110">DESCRIPTION</span></span>
<span data-ttu-id="bf17c-111">Disconnect-AzureRmAccount cmdlet kopplar från ett kopplat Azure-konto och tar bort alla autentiseringsuppgifter och kontexter (information om prenumeration och innehavare) som är kopplad till kontot.</span><span class="sxs-lookup"><span data-stu-id="bf17c-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="bf17c-112">När du har kört denna cmdlet måste du logga in igen med Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="bf17c-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="bf17c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf17c-113">EXAMPLES</span></span>

### <span data-ttu-id="bf17c-114">Logga ut från aktuellt konto</span><span class="sxs-lookup"><span data-stu-id="bf17c-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="bf17c-115">Loggar ut från det Azure-konto som är associerat med den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="bf17c-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="bf17c-116">Logga ut från det konto som är kopplat till en viss kontext</span><span class="sxs-lookup"><span data-stu-id="bf17c-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="bf17c-117">Loggar ut det konto som är kopplat till angiven kontext (med namnet "arbete").</span><span class="sxs-lookup"><span data-stu-id="bf17c-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="bf17c-118">Eftersom "CurrentUser"-området används kommer alla autentiseringsuppgifter och kontexter att tas bort permanent.</span><span class="sxs-lookup"><span data-stu-id="bf17c-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="bf17c-119">Logga ut en viss användare</span><span class="sxs-lookup"><span data-stu-id="bf17c-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="bf17c-120">Loggar ut den användare user1@contoso.org som är associerad med den här användaren kommer att tas bort.</span><span class="sxs-lookup"><span data-stu-id="bf17c-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="bf17c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf17c-121">PARAMETERS</span></span>

### <span data-ttu-id="bf17c-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf17c-122">-ApplicationId</span></span>
<span data-ttu-id="bf17c-123">ServicePrincipal-ID (globalt unikt ID)</span><span class="sxs-lookup"><span data-stu-id="bf17c-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="bf17c-124">-AzureContext</span></span>
<span data-ttu-id="bf17c-125">Snabb</span><span class="sxs-lookup"><span data-stu-id="bf17c-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="bf17c-126">-ContextName</span></span>
<span data-ttu-id="bf17c-127">Namn på kontexten för att logga ut från</span><span class="sxs-lookup"><span data-stu-id="bf17c-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf17c-128">-DefaultProfile</span></span>
<span data-ttu-id="bf17c-129">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf17c-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf17c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf17c-130">-InputObject</span></span>
<span data-ttu-id="bf17c-131">Det konto objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="bf17c-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-132">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="bf17c-132">-Scope</span></span>
<span data-ttu-id="bf17c-133">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="bf17c-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="bf17c-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="bf17c-134">-TenantId</span></span>
<span data-ttu-id="bf17c-135">Klient-ID (globalt unikt ID)</span><span class="sxs-lookup"><span data-stu-id="bf17c-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-136">-Username</span><span class="sxs-lookup"><span data-stu-id="bf17c-136">-Username</span></span>
<span data-ttu-id="bf17c-137">Användar namn för formuläret " user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="bf17c-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf17c-138">-Confirm</span></span>
<span data-ttu-id="bf17c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf17c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf17c-140">-WhatIf</span></span>
<span data-ttu-id="bf17c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf17c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf17c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf17c-142">The cmdlet is not executed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf17c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf17c-143">CommonParameters</span></span>
<span data-ttu-id="bf17c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf17c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf17c-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf17c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf17c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf17c-146">INPUTS</span></span>

### <span data-ttu-id="bf17c-147">Microsoft. Azure. commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="bf17c-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="bf17c-148">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="bf17c-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="bf17c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf17c-149">OUTPUTS</span></span>

### <span data-ttu-id="bf17c-150">Microsoft. Azure. commands. Profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="bf17c-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="bf17c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf17c-151">NOTES</span></span>

## <span data-ttu-id="bf17c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf17c-152">RELATED LINKS</span></span>
