---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525567"
---
# <span data-ttu-id="a502b-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a502b-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="a502b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a502b-102">SYNOPSIS</span></span>
<span data-ttu-id="a502b-103">Ta bort ett bok märke.</span><span class="sxs-lookup"><span data-stu-id="a502b-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="a502b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a502b-104">SYNTAX</span></span>

### <span data-ttu-id="a502b-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="a502b-105">BookmarkId.</span></span> <span data-ttu-id="a502b-106">Vis</span><span class="sxs-lookup"><span data-stu-id="a502b-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a502b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a502b-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a502b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a502b-108">DESCRIPTION</span></span>
<span data-ttu-id="a502b-109">Cmdleten **Remove-AzSentinelBookmark** tar bort ett bok märke permanent från en angiven arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a502b-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="a502b-110">Du kan skicka ett **Bookmark** -objekt med hjälp av pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="a502b-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a502b-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a502b-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a502b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a502b-112">EXAMPLES</span></span>

### <span data-ttu-id="a502b-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a502b-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="a502b-114">Det här kommandot tar bort bok märket från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a502b-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="a502b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a502b-115">PARAMETERS</span></span>

### <span data-ttu-id="a502b-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="a502b-116">-BookmarkId</span></span>
<span data-ttu-id="a502b-117">Bok märkes-ID,</span><span class="sxs-lookup"><span data-stu-id="a502b-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a502b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a502b-118">-DefaultProfile</span></span>
<span data-ttu-id="a502b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a502b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a502b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a502b-120">-InputObject</span></span>
<span data-ttu-id="a502b-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a502b-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a502b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a502b-122">-PassThru</span></span>
<span data-ttu-id="a502b-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="a502b-123">PassThru</span></span>

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

### <span data-ttu-id="a502b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a502b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a502b-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a502b-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a502b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a502b-126">-WorkspaceName</span></span>
<span data-ttu-id="a502b-127">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a502b-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a502b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a502b-128">-Confirm</span></span>
<span data-ttu-id="a502b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a502b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a502b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a502b-130">-WhatIf</span></span>
<span data-ttu-id="a502b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a502b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a502b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a502b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a502b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a502b-133">CommonParameters</span></span>
<span data-ttu-id="a502b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a502b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a502b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a502b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a502b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a502b-136">INPUTS</span></span>

### <span data-ttu-id="a502b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a502b-137">System.String</span></span>
### <span data-ttu-id="a502b-138">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a502b-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="a502b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a502b-139">OUTPUTS</span></span>

### <span data-ttu-id="a502b-140">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a502b-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="a502b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a502b-141">NOTES</span></span>

## <span data-ttu-id="a502b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a502b-142">RELATED LINKS</span></span>
