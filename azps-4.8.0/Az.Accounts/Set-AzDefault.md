---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258424"
---
# <span data-ttu-id="083ae-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="083ae-101">Set-AzDefault</span></span>

## <span data-ttu-id="083ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="083ae-102">SYNOPSIS</span></span>
<span data-ttu-id="083ae-103">Anger en standard i den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="083ae-103">Sets a default in the current context</span></span>

## <span data-ttu-id="083ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="083ae-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="083ae-105">DESCRIPTION</span></span>
<span data-ttu-id="083ae-106">Set-AzDefault cmdlet lägger till eller ändrar standardvärden i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="083ae-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="083ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="083ae-107">EXAMPLES</span></span>

### <span data-ttu-id="083ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="083ae-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="083ae-109">Det här kommandot anger standard resurs gruppen till den resurs grupp som användaren angett.</span><span class="sxs-lookup"><span data-stu-id="083ae-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="083ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="083ae-110">PARAMETERS</span></span>

### <span data-ttu-id="083ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083ae-111">-DefaultProfile</span></span>
<span data-ttu-id="083ae-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="083ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="083ae-113">-Force</span><span class="sxs-lookup"><span data-stu-id="083ae-113">-Force</span></span>
<span data-ttu-id="083ae-114">Skapa en ny resurs grupp om det angivna standardvärdet inte finns</span><span class="sxs-lookup"><span data-stu-id="083ae-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="083ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="083ae-116">Namnet på den resurs grupp som ska anges som standard</span><span class="sxs-lookup"><span data-stu-id="083ae-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083ae-117">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="083ae-117">-Scope</span></span>
<span data-ttu-id="083ae-118">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="083ae-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="083ae-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="083ae-119">-Confirm</span></span>
<span data-ttu-id="083ae-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="083ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083ae-121">-WhatIf</span></span>
<span data-ttu-id="083ae-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="083ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083ae-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="083ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083ae-124">CommonParameters</span></span>
<span data-ttu-id="083ae-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083ae-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083ae-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="083ae-127">INPUTS</span></span>

### <span data-ttu-id="083ae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="083ae-128">System.String</span></span>

## <span data-ttu-id="083ae-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="083ae-129">OUTPUTS</span></span>

### <span data-ttu-id="083ae-130">Microsoft. Azure. commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="083ae-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="083ae-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="083ae-131">NOTES</span></span>

## <span data-ttu-id="083ae-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="083ae-132">RELATED LINKS</span></span>