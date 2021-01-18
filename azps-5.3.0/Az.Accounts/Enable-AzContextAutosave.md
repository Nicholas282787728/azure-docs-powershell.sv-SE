---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525213"
---
# <span data-ttu-id="9958c-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="9958c-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="9958c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9958c-102">SYNOPSIS</span></span>
<span data-ttu-id="9958c-103">Azure-kontexter är PowerShell-objekt som representerar ditt aktiva abonnemang för att köra kommandon mot och autentiseringsinformation som behövs för att ansluta till ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="9958c-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="9958c-104">Med Azure-kontexter behöver Azure PowerShell inte omverifiera ditt konto varje gång du byter abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9958c-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="9958c-105">Mer information finns i [kontext objekt för Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="9958c-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="9958c-106">Denna cmdlet gör att Azure context-informationen sparas och läses in automatiskt när du startar en PowerShell-process.</span><span class="sxs-lookup"><span data-stu-id="9958c-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="9958c-107">Till exempel när du öppnar ett nytt fönster.</span><span class="sxs-lookup"><span data-stu-id="9958c-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="9958c-108">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9958c-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9958c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9958c-109">DESCRIPTION</span></span>

<span data-ttu-id="9958c-110">Gör att Azure context-informationen sparas och läses in automatiskt när en PowerShell-process startas.</span><span class="sxs-lookup"><span data-stu-id="9958c-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="9958c-111">Kontexten sparas i slutet av körningen av en cmdlet som påverkar kontexten.</span><span class="sxs-lookup"><span data-stu-id="9958c-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="9958c-112">Till exempel alla profil-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="9958c-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="9958c-113">Om du använder användarautentisering kan token uppdateras när en cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="9958c-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="9958c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9958c-114">EXAMPLES</span></span>

### <span data-ttu-id="9958c-115">Exempel 1: Aktivera Autospara-autentiseringsuppgifter för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="9958c-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="9958c-116">Aktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="9958c-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="9958c-117">När ett PowerShell-fönster öppnas sparas din nuvarande kontext utan att logga in.</span><span class="sxs-lookup"><span data-stu-id="9958c-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="9958c-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9958c-118">Example 2</span></span>

<span data-ttu-id="9958c-119">Tillåt att Azure Credential, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster i den här PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="9958c-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="9958c-120">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="9958c-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="9958c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9958c-121">PARAMETERS</span></span>

### <span data-ttu-id="9958c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9958c-122">-DefaultProfile</span></span>

<span data-ttu-id="9958c-123">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9958c-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="9958c-124">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9958c-124">-Scope</span></span>

<span data-ttu-id="9958c-125">Avgör omfattningen av kontext ändringar.</span><span class="sxs-lookup"><span data-stu-id="9958c-125">Determines the scope of context changes.</span></span> <span data-ttu-id="9958c-126">Till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="9958c-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="9958c-127">Ändringar som görs med omfattningen `CurrentUser` påverkar alla PowerShell-sessioner som användaren startat.</span><span class="sxs-lookup"><span data-stu-id="9958c-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="9958c-128">Om en speciell session måste ha olika inställningar använder du omfattningen `Process` .</span><span class="sxs-lookup"><span data-stu-id="9958c-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9958c-129">-Confirm</span></span>

<span data-ttu-id="9958c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9958c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9958c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9958c-131">-WhatIf</span></span>

<span data-ttu-id="9958c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9958c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9958c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9958c-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="9958c-134">Vanliga parametrar</span><span class="sxs-lookup"><span data-stu-id="9958c-134">Common Parameters</span></span>

<span data-ttu-id="9958c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9958c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9958c-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9958c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9958c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9958c-137">INPUTS</span></span>

### <span data-ttu-id="9958c-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="9958c-138">None</span></span>

## <span data-ttu-id="9958c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9958c-139">OUTPUTS</span></span>

### <span data-ttu-id="9958c-140">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="9958c-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="9958c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9958c-141">NOTES</span></span>

## <span data-ttu-id="9958c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9958c-142">RELATED LINKS</span></span>
