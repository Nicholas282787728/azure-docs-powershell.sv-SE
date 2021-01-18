---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525591"
---
# <span data-ttu-id="045b0-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="045b0-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="045b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="045b0-102">SYNOPSIS</span></span>
<span data-ttu-id="045b0-103">Skapa ett bok märke.</span><span class="sxs-lookup"><span data-stu-id="045b0-103">Get a Bookmark.</span></span>

## <span data-ttu-id="045b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="045b0-104">SYNTAX</span></span>

### <span data-ttu-id="045b0-105">WorkspaceScope (standard)</span><span class="sxs-lookup"><span data-stu-id="045b0-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="045b0-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="045b0-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="045b0-107">ID</span><span class="sxs-lookup"><span data-stu-id="045b0-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="045b0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="045b0-108">DESCRIPTION</span></span>
<span data-ttu-id="045b0-109">Cmdleten **Get-AzSentinelBookmark** hämtar ett bok märke från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="045b0-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="045b0-110">Om du anger parametern *BookmarkId* returneras ett enskilt **bok märkes** objekt.</span><span class="sxs-lookup"><span data-stu-id="045b0-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="045b0-111">Om du inte anger parametern *BookmarkId* returneras en matris med alla bok märken på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="045b0-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="045b0-112">Du kan använda **bok märkes** objekt för att uppdatera bok märket, till exempel att du kan lägga till anteckningar i **bok märket**.</span><span class="sxs-lookup"><span data-stu-id="045b0-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="045b0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="045b0-113">EXAMPLES</span></span>

### <span data-ttu-id="045b0-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="045b0-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="045b0-115">I det här exemplet hämtas alla **bok märken** på den angivna arbets ytan och lagras sedan i $Bookmarks variabel.</span><span class="sxs-lookup"><span data-stu-id="045b0-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="045b0-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="045b0-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="045b0-117">Det här exemplet får ett **bok märke** på den angivna arbets ytan och lagrar det sedan i $Bookmark variabel.</span><span class="sxs-lookup"><span data-stu-id="045b0-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="045b0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="045b0-118">PARAMETERS</span></span>

### <span data-ttu-id="045b0-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="045b0-119">-BookmarkId</span></span>
<span data-ttu-id="045b0-120">Bok märkes-ID,</span><span class="sxs-lookup"><span data-stu-id="045b0-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="045b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045b0-121">-DefaultProfile</span></span>
<span data-ttu-id="045b0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="045b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="045b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="045b0-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="045b0-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="045b0-125">-ResourceId</span></span>
<span data-ttu-id="045b0-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="045b0-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="045b0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="045b0-127">-WorkspaceName</span></span>
<span data-ttu-id="045b0-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="045b0-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="045b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045b0-129">CommonParameters</span></span>
<span data-ttu-id="045b0-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="045b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045b0-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="045b0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045b0-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="045b0-132">INPUTS</span></span>

### <span data-ttu-id="045b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="045b0-133">System.String</span></span>
## <span data-ttu-id="045b0-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="045b0-134">OUTPUTS</span></span>

### <span data-ttu-id="045b0-135">Microsoft. Azure. commands. SecurityInsights. Models. bok märken. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="045b0-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="045b0-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="045b0-136">NOTES</span></span>

## <span data-ttu-id="045b0-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="045b0-137">RELATED LINKS</span></span>
