---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 0e102d6c0c4db5bd3d93d4349a2a0e06284cd8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576827"
---
# <span data-ttu-id="d396a-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d396a-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="d396a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d396a-102">SYNOPSIS</span></span>
<span data-ttu-id="d396a-103">Ta bort en kontext från uppsättningen tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="d396a-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d396a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d396a-104">SYNTAX</span></span>

### <span data-ttu-id="d396a-105">RemoveByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="d396a-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d396a-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="d396a-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="d396a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d396a-107">DESCRIPTION</span></span>
<span data-ttu-id="d396a-108">Ta bort en Azure-kontext från uppsättningen kontexter</span><span class="sxs-lookup"><span data-stu-id="d396a-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="d396a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d396a-109">EXAMPLES</span></span>

### <span data-ttu-id="d396a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d396a-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="d396a-111">Ta bort kontexten som standard</span><span class="sxs-lookup"><span data-stu-id="d396a-111">Remove the context named default</span></span>

## <span data-ttu-id="d396a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d396a-112">PARAMETERS</span></span>

### <span data-ttu-id="d396a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d396a-113">-DefaultProfile</span></span>
<span data-ttu-id="d396a-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d396a-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d396a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d396a-115">-Force</span></span>
<span data-ttu-id="d396a-116">Ta bort kontext även om den är defualt</span><span class="sxs-lookup"><span data-stu-id="d396a-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="d396a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d396a-117">-InputObject</span></span>
<span data-ttu-id="d396a-118">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d396a-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d396a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d396a-119">-Name</span></span>
<span data-ttu-id="d396a-120">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="d396a-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d396a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d396a-121">-PassThru</span></span>
<span data-ttu-id="d396a-122">Returnera den borttagna kontexten</span><span class="sxs-lookup"><span data-stu-id="d396a-122">Return the removed context</span></span>

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

### <span data-ttu-id="d396a-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="d396a-123">-Scope</span></span>
<span data-ttu-id="d396a-124">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="d396a-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="d396a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d396a-125">-Confirm</span></span>
<span data-ttu-id="d396a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d396a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d396a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d396a-127">-WhatIf</span></span>
<span data-ttu-id="d396a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d396a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d396a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d396a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d396a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d396a-130">CommonParameters</span></span>
<span data-ttu-id="d396a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d396a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d396a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d396a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d396a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d396a-133">INPUTS</span></span>

### <span data-ttu-id="d396a-134">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d396a-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="d396a-135">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d396a-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d396a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d396a-136">OUTPUTS</span></span>

### <span data-ttu-id="d396a-137">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d396a-137">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="d396a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d396a-138">NOTES</span></span>

## <span data-ttu-id="d396a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d396a-139">RELATED LINKS</span></span>
