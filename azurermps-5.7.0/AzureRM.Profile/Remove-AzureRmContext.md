---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581052"
---
# <span data-ttu-id="b7cfc-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b7cfc-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="b7cfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cfc-103">Ta bort en kontext från uppsättningen tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="b7cfc-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7cfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7cfc-104">SYNTAX</span></span>

### <span data-ttu-id="b7cfc-105">RemoveByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="b7cfc-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cfc-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="b7cfc-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b7cfc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7cfc-107">DESCRIPTION</span></span>
<span data-ttu-id="b7cfc-108">Ta bort en Azure-kontext från uppsättningen kontexter</span><span class="sxs-lookup"><span data-stu-id="b7cfc-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="b7cfc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7cfc-109">EXAMPLES</span></span>

### <span data-ttu-id="b7cfc-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7cfc-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="b7cfc-111">Ta bort kontexten som standard</span><span class="sxs-lookup"><span data-stu-id="b7cfc-111">Remove the context named default</span></span>

## <span data-ttu-id="b7cfc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7cfc-112">PARAMETERS</span></span>

### <span data-ttu-id="b7cfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cfc-113">-DefaultProfile</span></span>
<span data-ttu-id="b7cfc-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7cfc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b7cfc-115">-Force</span></span>
<span data-ttu-id="b7cfc-116">Ta bort kontext även om den är defualt</span><span class="sxs-lookup"><span data-stu-id="b7cfc-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="b7cfc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cfc-117">-InputObject</span></span>
<span data-ttu-id="b7cfc-118">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cfc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7cfc-119">-Name</span></span>
<span data-ttu-id="b7cfc-120">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="b7cfc-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cfc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7cfc-121">-PassThru</span></span>
<span data-ttu-id="b7cfc-122">Returnera den borttagna kontexten</span><span class="sxs-lookup"><span data-stu-id="b7cfc-122">Return the removed context</span></span>

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

### <span data-ttu-id="b7cfc-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b7cfc-123">-Scope</span></span>
<span data-ttu-id="b7cfc-124">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="b7cfc-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b7cfc-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7cfc-125">-Confirm</span></span>
<span data-ttu-id="b7cfc-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7cfc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7cfc-127">-WhatIf</span></span>
<span data-ttu-id="b7cfc-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7cfc-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7cfc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cfc-130">CommonParameters</span></span>
<span data-ttu-id="b7cfc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cfc-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7cfc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cfc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7cfc-133">INPUTS</span></span>

### <span data-ttu-id="b7cfc-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7cfc-134">None</span></span>

## <span data-ttu-id="b7cfc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7cfc-135">OUTPUTS</span></span>

### <span data-ttu-id="b7cfc-136">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b7cfc-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="b7cfc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7cfc-137">NOTES</span></span>

## <span data-ttu-id="b7cfc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7cfc-138">RELATED LINKS</span></span>

