---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525559"
---
# <span data-ttu-id="98b06-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="98b06-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="98b06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98b06-102">SYNOPSIS</span></span>
<span data-ttu-id="98b06-103">Uppdatera ett bok märke.</span><span class="sxs-lookup"><span data-stu-id="98b06-103">Update a Bookmark.</span></span>

## <span data-ttu-id="98b06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98b06-104">SYNTAX</span></span>

### <span data-ttu-id="98b06-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="98b06-105">BookmarkId.</span></span> <span data-ttu-id="98b06-106">Vis</span><span class="sxs-lookup"><span data-stu-id="98b06-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b06-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="98b06-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b06-108">ID</span><span class="sxs-lookup"><span data-stu-id="98b06-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b06-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98b06-109">DESCRIPTION</span></span>
<span data-ttu-id="98b06-110">Cmdleten **Update-AzSentinelBookmark** uppdaterar bok märket på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="98b06-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="98b06-111">Du kan skicka ett **Bookmark** -objekt som en parameter eller med hjälp av pipeline-operatorn eller så kan du ange obligatoriska *BookmarkId* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="98b06-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="98b06-112">Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="98b06-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="98b06-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98b06-113">EXAMPLES</span></span>

### <span data-ttu-id="98b06-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98b06-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="98b06-115">Kommandot uppdaterar bok märket genom att ange egenskapen *Notes* .</span><span class="sxs-lookup"><span data-stu-id="98b06-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="98b06-116">Alla andra propreties är desamma.</span><span class="sxs-lookup"><span data-stu-id="98b06-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="98b06-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="98b06-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="98b06-118">Det första kommandot får bok märket genom *BookmarkId* från den angivna arbets ytan och lagrar det sedan i $Bookmark variabel.</span><span class="sxs-lookup"><span data-stu-id="98b06-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="98b06-119">Det andra kommandot uppdaterar egenskapen Notes.</span><span class="sxs-lookup"><span data-stu-id="98b06-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="98b06-120">Alla andra propreties är desamma.</span><span class="sxs-lookup"><span data-stu-id="98b06-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="98b06-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98b06-121">PARAMETERS</span></span>

### <span data-ttu-id="98b06-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="98b06-122">-BookmarkId</span></span>
<span data-ttu-id="98b06-123">Bok märkes-ID,</span><span class="sxs-lookup"><span data-stu-id="98b06-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b06-124">-DefaultProfile</span></span>
<span data-ttu-id="98b06-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98b06-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="98b06-126">-DisplayName</span></span>
<span data-ttu-id="98b06-127">Bok märkes regelns visnings namn.</span><span class="sxs-lookup"><span data-stu-id="98b06-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="98b06-128">-IncidentInfo</span></span>
<span data-ttu-id="98b06-129">Information om ett bok märkes problem.</span><span class="sxs-lookup"><span data-stu-id="98b06-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b06-130">-InputObject</span></span>
<span data-ttu-id="98b06-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="98b06-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-132">-Etikett</span><span class="sxs-lookup"><span data-stu-id="98b06-132">-Label</span></span>
<span data-ttu-id="98b06-133">Incident etiketter.</span><span class="sxs-lookup"><span data-stu-id="98b06-133">Incident Labels.</span></span>

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

### <span data-ttu-id="98b06-134">-Kommentarer</span><span class="sxs-lookup"><span data-stu-id="98b06-134">-Notes</span></span>
<span data-ttu-id="98b06-135">Lägga till bok märken.</span><span class="sxs-lookup"><span data-stu-id="98b06-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-136">-Fråga</span><span class="sxs-lookup"><span data-stu-id="98b06-136">-Query</span></span>
<span data-ttu-id="98b06-137">Bookmark-fråga.</span><span class="sxs-lookup"><span data-stu-id="98b06-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="98b06-138">-QueryResult</span></span>
<span data-ttu-id="98b06-139">Frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="98b06-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b06-140">-ResourceGroupName</span></span>
<span data-ttu-id="98b06-141">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="98b06-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98b06-142">-ResourceId</span></span>
<span data-ttu-id="98b06-143">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="98b06-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98b06-144">-WorkspaceName</span></span>
<span data-ttu-id="98b06-145">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="98b06-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b06-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98b06-146">-Confirm</span></span>
<span data-ttu-id="98b06-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98b06-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b06-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b06-148">-WhatIf</span></span>
<span data-ttu-id="98b06-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98b06-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b06-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98b06-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b06-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b06-151">CommonParameters</span></span>
<span data-ttu-id="98b06-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b06-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b06-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98b06-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b06-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98b06-154">INPUTS</span></span>

### <span data-ttu-id="98b06-155">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="98b06-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="98b06-156">System. String</span><span class="sxs-lookup"><span data-stu-id="98b06-156">System.String</span></span>

### <span data-ttu-id="98b06-157">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="98b06-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="98b06-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98b06-158">OUTPUTS</span></span>

### <span data-ttu-id="98b06-159">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="98b06-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="98b06-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98b06-160">NOTES</span></span>

## <span data-ttu-id="98b06-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98b06-161">RELATED LINKS</span></span>
