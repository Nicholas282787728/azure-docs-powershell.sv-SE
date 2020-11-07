---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756574"
---
# <span data-ttu-id="09ae6-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="09ae6-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="09ae6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="09ae6-103">Välja ett abonnemang och konto för mål i Azure PowerShell-cmdletar</span><span class="sxs-lookup"><span data-stu-id="09ae6-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09ae6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09ae6-104">SYNTAX</span></span>

### <span data-ttu-id="09ae6-105">Indatavärdet (standard)</span><span class="sxs-lookup"><span data-stu-id="09ae6-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ae6-106">Kontext namn</span><span class="sxs-lookup"><span data-stu-id="09ae6-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="09ae6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09ae6-107">DESCRIPTION</span></span>
<span data-ttu-id="09ae6-108">Välj ett abonnemang för mål (eller konto eller innehavare) i Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09ae6-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="09ae6-109">Efter denna cmdlet används den valda kontexten för framtida cmdletar.</span><span class="sxs-lookup"><span data-stu-id="09ae6-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="09ae6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09ae6-110">EXAMPLES</span></span>

### <span data-ttu-id="09ae6-111">Exempel 1: rikta en namngiven kontext</span><span class="sxs-lookup"><span data-stu-id="09ae6-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="09ae6-112">Mål framtida cmdlets för Azure PowerShell på kontot, innehavaren och prenumerationen i kontexten "arbete".</span><span class="sxs-lookup"><span data-stu-id="09ae6-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="09ae6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09ae6-113">PARAMETERS</span></span>

### <span data-ttu-id="09ae6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ae6-114">-DefaultProfile</span></span>
<span data-ttu-id="09ae6-115">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="09ae6-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09ae6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09ae6-116">-InputObject</span></span>
<span data-ttu-id="09ae6-117">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="09ae6-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ae6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="09ae6-118">-Name</span></span>
<span data-ttu-id="09ae6-119">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="09ae6-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ae6-120">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="09ae6-120">-Scope</span></span>
<span data-ttu-id="09ae6-121">Avgör omfattningen av kontext ändringar, till exempel wheher ändringar gäller endast för cusrrent-processen eller för alla sessioner som användaren startar</span><span class="sxs-lookup"><span data-stu-id="09ae6-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="09ae6-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09ae6-122">-Confirm</span></span>
<span data-ttu-id="09ae6-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09ae6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ae6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ae6-124">-WhatIf</span></span>
<span data-ttu-id="09ae6-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09ae6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ae6-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09ae6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ae6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ae6-127">CommonParameters</span></span>
<span data-ttu-id="09ae6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ae6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ae6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ae6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ae6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09ae6-130">INPUTS</span></span>

### <span data-ttu-id="09ae6-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="09ae6-131">None</span></span>

## <span data-ttu-id="09ae6-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09ae6-132">OUTPUTS</span></span>

### <span data-ttu-id="09ae6-133">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="09ae6-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="09ae6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09ae6-134">NOTES</span></span>

## <span data-ttu-id="09ae6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09ae6-135">RELATED LINKS</span></span>

