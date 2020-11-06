---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: 0e875087d52ecddbf216c6e49db96fefdf63e82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583120"
---
# <span data-ttu-id="ea9b6-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="ea9b6-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="ea9b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9b6-103">Tillåt att Azure-autentiseringsuppgiften, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea9b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea9b6-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea9b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9b6-106">Tillåt att Azure-autentiseringsuppgiften, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="ea9b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea9b6-107">EXAMPLES</span></span>

### <span data-ttu-id="ea9b6-108">Aktivera Autospara-autentiseringsuppgifter för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="ea9b6-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="ea9b6-109">Aktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="ea9b6-110">När ett PowerShell-fönster öppnas sparas den aktuella kontexten utan att logga in.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="ea9b6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea9b6-111">PARAMETERS</span></span>

### <span data-ttu-id="ea9b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9b6-112">-DefaultProfile</span></span>
<span data-ttu-id="ea9b6-113">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ea9b6-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea9b6-114">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="ea9b6-114">-Scope</span></span>
<span data-ttu-id="ea9b6-115">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="ea9b6-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ea9b6-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea9b6-116">-Confirm</span></span>
<span data-ttu-id="ea9b6-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9b6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9b6-118">-WhatIf</span></span>
<span data-ttu-id="ea9b6-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9b6-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9b6-121">CommonParameters</span></span>
<span data-ttu-id="ea9b6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9b6-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9b6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9b6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea9b6-124">INPUTS</span></span>

### <span data-ttu-id="ea9b6-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="ea9b6-125">None</span></span>

## <span data-ttu-id="ea9b6-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea9b6-126">OUTPUTS</span></span>

### <span data-ttu-id="ea9b6-127">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ea9b6-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="ea9b6-128">Information om aktuella inställningar för autosparande, inklusive om Spara automatiskt är aktiverat för den aktuella användaren, samt var kontext och autentiseringsuppgifter sparas.</span><span class="sxs-lookup"><span data-stu-id="ea9b6-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="ea9b6-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea9b6-129">NOTES</span></span>

## <span data-ttu-id="ea9b6-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea9b6-130">RELATED LINKS</span></span>

