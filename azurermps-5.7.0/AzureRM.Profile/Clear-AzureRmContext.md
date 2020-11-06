---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573388"
---
# <span data-ttu-id="33987-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="33987-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="33987-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33987-102">SYNOPSIS</span></span>
<span data-ttu-id="33987-103">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="33987-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33987-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33987-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33987-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33987-105">DESCRIPTION</span></span>
<span data-ttu-id="33987-106">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="33987-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="33987-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33987-107">EXAMPLES</span></span>

### <span data-ttu-id="33987-108">Rensa global kontext</span><span class="sxs-lookup"><span data-stu-id="33987-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="33987-109">Ta bort all information om konto, prenumeration och autentiseringsinformation för en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="33987-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="33987-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33987-110">PARAMETERS</span></span>

### <span data-ttu-id="33987-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33987-111">-DefaultProfile</span></span>
<span data-ttu-id="33987-112">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="33987-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33987-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33987-113">-Force</span></span>
<span data-ttu-id="33987-114">Ta bort alla användare och grupper från globalt scope utan att fråga</span><span class="sxs-lookup"><span data-stu-id="33987-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="33987-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33987-115">-PassThru</span></span>
<span data-ttu-id="33987-116">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="33987-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="33987-117">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="33987-117">-Scope</span></span>
<span data-ttu-id="33987-118">Rensa bara kontexten för den aktuella PowerShell-sessionen eller för alla sessioner.</span><span class="sxs-lookup"><span data-stu-id="33987-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33987-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33987-119">-Confirm</span></span>
<span data-ttu-id="33987-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33987-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33987-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33987-121">-WhatIf</span></span>
<span data-ttu-id="33987-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33987-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33987-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33987-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33987-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33987-124">CommonParameters</span></span>
<span data-ttu-id="33987-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33987-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33987-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33987-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33987-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33987-127">INPUTS</span></span>

### <span data-ttu-id="33987-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="33987-128">None</span></span>

## <span data-ttu-id="33987-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33987-129">OUTPUTS</span></span>

### <span data-ttu-id="33987-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33987-130">System.Boolean</span></span>
<span data-ttu-id="33987-131">Sant om kontexten har rensats, annars FALSE.</span><span class="sxs-lookup"><span data-stu-id="33987-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="33987-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33987-132">NOTES</span></span>

## <span data-ttu-id="33987-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33987-133">RELATED LINKS</span></span>

