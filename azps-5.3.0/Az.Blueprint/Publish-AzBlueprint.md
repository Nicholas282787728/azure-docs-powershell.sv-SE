---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527192"
---
# <span data-ttu-id="7f796-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f796-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="7f796-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f796-102">SYNOPSIS</span></span>
<span data-ttu-id="7f796-103">Publicera en ny version av en skiss.</span><span class="sxs-lookup"><span data-stu-id="7f796-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="7f796-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f796-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f796-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f796-105">DESCRIPTION</span></span>
<span data-ttu-id="7f796-106">Publicera en ny version av en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="7f796-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7f796-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f796-107">EXAMPLES</span></span>

### <span data-ttu-id="7f796-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f796-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="7f796-109">Publicera en ny version av en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="7f796-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="7f796-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f796-110">PARAMETERS</span></span>

### <span data-ttu-id="7f796-111">-Skiss</span><span class="sxs-lookup"><span data-stu-id="7f796-111">-Blueprint</span></span>
<span data-ttu-id="7f796-112">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="7f796-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f796-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="7f796-113">-ChangeNote</span></span>
<span data-ttu-id="7f796-114">Anteckningar som beskriver innehållet i den här skiss versionen.</span><span class="sxs-lookup"><span data-stu-id="7f796-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="7f796-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f796-115">-DefaultProfile</span></span>
<span data-ttu-id="7f796-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f796-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f796-117">-Version</span><span class="sxs-lookup"><span data-stu-id="7f796-117">-Version</span></span>
<span data-ttu-id="7f796-118">Version för ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="7f796-118">Version for the blueprint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f796-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f796-119">-Confirm</span></span>
<span data-ttu-id="7f796-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f796-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f796-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f796-121">-WhatIf</span></span>
<span data-ttu-id="7f796-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f796-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f796-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f796-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f796-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f796-124">CommonParameters</span></span>
<span data-ttu-id="7f796-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f796-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f796-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f796-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f796-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f796-127">INPUTS</span></span>

### <span data-ttu-id="7f796-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7f796-128">System.String</span></span>

### <span data-ttu-id="7f796-129">Microsoft. Azure. commands. skissa. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f796-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="7f796-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f796-130">OUTPUTS</span></span>

### <span data-ttu-id="7f796-131">Microsoft. Azure. commands. skissa. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="7f796-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="7f796-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f796-132">NOTES</span></span>

## <span data-ttu-id="7f796-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f796-133">RELATED LINKS</span></span>
