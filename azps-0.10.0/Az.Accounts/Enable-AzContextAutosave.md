---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6c0e557078bde5cbec7b1f7dd96f1fa2c71408a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922002"
---
# <span data-ttu-id="697ba-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="697ba-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="697ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="697ba-102">SYNOPSIS</span></span>
<span data-ttu-id="697ba-103">Tillåt att Azure-autentiseringsuppgiften, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster.</span><span class="sxs-lookup"><span data-stu-id="697ba-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="697ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="697ba-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="697ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="697ba-105">DESCRIPTION</span></span>
<span data-ttu-id="697ba-106">Tillåt att Azure-autentiseringsuppgiften, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster.</span><span class="sxs-lookup"><span data-stu-id="697ba-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="697ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="697ba-107">EXAMPLES</span></span>

### <span data-ttu-id="697ba-108">Aktivera Autospara-autentiseringsuppgifter för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="697ba-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="697ba-109">Aktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="697ba-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="697ba-110">När ett PowerShell-fönster öppnas sparas den aktuella kontexten utan att logga in.</span><span class="sxs-lookup"><span data-stu-id="697ba-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="697ba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="697ba-111">PARAMETERS</span></span>

### <span data-ttu-id="697ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="697ba-112">-DefaultProfile</span></span>
<span data-ttu-id="697ba-113">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="697ba-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="697ba-114">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="697ba-114">-Scope</span></span>
<span data-ttu-id="697ba-115">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="697ba-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="697ba-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="697ba-116">-Confirm</span></span>
<span data-ttu-id="697ba-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="697ba-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="697ba-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="697ba-118">-WhatIf</span></span>
<span data-ttu-id="697ba-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="697ba-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="697ba-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="697ba-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="697ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="697ba-121">CommonParameters</span></span>
<span data-ttu-id="697ba-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="697ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="697ba-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="697ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="697ba-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="697ba-124">INPUTS</span></span>

### <span data-ttu-id="697ba-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="697ba-125">None</span></span>

## <span data-ttu-id="697ba-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="697ba-126">OUTPUTS</span></span>

### <span data-ttu-id="697ba-127">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="697ba-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="697ba-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="697ba-128">NOTES</span></span>

## <span data-ttu-id="697ba-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="697ba-129">RELATED LINKS</span></span>
