---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 8bc129ddc1b4291ea7b3c9100a964bf5bb1dcee6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585391"
---
# <span data-ttu-id="6bcf2-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6bcf2-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="6bcf2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcf2-103">Ta bort en kontext från uppsättningen tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="6bcf2-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bcf2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bcf2-104">SYNTAX</span></span>

### <span data-ttu-id="6bcf2-105">Indatavärdet (standard)</span><span class="sxs-lookup"><span data-stu-id="6bcf2-105">Input Object (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bcf2-106">Namngiven kontext</span><span class="sxs-lookup"><span data-stu-id="6bcf2-106">Named Context</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="6bcf2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bcf2-107">DESCRIPTION</span></span>
<span data-ttu-id="6bcf2-108">Ta bort en Azure-kontext från uppsättningen kontexter</span><span class="sxs-lookup"><span data-stu-id="6bcf2-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="6bcf2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bcf2-109">EXAMPLES</span></span>

### <span data-ttu-id="6bcf2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6bcf2-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="6bcf2-111">Ta bort kontexten som standard</span><span class="sxs-lookup"><span data-stu-id="6bcf2-111">Remove the context named default</span></span>

## <span data-ttu-id="6bcf2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bcf2-112">PARAMETERS</span></span>

### <span data-ttu-id="6bcf2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcf2-113">-DefaultProfile</span></span>
<span data-ttu-id="6bcf2-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bcf2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6bcf2-115">-Force</span></span>
<span data-ttu-id="6bcf2-116">Ta bort kontext även om den är defualt</span><span class="sxs-lookup"><span data-stu-id="6bcf2-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="6bcf2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bcf2-117">-InputObject</span></span>
<span data-ttu-id="6bcf2-118">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6bcf2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6bcf2-119">-Name</span></span>
<span data-ttu-id="6bcf2-120">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="6bcf2-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Named Context
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcf2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bcf2-121">-PassThru</span></span>
<span data-ttu-id="6bcf2-122">Returnera den borttagna kontexten</span><span class="sxs-lookup"><span data-stu-id="6bcf2-122">Return the removed context</span></span>

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

### <span data-ttu-id="6bcf2-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6bcf2-123">-Scope</span></span>
<span data-ttu-id="6bcf2-124">Avgör omfattningen av kontext ändringar, till exempel wheher ändringar gäller endast för cusrrent-processen eller för alla sessioner som användaren startar</span><span class="sxs-lookup"><span data-stu-id="6bcf2-124">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="6bcf2-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6bcf2-125">-Confirm</span></span>
<span data-ttu-id="6bcf2-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcf2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcf2-127">-WhatIf</span></span>
<span data-ttu-id="6bcf2-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bcf2-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcf2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcf2-130">CommonParameters</span></span>
<span data-ttu-id="6bcf2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcf2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcf2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcf2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcf2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bcf2-133">INPUTS</span></span>

### <span data-ttu-id="6bcf2-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="6bcf2-134">None</span></span>

## <span data-ttu-id="6bcf2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bcf2-135">OUTPUTS</span></span>

### <span data-ttu-id="6bcf2-136">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6bcf2-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="6bcf2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bcf2-137">NOTES</span></span>

## <span data-ttu-id="6bcf2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bcf2-138">RELATED LINKS</span></span>

