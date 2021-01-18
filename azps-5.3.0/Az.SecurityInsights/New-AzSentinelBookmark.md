---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525583"
---
# <span data-ttu-id="cce80-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="cce80-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="cce80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cce80-102">SYNOPSIS</span></span>
<span data-ttu-id="cce80-103">Skapa ett bok märke.</span><span class="sxs-lookup"><span data-stu-id="cce80-103">Create a Bookmark.</span></span>

## <span data-ttu-id="cce80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cce80-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cce80-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cce80-105">DESCRIPTION</span></span>
<span data-ttu-id="cce80-106">Cmdleten **New-AzSentinelBookmark** skapar ett bok märke från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cce80-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="cce80-107">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cce80-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cce80-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cce80-108">EXAMPLES</span></span>

### <span data-ttu-id="cce80-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cce80-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="cce80-110">I det här exemplet skapas ett **bok märke** på den angivna arbets ytan och det lagrar det sedan i $Bookmark variabel.</span><span class="sxs-lookup"><span data-stu-id="cce80-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="cce80-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cce80-111">PARAMETERS</span></span>

### <span data-ttu-id="cce80-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="cce80-112">-BookmarkId</span></span>
<span data-ttu-id="cce80-113">Bok märkes-ID,</span><span class="sxs-lookup"><span data-stu-id="cce80-113">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce80-114">-DefaultProfile</span></span>
<span data-ttu-id="cce80-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cce80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cce80-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cce80-116">-DisplayName</span></span>
<span data-ttu-id="cce80-117">Bok märkes regelns visnings namn.</span><span class="sxs-lookup"><span data-stu-id="cce80-117">Bookmark Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="cce80-118">-IncidentInfo</span></span>
<span data-ttu-id="cce80-119">Information om ett bok märkes problem.</span><span class="sxs-lookup"><span data-stu-id="cce80-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-120">-Etikett</span><span class="sxs-lookup"><span data-stu-id="cce80-120">-Label</span></span>
<span data-ttu-id="cce80-121">Incident etiketter.</span><span class="sxs-lookup"><span data-stu-id="cce80-121">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-122">-Kommentarer</span><span class="sxs-lookup"><span data-stu-id="cce80-122">-Notes</span></span>
<span data-ttu-id="cce80-123">Lägga till bok märken.</span><span class="sxs-lookup"><span data-stu-id="cce80-123">Bookmark Notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-124">-Fråga</span><span class="sxs-lookup"><span data-stu-id="cce80-124">-Query</span></span>
<span data-ttu-id="cce80-125">Bookmark-fråga.</span><span class="sxs-lookup"><span data-stu-id="cce80-125">Bookmark Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="cce80-126">-QueryResult</span></span>
<span data-ttu-id="cce80-127">Frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="cce80-127">Bookmark Query Result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce80-128">-ResourceGroupName</span></span>
<span data-ttu-id="cce80-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="cce80-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cce80-130">-WorkspaceName</span></span>
<span data-ttu-id="cce80-131">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cce80-131">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cce80-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cce80-132">-Confirm</span></span>
<span data-ttu-id="cce80-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cce80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cce80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cce80-134">-WhatIf</span></span>
<span data-ttu-id="cce80-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cce80-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cce80-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cce80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cce80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce80-137">CommonParameters</span></span>
<span data-ttu-id="cce80-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce80-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cce80-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce80-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cce80-140">INPUTS</span></span>

### <span data-ttu-id="cce80-141">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="cce80-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="cce80-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cce80-142">OUTPUTS</span></span>

### <span data-ttu-id="cce80-143">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="cce80-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="cce80-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cce80-144">NOTES</span></span>

## <span data-ttu-id="cce80-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cce80-145">RELATED LINKS</span></span>
