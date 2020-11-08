---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 7c9c519087fc5f60ef0855eb4caef28e303daf6c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089729"
---
# <span data-ttu-id="a3ce8-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="a3ce8-101">Rename-AzContext</span></span>

## <span data-ttu-id="a3ce8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ce8-103">Byta namn på en Azure-kontext.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-103">Rename an Azure context.</span></span>  <span data-ttu-id="a3ce8-104">Som standard får kontexterna namn av användar konto och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="a3ce8-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3ce8-105">SYNTAX</span></span>

### <span data-ttu-id="a3ce8-106">RenameByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="a3ce8-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="a3ce8-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="a3ce8-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="a3ce8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3ce8-108">DESCRIPTION</span></span>
<span data-ttu-id="a3ce8-109">Byta namn på en Azure-kontext.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-109">Rename an Azure context.</span></span>  <span data-ttu-id="a3ce8-110">Som standard får kontexterna namn av användar konto och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="a3ce8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3ce8-111">EXAMPLES</span></span>

### <span data-ttu-id="a3ce8-112">Byta namn på en kontext med namngivna parametrar</span><span class="sxs-lookup"><span data-stu-id="a3ce8-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="a3ce8-113">Byt namn på kontexten för ' user1@contoso.org ' med abonnemanget ' 12345-6789-2345-3567890 ' till ' ARB '.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="a3ce8-114">Efter det här kommandot kan du använda "Välj-AzContext arbete".</span><span class="sxs-lookup"><span data-stu-id="a3ce8-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="a3ce8-115">Observera att du kan tabba genom värdena för "SourceName" med hjälp av tabb-slutförande.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="a3ce8-116">Byta namn på en kontext med positions parametrar</span><span class="sxs-lookup"><span data-stu-id="a3ce8-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="a3ce8-117">Byt namn på kontexten med namnet "min kontext" till "arbete".</span><span class="sxs-lookup"><span data-stu-id="a3ce8-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="a3ce8-118">Efter det här kommandot kan du rikta kontexten till med Select-AzContext arbete</span><span class="sxs-lookup"><span data-stu-id="a3ce8-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="a3ce8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3ce8-119">PARAMETERS</span></span>

### <span data-ttu-id="a3ce8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ce8-120">-DefaultProfile</span></span>
<span data-ttu-id="a3ce8-121">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3ce8-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3ce8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a3ce8-122">-Force</span></span>
<span data-ttu-id="a3ce8-123">Byt namn på kontexten även om mål kontexten redan finns</span><span class="sxs-lookup"><span data-stu-id="a3ce8-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="a3ce8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ce8-124">-InputObject</span></span>
<span data-ttu-id="a3ce8-125">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3ce8-126">-PassThru</span></span>
<span data-ttu-id="a3ce8-127">Returnera det omväxlade sammanhanget.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="a3ce8-128">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a3ce8-128">-Scope</span></span>
<span data-ttu-id="a3ce8-129">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="a3ce8-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="a3ce8-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="a3ce8-130">-SourceName</span></span>
<span data-ttu-id="a3ce8-131">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="a3ce8-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce8-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="a3ce8-132">-TargetName</span></span>
<span data-ttu-id="a3ce8-133">Det nya namnet på kontexten</span><span class="sxs-lookup"><span data-stu-id="a3ce8-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ce8-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3ce8-134">-Confirm</span></span>
<span data-ttu-id="a3ce8-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ce8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ce8-136">-WhatIf</span></span>
<span data-ttu-id="a3ce8-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ce8-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ce8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ce8-139">CommonParameters</span></span>
<span data-ttu-id="a3ce8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ce8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ce8-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ce8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ce8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3ce8-142">INPUTS</span></span>

### <span data-ttu-id="a3ce8-143">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a3ce8-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a3ce8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3ce8-144">OUTPUTS</span></span>

### <span data-ttu-id="a3ce8-145">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a3ce8-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="a3ce8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3ce8-146">NOTES</span></span>

## <span data-ttu-id="a3ce8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3ce8-147">RELATED LINKS</span></span>