---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: 4ad2b7db5e212cf15748ac81ae28b9471d1678b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407259"
---
# <span data-ttu-id="ac941-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="ac941-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="ac941-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac941-102">SYNOPSIS</span></span>
<span data-ttu-id="ac941-103">Lista över objekt på Start-menyn i den angivna program gruppen.</span><span class="sxs-lookup"><span data-stu-id="ac941-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="ac941-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac941-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ac941-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac941-105">DESCRIPTION</span></span>
<span data-ttu-id="ac941-106">Lista över objekt på Start-menyn i den angivna program gruppen.</span><span class="sxs-lookup"><span data-stu-id="ac941-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="ac941-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac941-107">EXAMPLES</span></span>

### <span data-ttu-id="ac941-108">Exempel 2: lista objekt på Start-menyn i Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="ac941-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="ac941-109">Det här kommandot visar objekt på Start-menyn i en applicaton-grupp.</span><span class="sxs-lookup"><span data-stu-id="ac941-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="ac941-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac941-110">PARAMETERS</span></span>

### <span data-ttu-id="ac941-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="ac941-111">-ApplicationGroupName</span></span>
<span data-ttu-id="ac941-112">Namnet på program gruppen</span><span class="sxs-lookup"><span data-stu-id="ac941-112">The name of the application group</span></span>

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

### <span data-ttu-id="ac941-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac941-113">-DefaultProfile</span></span>
<span data-ttu-id="ac941-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac941-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac941-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac941-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac941-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ac941-116">The name of the resource group.</span></span>
<span data-ttu-id="ac941-117">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ac941-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac941-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac941-118">-SubscriptionId</span></span>
<span data-ttu-id="ac941-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ac941-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac941-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac941-120">CommonParameters</span></span>
<span data-ttu-id="ac941-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac941-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac941-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac941-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac941-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac941-123">INPUTS</span></span>

## <span data-ttu-id="ac941-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac941-124">OUTPUTS</span></span>

### <span data-ttu-id="ac941-125">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="ac941-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IStartMenuItem</span></span>

## <span data-ttu-id="ac941-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac941-126">NOTES</span></span>

<span data-ttu-id="ac941-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac941-127">ALIASES</span></span>

## <span data-ttu-id="ac941-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac941-128">RELATED LINKS</span></span>

