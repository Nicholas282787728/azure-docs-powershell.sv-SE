---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583103"
---
# <span data-ttu-id="00211-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="00211-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="00211-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00211-102">SYNOPSIS</span></span>
<span data-ttu-id="00211-103">Välja ett abonnemang och konto för mål i Azure PowerShell-cmdletar</span><span class="sxs-lookup"><span data-stu-id="00211-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00211-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00211-104">SYNTAX</span></span>

### <span data-ttu-id="00211-105">SelectByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="00211-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00211-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="00211-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="00211-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00211-107">DESCRIPTION</span></span>
<span data-ttu-id="00211-108">Välj ett abonnemang för mål (eller konto eller innehavare) i Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="00211-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="00211-109">Efter denna cmdlet används den valda kontexten för framtida cmdletar.</span><span class="sxs-lookup"><span data-stu-id="00211-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="00211-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00211-110">EXAMPLES</span></span>

### <span data-ttu-id="00211-111">Exempel 1: rikta en namngiven kontext</span><span class="sxs-lookup"><span data-stu-id="00211-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="00211-112">Mål framtida cmdlets för Azure PowerShell på kontot, innehavaren och prenumerationen i kontexten "arbete".</span><span class="sxs-lookup"><span data-stu-id="00211-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="00211-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00211-113">PARAMETERS</span></span>

### <span data-ttu-id="00211-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00211-114">-DefaultProfile</span></span>
<span data-ttu-id="00211-115">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00211-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00211-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00211-116">-InputObject</span></span>
<span data-ttu-id="00211-117">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="00211-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00211-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="00211-118">-Name</span></span>
<span data-ttu-id="00211-119">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="00211-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00211-120">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="00211-120">-Scope</span></span>
<span data-ttu-id="00211-121">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="00211-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="00211-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00211-122">-Confirm</span></span>
<span data-ttu-id="00211-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00211-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00211-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00211-124">-WhatIf</span></span>
<span data-ttu-id="00211-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00211-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00211-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00211-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00211-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00211-127">CommonParameters</span></span>
<span data-ttu-id="00211-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00211-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00211-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00211-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00211-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00211-130">INPUTS</span></span>

### <span data-ttu-id="00211-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="00211-131">None</span></span>

## <span data-ttu-id="00211-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00211-132">OUTPUTS</span></span>

### <span data-ttu-id="00211-133">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="00211-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="00211-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00211-134">NOTES</span></span>

## <span data-ttu-id="00211-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00211-135">RELATED LINKS</span></span>

