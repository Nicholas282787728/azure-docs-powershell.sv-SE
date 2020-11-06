---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576825"
---
# <span data-ttu-id="56ae2-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="56ae2-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="56ae2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="56ae2-103">Byta namn på en Azure-kontext.</span><span class="sxs-lookup"><span data-stu-id="56ae2-103">Rename an Azure context.</span></span>  <span data-ttu-id="56ae2-104">Som standard får kontexterna namn av användar konto och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="56ae2-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ae2-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56ae2-105">SYNTAX</span></span>

### <span data-ttu-id="56ae2-106">RenameByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="56ae2-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="56ae2-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="56ae2-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="56ae2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56ae2-108">DESCRIPTION</span></span>
<span data-ttu-id="56ae2-109">Byta namn på en Azure-kontext.</span><span class="sxs-lookup"><span data-stu-id="56ae2-109">Rename an Azure context.</span></span>  <span data-ttu-id="56ae2-110">Som standard får kontexterna namn av användar konto och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="56ae2-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="56ae2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56ae2-111">EXAMPLES</span></span>

### <span data-ttu-id="56ae2-112">Byta namn på en kontext med namngivna parametrar</span><span class="sxs-lookup"><span data-stu-id="56ae2-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="56ae2-113">Byt namn på kontexten för ' user1@contoso.org ' med abonnemanget ' 12345-6789-2345-3567890 ' till ' ARB '.</span><span class="sxs-lookup"><span data-stu-id="56ae2-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="56ae2-114">Efter det här kommandot kan du använda "Välj-AzureRmContext arbete".</span><span class="sxs-lookup"><span data-stu-id="56ae2-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="56ae2-115">Observera att du kan tabba genom värdena för "SourceName" med hjälp av tabb-slutförande.</span><span class="sxs-lookup"><span data-stu-id="56ae2-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="56ae2-116">Byta namn på en kontext med positions parametrar</span><span class="sxs-lookup"><span data-stu-id="56ae2-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="56ae2-117">Byt namn på kontexten med namnet "min kontext" till "arbete".</span><span class="sxs-lookup"><span data-stu-id="56ae2-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="56ae2-118">Efter det här kommandot kan du rikta kontexten till med Select-AzureRmContext arbete</span><span class="sxs-lookup"><span data-stu-id="56ae2-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="56ae2-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56ae2-119">PARAMETERS</span></span>

### <span data-ttu-id="56ae2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ae2-120">-DefaultProfile</span></span>
<span data-ttu-id="56ae2-121">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="56ae2-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ae2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="56ae2-122">-Force</span></span>
<span data-ttu-id="56ae2-123">Byt namn på kontexten även om mål kontexten redan finns</span><span class="sxs-lookup"><span data-stu-id="56ae2-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="56ae2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56ae2-124">-InputObject</span></span>
<span data-ttu-id="56ae2-125">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="56ae2-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56ae2-126">-PassThru</span></span>
<span data-ttu-id="56ae2-127">Returnera det omväxlade sammanhanget.</span><span class="sxs-lookup"><span data-stu-id="56ae2-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="56ae2-128">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="56ae2-128">-Scope</span></span>
<span data-ttu-id="56ae2-129">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="56ae2-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="56ae2-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="56ae2-130">-SourceName</span></span>
<span data-ttu-id="56ae2-131">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="56ae2-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="56ae2-132">-TargetName</span></span>
<span data-ttu-id="56ae2-133">Det nya namnet på kontexten</span><span class="sxs-lookup"><span data-stu-id="56ae2-133">The new name of the context</span></span>

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

### <span data-ttu-id="56ae2-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56ae2-134">-Confirm</span></span>
<span data-ttu-id="56ae2-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56ae2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ae2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ae2-136">-WhatIf</span></span>
<span data-ttu-id="56ae2-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56ae2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ae2-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56ae2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ae2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ae2-139">CommonParameters</span></span>
<span data-ttu-id="56ae2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ae2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ae2-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ae2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ae2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56ae2-142">INPUTS</span></span>

### <span data-ttu-id="56ae2-143">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="56ae2-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="56ae2-144">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="56ae2-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="56ae2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56ae2-145">OUTPUTS</span></span>

### <span data-ttu-id="56ae2-146">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="56ae2-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="56ae2-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56ae2-147">NOTES</span></span>

## <span data-ttu-id="56ae2-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56ae2-148">RELATED LINKS</span></span>
